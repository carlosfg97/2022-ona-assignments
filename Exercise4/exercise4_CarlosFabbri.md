Untitled
================

``` r
library(tidyverse)
```

    ## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --

    ## v ggplot2 3.3.5     v purrr   0.3.4
    ## v tibble  3.1.4     v dplyr   1.0.7
    ## v tidyr   1.1.3     v stringr 1.4.0
    ## v readr   2.0.1     v forcats 0.5.1

    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
library(lubridate)
```

    ## 
    ## Attaching package: 'lubridate'

    ## The following objects are masked from 'package:base':
    ## 
    ##     date, intersect, setdiff, union

``` r
library(arrow)
```

    ## Warning: package 'arrow' was built under R version 4.1.3

    ## 
    ## Attaching package: 'arrow'

    ## The following object is masked from 'package:lubridate':
    ## 
    ##     duration

    ## The following object is masked from 'package:utils':
    ## 
    ##     timestamp

``` r
load(file='applications.Rda')

load(file='edges')



names(applications)
```

    ##  [1] "application_number"   "filing_date"          "examiner_name_last"  
    ##  [4] "examiner_name_first"  "examiner_name_middle" "examiner_id"         
    ##  [7] "examiner_art_unit"    "uspc_class"           "uspc_subclass"       
    ## [10] "patent_number"        "patent_issue_date"    "abandon_date"        
    ## [13] "disposal_type"        "appl_status_code"     "appl_status_date"    
    ## [16] "tc"                   "gender"               "race"                
    ## [19] "earliest_date"        "latest_date"          "tenure_days"

``` r
names(edges)
```

    ## [1] "application_number" "advice_date"        "ego_examiner_id"   
    ## [4] "alter_examiner_id"

To create our list of valid applications, we keep only those that have
either an abandont date or an issue date.

``` r
# creating variable for processing time

applications_abandonned = applications[!is.na(applications$abandon_date),]

applications_abandonned = applications_abandonned %>% rename(end_date = abandon_date) %>% select(-c('patent_issue_date'))

applications_issued = applications[!is.na(applications$patent_issue_date),]

applications_issued = applications_issued %>% rename(end_date = patent_issue_date) %>% select(-c('abandon_date'))

applications2 = rbind(applications_abandonned, applications_issued)
```

Now we create the processing time feature by subtracting the filing date
to the end date. We make sure to keep rows only where the difference is
positive.

``` r
names(applications_abandonned)
```

    ##  [1] "application_number"   "filing_date"          "examiner_name_last"  
    ##  [4] "examiner_name_first"  "examiner_name_middle" "examiner_id"         
    ##  [7] "examiner_art_unit"    "uspc_class"           "uspc_subclass"       
    ## [10] "patent_number"        "end_date"             "disposal_type"       
    ## [13] "appl_status_code"     "appl_status_date"     "tc"                  
    ## [16] "gender"               "race"                 "earliest_date"       
    ## [19] "latest_date"          "tenure_days"

``` r
proc_t = applications2$end_date - applications2$filing_date
proc_t = as.numeric(proc_t)
summary(proc_t)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  -13636     765    1079    1190    1481   17898

``` r
applications2$app_proc_time = proc_t

applications3 = applications2[applications2$app_proc_time >0 , ]

edges_filt = edges %>% inner_join(applications3[c('application_number')] , by = 'application_number') 

edges_filt
```

    ## # A tibble: 32,794 x 4
    ##    application_number advice_date ego_examiner_id alter_examiner_id
    ##    <chr>              <date>                <dbl>             <dbl>
    ##  1 09402488           2008-11-17            84356             66266
    ##  2 09402488           2008-11-17            84356             63519
    ##  3 09402488           2008-11-17            84356             98531
    ##  4 09445135           2008-08-21            92953             71313
    ##  5 09445135           2008-08-21            92953             93865
    ##  6 09445135           2008-08-21            92953             91818
    ##  7 09479304           2008-12-15            61767             69277
    ##  8 09479304           2008-12-15            61767             92446
    ##  9 09479304           2008-12-15            61767             66805
    ## 10 09479304           2008-12-15            61767             70919
    ## # ... with 32,784 more rows

Now lets create our graph based on these edges.

``` r
library(tidygraph)
```

    ## Warning: package 'tidygraph' was built under R version 4.1.3

    ## 
    ## Attaching package: 'tidygraph'

    ## The following object is masked from 'package:stats':
    ## 
    ##     filter

``` r
library(tidyverse)
library(ggraph)
```

    ## Warning: package 'ggraph' was built under R version 4.1.3

``` r
edges_filt = edges_filt %>% rename(to = alter_examiner_id ,
                     from = ego_examiner_id )

graph = as_tbl_graph(x = edges_filt[c('to','from')], directed = TRUE , mode = 'out') #directed from ego examiner to alter examiner iD
```

    ## Warning in graph_from_data_frame(x, directed = directed): In `d' `NA' elements
    ## were replaced with string "NA"

