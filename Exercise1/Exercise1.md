Untitled
================

## Read the data

``` r
data = read.csv('Connections.csv', encoding = 'UTF-8')
```

``` r
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
data %>% group_by(Company) %>% count() %>% arrange(desc(n))
```

    ## # A tibble: 792 x 2
    ## # Groups:   Company [792]
    ##    Company                                                   n
    ##    <chr>                                                 <int>
    ##  1 "Belcorp"                                                64
    ##  2 "McGill University - Desautels Faculty of Management"    23
    ##  3 "Banco de Crédito BCP"                                   19
    ##  4 "Interbank"                                              19
    ##  5 ""                                                       18
    ##  6 "Scotiabank"                                             16
    ##  7 "Entel Perú"                                             15
    ##  8 "Rappi"                                                  13
    ##  9 "Alicorp"                                                12
    ## 10 "EY"                                                     12
    ## # ... with 782 more rows

``` r
#library(tidygraph)
#library(ggraph)

# not being used for now
```

``` r
names(data)
```

    ## [1] "First.Name"    "Last.Name"     "Email.Address" "Company"      
    ## [5] "Position"      "Connected.On"

``` r
data$Last_name_initial = substr(data$Last.Name, 1,1)


data = data %>% mutate(
  name = paste(First.Name, Last_name_initial, sep = " ")
)


data$index <- 1:nrow(data)

unique(data$Company)
```

    ##   [1] "Maple (getmaple.ca)"                                                               
    ##   [2] "Shared-X"                                                                          
    ##   [3] "Pratt & Whitney"                                                                   
    ##   [4] ""                                                                                  
    ##   [5] "Intelligems"                                                                       
    ##   [6] "Interbank"                                                                         
    ##   [7] "Investissements PSP"                                                               
    ##   [8] "Dataiku"                                                                           
    ##   [9] "Pratt & Whitney Canada"                                                            
    ##  [10] "HSBC"                                                                              
    ##  [11] "Transat"                                                                           
    ##  [12] "Ontop"                                                                             
    ##  [13] "Hootsuite"                                                                         
    ##  [14] "WindTech AI"                                                                       
    ##  [15] "Rely On Dreams"                                                                    
    ##  [16] "Google"                                                                            
    ##  [17] "HelloFresh"                                                                        
    ##  [18] "Shopify"                                                                           
    ##  [19] "Bazar del Bosque"                                                                  
    ##  [20] "AMLUL"                                                                             
    ##  [21] "Starbucks"                                                                         
    ##  [22] "LAIVE S.A."                                                                        
    ##  [23] "Lambton College"                                                                   
    ##  [24] "BOMBARDIER"                                                                        
    ##  [25] "Pezer Investments Corp."                                                           
    ##  [26] "Sia Partners"                                                                      
    ##  [27] "McGill University - Desautels Faculty of Management"                               
    ##  [28] "AC Capitales"                                                                      
    ##  [29] "SIA Innovations Inc."                                                              
    ##  [30] "Frollo"                                                                            
    ##  [31] "SharpestMinds"                                                                     
    ##  [32] "Desautels Business Technology Club"                                                
    ##  [33] "Keurig Dr Pepper Inc."                                                             
    ##  [34] "Luxaviation Group"                                                                 
    ##  [35] "Boston Consulting Group (BCG)"                                                     
    ##  [36] "Optima Energía"                                                                    
    ##  [37] "TELUS"                                                                             
    ##  [38] "Novartis"                                                                          
    ##  [39] "Metrolinx"                                                                         
    ##  [40] "ArcelorMittal"                                                                     
    ##  [41] "Lens Technology"                                                                   
    ##  [42] "Sociedad Era Contratistas Generales"                                               
    ##  [43] "Banque Nationale du Canada"                                                        
    ##  [44] "CFG Investment-Copeinca"                                                           
    ##  [45] "Arshinkooh Co."                                                                    
    ##  [46] "NTT DATA Europe & LATAM"                                                           
    ##  [47] "Moov AI"                                                                           
    ##  [48] "wymaq.com"                                                                         
    ##  [49] "Overhaul Machineries"                                                              
    ##  [50] "Hiraoka"                                                                           
    ##  [51] "Rappi"                                                                             
    ##  [52] "Pisco Huamaní"                                                                     
    ##  [53] "Consultor Independiente."                                                          
    ##  [54] "aNumak & Company"                                                                  
    ##  [55] "APOYO Consultoría"                                                                 
    ##  [56] "Betsson Group"                                                                     
    ##  [57] "CGI"                                                                               
    ##  [58] "McKesson Canada"                                                                   
    ##  [59] "Laps"                                                                              
    ##  [60] "DHL"                                                                               
    ##  [61] "Verint"                                                                            
    ##  [62] "Banco de Crédito BCP"                                                              
    ##  [63] "KPI Digital Solutions"                                                             
    ##  [64] "IBM"                                                                               
    ##  [65] "Grupo AJE"                                                                         
    ##  [66] "Arquinsa"                                                                          
    ##  [67] "Rimac Seguros y Reaseguros"                                                        
    ##  [68] "EFIC Partners"                                                                     
    ##  [69] "McGill University"                                                                 
    ##  [70] "Targray"                                                                           
    ##  [71] "Kavak.com"                                                                         
    ##  [72] "Monithor"                                                                          
    ##  [73] "KPMG"                                                                              
    ##  [74] "Rio Tinto"                                                                         
    ##  [75] "Deloitte"                                                                          
    ##  [76] "EY"                                                                                
    ##  [77] "École Polytechnique de Montréal"                                                   
    ##  [78] "Twitch"                                                                            
    ##  [79] "Morgan Stanley"                                                                    
    ##  [80] "KPMG Canada"                                                                       
    ##  [81] "Air Transat"                                                                       
    ##  [82] "École de technologie supérieure"                                                   
    ##  [83] "Marsh Latinoamérica"                                                               
    ##  [84] "LABOCER S.A."                                                                      
    ##  [85] "HEC Montréal"                                                                      
    ##  [86] "Wilfrid Laurier University"                                                        
    ##  [87] "Abbott"                                                                            
    ##  [88] "Procter & Gamble"                                                                  
    ##  [89] "180 Degrees Consulting UP "                                                        
    ##  [90] "BBVA"                                                                              
    ##  [91] "Centro Gagliuffi"                                                                  
    ##  [92] "Montebello Packaging"                                                              
    ##  [93] "Kovacs & Asociados SAC"                                                            
    ##  [94] "SAP - Sports & Entertainment - North America"                                      
    ##  [95] "PepsiCo"                                                                           
    ##  [96] "International Development Group LLC (IDG)"                                         
    ##  [97] "HOCHSCHILD"                                                                        
    ##  [98] "Scotiabank"                                                                        
    ##  [99] "Héroux-Devtek"                                                                     
    ## [100] "Mistplay"                                                                          
    ## [101] "COVID-19 Immunity Task Force | Groupe de travail sur l’immunité face à la COVID-19"
    ## [102] "Keurig Dr Pepper Canada"                                                           
    ## [103] "PwC"                                                                               
    ## [104] "Backus"                                                                            
    ## [105] "Bernal Partners"                                                                   
    ## [106] "XGIMI Technology"                                                                  
    ## [107] "Banco Santander"                                                                   
    ## [108] "Autodesk"                                                                          
    ## [109] "Resolute Forest Products"                                                          
    ## [110] "Robi Axiata Limited"                                                               
    ## [111] "Dora Desino"                                                                       
    ## [112] "CAE"                                                                               
    ## [113] "JOKR"                                                                              
    ## [114] "Rogers Communications"                                                             
    ## [115] "Millennial"                                                                        
    ## [116] "Ubisoft Montréal"                                                                  
    ## [117] "RBC"                                                                               
    ## [118] "Korn Ferry"                                                                        
    ## [119] "SAP"                                                                               
    ## [120] "BGIS"                                                                              
    ## [121] "Wall Street English"                                                               
    ## [122] "Atria Energía"                                                                     
    ## [123] "Glencore"                                                                          
    ## [124] "Polysistemas"                                                                      
    ## [125] "Vikingo store"                                                                     
    ## [126] "Agroved Fruit Sac"                                                                 
    ## [127] "<U+6B27><U+83B1><U+96C5>"                                                          
    ## [128] "Hotstar"                                                                           
    ## [129] "D2V Analytics"                                                                     
    ## [130] "CN"                                                                                
    ## [131] "Monarchy Build"                                                                    
    ## [132] "IPM World Properties"                                                              
    ## [133] "ServiceNow"                                                                        
    ## [134] "Consulting"                                                                        
    ## [135] "BMO Commercial Bank"                                                               
    ## [136] "Alicorp"                                                                           
    ## [137] "Right Curly Bracket"                                                               
    ## [138] "AssetIO Wealth Management"                                                         
    ## [139] "FrienDuel"                                                                         
    ## [140] "Entel Perú"                                                                        
    ## [141] "Sanofi"                                                                            
    ## [142] "Mibanco"                                                                           
    ## [143] "MAPFRE PERÚ"                                                                       
    ## [144] "Loblaw Companies Limited"                                                          
    ## [145] "Tempo Software"                                                                    
    ## [146] "Bajaj Allianz General Insurance"                                                   
    ## [147] "MindGeek"                                                                          
    ## [148] "IGA, INC."                                                                         
    ## [149] "Aktana"                                                                            
    ## [150] "Nasdaq"                                                                            
    ## [151] "Noon - The Social Learning Platform"                                               
    ## [152] "Hikari Group"                                                                      
    ## [153] "Talent2Win USA"                                                                    
    ## [154] "Adecco"                                                                            
    ## [155] "Banco de Crédito del Perú - BCP"                                                   
    ## [156] "Stori"                                                                             
    ## [157] "Offeteria"                                                                         
    ## [158] "CERTUS"                                                                            
    ## [159] "Wall Street English - Peru"                                                        
    ## [160] "SmartPrint Perú"                                                                   
    ## [161] "Odette School of Business"                                                         
    ## [162] "Brother Canada"                                                                    
    ## [163] "BNP Paribas"                                                                       
    ## [164] "Slalom"                                                                            
    ## [165] "Shell"                                                                             
    ## [166] "Verizon"                                                                           
    ## [167] "Bombonería Pons"                                                                   
    ## [168] "DHL eCommerce Solutions"                                                           
    ## [169] "McKesson"                                                                          
    ## [170] "Antamina"                                                                          
    ## [171] "Viatris"                                                                           
    ## [172] "Macdonald Campus Students' Society"                                                
    ## [173] "Apple"                                                                             
    ## [174] "Diners Club Perú"                                                                  
    ## [175] "IGT"                                                                               
    ## [176] "Bell"                                                                              
    ## [177] "GRUPO DNA"                                                                         
    ## [178] "McGill University - Faculty of Science"                                            
    ## [179] "TOCA Football"                                                                     
    ## [180] "CARS24"                                                                            
    ## [181] "Beat"                                                                              
    ## [182] "TD Insurance"                                                                      
    ## [183] "Belcorp"                                                                           
    ## [184] "Pentación Espectáculos"                                                            
    ## [185] "Unity"                                                                             
    ## [186] "Waterborne Skateboards"                                                            
    ## [187] "Gorgias"                                                                           
    ## [188] "Mosaic-HEC Montréal"                                                               
    ## [189] "Global Affairs Canada | Affaires mondiales Canada"                                 
    ## [190] "Accenture"                                                                         
    ## [191] "Plus 5XP"                                                                          
    ## [192] "WeSpire"                                                                           
    ## [193] "CAT-Barcelona"                                                                     
    ## [194] "C-F Business Links (CFBL Consulting)"                                              
    ## [195] "Mercado Libre"                                                                     
    ## [196] "MG gastronomia"                                                                    
    ## [197] "APP GROUP"                                                                         
    ## [198] "Selina"                                                                            
    ## [199] "Endeavor Perú"                                                                     
    ## [200] "Universidad del Pacifico"                                                          
    ## [201] "Amazon"                                                                            
    ## [202] "Banco de la Nación de Perú"                                                        
    ## [203] "Talent2Win Latam"                                                                  
    ## [204] "Atento"                                                                            
    ## [205] "Imdex Limited"                                                                     
    ## [206] "Logitravel Group"                                                                  
    ## [207] "Onapsis Inc."                                                                      
    ## [208] "York Consulting Group (YCG)"                                                       
    ## [209] "Grupo CRES | Camet Real Estate Services (comercial, residencial e industrial)"     
    ## [210] "3ERIZA"                                                                            
    ## [211] "Colgate-Palmolive"                                                                 
    ## [212] "Michael Page"                                                                      
    ## [213] "Vooxell"                                                                           
    ## [214] "Neo Consulting - Consultora de Innovación y Estrategia Digital"                    
    ## [215] "Data Engineering LATAM"                                                            
    ## [216] "Factorial HR"                                                                      
    ## [217] "Cheil Peru"                                                                        
    ## [218] "People Analytics Perú"                                                             
    ## [219] "QROMA"                                                                             
    ## [220] "Keyrus"                                                                            
    ## [221] "Credicorp Capital"                                                                 
    ## [222] "Métrica Perú"                                                                      
    ## [223] "Doulton Drinking Water"                                                            
    ## [224] "Entel"                                                                             
    ## [225] "Yanbal"                                                                            
    ## [226] "Cencosud S.A."                                                                     
    ## [227] "Entel Empresas Perú"                                                               
    ## [228] "Mondelez International"                                                            
    ## [229] "Pacífico Seguros"                                                                  
    ## [230] "Huevos La Calera"                                                                  
    ## [231] "Applaudo Studios"                                                                  
    ## [232] "Culqi"                                                                             
    ## [233] "Red Bull"                                                                          
    ## [234] "Rodrigo, Elias & Medrano Abogados"                                                 
    ## [235] "PUMA Group"                                                                        
    ## [236] "Winston Capital Advisors "                                                         
    ## [237] "Management Solutions"                                                              
    ## [238] "Salesforce"                                                                        
    ## [239] "Dilat.arq"                                                                         
    ## [240] "Sapia Oficial"                                                                     
    ## [241] "Primax S.A"                                                                        
    ## [242] "Juntas"                                                                            
    ## [243] "Universidad San Ignacio de Loyola"                                                 
    ## [244] "Analytica Software and Technologies"                                               
    ## [245] "BRECA"                                                                             
    ## [246] "Igma Sports "                                                                      
    ## [247] "IDEM Organización Educativa"                                                       
    ## [248] "VNYSA Studio"                                                                      
    ## [249] "Cementos Pacasmayo SAA"                                                            
    ## [250] "cbc"                                                                               
    ## [251] "Garrigues"                                                                         
    ## [252] "MF Asesoría y Consultoría SAC"                                                     
    ## [253] "Ayni Educativo"                                                                    
    ## [254] "Azzorti"                                                                           
    ## [255] "Paper"                                                                             
    ## [256] "Colegio Santa María Marianistas"                                                   
    ## [257] "DataKnow"                                                                          
    ## [258] "Romex"                                                                             
    ## [259] "Cognizant"                                                                         
    ## [260] "ALMA VITTA"                                                                        
    ## [261] "CLUB NACIONAL"                                                                     
    ## [262] "BBVA en Perú"                                                                      
    ## [263] "Kimberly-Clark"                                                                    
    ## [264] "Falcon Management Partners"                                                        
    ## [265] "Autónomo"                                                                          
    ## [266] "Banco Santander Peru"                                                              
    ## [267] "Volcan Cia Minera SAA"                                                             
    ## [268] "Baylor University"                                                                 
    ## [269] "Institute of Computing Technology, Chinese Academy of Sciences"                    
    ## [270] "FLX AI, Inc."                                                                      
    ## [271] "Soft group - Marketing y Trade"                                                    
    ## [272] "University of Rochester"                                                           
    ## [273] "SKY Airline"                                                                       
    ## [274] "Dive Consulting"                                                                   
    ## [275] "Rebaza Alcázar & De Las Casas"                                                     
    ## [276] "Untamed"                                                                           
    ## [277] "Columbia Climate School"                                                           
    ## [278] "University of Pennsylvania"                                                        
    ## [279] "Bilkom"                                                                            
    ## [280] "Columbia Economics Society"                                                        
    ## [281] "Park City"                                                                         
    ## [282] "TGP Perú"                                                                          
    ## [283] "Tienda Pago"                                                                       
    ## [284] "Intercorp Retail"                                                                  
    ## [285] "START Barcelona"                                                                   
    ## [286] "Baufest"                                                                           
    ## [287] "BHG CORP"                                                                          
    ## [288] "Cedars-Sinai"                                                                      
    ## [289] "Equifax"                                                                           
    ## [290] "Seidor"                                                                            
    ## [291] "ASSOCIATION FOR COMPUTATIONAL LINGUISTICS INC"                                     
    ## [292] "Sociedad Nacional de Industrias"                                                   
    ## [293] "ALEGREVO | Grupo Educativo"                                                        
    ## [294] "APD Perú"                                                                          
    ## [295] "Barchovia"                                                                         
    ## [296] "Trade Republic"                                                                    
    ## [297] "Franco Ferraro Arquitectura"                                                       
    ## [298] "IA Collaborative"                                                                  
    ## [299] "<U+5143><U+542F><U+8D44><U+672C> Thriving Capital"                                 
    ## [300] "Haystack News"                                                                     
    ## [301] "Bloom Insurance"                                                                   
    ## [302] "Ripley Perú"                                                                       
    ## [303] "Hidroponika"                                                                       
    ## [304] "The University of New Mexico"                                                      
    ## [305] "México & Perú IT Business Services"                                                
    ## [306] "Shearman & Sterling LLP"                                                           
    ## [307] "Media Pro"                                                                         
    ## [308] "Edinburgh University Consulting Club"                                              
    ## [309] "Vodanovic Legal"                                                                   
    ## [310] "WWIN Planners by Wendy Wunder"                                                     
    ## [311] "Bluetab, an IBM Company"                                                           
    ## [312] "Moovx"                                                                             
    ## [313] "Manya"                                                                             
    ## [314] "Inetum"                                                                            
    ## [315] "WOM Colombia"                                                                      
    ## [316] "Cambridge Spark"                                                                   
    ## [317] "Goldman Sachs"                                                                     
    ## [318] "Wells Fargo"                                                                       
    ## [319] "WePay"                                                                             
    ## [320] "Barclay & Crousse Architecture "                                                   
    ## [321] "Marcobre"                                                                          
    ## [322] "RecoveryLink"                                                                      
    ## [323] "AzLab"                                                                             
    ## [324] "Gallagher"                                                                         
    ## [325] "A.G.S INT LLC "                                                                    
    ## [326] "Sealand – A Maersk Company"                                                        
    ## [327] "Nestlé"                                                                            
    ## [328] "Prestamype"                                                                        
    ## [329] "Libero Esports - grupo La República "                                              
    ## [330] "INNSPIRAL"                                                                         
    ## [331] "NewCapital Securities"                                                             
    ## [332] "Servicio de Administración Tributaria de Lima - SAT"                               
    ## [333] "Cafin"                                                                             
    ## [334] "Una Solutions - Innovación & Transformación Digital"                               
    ## [335] "Rehabilitation Enables Dreams"                                                     
    ## [336] "Servientrega Perú"                                                                 
    ## [337] "Profesional independiente"                                                         
    ## [338] "KIACORP"                                                                           
    ## [339] "R COORP"                                                                           
    ## [340] "Arquinfo SAC - Perú"                                                               
    ## [341] "Pas Une Marque"                                                                    
    ## [342] "Comunidad de Analytics Translators LAC"                                            
    ## [343] "Voyantic"                                                                          
    ## [344] "Capitalismo Consciente Peru"                                                       
    ## [345] "Favo"                                                                              
    ## [346] "SURA Perú"                                                                         
    ## [347] "Ministerio de Relaciones Exteriores - Peru"                                        
    ## [348] "Anheuser-Busch InBev"                                                              
    ## [349] "BREIN"                                                                             
    ## [350] "Consersa Perú"                                                                     
    ## [351] "Oh Zsa Zsa "                                                                       
    ## [352] "Ookla"                                                                             
    ## [353] "Inteligo Group"                                                                    
    ## [354] "Arca Continental Lindley"                                                          
    ## [355] "Credicorp"                                                                         
    ## [356] "Auna"                                                                              
    ## [357] "Grupo Intercorp"                                                                   
    ## [358] "Natura"                                                                            
    ## [359] "Corporación Antezana SAC"                                                          
    ## [360] "Supermercados Peruanos S.A."                                                       
    ## [361] "HP"                                                                                
    ## [362] "ZINC INDUSTRIAS NACIONALES S.A. (ZINSA)"                                           
    ## [363] "3M"                                                                                
    ## [364] "Entelgy"                                                                           
    ## [365] "Hunt Oil Company"                                                                  
    ## [366] "Ghanimah"                                                                          
    ## [367] "Perufarma S.A."                                                                    
    ## [368] "Mercedes-Benz AG"                                                                  
    ## [369] "Consultoría"                                                                       
    ## [370] "IT Company "                                                                       
    ## [371] "Grupo Plenum"                                                                      
    ## [372] "Phenom"                                                                            
    ## [373] "Alfil Sports"                                                                      
    ## [374] "The University of Adelaide College"                                                
    ## [375] "Mevoydeviaje.com"                                                                  
    ## [376] "Workday"                                                                           
    ## [377] "Encora Inc."                                                                       
    ## [378] "Innova Hunting Group"                                                              
    ## [379] "Bitel Perú"                                                                        
    ## [380] "IBservice"                                                                         
    ## [381] "FORCECLOSE"                                                                        
    ## [382] "PedidosYa"                                                                         
    ## [383] "The HEINEKEN Company"                                                              
    ## [384] "Cool Earth"                                                                        
    ## [385] "Uno Salud Dental"                                                                  
    ## [386] "DSV - Global Transport and Logistics"                                              
    ## [387] "Best selection Peru"                                                               
    ## [388] "Escuela de Postgrado de la Universidad San Ignacio de Loyola"                      
    ## [389] "Odisea"                                                                            
    ## [390] "Fundación Capital"                                                                 
    ## [391] "Centro Odontológico Francesqui"                                                    
    ## [392] "DPP Abogados"                                                                      
    ## [393] "Coopeuch"                                                                          
    ## [394] "Independiente SAF"                                                                 
    ## [395] "El Roble Cava y Quesos"                                                            
    ## [396] "Asociación Peruana de Facility Management"                                         
    ## [397] "PwC Perú"                                                                          
    ## [398] "Banco Ripley Chile"                                                                
    ## [399] "Matemáticamente posible"                                                           
    ## [400] "LATAM Airlines"                                                                    
    ## [401] "DMB Sports Agency"                                                                 
    ## [402] "Ecommerce Medical"                                                                 
    ## [403] "Gourmet Logistics Company"                                                         
    ## [404] "Seaboard Overseas Perú S.A."                                                       
    ## [405] "Ministry of Economy and Finance"                                                   
    ## [406] "FILTROS LYS"                                                                       
    ## [407] "Dell Technologies"                                                                 
    ## [408] "Clairfield International"                                                          
    ## [409] "San Miguel Industrias PET S.A."                                                    
    ## [410] "Chubb"                                                                             
    ## [411] "MegaNext"                                                                          
    ## [412] "Pernod Ricard"                                                                     
    ## [413] "Aldeamo"                                                                           
    ## [414] "Reviur Inc"                                                                        
    ## [415] "RITMO"                                                                             
    ## [416] "VTEX"                                                                              
    ## [417] "Laboratorios Smasac"                                                               
    ## [418] "Macroconsult"                                                                      
    ## [419] "Macquarie Group"                                                                   
    ## [420] "Clara"                                                                             
    ## [421] "Datum Internacional"                                                               
    ## [422] "DataRobot"                                                                         
    ## [423] "Oracle"                                                                            
    ## [424] "NG Restaurants S.A."                                                               
    ## [425] "Center for Brains, Minds and Machines"                                             
    ## [426] "Manuchar Perú"                                                                     
    ## [427] "AB InBev"                                                                          
    ## [428] "Ericsson"                                                                          
    ## [429] "Desjardins"                                                                        
    ## [430] "Gestión y Sistemas"                                                                
    ## [431] "Adobe"                                                                             
    ## [432] "Minsky"                                                                            
    ## [433] "EFC"                                                                               
    ## [434] "Tuxpas - Workplace from Facebook & AWS Partner"                                    
    ## [435] "Globant"                                                                           
    ## [436] "Listopro"                                                                          
    ## [437] "Citi"                                                                              
    ## [438] "Roche"                                                                             
    ## [439] "Universidad Peruana de Ciencias Aplicadas"                                         
    ## [440] "Humanistische Kindertagesstätte Wilde Hummel"                                      
    ## [441] "Stealth Mode Startup"                                                              
    ## [442] "Qbiz Inc."                                                                         
    ## [443] "Interseguro Compañía de Seguros"                                                   
    ## [444] "Future Visions"                                                                    
    ## [445] "Primal Instinct"                                                                   
    ## [446] "Uber"                                                                              
    ## [447] "ERA PR + NETWORKING"                                                               
    ## [448] "Zone Nine Survival"                                                                
    ## [449] "Tottus"                                                                            
    ## [450] "MyPay App"                                                                         
    ## [451] "Nexus Group"                                                                       
    ## [452] "Kantar"                                                                            
    ## [453] "Ironhack"                                                                          
    ## [454] "Talently"                                                                          
    ## [455] "Niubiz"                                                                            
    ## [456] "JZM & Asociados SAC"                                                               
    ## [457] "Caja Arequipa"                                                                     
    ## [458] "UTEC - Educación Ejecutiva"                                                        
    ## [459] "Havas Group"                                                                       
    ## [460] "DINET, Operador Logístico"                                                         
    ## [461] "AGREF"                                                                             
    ## [462] "Pacific Control"                                                                   
    ## [463] "Caylent"                                                                           
    ## [464] "Tismart"                                                                           
    ## [465] "Lucha Startup Studio"                                                              
    ## [466] "APOYO Comunicación"                                                                
    ## [467] "Aimo"                                                                              
    ## [468] "Razor Group"                                                                       
    ## [469] "Profuturo AFP"                                                                     
    ## [470] "Stadtverwaltung Zürich"                                                            
    ## [471] "West Monroe"                                                                       
    ## [472] "Singular Advisors"                                                                 
    ## [473] "GRIO - Grupo Romero Investment Office "                                            
    ## [474] "Pontificia Universidad Católica del Perú"                                          
    ## [475] "Tsoft"                                                                             
    ## [476] "AlixPartners"                                                                      
    ## [477] "DCH - Organización Internacional de Directivos de Capital Humano"                  
    ## [478] "Laboratorio de Big Data México"                                                    
    ## [479] "BBVA Continental"                                                                  
    ## [480] "Kanto"                                                                             
    ## [481] "Sigmoid"                                                                           
    ## [482] "Partido Morado"                                                                    
    ## [483] "AGRICOLA SANTA AZUL "                                                              
    ## [484] "J.P. Morgan"                                                                       
    ## [485] "La Victoria Lab"                                                                   
    ## [486] "Desarrollo Digital SpA"                                                            
    ## [487] "L'Oréal"                                                                           
    ## [488] "CloudSystems.ES en Perú"                                                           
    ## [489] "La Fornaia Pastificio"                                                             
    ## [490] "Surf Place Perú"                                                                   
    ## [491] "SAS"                                                                               
    ## [492] "Devlane"                                                                           
    ## [493] "Experis Perú"                                                                      
    ## [494] "BFA Industries"                                                                    
    ## [495] "Smart Eye"                                                                         
    ## [496] "Albertsons Companies"                                                              
    ## [497] "HEMAGGI EIRL"                                                                      
    ## [498] "Payet, Rey, Cauvi, Pérez Abogados"                                                 
    ## [499] "Executive Insight, Healthcare Consultants"                                         
    ## [500] "McKinsey & Company"                                                                
    ## [501] "Universidad de Lima"                                                               
    ## [502] "Global66"                                                                          
    ## [503] "Sedapal Oficial"                                                                   
    ## [504] "Equifax Perú"                                                                      
    ## [505] "Santander Consumer Peru"                                                           
    ## [506] "Queloco"                                                                           
    ## [507] "BJSS"                                                                              
    ## [508] "NTT DATA Services"                                                                 
    ## [509] "WOWPERÚ"                                                                           
    ## [510] "WITZ SAC"                                                                          
    ## [511] "CAJA TRUJILLO"                                                                     
    ## [512] "Cocinas Ocultas"                                                                   
    ## [513] "Polymath Ventures"                                                                 
    ## [514] "Pan American Silver Corp."                                                         
    ## [515] "Turquoise Health"                                                                  
    ## [516] "Kushki"                                                                            
    ## [517] "Compra Agora"                                                                      
    ## [518] "AGP eGlass"                                                                        
    ## [519] "Amaru Superfoods"                                                                  
    ## [520] "Séntisis Intelligence"                                                             
    ## [521] "IGNIS Energía"                                                                     
    ## [522] "Modo Beta"                                                                         
    ## [523] "Almer Technologies"                                                                
    ## [524] "Armo's & Company"                                                                  
    ## [525] "Chaccu Trading"                                                                    
    ## [526] "TyC Sports"                                                                        
    ## [527] "B89"                                                                               
    ## [528] "Instituto del Futuro"                                                              
    ## [529] "Jellysmack"                                                                        
    ## [530] "PromoInvest SAF"                                                                   
    ## [531] "Amazon Web Services (AWS)"                                                         
    ## [532] "Tebca Perú"                                                                        
    ## [533] "Business Agility Institute"                                                        
    ## [534] "Es Hoy"                                                                            
    ## [535] "DRA Global"                                                                        
    ## [536] "Stealth Startup"                                                                   
    ## [537] "Centria - CSC Grupo Breca"                                                         
    ## [538] "MAB Perú "                                                                         
    ## [539] "Capgemini Engineering"                                                             
    ## [540] "AVC Real Estate"                                                                   
    ## [541] "Sunarp"                                                                            
    ## [542] "Maygel Coronel"                                                                    
    ## [543] "Universidad del Pacífico (PE)"                                                     
    ## [544] "North Carolina State University"                                                   
    ## [545] "Accéder"                                                                           
    ## [546] "BPC Business School"                                                               
    ## [547] "Mandü"                                                                             
    ## [548] "eTeacher Group"                                                                    
    ## [549] "Jaguar Plásticos"                                                                  
    ## [550] "Accenture AI"                                                                      
    ## [551] "UBS"                                                                               
    ## [552] "Quantum Talent"                                                                    
    ## [553] "hp"                                                                                
    ## [554] "Orión"                                                                             
    ## [555] "Magnus"                                                                            
    ## [556] "Universidad Nacional Micaela Bastidas de Apurimac"                                 
    ## [557] "BAT"                                                                               
    ## [558] "Acero-Deck Placa Colaborante"                                                      
    ## [559] "Wabu"                                                                              
    ## [560] "Postgrado UPC"                                                                     
    ## [561] "ISA Interconexión Eléctrica S.A. E.S.P."                                           
    ## [562] "Applying Consulting Latam"                                                         
    ## [563] "ISIL"                                                                              
    ## [564] "Matrix Consulting"                                                                 
    ## [565] "Clarity AI"                                                                        
    ## [566] "Cape Analytics"                                                                    
    ## [567] "Delta Partners"                                                                    
    ## [568] "EY-Parthenon"                                                                      
    ## [569] "A. E. LUMINUS DEI"                                                                 
    ## [570] "GHL PUBLICIDAD"                                                                    
    ## [571] "CSTI Corp"                                                                         
    ## [572] "izipay"                                                                            
    ## [573] "Ferreycorp S.A.A"                                                                  
    ## [574] "GRETEL INTERNATIONAL"                                                              
    ## [575] "Voltron Data"                                                                      
    ## [576] "Business & Decision Belgium"                                                       
    ## [577] "Cuatrecasas"                                                                       
    ## [578] "CIUP, Universidad del Pacífico"                                                    
    ## [579] "Gruas del sur"                                                                     
    ## [580] "Cisco"                                                                             
    ## [581] "Platanitos"                                                                        
    ## [582] "Marsh & McLennan Companies"                                                        
    ## [583] "Pulso"                                                                             
    ## [584] "Digica"                                                                            
    ## [585] "AdJinn"                                                                            
    ## [586] "Yape"                                                                              
    ## [587] "Anida Latam"                                                                       
    ## [588] "Velogig"                                                                           
    ## [589] "Johnson & Johnson"                                                                 
    ## [590] "Lava Quick"                                                                        
    ## [591] "Casino Atlantic City "                                                             
    ## [592] "LINKIT"                                                                            
    ## [593] "UTEC - Universidad de Ingeniería y Tecnología"                                     
    ## [594] "Space AG"                                                                          
    ## [595] "Banco Ripley Perú"                                                                 
    ## [596] "BBVA AI Factory"                                                                   
    ## [597] "Vinatea & Toyama"                                                                  
    ## [598] "BP Perú"                                                                           
    ## [599] "Claro Perú"                                                                        
    ## [600] "Labofta "                                                                          
    ## [601] "COPEINCA"                                                                          
    ## [602] "RESEMIN"                                                                           
    ## [603] "falabella.com"                                                                     
    ## [604] "Salkantay Ventures"                                                                
    ## [605] "Data Science Research Perú"                                                        
    ## [606] "Leader Talent"                                                                     
    ## [607] "Promotora Inmobiliaria Industrial de Piura"                                        
    ## [608] "innova Pucp"                                                                       
    ## [609] "Cloudera"                                                                          
    ## [610] "Beliv Company"                                                                     
    ## [611] "Nitron Group LLC"                                                                  
    ## [612] "América Televisión"                                                                
    ## [613] "America Movil Peru SAC"                                                            
    ## [614] "Swissport"                                                                         
    ## [615] "Banco Santander Perú"                                                              
    ## [616] "TechStart Perú"                                                                    
    ## [617] "Andino Capital"                                                                    
    ## [618] "Falabella Perú"                                                                    
    ## [619] "Cornershop by Uber"                                                                
    ## [620] "Consultora "                                                                       
    ## [621] "Ministerio de Energía y Minas"                                                     
    ## [622] "SONDA"                                                                             
    ## [623] "Stefanini Brasil"                                                                  
    ## [624] "Farmaniacos"                                                                       
    ## [625] "Selectum Professional Hunting"                                                     
    ## [626] "Registro Nacional de Identificación y Estado Civil - RENIEC"                       
    ## [627] "Athenea Dental Institute"                                                          
    ## [628] "Farmacias Peruanas"                                                                
    ## [629] "Pontificia Universidad Catolica del Peru"                                          
    ## [630] "Hospital Nacional Docente Madre Niño San Bartolomé"                                
    ## [631] "Infor"                                                                             
    ## [632] "UPT - LIMA UNIVERSIDAD PRIVADA TELESUP”"                                           
    ## [633] "Crehana"                                                                           
    ## [634] "Cooperativa BCRP"                                                                  
    ## [635] "Instituto Ayrton Senna"                                                            
    ## [636] "GRUPO AUREN"                                                                       
    ## [637] "Fitesa"                                                                            
    ## [638] "Asociación de Internet MX"                                                         
    ## [639] "Valia"                                                                             
    ## [640] "CENTRUM PUCP"                                                                      
    ## [641] "Indra"                                                                             
    ## [642] "PROSERVICES GESTION INMOBILIARIA"                                                  
    ## [643] "Real Plaza - Intercorp Retail"                                                     
    ## [644] "Courier Kunan Express"                                                             
    ## [645] "GesNext"                                                                           
    ## [646] "La Llave S.A."                                                                     
    ## [647] "Afore Coppel"                                                                      
    ## [648] "GMF S.A.C. - AnphiCorp"                                                            
    ## [649] "casa de família ou Hospital "                                                      
    ## [650] "HR Business Consultant"                                                            
    ## [651] "TEST & CONTROL SAC"                                                                
    ## [652] "Condor Agency"                                                                     
    ## [653] "Suscri"                                                                            
    ## [654] "Grupo INMAC"                                                                       
    ## [655] "INTELIGO"                                                                          
    ## [656] "Verde&Más"                                                                         
    ## [657] "Altozano"                                                                          
    ## [658] "Voxiva Perú"                                                                       
    ## [659] "Sociedad Agrícola Rapel SAC"                                                       
    ## [660] "msKompas"                                                                          
    ## [661] "OlamFX Ltd"                                                                        
    ## [662] "Comunal"                                                                           
    ## [663] "Crédit Agricole CIB"                                                               
    ## [664] "Libélula"                                                                          
    ## [665] "Seequent"                                                                          
    ## [666] "Grupo Pucón Perú"                                                                  
    ## [667] "Spencer Stuart"                                                                    
    ## [668] "Almendra Software"                                                                 
    ## [669] "Immunotec"                                                                         
    ## [670] "Proarándanos"                                                                      
    ## [671] "Clinica San Juan de Dios - Lima"                                                   
    ## [672] "Black Andes Analytics"                                                             
    ## [673] "Tandia"                                                                            
    ## [674] "Club De La Union"                                                                  
    ## [675] "Magistragos"                                                                       
    ## [676] "Attach"                                                                            
    ## [677] "EA Corp"                                                                           
    ## [678] "Santander Global Tech"                                                             
    ## [679] "brownie express"                                                                   
    ## [680] "HLM Soluciones en Tecnología de la Información"                                    
    ## [681] "LLYC"                                                                              
    ## [682] "JFV CONSTRUCCIONES E ING"                                                          
    ## [683] "Perfumerías Unidas"                                                                
    ## [684] "Agata Zumaeta"                                                                     
    ## [685] "Universidad Carlos III de Madrid"                                                  
    ## [686] "PRECISA Laboratorios - Subsidiaria de Pacifico EPS"                                
    ## [687] "Prediqt - Data to AI"                                                              
    ## [688] "GRUPORPP"                                                                          
    ## [689] "Performing Brands"                                                                 
    ## [690] "Apuesta Total"                                                                     
    ## [691] "BairesDev"                                                                         
    ## [692] "EVOL (TSnet)"                                                                      
    ## [693] "Mapsalud SAC"                                                                      
    ## [694] "Anglo American"                                                                    
    ## [695] "Ventas"                                                                            
    ## [696] "Ministerio de Desarrollo e Inclusión Social"                                       
    ## [697] "Grupo Medixon"                                                                     
    ## [698] "Twilio"                                                                            
    ## [699] "Diageo"                                                                            
    ## [700] "Grupo Hinode - Oficial"                                                            
    ## [701] "Global Reporting Initiative (GRI)"                                                 
    ## [702] "CLUSTER CONSULTING"                                                                
    ## [703] "Grünenthal Group"                                                                  
    ## [704] "SURA Asset Management"                                                             
    ## [705] "MGM "                                                                              
    ## [706] "TC1 Labs"                                                                          
    ## [707] "State University of Campinas"                                                      
    ## [708] "Derco Perú"                                                                        
    ## [709] "Prima AFP"                                                                         
    ## [710] "Udacity"                                                                           
    ## [711] "Bain & Company"                                                                    
    ## [712] "Pacifica Continental"                                                              
    ## [713] "INDEPENDIENTE"                                                                     
    ## [714] "Grupo Salinas"                                                                     
    ## [715] "DMC Perú"                                                                          
    ## [716] "Remax Platinum Miguel Dasso"                                                       
    ## [717] "FITCO, Inc."                                                                       
    ## [718] "CCE - PUC-Rio"                                                                     
    ## [719] "Super Fast Python"                                                                 
    ## [720] "Peruvian Sourcing Group SAC"                                                       
    ## [721] "SERVIFASTPERU "                                                                    
    ## [722] "Marco Vinelli"                                                                     
    ## [723] "Afilnet"                                                                           
    ## [724] "Hult Workshop Club"                                                                
    ## [725] "Citadel"                                                                           
    ## [726] "WeHunterz"                                                                         
    ## [727] "Big Data Academy"                                                                  
    ## [728] "Caterpillar Financial Services Corporation"                                        
    ## [729] "Tenpo"                                                                             
    ## [730] "Grupo Sypsa"                                                                       
    ## [731] "G.W. Yichang & Cia"                                                                
    ## [732] "Beta Gamma Sigma"                                                                  
    ## [733] "torre.co"                                                                          
    ## [734] "AFP Habitat Perú"                                                                  
    ## [735] "POTRO Lima"                                                                        
    ## [736] "Invertir"                                                                          
    ## [737] "CreaCode"                                                                          
    ## [738] "Surfline\\Wavetrak, Inc."                                                          
    ## [739] "Arimathea Konsulting"                                                              
    ## [740] "Consorcio Aulas para el Perú"                                                      
    ## [741] "Falabella Corporativo Perú"                                                        
    ## [742] "Bauen"                                                                             
    ## [743] "Northwestern University Medill School"                                             
    ## [744] "Bank of America"                                                                   
    ## [745] "CGIAR"                                                                             
    ## [746] "AGP Group"                                                                         
    ## [747] "Giovanni Arias"                                                                    
    ## [748] "Grupo Grameco"                                                                     
    ## [749] "Casas Colonia Inmobiliaria y Más"                                                  
    ## [750] "CreaCode Peru"                                                                     
    ## [751] "ucrop.it"                                                                          
    ## [752] "Wait N' Rest"                                                                      
    ## [753] "Policía Nacional del Perú"                                                         
    ## [754] "Universidad de Ingeniería & Tecnología - UTEC"                                     
    ## [755] "Universidad del Pacífico"                                                          
    ## [756] "Cervecería Barbarian"                                                              
    ## [757] "responsAbility Investments AG"                                                     
    ## [758] "Core Partners Perú"                                                                
    ## [759] "Café con Leche Comfy Wear"                                                         
    ## [760] "ebombo events"                                                                     
    ## [761] "NFTicket"                                                                          
    ## [762] "Pontificia Universidad Católica del Peru - PUCP"                                   
    ## [763] "LIFT - smart eats"                                                                 
    ## [764] "AYNITECH GROUP"                                                                    
    ## [765] "Koopa"                                                                             
    ## [766] "FITCO"                                                                             
    ## [767] "The Main Millennial Advisory - THEMMA"                                             
    ## [768] "Colegio Santa Maria Marianistas"                                                   
    ## [769] "Ocucaje"                                                                           
    ## [770] "FERREYCORP SAA"                                                                    
    ## [771] "JCM Management Company, Inc."                                                      
    ## [772] "Ferreycorp SAA"                                                                    
    ## [773] "Solidaridad en Marcha"                                                             
    ## [774] "Outbound Ventures"                                                                 
    ## [775] "Pear VC"                                                                           
    ## [776] "Samsung Electronics America"                                                       
    ## [777] "Katari "                                                                           
    ## [778] "The Coca-Cola Company"                                                             
    ## [779] "Meta"                                                                              
    ## [780] "Imacom EIRL"                                                                       
    ## [781] "IESE Business School"                                                              
    ## [782] "Condor Travel"                                                                     
    ## [783] "La Purita Verdad SAC"                                                              
    ## [784] "Zillow"                                                                            
    ## [785] "ESADE Business & Law School"                                                       
    ## [786] "Automotores Gildemeister SA"                                                       
    ## [787] "University of Guelph"                                                              
    ## [788] "Infotek Perú S.A.C."                                                               
    ## [789] "MESA 24/7"                                                                         
    ## [790] "Murdoch Sistemas SA"                                                               
    ## [791] "Fluyez"                                                                            
    ## [792] "Markham College"

``` r
df1 <- data.frame()

# iterate through each company and generate the edges 
for (company in unique(data$Company) ){
  
company_edges = data %>% filter(Company==company) %>% pull(index)

edges = expand.grid(company_edges, company_edges)

# remove the connections with themselves
edges = edges %>% filter(Var1 != Var2)

# append to main df1
df1 <- rbind(df1, edges)

print(dim(df1))
  
}
```

    ## [1] 0 2
    ## [1] 0 2
    ## [1] 0 2
    ## [1] 306   2
    ## [1] 306   2
    ## [1] 648   2
    ## [1] 648   2
    ## [1] 648   2
    ## [1] 660   2
    ## [1] 660   2
    ## [1] 660   2
    ## [1] 672   2
    ## [1] 672   2
    ## [1] 672   2
    ## [1] 672   2
    ## [1] 674   2
    ## [1] 676   2
    ## [1] 676   2
    ## [1] 676   2
    ## [1] 676   2
    ## [1] 676   2
    ## [1] 676   2
    ## [1] 676   2
    ## [1] 688   2
    ## [1] 688   2
    ## [1] 694   2
    ## [1] 1200    2
    ## [1] 1200    2
    ## [1] 1200    2
    ## [1] 1200    2
    ## [1] 1200    2
    ## [1] 1200    2
    ## [1] 1202    2
    ## [1] 1202    2
    ## [1] 1204    2
    ## [1] 1204    2
    ## [1] 1206    2
    ## [1] 1226    2
    ## [1] 1232    2
    ## [1] 1232    2
    ## [1] 1232    2
    ## [1] 1232    2
    ## [1] 1232    2
    ## [1] 1232    2
    ## [1] 1232    2
    ## [1] 1234    2
    ## [1] 1246    2
    ## [1] 1246    2
    ## [1] 1246    2
    ## [1] 1246    2
    ## [1] 1402    2
    ## [1] 1402    2
    ## [1] 1402    2
    ## [1] 1402    2
    ## [1] 1422    2
    ## [1] 1424    2
    ## [1] 1430    2
    ## [1] 1442    2
    ## [1] 1444    2
    ## [1] 1444    2
    ## [1] 1444    2
    ## [1] 1786    2
    ## [1] 1786    2
    ## [1] 1806    2
    ## [1] 1818    2
    ## [1] 1818    2
    ## [1] 1890    2
    ## [1] 1890    2
    ## [1] 1920    2
    ## [1] 1920    2
    ## [1] 1926    2
    ## [1] 1926    2
    ## [1] 1932    2
    ## [1] 1932    2
    ## [1] 1952    2
    ## [1] 2084    2
    ## [1] 2084    2
    ## [1] 2084    2
    ## [1] 2090    2
    ## [1] 2092    2
    ## [1] 2112    2
    ## [1] 2112    2
    ## [1] 2112    2
    ## [1] 2112    2
    ## [1] 2112    2
    ## [1] 2112    2
    ## [1] 2112    2
    ## [1] 2168    2
    ## [1] 2168    2
    ## [1] 2188    2
    ## [1] 2188    2
    ## [1] 2188    2
    ## [1] 2188    2
    ## [1] 2188    2
    ## [1] 2190    2
    ## [1] 2190    2
    ## [1] 2196    2
    ## [1] 2436    2
    ## [1] 2436    2
    ## [1] 2436    2
    ## [1] 2436    2
    ## [1] 2436    2
    ## [1] 2436    2
    ## [1] 2448    2
    ## [1] 2448    2
    ## [1] 2448    2
    ## [1] 2460    2
    ## [1] 2480    2
    ## [1] 2480    2
    ## [1] 2480    2
    ## [1] 2480    2
    ## [1] 2480    2
    ## [1] 2492    2
    ## [1] 2504    2
    ## [1] 2504    2
    ## [1] 2504    2
    ## [1] 2504    2
    ## [1] 2504    2
    ## [1] 2506    2
    ## [1] 2506    2
    ## [1] 2506    2
    ## [1] 2508    2
    ## [1] 2508    2
    ## [1] 2508    2
    ## [1] 2508    2
    ## [1] 2508    2
    ## [1] 2508    2
    ## [1] 2508    2
    ## [1] 2508    2
    ## [1] 2510    2
    ## [1] 2510    2
    ## [1] 2510    2
    ## [1] 2510    2
    ## [1] 2510    2
    ## [1] 2510    2
    ## [1] 2642    2
    ## [1] 2642    2
    ## [1] 2642    2
    ## [1] 2642    2
    ## [1] 2852    2
    ## [1] 2852    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2864    2
    ## [1] 2866    2
    ## [1] 2866    2
    ## [1] 2866    2
    ## [1] 2866    2
    ## [1] 2868    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2870    2
    ## [1] 2876    2
    ## [1] 2876    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2878    2
    ## [1] 2884    2
    ## [1] 2884    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6916    2
    ## [1] 6918    2
    ## [1] 6960    2
    ## [1] 7002    2
    ## [1] 7004    2
    ## [1] 7004    2
    ## [1] 7006    2
    ## [1] 7006    2
    ## [1] 7006    2
    ## [1] 7006    2
    ## [1] 7006    2
    ## [1] 7006    2
    ## [1] 7006    2
    ## [1] 7008    2
    ## [1] 7014    2
    ## [1] 7014    2
    ## [1] 7014    2
    ## [1] 7014    2
    ## [1] 7014    2
    ## [1] 7014    2
    ## [1] 7014    2
    ## [1] 7020    2
    ## [1] 7020    2
    ## [1] 7032    2
    ## [1] 7034    2
    ## [1] 7034    2
    ## [1] 7034    2
    ## [1] 7040    2
    ## [1] 7042    2
    ## [1] 7042    2
    ## [1] 7054    2
    ## [1] 7084    2
    ## [1] 7084    2
    ## [1] 7084    2
    ## [1] 7114    2
    ## [1] 7114    2
    ## [1] 7116    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7118    2
    ## [1] 7138    2
    ## [1] 7138    2
    ## [1] 7138    2
    ## [1] 7138    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7194    2
    ## [1] 7196    2
    ## [1] 7196    2
    ## [1] 7196    2
    ## [1] 7226    2
    ## [1] 7232    2
    ## [1] 7232    2
    ## [1] 7234    2
    ## [1] 7234    2
    ## [1] 7234    2
    ## [1] 7234    2
    ## [1] 7234    2
    ## [1] 7234    2
    ## [1] 7234    2
    ## [1] 7234    2
    ## [1] 7236    2
    ## [1] 7236    2
    ## [1] 7236    2
    ## [1] 7236    2
    ## [1] 7236    2
    ## [1] 7256    2
    ## [1] 7256    2
    ## [1] 7256    2
    ## [1] 7256    2
    ## [1] 7256    2
    ## [1] 7256    2
    ## [1] 7276    2
    ## [1] 7276    2
    ## [1] 7276    2
    ## [1] 7276    2
    ## [1] 7276    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7278    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7290    2
    ## [1] 7292    2
    ## [1] 7292    2
    ## [1] 7292    2
    ## [1] 7298    2
    ## [1] 7298    2
    ## [1] 7298    2
    ## [1] 7298    2
    ## [1] 7298    2
    ## [1] 7298    2
    ## [1] 7298    2
    ## [1] 7300    2
    ## [1] 7300    2
    ## [1] 7300    2
    ## [1] 7300    2
    ## [1] 7300    2
    ## [1] 7300    2
    ## [1] 7300    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7302    2
    ## [1] 7314    2
    ## [1] 7314    2
    ## [1] 7314    2
    ## [1] 7314    2
    ## [1] 7314    2
    ## [1] 7314    2
    ## [1] 7314    2
    ## [1] 7314    2
    ## [1] 7356    2
    ## [1] 7358    2
    ## [1] 7358    2
    ## [1] 7414    2
    ## [1] 7434    2
    ## [1] 7434    2
    ## [1] 7434    2
    ## [1] 7434    2
    ## [1] 7434    2
    ## [1] 7434    2
    ## [1] 7440    2
    ## [1] 7460    2
    ## [1] 7466    2
    ## [1] 7466    2
    ## [1] 7466    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7468    2
    ## [1] 7474    2
    ## [1] 7474    2
    ## [1] 7474    2
    ## [1] 7476    2
    ## [1] 7476    2
    ## [1] 7476    2
    ## [1] 7478    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7480    2
    ## [1] 7482    2
    ## [1] 7482    2
    ## [1] 7482    2
    ## [1] 7482    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7484    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7486    2
    ## [1] 7492    2
    ## [1] 7492    2
    ## [1] 7492    2
    ## [1] 7492    2
    ## [1] 7492    2
    ## [1] 7492    2
    ## [1] 7492    2
    ## [1] 7492    2
    ## [1] 7522    2
    ## [1] 7522    2
    ## [1] 7522    2
    ## [1] 7522    2
    ## [1] 7534    2
    ## [1] 7534    2
    ## [1] 7534    2
    ## [1] 7534    2
    ## [1] 7536    2
    ## [1] 7536    2
    ## [1] 7536    2
    ## [1] 7536    2
    ## [1] 7536    2
    ## [1] 7536    2
    ## [1] 7538    2
    ## [1] 7538    2
    ## [1] 7540    2
    ## [1] 7540    2
    ## [1] 7540    2
    ## [1] 7546    2
    ## [1] 7546    2
    ## [1] 7546    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7548    2
    ## [1] 7550    2
    ## [1] 7550    2
    ## [1] 7550    2
    ## [1] 7550    2
    ## [1] 7550    2
    ## [1] 7550    2
    ## [1] 7550    2
    ## [1] 7550    2
    ## [1] 7562    2
    ## [1] 7562    2
    ## [1] 7562    2
    ## [1] 7574    2
    ## [1] 7574    2
    ## [1] 7574    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7576    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7578    2
    ## [1] 7580    2
    ## [1] 7580    2
    ## [1] 7580    2
    ## [1] 7580    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7582    2
    ## [1] 7584    2
    ## [1] 7584    2
    ## [1] 7626    2
    ## [1] 7626    2
    ## [1] 7628    2
    ## [1] 7630    2
    ## [1] 7672    2
    ## [1] 7672    2
    ## [1] 7672    2
    ## [1] 7672    2
    ## [1] 7672    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7674    2
    ## [1] 7680    2
    ## [1] 7680    2
    ## [1] 7680    2
    ## [1] 7680    2
    ## [1] 7682    2
    ## [1] 7682    2
    ## [1] 7682    2
    ## [1] 7684    2
    ## [1] 7684    2
    ## [1] 7684    2
    ## [1] 7684    2
    ## [1] 7684    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7686    2
    ## [1] 7688    2
    ## [1] 7688    2
    ## [1] 7688    2
    ## [1] 7688    2
    ## [1] 7690    2
    ## [1] 7690    2
    ## [1] 7690    2
    ## [1] 7690    2
    ## [1] 7690    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7692    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7704    2
    ## [1] 7710    2
    ## [1] 7710    2
    ## [1] 7710    2
    ## [1] 7710    2
    ## [1] 7710    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7716    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7718    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7720    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2
    ## [1] 7722    2