``` r
nodes_df = graph %>%
  activate(nodes) %>%
  mutate(centrality_degree = centrality_degree(), 
         closeness = centrality_closeness(),
         betweenness = centrality_betweenness(),
         authority = centrality_authority()) %>% 
  rename(examiner_id = name) %>%  data.frame()
```

    ## Warning in betweenness(graph = graph, v = V(graph), directed = directed, :
    ## 'nobigint' is deprecated since igraph 1.3 and will be removed in igraph 1.4

``` r
applications3$examiner_id = as.character(applications3$examiner_id)


applications3 = applications3 %>% left_join(nodes_df, by = 'examiner_id')
```

Once we have added the centrality scores to the patent application
records, we have a complete dataset to use for regression

``` r
attach(applications3)


save(applications3,file="applications3.Rda")

load("applications3.Rda")


colSums(is.na(applications3))
```

    ##   application_number          filing_date   examiner_name_last 
    ##                    0                    0                    0 
    ##  examiner_name_first examiner_name_middle          examiner_id 
    ##                    0               390395                 3745 
    ##    examiner_art_unit           uspc_class        uspc_subclass 
    ##                    0                    4                 1555 
    ##        patent_number             end_date        disposal_type 
    ##               601849                    0                    0 
    ##     appl_status_code     appl_status_date                   tc 
    ##                  355                  356                    0 
    ##               gender                 race        earliest_date 
    ##               253870                    0                18239 
    ##          latest_date          tenure_days        app_proc_time 
    ##                18239                18239                    0 
    ##    centrality_degree            closeness          betweenness 
    ##               612758               980121               612758 
    ##            authority 
    ##               612758

``` r
applications3 = applications3 %>%  drop_na(app_proc_time, centrality_degree,closeness, betweenness,
authority, gender, race,tenure_days )

attach(applications3)
```

    ## The following objects are masked from applications3 (pos = 3):
    ## 
    ##     app_proc_time, appl_status_code, appl_status_date,
    ##     application_number, authority, betweenness, centrality_degree,
    ##     closeness, disposal_type, earliest_date, end_date,
    ##     examiner_art_unit, examiner_id, examiner_name_first,
    ##     examiner_name_last, examiner_name_middle, filing_date, gender,
    ##     latest_date, patent_number, race, tc, tenure_days, uspc_class,
    ##     uspc_subclass

``` r
model1 = lm(app_proc_time ~ centrality_degree + closeness + betweenness +  authority + gender + race + tenure_days + 
     gender * centrality_degree +
     gender * betweenness + 
     gender * closeness + 
    gender * authority)

#options(scipen=999)

summary(model1)
```

    ## 
    ## Call:
    ## lm(formula = app_proc_time ~ centrality_degree + closeness + 
    ##     betweenness + authority + gender + race + tenure_days + gender * 
    ##     centrality_degree + gender * betweenness + gender * closeness + 
    ##     gender * authority)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -1321.0  -440.7  -118.1   305.2  4996.2 
    ## 
    ## Coefficients:
    ##                                Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)                   1.496e+03  8.373e+00 178.678  < 2e-16 ***
    ## centrality_degree             2.445e-01  5.415e-02   4.515 6.34e-06 ***
    ## closeness                    -1.002e+02  4.316e+00 -23.216  < 2e-16 ***
    ## betweenness                  -6.379e-04  2.332e-04  -2.735  0.00624 ** 
    ## authority                    -1.924e+03  2.214e+02  -8.692  < 2e-16 ***
    ## gendermale                    3.489e+01  2.749e+00  12.693  < 2e-16 ***
    ## raceblack                     2.256e+01  4.829e+00   4.672 2.99e-06 ***
    ## raceHispanic                  2.740e+01  5.680e+00   4.824 1.41e-06 ***
    ## raceother                    -3.443e+00  3.606e+01  -0.096  0.92392    
    ## racewhite                    -5.883e+01  1.927e+00 -30.525  < 2e-16 ***
    ## tenure_days                  -3.378e-02  1.345e-03 -25.111  < 2e-16 ***
    ## centrality_degree:gendermale -6.010e-01  6.181e-02  -9.723  < 2e-16 ***
    ## betweenness:gendermale        2.727e-03  2.750e-04   9.915  < 2e-16 ***
    ## closeness:gendermale         -2.176e+01  5.177e+00  -4.203 2.63e-05 ***
    ## authority:gendermale          1.538e+03  2.299e+02   6.693 2.19e-11 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 644.8 on 592687 degrees of freedom
    ## Multiple R-squared:  0.01034,    Adjusted R-squared:  0.01032 
    ## F-statistic: 442.3 on 14 and 592687 DF,  p-value: < 2.2e-16

### Interpretations from the model

-   From the 4 centrality scores analyzed, degree and betweenness seem
    to show very small influence in the processing time of an
    application. On the contrary, closeness and authority scores seem to
    have strong effect in the duration of an application. On average,
    the processing time an application is reduced by 1900 days for each
    additional degree of authority centrality that an examiner has. The
    effect is of 100 days for the case of the closeness degree.

-   On average, applications reviewed by males tend to take 34 more days
    of processing than the ones handled by females. But, for every extra
    closeness degree that the male has, he will reduce the processing
    time in 21 days less than his female counterpart.

-   According to the model, white race tends to process applications in
    58 days less than the Asian race. However lets remember that this
    data set has a heavy oversampling of white employees so this result
    should be taken carefully.