``` r
# nodes = data$index
# edges = df1

df1$temp <- apply(df1, 1, function(x) paste(sort(x), collapse=""))

df1 = df1[!duplicated(df1$temp), 1:2] # remove duplicate (each combination appears once)
```

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
#install.packages('network')
library(network)
```

    ## Warning: package 'network' was built under R version 4.1.3

    ## 
    ## 'network' 1.17.1 (2021-06-12), part of the Statnet Project
    ## * 'news(package="network")' for changes since last version
    ## * 'citation("network")' for citation information
    ## * 'https://statnet.org' for help, support, and other information

``` r
linkedin_network <- network(df1, attr = data,  matrix.type = "edgelist",directed=FALSE)

linkedin_network
```

    ##  Network attributes:
    ##   vertices = 635 
    ##   directed = FALSE 
    ##   hyper = FALSE 
    ##   loops = FALSE 
    ##   multiple = FALSE 
    ##   bipartite = FALSE 
    ##   total edges= 3860 
    ##     missing edges= 0 
    ##     non-missing edges= 3860 
    ## 
    ##  Vertex attribute names: 
    ##     vertex.names 
    ## 
    ##  Edge attribute names not shown

``` r
plot(linkedin_network )
```

![](Exercise1_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

``` r
#to do: print names of nodes
```
