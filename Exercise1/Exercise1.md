Untitled
================

## Read the data

``` r
data = read.csv('Connections.csv', encoding = 'UTF-8')

data
```

    ##                              First.Name
    ## 1                               Mohamed
    ## 2                                 David
    ## 3                             Jefferson
    ## 4                                Adrian
    ## 5                                 Uzair
    ## 6                         Oscar Gabriel
    ## 7                             Alejandra
    ## 8                                Ardith
    ## 9                               Cecilia
    ## 10                              Paulina
    ## 11                                  Ali
    ## 12                              Joaquin
    ## 13                               Stefan
    ## 14                               Sandro
    ## 15                                Baris
    ## 16                          Juan Carlos
    ## 17                                Racha
    ## 18                               Delina
    ## 19                                 Lucy
    ## 20                              Claudia
    ## 21                       Maria Fernanda
    ## 22                              Fabiana
    ## 23                               Fátima
    ## 24                            Sébastien
    ## 25                               Yuvraj
    ## 26                              Anthony
    ## 27                               Adrien
    ## 28                                Jacob
    ## 29                               Saibal
    ## 30                              Arantza
    ## 31                             Immanuel
    ## 32                              Mohssen
    ## 33                             Chunshan
    ## 34                              Hossein
    ## 35                             Abhijeet
    ## 36                             Kushagra
    ## 37                              Patrick
    ## 38                               Triana
    ## 39                            Christian
    ## 40                            Alexandre
    ## 41                            Elisabeth
    ## 42                                Tehut
    ## 43                               Ny Ony
    ## 44                                Nehal
    ## 45                               Joseph
    ## 46                             Santiago
    ## 47                              Antoine
    ## 48                                 Luka
    ## 49                               Alonso
    ## 50                             Shahriar
    ## 51                               Renato
    ## 52                                Ariel
    ## 53                                 Dave
    ## 54                      Martin Santiago
    ## 55                                 Luis
    ## 56                                   Ed
    ## 57                                Mohit
    ## 58                               Julián
    ## 59                                Percy
    ## 60                               Marita
    ## 61                             Fernando
    ## 62                              Rodrigo
    ## 63                               Mingyi
    ## 64                                 Jack
    ## 65                                Julie
    ## 66                                  Jan
    ## 67                               Zhijia
    ## 68                              Rebecca
    ## 69                      David Christian
    ## 70                                Benny
    ## 71                          Jose Emilio
    ## 72                               Alexia
    ## 73                            Antonella
    ## 74                              Lorenzo
    ## 75                              Ricardo
    ## 76                              Mathias
    ## 77                                  Joy
    ## 78                             Shivangi
    ## 79                               Fatima
    ## 80                              Gonzalo
    ## 81                            Francesca
    ## 82                                 Alex
    ## 83                        Bilguun (Bil)
    ## 84                           Yue(Chris)
    ## 85                                Foteh
    ## 86                               Thomas
    ## 87                                 Jake
    ## 88                              Alfonso
    ## 89                                Pedro
    ## 90                                Félix
    ## 91                               Melany
    ## 92                   Christophe Seiichi
    ## 93                              Vaibhav
    ## 94                                Islem
    ## 95                       Gabriel Victor
    ## 96                             Vittoria
    ## 97                                 Nima
    ## 98                                Yanda
    ## 99                       Zheyuan (Joey)
    ## 100                              Yichen
    ## 101                             Sundeep
    ## 102                           Madeleine
    ## 103                              Camila
    ## 104                          Alessandra
    ## 105                            Carolina
    ## 106                                Yuqi
    ## 107                                Matt
    ## 108                        Miguel Angel
    ## 109                              Monika
    ## 110                               Scott
    ## 111                             Clement
    ## 112                             Charles
    ## 113                              Nadine
    ## 114                               Javad
    ## 115                             Animesh
    ## 116                              Audrey
    ## 117                              Agathe
    ## 118                            Almudena
    ## 119                                Thal
    ## 120                             Morgane
    ## 121                             Esteban
    ## 122                              Samuel
    ## 123                              Duncan
    ## 124                               Hanna
    ## 125                              Maxime
    ## 126                                Alya
    ## 127                             Mathieu
    ## 128                         Oludamilola
    ## 129                           Valentina
    ## 130                     Luisa Fernanda 
    ## 131                           Joséphine
    ## 132                           Francesca
    ## 133                               Xinyi
    ## 134                            Jingyuan
    ## 135                              Mesaye
    ## 136                                 Ram
    ## 137                              Apoorv
    ## 138                               Rifat
    ## 139                                Anku
    ## 140                              Hadyan
    ## 141                            Mariapia
    ## 142                             Daniela
    ## 143                              Nathan
    ## 144                             Micaela
    ## 145                              Bogdan
    ## 146                               Warut
    ## 147                               Senan
    ## 148                               Marek
    ## 149                               Jules
    ## 150                               Kexin
    ## 151                            Vivianne
    ## 152                             Sanchit
    ## 153                           Yi (Zora)
    ## 154                            Fernando
    ## 155                              Roxana
    ## 156                               Paula
    ## 157                           Jean Paul
    ## 158                              Sergio
    ## 159                             Gabriel
    ## 160                                Andi
    ## 161                            Cristina
    ## 162                                  Yu
    ## 163                              Elaine
    ## 164                          Hirdyanshu
    ## 165                              Daniel
    ## 166                             Antonia
    ## 167                              Steven
    ## 168                            Cristina
    ## 169                             Michela
    ## 170                  Cheok Ieng (Betty)
    ## 171                              Mehmet
    ## 172                             Kenneth
    ## 173                                  Di
    ## 174                           Aishwarya
    ## 175                               Rocío
    ## 176                               Scott
    ## 177                            Shehryar
    ## 178                                Luis
    ## 179                                Jose
    ## 180                               Kexin
    ## 181                         Deyvis Raúl
    ## 182                             Jessica
    ## 183                               Nupur
    ## 184                               Luren
    ## 185                              Matías
    ## 186                               Mateo
    ## 187                         Juan Camilo
    ## 188                      Yiming(Vivian)
    ## 189                               Mehdi
    ## 190                            Anukriti
    ## 191                          Shubanghni
    ## 192                              Pascal
    ## 193                              Aditya
    ## 194                             William
    ## 195                             Rodrigo
    ## 196                                Ramy
    ## 197                    Junxiang (Eldon)
    ## 198                            Maguette
    ## 199                              Johnny
    ## 200                               Noman
    ## 201                      Matías Esteban
    ## 202                        Miguel Angel
    ## 203                     Sebastián Jesús
    ## 204                            Mauricio
    ## 205                         María Luisa
    ## 206                               César
    ## 207                              Alvaro
    ## 208                             Pranesh
    ## 209                      Luiggi Agustin
    ## 210                               Nilva
    ## 211                            Nicolás 
    ## 212                        SVEC TRADING
    ## 213                               Jorge
    ## 214                                Finn
    ## 215                              Andrea
    ## 216                                Omar
    ## 217                       Beiqi (Becky)
    ## 218                          Katherine 
    ## 219                             Mounira
    ## 220                               Richa
    ## 221                              Nikhil
    ## 222                          Jose Mario
    ## 223                                Reza
    ## 224                               Cindy
    ## 225                              Jingyu
    ## 226                             Gayatri
    ## 227                             Gautami
    ## 228                              Carlos
    ## 229                               Alice
    ## 230                               Vahid
    ## 231                                Keel
    ## 232                               Mehdi
    ## 233                             Winston
    ## 234                              Marion
    ## 235                 Zhiyuan (Christina)
    ## 236                   Corrine (Yingxin)
    ## 237                            Isabella
    ## 238                             Rodrigo
    ## 239                               Louis
    ## 240                               Hirad
    ## 241                              Hisham
    ## 242                             Rosanna
    ## 243                       Anqi (Angela)
    ## 244                               Siraj
    ## 245                            Matthieu
    ## 246                          Alessandra
    ## 247                                Ziye
    ## 248                              Smitul
    ## 249                           Shivanshu
    ## 250                              Roopin
    ## 251                           Aishwarya
    ## 252                               Arpit
    ## 253                           Alejandra
    ## 254                               Kelly
    ## 255                               Nancy
    ## 256                           Zhi Cheng
    ## 257                                Dany
    ## 258                            Cayetana
    ## 259                             Antonio
    ## 260                             Mariana
    ## 261                             Arunima
    ## 262                               Diwei
    ## 263                               Atrin
    ## 264                              Ananya
    ## 265                        Juan Eduardo
    ## 266                             Solomon
    ## 267                                Hugo
    ## 268                              Haydee
    ## 269                               Ilias
    ## 270                             Alfonso
    ## 271                                Oleg
    ## 272                             Matthew
    ## 273                              Alexis
    ## 274                             Mohamad
    ## 275                             Chelsea
    ## 276                               Peter
    ## 277                               Pablo
    ## 278                           Alexandra
    ## 279                             Valeria
    ## 280                             Michael
    ## 281                                Saad
    ## 282                                Hugo
    ## 283                             Rodrigo
    ## 284                              Alvaro
    ## 285                             Nicolas
    ## 286                            Daniella
    ## 287                              Pierre
    ## 288                            Milagros
    ## 289                             Fabiana
    ## 290                            Catalina
    ## 291                              Meiker
    ## 292                               ANGEL
    ## 293                         Julio Cesar
    ## 294                                Ana 
    ## 295                              Rafael
    ## 296                              Ursula
    ## 297                             Antonio
    ## 298                               Jimmy
    ## 299                           Katherine
    ## 300                              Felipe
    ## 301                       Maria Isabel 
    ## 302                           Salvatore
    ## 303                               Fabio
    ## 304                                Luis
    ## 305                              Camila
    ## 306                               David
    ## 307                           Sebastian
    ## 308                              Ariana
    ## 309                              Ursula
    ## 310                      Gabriela María
    ## 311                           Sebastian
    ## 312                        José Antonio
    ## 313                             Mariana
    ## 314                      Carlos Eduardo
    ## 315                     Rodrigo Alfonso
    ## 316                         José Miguel
    ## 317                            Salvador
    ## 318                             Rodrigo
    ## 319                          Geanfranco
    ## 320                          Maria Jose
    ## 321                             Lourdes
    ## 322                               Marco
    ## 323                             Valeria
    ## 324                        Jimmy George
    ## 325                            Nathalie
    ## 326                             Ignacio
    ## 327                              Evelin
    ## 328                              Carlos
    ## 329                         Juan Carlos
    ## 330                      Carlos Alberto
    ## 331                              Sergio
    ## 332                         Juan Carlos
    ## 333                            Gabriela
    ## 334                              Flavia
    ## 335                           Alexandra
    ## 336                             Valeria
    ## 337                            Devanshu
    ## 338                        Juan Antonio
    ## 339                                Nain
    ## 340                             Alfonso
    ## 341                             Barbara
    ## 342                           Alexandra
    ## 343                             Valeria
    ## 344                               Diego
    ## 345                             Valeria
    ## 346                            Isabella
    ## 347                             Gonzalo
    ## 348                              Nicole
    ## 349                               Franz
    ## 350                              Mehmet
    ## 351                              Pamela
    ## 352                          Juan Diego
    ## 353                               Ruben
    ## 354                             Ricardo
    ## 355                            Santiago
    ## 356                              Vannia
    ## 357                               Fabia
    ## 358                      Matias Eduardo
    ## 359                         Maria Jose 
    ## 360                           Alejandro
    ## 361                             Mariana
    ## 362                             Ignacio
    ## 363                         José Carlos
    ## 364                              Daniel
    ## 365                               Pável
    ## 366                       Luis Fernando
    ## 367                             Gabriel
    ## 368                               Marco
    ## 369                       Carlos Andrés
    ## 370                             Nicolás
    ## 371                         Juan Carlos
    ## 372                             Adriana
    ## 373                              Vanesa
    ## 374                               Thais
    ## 375                               Angel
    ## 376                           Alejandro
    ## 377                             Antonio
    ## 378                               Irvin
    ## 379                               Laura
    ## 380                             Rodrigo
    ## 381                               Shoeb
    ## 382                           Sebastian
    ## 383                              Jackie
    ## 384                     Roberto Alfredo
    ## 385                          Ingeniería
    ## 386                           José Luis
    ## 387                         Jose Alonso
    ## 388                              Marina
    ## 389                              Brenda
    ## 390                              Hanjia
    ## 391                           Maria Luz
    ## 392                       William Jacob
    ## 393                             Mariana
    ## 394                                Lisa
    ## 395                             Joaquin
    ## 396                             Gustavo
    ## 397                     Francisco Mauro
    ## 398                              Ximena
    ## 399                               Diego
    ## 400                          María José
    ## 401                                Alex
    ## 402                           Boon Thau
    ## 403                               Emrah
    ## 404                              Ariana
    ## 405                            Rafaella
    ## 406                               Bruno
    ## 407                               Jimmy
    ## 408                              Samuel
    ## 409                  Enrique Basauri Q.
    ## 410                               Bruno
    ## 411                               Paula
    ## 412                             Ricardo
    ## 413                              Alvaro
    ## 414                             Gustavo
    ## 415                             Daniela
    ## 416                            Jason H.
    ## 417                             Charles
    ## 418                               Selah
    ## 419                       Benjamin Jose
    ## 420                               Chris
    ## 421                              Andrea
    ## 422                              Alonso
    ## 423                        Maria Clelia
    ## 424                              Konrad
    ## 425                             Joaquin
    ## 426                             Ibrahim
    ## 427                             Rafaela
    ## 428                             Nicolle
    ## 429                               Zihan
    ## 430                               Kevin
    ## 431                            Fernando
    ## 432                        Jose Antonio
    ## 433                              Karlos
    ## 434                              Mridul
    ## 435                            Santiago
    ## 436                            Santiago
    ## 437                             Enrique
    ## 438                Cecilia Perla Isabel
    ## 439                                Jose
    ## 440                           Sebastian
    ## 441                               Mateo
    ## 442                        Maria Gracia
    ## 443                          Alessandro
    ## 444                               Wendy
    ## 445                            Jonathan
    ## 446                                Luis
    ## 447                             Braulio
    ## 448                              Marcos
    ## 449                              Ramiro
    ## 450                               Kevin
    ## 451                                Tien
    ## 452                               Marko
    ## 453                               Mohit
    ## 454                            Andreina
    ## 455                               Lucia
    ## 456                          Juan Diego
    ## 457                               Harry
    ## 458                               Zinan
    ## 459                             Gabriel
    ## 460                                Jack
    ## 461                              Gastón
    ## 462                              Paloma
    ## 463                              Álvaro
    ## 464                              Melany
    ## 465                            Williams
    ## 466                             Nicolás
    ## 467                            Santiago
    ## 468                            Gabriela
    ## 469                              Arturo
    ## 470                               Jorge
    ## 471                            Milagros
    ## 472                            Geofret 
    ## 473                                 Ken
    ## 474                              David 
    ## 475                              Andrea
    ## 476                             Gonzalo
    ## 477                     Ignacio Nicolas
    ## 478                              Noelia
    ## 479                            Lucciano
    ## 480                            Williams
    ## 481                               Nancy
    ## 482                           Alexander
    ## 483                             Gustavo
    ## 484  Comunidad de Analytics Translators
    ## 485                     Astrid Carolina
    ## 486                              Joshua
    ## 487                           Guillermo
    ## 488                               Jorge
    ## 489                             Rodrigo
    ## 490                       Cesar Mariano
    ## 491                               Diego
    ## 492                             Marcela
    ## 493                            Fernando
    ## 494                              Miguel
    ## 495                               Tomás
    ## 496                              Alonso
    ## 497                               Jesus
    ## 498                      Christian Jose
    ## 499                             Gonzalo
    ## 500                           Sebastián
    ## 501                              Sandra
    ## 502                         Jaime Angel
    ## 503                                Aldo
    ## 504                            Fernando
    ## 505                          Alessandra
    ## 506                           Cristhian
    ## 507                            Greghory
    ## 508                              Mirian
    ## 509                              Manuel
    ## 510                      Miriam Valeria
    ## 511                             Valeria
    ## 512                             Michael
    ## 513                            Gianluca
    ## 514                             Stefano
    ## 515                               Diego
    ## 516                               Josue
    ## 517                             Jacques
    ## 518                              Andres
    ## 519                          Juan Diego
    ## 520                               Sayem
    ## 521                               Diego
    ## 522                            Carolina
    ## 523                                Mike
    ## 524                             Daniela
    ## 525                               Alexa
    ## 526                     Evelyn Yessenia
    ## 527                              Víctor
    ## 528                            Mauricio
    ## 529                          Juan Diego
    ## 530                     Muhammad Kamran
    ## 531                          Alessandro
    ## 532                            Nathalie
    ## 533                             Gonzalo
    ## 534                              Alexis
    ## 535                                 Tim
    ## 536                           Alonso M.
    ## 537                            Mauricio
    ## 538                               Juhii
    ## 539                           Sebastián
    ## 540                               Arpit
    ## 541                          Gianfranco
    ## 542                               Luisa
    ## 543                              David 
    ## 544                              Jeremy
    ## 545                            Brigitte
    ## 546                               Bruno
    ## 547                              Alonso
    ## 548                             Jessica
    ## 549                            Humberto
    ## 550                           Ana Lucía
    ## 551                              Martin
    ## 552                              Alonso
    ## 553                              Alicia
    ## 554                     Eduardo Antonio
    ## 555                               Diana
    ## 556                              Andrés
    ## 557                               Nancy
    ## 558                       Alicia Karina
    ## 559                            Santiago
    ## 560                          María Dina
    ## 561                           Guillermo
    ## 562                             Daniela
    ## 563                              Emilio
    ## 564                           Sebastián
    ## 565                             Nicolas
    ## 566                             Melissa
    ## 567                              Emilio
    ## 568                                    
    ## 569                                Ivan
    ## 570                            Santiago
    ## 571                              Apefam
    ## 572                      Carlos Alberto
    ## 573                               David
    ## 574                         Juan Carlos
    ## 575                              Alonso
    ## 576                              Matías
    ## 577                             Mosalam
    ## 578                              Triana
    ## 579                              Isabel
    ## 580                              Andrés
    ## 581                             Mariano
    ## 582                             Larissa
    ## 583                               Diego
    ## 584                              Andrew
    ## 585                             Stefano
    ## 586                         Jorge Mario
    ## 587                                Paúl
    ## 588                    Claudia Lastrera
    ## 589                             Nicolle
    ## 590                              Miguel
    ## 591                            Esteban 
    ## 592                         Juan Manuel
    ## 593                            Mauricio
    ## 594                     Ronald Antonio 
    ## 595                             Joaquin
    ## 596                               Lucas
    ## 597                               Renzo
    ## 598                              Thomas
    ## 599                              Camila
    ## 600                           Maria Paz
    ## 601                            Fabrizio
    ## 602                               Rexvi
    ## 603                               Angel
    ## 604                             Gonzalo
    ## 605                           Francisco
    ## 606                              Stuart
    ## 607                             Roberto
    ## 608                      Anghelo Moisés
    ## 609                             Rodrigo
    ## 610                 JOSE MARIA NAZARETH
    ## 611                 <U+0001F6E9> Andres
    ## 612                                Omar
    ## 613                              Andrea
    ## 614                      Maria Fernanda
    ## 615                   Giovanna Guissela
    ## 616                        Luis Enrique
    ## 617                             William
    ## 618                           Alejandra
    ## 619                              Ariana
    ## 620                             Kremlin
    ## 621                              Eileen
    ## 622                               Arpit
    ## 623                              Marcos
    ## 624                               Deisy
    ## 625                        Eduardo José
    ## 626                              Justin
    ## 627                     María Guadalupe
    ## 628                               David
    ## 629                              Mónica
    ## 630                    Daniel Alexandro
    ## 631                             Valeria
    ## 632                               Belen
    ## 633                             Carmina
    ## 634                             Micaela
    ## 635                            Fernando
    ## 636                            Stefania
    ## 637                             Natalie
    ## 638                       Marco Antonio
    ## 639                             Daniela
    ## 640                               Vatul
    ## 641                              Bianca
    ## 642                               Mayra
    ## 643                               André
    ## 644                                Raul
    ## 645                              Ariana
    ## 646                           Ana-Lucía
    ## 647                             Cecilia
    ## 648                             Ricardo
    ## 649                          Alessandra
    ## 650                             Luciana
    ## 651                               Ankur
    ## 652                            Milagros
    ## 653                               César
    ## 654                         Juan Carlos
    ## 655                               Mateo
    ## 656                             Jasmina
    ## 657                             Deborah
    ## 658                                Luis
    ## 659                             Mariana
    ## 660                    Mayly Alessandra
    ## 661                               Renzo
    ## 662                             Gustavo
    ## 663                             Valeria
    ## 664                     José del Carmen
    ## 665                               Mateo
    ## 666                        Luis Ernesto
    ## 667                              Zayuri
    ## 668                             Ricardo
    ## 669                             Enrique
    ## 670                             Alberto
    ## 671                          Rodrigo E.
    ## 672                               Jaime
    ## 673                             Rodrigo
    ## 674                              Carlos
    ## 675                               Josue
    ## 676                                Yoel
    ## 677                           Alejandra
    ## 678                             Douglas
    ## 679                        Miguel André
    ## 680                              Evelyn
    ## 681                          Gian-André
    ## 682                              Alisia
    ## 683                             Joaquín
    ## 684                             Manuela
    ## 685                             Douglas
    ## 686                     Jonathan Stiven
    ## 687                              Alvaro
    ## 688                             Micaela
    ## 689                                Iván
    ## 690                         Juan Carlos
    ## 691                               César
    ## 692                               Jesus
    ## 693                             Ricardo
    ## 694                            Jonathan
    ## 695                             Leandro
    ## 696                            Bernardo
    ## 697                         Luis Carlos
    ## 698                     Jesús Alejandro
    ## 699                       Marco Antonio
    ## 700                       Robert Alonso
    ## 701                           Sebastian
    ## 702                               Italo
    ## 703                               Rahul
    ## 704                              Rafael
    ## 705                              Andres
    ## 706                           Guillermo
    ## 707                               Jorge
    ## 708                             Lorenzo
    ## 709                              Martin
    ## 710                            Fernando
    ## 711                    Alejandro Javier
    ## 712                               Moshe
    ## 713                             Rodrigo
    ## 714                             Valeria
    ## 715                               Cesar
    ## 716                           Serenella
    ## 717                      Manuel Enrique
    ## 718                             Ricardo
    ## 719                               Paola
    ## 720                               Lucas
    ## 721                                Iain
    ## 722                             William
    ## 723                               Nipza
    ## 724                      Marcos Vinicio
    ## 725                            Mauricio
    ## 726                                Rana
    ## 727                             Deborah
    ## 728                              Miguel
    ## 729                               Erich
    ## 730                              Miguel
    ## 731                           Max Renzo
    ## 732                               Pilar
    ## 733                             Enrique
    ## 734                             Natalia
    ## 735                             Mariana
    ## 736                               Pablo
    ## 737                              Matias
    ## 738                               Yoshi
    ## 739                              Martin
    ## 740                              Víctor
    ## 741                               Kevin
    ## 742                              Andrea
    ## 743                             Roberto
    ## 744                              Fabian
    ## 745                                Jose
    ## 746                             Karthik
    ## 747                           Gianmarco
    ## 748                             Claudio
    ## 749                       Aditya Pratap
    ## 750                              Jimena
    ## 751                            Natiuska
    ## 752                    Clidford Orlando
    ## 753                             Stefany
    ## 754                                Luis
    ## 755                                Juan
    ## 756                                  JP
    ## 757                              Danilo
    ## 758                              Carlos
    ## 759                              Martín
    ## 760                                Adam
    ## 761                               Jorge
    ## 762                              Wander
    ## 763                             Lorenzo
    ## 764                              Rafael
    ## 765                           Alejandro
    ## 766                           Alejandra
    ## 767                           Fabrizzio
    ## 768                              Alvaro
    ## 769                                Luis
    ## 770                                 Joy
    ## 771                        Manuel Pablo
    ## 772                             Antonio
    ## 773                             Luciana
    ## 774                            Isabella
    ## 775                             Edmundo
    ## 776                   Alejandro Gabriel
    ## 777                             Ignacio
    ## 778                                Alex
    ## 779                      Martín Horacio
    ## 780                               Lucia
    ## 781                           Sebastian
    ## 782                             Rodrigo
    ## 783                            Fernando
    ## 784                        Jose Alberto
    ## 785                           Sebastian
    ## 786                            Santiago
    ## 787                             Rodrigo
    ## 788                               Diego
    ## 789                                Paul
    ## 790                              Sergio
    ## 791                             Gustavo
    ## 792                              Dannia
    ## 793                             Alfredo
    ## 794                              Felipe
    ## 795                              Carlos
    ## 796                            Verónica
    ## 797                             Mariana
    ## 798                             Michael
    ## 799                           Valentina
    ## 800                           Alejandra
    ## 801                      Johnny Leandro
    ## 802                             Amarely
    ## 803                              Nicole
    ## 804                              Roxana
    ## 805                       Vanessa Laura
    ## 806                               Diego
    ## 807                                Luis
    ## 808                      Maria Fernanda
    ## 809                              Sandra
    ## 810                              Carlos
    ## 811                         Jordi Lluis
    ## 812                             Antonio
    ## 813                           Ana Lucía
    ## 814                              Javier
    ## 815                            Nathalia
    ## 816                    Carlos Sebastián
    ## 817                              Maggie
    ## 818                               Diego
    ## 819                              Ximena
    ## 820                              Sandra
    ## 821                               Oscar
    ## 822                           Alejandra
    ## 823                              Martín
    ## 824                               Andre
    ## 825                             Ricardo
    ## 826                      Leticia Roxana
    ## 827                             Joselin
    ## 828                           Lucia Ana
    ## 829                                Iván
    ## 830                              Daniel
    ## 831                            Macarena
    ## 832                           Francesca
    ## 833                              Briana
    ## 834                              Selina
    ## 835                           Alejandro
    ## 836                           Juan José
    ## 837                             Alfredo
    ## 838                              Chiara
    ## 839                              Milton
    ## 840                                Bram
    ## 841                  Stephany Alexandra
    ## 842                              Sandra
    ## 843                             Gabriel
    ## 844                          María Inés
    ## 845                              Rollin
    ## 846                              Daniel
    ## 847                               Jimmy
    ## 848                              Karina
    ## 849                               David
    ## 850                            Vladimir
    ## 851                        Sandra Roman
    ## 852                Instituto deFinanzas
    ## 853                               Diego
    ## 854                 Tomás de Villanueva
    ## 855                               Sarah
    ## 856                             Gabriel
    ## 857                       Luis Fernando
    ## 858                               Renzo
    ## 859                           Sebastian
    ## 860                              Alonso
    ## 861                                Erik
    ## 862                              Franco
    ## 863                            Nicholas
    ## 864                               Jenry
    ## 865                               Diego
    ## 866                             Johanna
    ## 867                     Diego Francisco
    ## 868                             Gerardo
    ## 869                              Venkat
    ## 870                              Nicola
    ## 871                             Alberto
    ## 872                              Ximena
    ## 873                            Patricio
    ## 874                             Enrique
    ## 875                             William
    ## 876                            Philippe
    ## 877                             Rodrigo
    ## 878                             Micaela
    ## 879                               David
    ## 880                               Paula
    ## 881                               Tomás
    ## 882                             Ernesto
    ## 883                           Alejandro
    ## 884                      Claudia Isabel
    ## 885                                Aron
    ## 886                         Maria Paula
    ## 887                             Arantxa
    ## 888                      Andrea Valeria
    ## 889                           Guillermo
    ## 890                              Andrea
    ## 891                            Fernanda
    ## 892                             Gonzalo
    ## 893                              Lukasz
    ## 894                            Cristina
    ## 895                              Carlos
    ## 896                              Silvia
    ## 897                           Iván José
    ## 898                           Sebastián
    ## 899                               Mateo
    ## 900                       Mag. Fernando
    ## 901                              Daniel
    ## 902                             Nicolas
    ## 903                              Marcos
    ## 904                              Andres
    ## 905                           Francisco
    ## 906                           Jose Luis
    ## 907                          Juan David
    ## 908                           Guillermo
    ## 909                        Everth Roman
    ## 910                               César
    ## 911                           Sebastian
    ## 912                             Gonzalo
    ## 913                               Thaiz
    ## 914                              Isaias
    ## 915                                Rosa
    ## 916                          John Franz
    ## 917                            Fernando
    ## 918                                 Ely
    ## 919                                Numa
    ## 920                            Patricia
    ## 921                               Bruno
    ## 922                               Marco
    ## 923                      Javier Richard
    ## 924                              Lorena
    ## 925                               Pavel
    ## 926                               Lucia
    ## 927                              Javier
    ## 928                              Jairo 
    ## 929                             Enrique
    ## 930                          Luis Jesús
    ## 931                              Daniel
    ## 932                             Gabriel
    ## 933                              Carlos
    ## 934                                Alex
    ## 935                             Claudia
    ## 936                              Sergio
    ## 937                             Claudia
    ## 938                      Jeyson William
    ## 939                             Orlando
    ## 940                          Maria Jose
    ## 941                       Cesar Augusto
    ## 942                               Boris
    ## 943                              Daniel
    ## 944                               Zarko
    ## 945                               Mateo
    ## 946                                Aldo
    ## 947                           Sebastian
    ## 948                          Alessandra
    ## 949                             Niccolo
    ## 950                           Francisco
    ## 951                             Luciana
    ## 952                         Maria Laura
    ## 953                              Lucero
    ## 954                             Micaela
    ## 955                             Nicolle
    ## 956                             Horacio
    ## 957                         Hans Marlon
    ## 958                         Henry Pablo
    ## 959                              Freddy
    ## 960                               Karla
    ## 961                               Renzo
    ## 962                              Daphne
    ## 963                       Manuel Andres
    ## 964                               Diego
    ## 965                             Alfonso
    ## 966                            Mauricio
    ## 967                      Eduardo Andres
    ## 968                               David
    ## 969                        Miguel Angel
    ## 970                                Mary
    ## 971                              Jhonny
    ## 972                               Elvis
    ## 973                                Alan
    ## 974                       Daniel Martin
    ## 975                             Rodolfo
    ## 976                             Trixcia
    ## 977                             Rolando
    ## 978                              Grecia
    ## 979                             Kenneth
    ## 980                           John Paul
    ## 981                          Diego León
    ## 982                           Katherine
    ## 983                         Kurt Walter
    ## 984                             william
    ## 985                                Luis
    ## 986                             Gonzalo
    ## 987                                    
    ## 988                     Melanie Valeria
    ## 989                          Gianfranco
    ## 990                                Luis
    ## 991                               Renán
    ## 992                              Néstor
    ## 993                              Carlos
    ## 994                      MBA CPC Walter
    ## 995                               David
    ## 996                              Fabian
    ## 997                     Javier Hernando
    ## 998                               Julio
    ## 999                             Mariana
    ## 1000                            Leoncio
    ## 1001                  Cesar Bustamante,
    ## 1002                        María Belén
    ## 1003                              Angel
    ## 1004                              Lilia
    ## 1005                             Winder
    ## 1006                             Carlos
    ## 1007                             Janete
    ## 1008                            Alberto
    ## 1009                      Luis Humberto
    ## 1010                            Henning
    ## 1011                             Camila
    ## 1012                          Francisco
    ## 1013                     Juan Francisco
    ## 1014                              Cesar
    ## 1015                             Isabel
    ## 1016                            Valeria
    ## 1017                   Lizeth Alexandra
    ## 1018                              Jorge
    ## 1019                            Alessio
    ## 1020                            Claudio
    ## 1021                            Ricardo
    ## 1022                             Ronnie
    ## 1023                           Jheysson
    ## 1024                             Jobian
    ## 1025                             Elias 
    ## 1026                              Elena
    ## 1027                      Miguel Alonso
    ## 1028                             Carlos
    ## 1029                        Diego André
    ## 1030                             Manuel
    ## 1031                            Claudia
    ## 1032                           Vladimir
    ## 1033                               Jose
    ## 1034                              Diego
    ## 1035                         Jorge Luis
    ## 1036                            Jessica
    ## 1037                          Sebastian
    ## 1038                             Miguel
    ## 1039                        Juan Manuel
    ## 1040                               Sven
    ## 1041                              Anush
    ## 1042                             Branko
    ## 1043                            Nicolas
    ## 1044                              Ronan
    ## 1045                            Augusto
    ## 1046                             Alvaro
    ## 1047                        Luis Carlos
    ## 1048                      Eduardo Andre
    ## 1049                             Alvaro
    ## 1050                      Diego Gonzalo
    ## 1051                            Marcelo
    ## 1052                             Chiara
    ## 1053                            Stefano
    ## 1054                             Martin
    ## 1055                             Walter
    ## 1056                       Manuel David
    ## 1057                               Luis
    ## 1058                              Jorge
    ## 1059                          Francisco
    ## 1060                            Cecilia
    ## 1061                            Vanessa
    ## 1062                           Daniella
    ## 1063                              Diego
    ## 1064                            Marcelo
    ## 1065                       José Rodrigo
    ## 1066                            Rodrigo
    ## 1067                            Nicolas
    ## 1068                             Camila
    ## 1069                      César Ernesto
    ## 1070                              Karen
    ## 1071                          Francisco
    ## 1072                             Daniel
    ## 1073                       María Gracia
    ## 1074                              Ágata
    ## 1075                              Tarek
    ## 1076                            Gabriel
    ## 1077                           Bernardo
    ## 1078                           Pablo J.
    ## 1079                        JOSE CARLOS
    ## 1080                             Isaias
    ## 1081                               Jose
    ## 1082                               José
    ## 1083                            Nicolás
    ## 1084                            Rodrigo
    ## 1085                             Alonso
    ## 1086                             Andrea
    ## 1087                             Hector
    ## 1088                             Andrés
    ## 1089                     Alvaro Gustavo
    ## 1090                             Ximena
    ## 1091                             Carola
    ## 1092                              Jorge
    ## 1093                            Daniela
    ## 1094                             Sergio
    ## 1095                             Silvia
    ## 1096                              Mario
    ## 1097                             Renato
    ## 1098                        Jose Israel
    ## 1099                             Manuel
    ## 1100                          Christian
    ## 1101                              Piero
    ## 1102                         Juan David
    ## 1103                               Luis
    ## 1104                              Brian
    ## 1105                      Lee Alexander
    ## 1106                              Kevin
    ## 1107                            Stefano
    ## 1108                          Alejandro
    ## 1109                          Sebastian
    ## 1110                             Carlos
    ## 1111                          Maria Paz
    ## 1112                          Florencia
    ## 1113                             Renato
    ## 1114                          Sebastián
    ## 1115                      Gustavo André
    ## 1116                          Francisco
    ## 1117                             Daniel
    ## 1118                             Matías
    ## 1119                          Francesca
    ## 1120                      Nadia Nathaly
    ## 1121                           Milagros
    ## 1122                            Gonzalo
    ## 1123                           Reynaldo
    ## 1124                             Andres
    ## 1125                          Alejandro
    ## 1126                              Fabio
    ## 1127                             Mariel
    ## 1128                           MARIELLY
    ## 1129                              Robby
    ## 1130                          Maria Luz
    ## 1131                             Junior
    ## 1132                           Dionicio
    ## 1133                      Marco Antonio
    ## 1134                              Jonny
    ## 1135                          Grover H.
    ## 1136                              Nadia
    ## 1137                             Camila
    ## 1138                             Andres
    ## 1139                             Sergio
    ## 1140                            Marcelo
    ## 1141                              Elias
    ## 1142                         Juan Pablo
    ## 1143               Michael Christian R.
    ## 1144                            Aldair 
    ## 1145                             Geider
    ## 1146                      Marco Antonio
    ## 1147                            Augusto
    ## 1148                              Elena
    ## 1149                              David
    ## 1150                             Andrea
    ## 1151                          Cristian 
    ## 1152                              Jason
    ## 1153                              Julio
    ## 1154                            Nicolas
    ## 1155                             Oscar 
    ## 1156                              Bryan
    ## 1157                              Marco
    ## 1158                            Valeria
    ## 1159                              Diego
    ## 1160                            Rodrigo
    ## 1161                         Edgardo J.
    ## 1162                               Ryan
    ## 1163                             Emilio
    ## 1164                             Werner
    ## 1165                             Alonso
    ## 1166                              Mateo
    ## 1167                           Mauricio
    ## 1168                            Adriana
    ## 1169                             Carlos
    ## 1170                              Diego
    ## 1171                           Gabriela
    ## 1172                           Victoria
    ## 1173                            Nicolas
    ## 1174                             Alvaro
    ## 1175                      Jorge Hiroshi
    ## 1176                            Nicolás
    ## 1177                             Manuel
    ## 1178                             Ursula
    ## 1179                              Erick
    ## 1180                           Maurizio
    ## 1181                    María Alejandra
    ## 1182                              Karin
    ## 1183                             Daniel
    ## 1184                            Dolores
    ## 1185                          Cutter J.
    ## 1186                          Alexander
    ## 1187                           Norberto
    ## 1188                          Sebastian
    ## 1189                          Francisco
    ## 1190                               Juan
    ## 1191                              Karlo
    ## 1192                            Rodrigo
    ## 1193                            Marcelo
    ## 1194                              Pablo
    ## 1195                           EMPRENDE
    ## 1196                             Sergio
    ## 1197                            Joaquín
    ## 1198                            Gonzalo
    ## 1199                              Oscar
    ## 1200                              Paolo
    ## 1201                            Esteban
    ## 1202                              Jorge
    ## 1203                             Rafael
    ## 1204                             Manuel
    ## 1205                    Giovanni Miguel
    ## 1206                             Franco
    ## 1207                             Daniel
    ## 1208                            Rodrigo
    ## 1209                              Antar
    ## 1210                         Juan Diego
    ## 1211                           Eidelman
    ## 1212                      Carlos Daniel
    ## 1213                             Duilio
    ## 1214                             Adolfo
    ## 1215                            Joaquín
    ## 1216                           Michelle
    ## 1217                               Luis
    ## 1218                               Jose
    ## 1219                              Mario
    ## 1220                          Alejandro
    ## 1221                            Ignacio
    ## 1222                          Sebastián
    ## 1223                         Alessandro
    ## 1224                             Miguel
    ## 1225                             Carlos
    ## 1226                           Fernanda
    ## 1227                            Claudio
    ## 1228                         Dr. Javier
    ## 1229                            Gonzalo
    ## 1230                             Franco
    ## 1231                           Santiago
    ## 1232                               Hugo
    ## 1233                             Andrés
    ## 1234                            Valeria
    ## 1235                             Carlos
    ## 1236                            Lorenzo
    ## 1237                        Maria Laura
    ## 1238                             Andrés
    ## 1239                          Francisco
    ## 1240                             Manuel
    ## 1241                            Gonzalo
    ## 1242                             Carlos
    ## 1243                            Gonzalo
    ## 1244                           Patricia
    ## 1245                             Lorena
    ## 1246                              Josie
    ## 1247                            Mariela
    ## 1248                              Alejo
    ## 1249                            Patrick
    ## 1250                           Gianluca
    ## 1251                         Juan Diego
    ## 1252                          Sebastian
    ## 1253                          Juandiego
    ## 1254                          Alexandra
    ## 1255                          Gianmarco
    ## 1256                             Alvaro
    ## 1257                             Stefan
    ## 1258                           Carolina
    ## 1259                           Williams
    ## 1260                             Andrea
    ## 1261                      Máximo Houver
    ## 1262                            Roberto
    ## 1263                             Lorena
    ## 1264                          Christian
    ## 1265                              Erick
    ## 1266                               Nilo
    ## 1267                               Inés
    ## 1268                              César
    ## 1269                            Enrique
    ## 1270                               Jojo
    ## 1271                              Jordi
    ## 1272                              Oscar
    ## 1273                          Jose Luis
    ## 1274                     Albert Antonio
    ## 1275                             Emilio
    ## 1276                              Jimmi
    ## 1277                            Antonio
    ## 1278                              Pedro
    ## 1279                            Natalia
    ## 1280                          Sebastian
    ## 1281                          Alejandro
    ## 1282                              David
    ## 1283                            Augusto
    ## 1284                       Luis Eduardo
    ## 1285                             Jimena
    ## 1286                              Diego
    ## 1287                   Manchego turismo
    ## 1288                      David Ernesto
    ##                                          Last.Name
    ## 1                                   Awad MD. CCFP.
    ## 2                                    Ospino Ibarra
    ## 3                                               Wu
    ## 4                                 Gonzalez Mahamud
    ## 5                                            Ahmad
    ## 6                                     Moreno Veliz
    ## 7                                 Rodríguez Vidrio
    ## 8                                      Daly, Ed.M.
    ## 9                                          Donayre
    ## 10                                        Portugal
    ## 11                                      ALSAMURAEE
    ## 12                                 Vasquez Carozzo
    ## 13                                           Trifu
    ## 14                                           Agama
    ## 15                                           Kagan
    ## 16                                       Rodríguez
    ## 17                                          Slaoui
    ## 18                                         Ivanova
    ## 19                                            Meng
    ## 20                               Chirinos Calderon
    ## 21                                Gallegos Tweddle
    ## 22                                           Casis
    ## 23                                Chávez-Fernández
    ## 24                                   Lozano-Forero
    ## 25                                       Prabhakar
    ## 26                                           Pezer
    ## 27                                          GRIMAL
    ## 28                                            Dubé
    ## 29                                             Ray
    ## 30                                       Berenguel
    ## 31                                          Giulea
    ## 32                                         Ghafari
    ## 33                                            Feng
    ## 34                                        Hejazian
    ## 35                                         Meshram
    ## 36                                           Gupta
    ## 37                                          Hansen
    ## 38                                   Alonso Zileri
    ## 39                                Mayer Martinelli
    ## 40                                       Guilbault
    ## 41                                             Cyr
    ## 42                                            Biru
    ## 43                                    Razafindrabe
    ## 44                                            Jain
    ## 45                                              Wu
    ## 46                                      Rios Meier
    ## 47                                            Main
    ## 48                                         Vukovic
    ## 49                               Castillo Valencia
    ## 50                                           Asadi
    ## 51                               Trisollini Parodi
    ## 52                                           Zhang
    ## 53                                          Berube
    ## 54                                           Gomez
    ## 55                                       Gonzales 
    ## 56                                   Condori Ccora
    ## 57                                          Balani
    ## 58                                           Suito
    ## 59                                   Hooker Ortega
    ## 60                             Huaman Peralta, MBA
    ## 61                                           López
    ## 62                                         Fort C.
    ## 63                                             Liu
    ## 64                                           Liang
    ## 65                                         Laroche
    ## 66                                            Gora
    ## 67                                           Zhang
    ## 68                                          Mukena
    ## 69                                    Alata Vences
    ## 70                                           Cohen
    ## 71                                   Rivero Proaño
    ## 72                               Pedraza Ibarguren
    ## 73                                Gallegos Cohello
    ## 74                                  Wiesse Paredes
    ## 75                                  Quiroz Ramirez
    ## 76                                      Saba Farah
    ## 77                                         Bennett
    ## 78                                            Soni
    ## 79                                          Nadeem
    ## 80                                        Alvarado
    ## 81                                Casalino Hohagen
    ## 82                               Bouchard-Tremblay
    ## 83                                     Nandinbilig
    ## 84                                           Xiang
    ## 85                                         Gafarov
    ## 86                                          Hurtut
    ## 87                                           Hogan
    ## 88                                         Belmont
    ## 89                                  Garcia Fontova
    ## 90                                        Chrétien
    ## 91                               Delgado (Her/She)
    ## 92                                          Martin
    ## 93                                          Vishal
    ## 94                                         Saidani
    ## 95                                     Proaño Noel
    ## 96                                        Queirolo
    ## 97                                       Rafizadeh
    ## 98                                             Tao
    ## 99                                              Du
    ## 100                                           Wang
    ## 101                                          Ahuja
    ## 102                                     Anthonisen
    ## 103                                         García
    ## 104                                Ventolini Raffo
    ## 105                            Flores-Araoz Bedoya
    ## 106                                           Wang
    ## 107                                      Lundrigan
    ## 108                                     Lopez Diaz
    ## 109                                        Brozyna
    ## 110                                      MacIntosh
    ## 111                                          Morin
    ## 112                                            Tat
    ## 113                                          Hamra
    ## 114                                         Nasiry
    ## 115                                        Animesh
    ## 116                                            Cyr
    ## 117                                       Chapelle
    ## 118                         Escalante Miró Quesada
    ## 119                                        Zaidman
    ## 120                                      Salvignol
    ## 121                                      Fernandez
    ## 122                                           Dion
    ## 123                                           Wang
    ## 124                                          Swail
    ## 125                                          Cohen
    ## 126                                          Gabsi
    ## 127                                         Dubois
    ## 128                                        Ajisafe
    ## 129                                 García Garrués
    ## 130                                          Ortiz
    ## 131                                            Lai
    ## 132                                  Picasso Arias
    ## 133                                             Hu
    ## 134                                           Wang
    ## 135                                         Bahiru
    ## 136                                           Babu
    ## 137                                          Mehta
    ## 138                                         Fariha
    ## 139                                       Bhardwaj
    ## 140                                        Fahreza
    ## 141                                Soriano Cogorno
    ## 142                                   Tello Lumbre
    ## 143                                       Murstein
    ## 144                                  Dibos Freundt
    ## 145                                        Tanasie
    ## 146                                  Khern-am-nuai
    ## 147                                       Agblonon
    ## 148                                       Krowicki
    ## 149                                      Zielinski
    ## 150                                           Chen
    ## 151                                            Yao
    ## 152                                        Ahirrao
    ## 153                                          Kuang
    ## 154                                           Deza
    ## 155                                  Ponce de León
    ## 156                               Elias Pastorutti
    ## 157                                  Piotraszewski
    ## 158                           De La Piedra Gavidia
    ## 159                                        Quevedo
    ## 160                                             Li
    ## 161                                       Esposito
    ## 162                                             Ma
    ## 163                                     Pelletier 
    ## 164                                          Arora
    ## 165                                         Pieper
    ## 166                                   De Las Casas
    ## 167                                          Liang
    ## 168                                   Merino-Reyna
    ## 169                          Bertello Del Castillo
    ## 170                                             Au
    ## 171                                      Gunturkun
    ## 172                                Richardson, CFA
    ## 173                                            Gao
    ## 174                                      Choukekar
    ## 175                                      Lizárraga
    ## 176                                       Brereton
    ## 177                                        Hussain
    ## 178                                         Rivero
    ## 179                                    Inurritegui
    ## 180                                           Wang
    ## 181                              Atencio Velasquez
    ## 182                                          Jonas
    ## 183                                         Mittal
    ## 184                                     Debernardi
    ## 185                                        Alvarez
    ## 186                                   Correa Risso
    ## 187                                           NINO
    ## 188                                           Yang
    ## 189                                         Karoui
    ## 190                                          Yadav
    ## 191                                          Vatsh
    ## 192                                    Nguyen Tang
    ## 193                                           Sood
    ## 194                                      Deschenes
    ## 195                                       Manrique
    ## 196                                         Hammam
    ## 197                                            Wen
    ## 198                                           Paye
    ## 199                                           Qiao
    ## 200                                         Yousaf
    ## 201                                 Utrilla Olguín
    ## 202                                   Cutipa Luque
    ## 203                               Sandoval Canales
    ## 204                                  Soldi Dulanto
    ## 205                                        Padilla
    ## 206          Velazco Dextre,  MBI, MBA, MMA, CQRM.
    ## 207                                     Chinchayan
    ## 208                                          Patel
    ## 209                                 Moreno Barrera
    ## 210                                      Fernandez
    ## 211                                      Peñaranda
    ## 212                                            SAC
    ## 213                                          Hawie
    ## 214                                           Dong
    ## 215                                         Yzeiri
    ## 216                                         Chehab
    ## 217                                           Zhou
    ## 218                                           Zhao
    ## 219                                         Djebri
    ## 220                                         Ranjan
    ## 221                                            Jha
    ## 222                                 Osores Bustios
    ## 223                                      Soleimani
    ## 224                                             Qu
    ## 225                                           Chen
    ## 226                                 Krishnamoorthy
    ## 227                                          Edara
    ## 228                                         Durand
    ## 229                                            Liu
    ## 230                                         Hedley
    ## 231                                        Scruton
    ## 232                                       Yachfine
    ## 233                                           Wang
    ## 234                                         Laniel
    ## 235                                           Ming
    ## 236                                          Jiang
    ## 237                                     Pierantoni
    ## 238                                Quintana Negrón
    ## 239                                        D'Hulst
    ## 240                                     Nourbakhsh
    ## 241                                          Salem
    ## 242                                        Persaud
    ## 243                                           Chen
    ## 244                                         Hatoum
    ## 245                                       Jacquand
    ## 246                                          Penny
    ## 247                                          Zhang
    ## 248                                           Soni
    ## 249                                          Gupta
    ## 250                                        Roopala
    ## 251                                            Rao
    ## 252                                         Nagpal
    ## 253                                        Linares
    ## 254                                          Agnew
    ## 255                                         Samuel
    ## 256                                            Tan
    ## 257                                         Stefan
    ## 258                                         Rivero
    ## 259                               D'Angelo Piaggio
    ## 260                               Romero Fernandez
    ## 261                                        Agrawal
    ## 262                                            Zhu
    ## 263                                Morteza Ghasemi
    ## 264                                           Nair
    ## 265                                        Ascenzo
    ## 266                                          Gomez
    ## 267                                         Garcia
    ## 268                                          Young
    ## 269                                    Xerovasilas
    ## 270                               Fernandez Pelayo
    ## 271                                     Kartavtsev
    ## 272                                   Buttler Ives
    ## 273                                  de Pampelonne
    ## 274                                        Khalili
    ## 275                                            Hon
    ## 276                                     Croubalian
    ## 277                                         Mujica
    ## 278                                   Gainza Llosa
    ## 279                                Bustamante Papa
    ## 280                                  Church Carson
    ## 281                                          Tariq
    ## 282                                      Beraun P.
    ## 283                                        Barbosa
    ## 284                                        Quevedo
    ## 285                                       Cevallos
    ## 286                                  Picasso Arias
    ## 287                                         Caldas
    ## 288                                        Freitas
    ## 289                           Guzman-Barron Villar
    ## 290                              Hidalgo Bonicelli
    ## 291                                          Lazo 
    ## 292                                  JORGE SALAZAR
    ## 293                                   Casas Quiroz
    ## 294                                  Ugaz Calderón
    ## 295                                   Flores Azaña
    ## 296                                       Bermudez
    ## 297                                 Sanchez-Lancha
    ## 298                                   (jimsrc.nft)
    ## 299                                         Macuri
    ## 300                                  Camet Piccone
    ## 301                                        Ortega 
    ## 302                                  Balza Tassara
    ## 303                                       Nicolini
    ## 304                                       Bautista
    ## 305                                 Jimenez Echave
    ## 306                                       Regalado
    ## 307                                         Weston
    ## 308                                   Romero Llosa
    ## 309                                        Pedraza
    ## 310                                  Barrios Hoyle
    ## 311                                      Goytisolo
    ## 312                                Durand Palomino
    ## 313                                Sousa Stockholm
    ## 314                                   Diaz Mendoza
    ## 315                                     Novoa Dyer
    ## 316                             Wiesse Cacho-Sousa
    ## 317                                  Suarez Vertiz
    ## 318                                         Osorio
    ## 319                                       Palomino
    ## 320                               Tola Dourojeanni
    ## 321                                 Sotelo Córdova
    ## 322                                  Farfan Quispe
    ## 323                        Hurtado de Mendoza Diaz
    ## 324                                Robles Arenales
    ## 325                               Morris Ciardello
    ## 326                                        Delgado
    ## 327                                Ortega Guerrero
    ## 328                                   Siles Alfaro
    ## 329                          Rizo-Patron Peschiera
    ## 330                                Pérez Betancour
    ## 331                             Villarruel Vásquez
    ## 332                                    Torres Napa
    ## 333                              Llosa De la Torre
    ## 334                           Mauricio Santisteban
    ## 335                                         Parodi
    ## 336                                  Vasquez Boero
    ## 337                                         Khurma
    ## 338                              Aguirre De Romaña
    ## 339                                          Icaza
    ## 340                                        Cabello
    ## 341                                        Aveggio
    ## 342                                  Vives Piñeiro
    ## 343                                        Lobatón
    ## 344                                          Muñiz
    ## 345                                Gonzales Lozano
    ## 346                                           Novy
    ## 347                                     Tagle Tori
    ## 348                                    Hartley Fry
    ## 349                                    Mitterhofer
    ## 350                                          Gumus
    ## 351                                Pimentel Huerta
    ## 352                                    Llosa Tagle
    ## 353                                      Rodríguez
    ## 354                                         Acosta
    ## 355                                  Payet Palacio
    ## 356                                         Flores
    ## 357                               Guerinoni Lahoud
    ## 358                               Ayarza Valcarcel
    ## 359                                  Romero Valdez
    ## 360                              Prado de Orbegoso
    ## 361                                   Tapia Melgar
    ## 362                                        Ferrero
    ## 363                   Díaz Suxe, CAPM® SSYB\231 SFPC®
    ## 364                                         Sitima
    ## 365                                    Cotacallapa
    ## 366                                         Muroya
    ## 367                                        Noriega
    ## 368                                          Rivas
    ## 369                                Murillo Gallego
    ## 370                                    Nugent Lora
    ## 371                          Rosa-Medina, MBA, MMA
    ## 372                                   Salazar Cash
    ## 373                                Alcántara Panta
    ## 374                                        Uccelli
    ## 375                                       Bernardo
    ## 376                                Huaman Calderon
    ## 377                                Figari Gonzalez
    ## 378                               Martinez Arteaga
    ## 379                     Battistini Castro-Mendivil
    ## 380                                   Tapia Vargas
    ## 381                                         Hosain
    ## 382                              Salazar Sotomayor
    ## 383                                       Saettone
    ## 384                                   Mendez Vilca
    ## 385                                             UP
    ## 386                                 Ortega Cáceres
    ## 387                                  Garcia Daneri
    ## 388                                         Kupina
    ## 389                                         Tafur 
    ## 390                                            Lyu
    ## 391                       Fernandez Gandarias, PMP
    ## 392                                        Sehnert
    ## 393                            Villarán Bustamante
    ## 394                                         Altman
    ## 395                                          Vidal
    ## 396                                       Alvarado
    ## 397                                Espinoza Tacuri
    ## 398                                         Campos
    ## 399                                         Dueñas
    ## 400                                         Calmet
    ## 401                                       Halliday
    ## 402                                            Loo
    ## 403                                          Sezer
    ## 404                                         Gamero
    ## 405                                       Corvetto
    ## 406                               Peramás Cárdenas
    ## 407                                           Rios
    ## 408                                Ventura Ordoñez
    ## 409                           SMC, SPOC, AEC, ITIL
    ## 410                               Cavagnaro Olcese
    ## 411                        Rodriguez Larrain Junge
    ## 412                        Concha-Fernández Valdés
    ## 413                                           Cuba
    ## 414                                          Ieong
    ## 415                                Barrantes Rosas
    ## 416                Moore, PhD, FACMI, FIAHSI, FASA
    ## 417                                       Caillaux
    ## 418                                          Lynch
    ## 419                                Neira Maldonado
    ## 420                                 Callison-Burch
    ## 421                              Gamarra Serveleón
    ## 422                                         Alegre
    ## 423                                    Ferraro Rey
    ## 424                                        Kording
    ## 425                                   Lira Macchiu
    ## 426                                      El Moufti
    ## 427                                         Figari
    ## 428                                       Belaunde
    ## 429                                             XU
    ## 430                                      Languasco
    ## 431                                 García Álvarez
    ## 432                                       Olivares
    ## 433                            Hernandez Marallano
    ## 434                                         Chavan
    ## 435                                 Medina Pizarro
    ## 436                                         Romero
    ## 437                                          Lulli
    ## 438                                   Quinto Ramos
    ## 439                                        Mendoza
    ## 440                                   de la Puente
    ## 441                            Del Campo Vizquerra
    ## 442                                       Valdivia
    ## 443                                Heredia Noriega
    ## 444                                         Wunder
    ## 445                               Galvan Mozombite
    ## 446                                          Borit
    ## 447                                          Palús
    ## 448                                        Catunta
    ## 449                                        Lafarga
    ## 450                                       Lemagnen
    ## 451                                           Pham
    ## 452                                        Zotovic
    ## 453                                          Bagri
    ## 454                                 Castillo López
    ## 455                                 Tagle Belaunde
    ## 456                           García Montúfar M.Q.
    ## 457                                           Wang
    ## 458                                            Liu
    ## 459                                        Rosazza
    ## 460                                   Allan Bartra
    ## 461                           Larco Pooley CertCII
    ## 462                          Salaverry Santa María
    ## 463                          Yépez Pérez del Solar
    ## 464                                Salazar Alvarez
    ## 465                                          Fu Ye
    ## 466                                   García Auler
    ## 467                                 Casabonne Peña
    ## 468                                 Segura Fonseca
    ## 469                                Herrera Sapunar
    ## 470                                         Lozano
    ## 471                                Barrientos Juyo
    ## 472                             Montalván Castillo
    ## 473                                   Saito Hanawa
    ## 474                                        García 
    ## 475                               Villanca Rosales
    ## 476                                Rosselló Monaco
    ## 477                                        Aguirre
    ## 478                                         Avalos
    ## 479                                Gardella Rivero
    ## 480                                         Olivos
    ## 481                                     Rimarachin
    ## 482                                 Pacaya Pacheco
    ## 483                                      Benavides
    ## 484             de Latinoamérica y el Caribe (LAC)
    ## 485                               Llerena Trujillo
    ## 486                              Suasnabar Huapaya
    ## 487                                            Cox
    ## 488                                  Medina Mendez
    ## 489                                      Mosqueira
    ## 490                               Enrico de Cossio
    ## 491                                 Padilla Ybañez
    ## 492                             Rodriguez Mantilla
    ## 493                                  Vergaray Uria
    ## 494                                 Alcalde Aliaga
    ## 495                                          Silva
    ## 496                                       Villarán
    ## 497                              Huaycochea Bayton
    ## 498                                  Vega Barturen
    ## 499                                        Tripoli
    ## 500                              Lizana Mariátegui
    ## 501                                 Valencia Ponce
    ## 502                                Toribio Arrieta
    ## 503                               Casalino Hohagen
    ## 504                                         Pareja
    ## 505                              Bobadilla Andrade
    ## 506                                  Castro Chávez
    ## 507                                  Rios Ordiales
    ## 508                             Cahuancama Mendoza
    ## 509                                   Tello Solano
    ## 510                                Seminario Nuñez
    ## 511                              Valdivia Mazzetti
    ## 512                                       Quintana
    ## 513                                Larrauri Conroy
    ## 514                              de Cossio Moncloa
    ## 515                                Flores Osambela
    ## 516                                 Guevara Guerra
    ## 517                              d'Auriol Augusto 
    ## 518                            Olcese Gastelumendi
    ## 519                                  Soria Miranda
    ## 520                                 Antezana Ochoa
    ## 521                                   Pena Suclupe
    ## 522                                      Ortiz Loo
    ## 523                                       Holmberg
    ## 524                                 Villa Palacios
    ## 525                               Daly Miloslavich
    ## 526                             Ancajima Minguillo
    ## 527                                 Ramírez Dúmett
    ## 528                                  Vergani Serpa
    ## 529                            de la Piedra Alayza
    ## 530                                          Hasan
    ## 531                                    Pez Gubbins
    ## 532                                        Kurfess
    ## 533                               del Solar Vargas
    ## 534                                     Carrillo R
    ## 535                                          Dalls
    ## 536                             Guerrero Castañeda
    ## 537                               Angeles Martinez
    ## 538                                              .
    ## 539                                 Rodrigo Bedoya
    ## 540                                           Gole
    ## 541                                          Piera
    ## 542                                      Quispe O.
    ## 543                                         Torres
    ## 544                                          Urday
    ## 545                               Córdova Martínez
    ## 546                            Salvador Eyzaguirre
    ## 547                                         Agüero
    ## 548                                        Noriega
    ## 549                                       Nacarino
    ## 550                                Cabrera Basurco
    ## 551                                      Simonneau
    ## 552                                 Dávila Chocano
    ## 553                                        Cabrera
    ## 554                                Villagra Zúñiga
    ## 555                              Fernández Paredes
    ## 556                                        Delgado
    ## 557                                      Escalante
    ## 558                                 Morales Máximo
    ## 559                                          Leyva
    ## 560                                 Rengifo García
    ## 561                                 Delgado, CSPO®
    ## 562                              Francesqui Casuso
    ## 563                               Echeandía Orrego
    ## 564                                Sánchez Mendoza
    ## 565                                Dañino Cabieses
    ## 566                                  Marengo Ojeda
    ## 567                                          Rojas
    ## 568                                               
    ## 569                                 Carbo Gonzalez
    ## 570                                         Castro
    ## 571                                           Peru
    ## 572                             Arroyo Marticorena
    ## 573                      Tafur (peladodigital.eth)
    ## 574                                        Saravia
    ## 575                            Flores-Araoz Bedoya
    ## 576                            Schwartzmann Wisdom
    ## 577                                       Ebrahimi
    ## 578                              del Rio Albertini
    ## 579                                       Felandro
    ## 580                                          Soria
    ## 581                                Echevarría Ossa
    ## 582                                        Swisher
    ## 583                                  Vásquez Neyra
    ## 584                                          Johns
    ## 585                                           Tola
    ## 586                                Kraenau Espinal
    ## 587                                     Lulo Rojas
    ## 588                  Ejecutiva Senior en Tesorería
    ## 589                               Guerinoni Lahoud
    ## 590                                          Drago
    ## 591                              Galliani Nadramia
    ## 592                            Bacigalupo Carrillo
    ## 593                                Flores Abusabal
    ## 594                               Basualdo Najera 
    ## 595                                Gallegos Cooper
    ## 596                                         Chávez
    ## 597                                     Villanueva
    ## 598                                          Telge
    ## 599                                  Catter Coello
    ## 600                                        Herrera
    ## 601                                 Bassino Dapelo
    ## 602                                 Rivera Guillén
    ## 603                                        Guillen
    ## 604                                        Vasquez
    ## 605                                 Carmona Farfán
    ## 606                                          Brown
    ## 607                                    Arbe Andreu
    ## 608                                   Inga Ramírez
    ## 609                                Dañino Cabieses
    ## 610                                  GARCIA TULICH
    ## 611                                          Arana
    ## 612                                        Vigetti
    ## 613                                       Balbuena
    ## 614                                        Alcocer
    ## 615                                 Milla Zavaleta
    ## 616                                 Almeyda Pachas
    ## 617                                        Berrios
    ## 618                                    Novoa Farro
    ## 619                                         Parodi
    ## 620                                         Huaman
    ## 621                                        Wakeham
    ## 622                                        Sisodia
    ## 623                                        Durbano
    ## 624                                     Verde Jara
    ## 625                                 Costa Ludowieg
    ## 626                                           Wong
    ## 627                                Noriega Guevara
    ## 628                                      Melinchon
    ## 629                               Cavero-Egúsquiza
    ## 630                               Lingan Caballero
    ## 631                                  Ojeda Cabrera
    ## 632                                   Galdos Serra
    ## 633                                Aramburú García
    ## 634                                Navarro Mandayo
    ## 635                                           Vega
    ## 636                              Zavala Echevarría
    ## 637                                Freundt Garland
    ## 638                                Guerrero Alfaro
    ## 639                                Acosta Martínez
    ## 640                                         Parakh
    ## 641                                          Forti
    ## 642                                       Madrigal
    ## 643                                   Castro Tafur
    ## 644                            Encalada Verastegui
    ## 645                         Hidalgo Garcia Pacheco
    ## 646                                         Moreno
    ## 647                                 Fitts Trefogli
    ## 648                        Bustamante de la Piedra
    ## 649                               Mayorca Alvarado
    ## 650                                O'Donnell Barco
    ## 651                                         Borah 
    ## 652                                    Ramos Reyna
    ## 653                                  Granda Baertl
    ## 654                                 Ibarra Ventura
    ## 655                                 Quimper Osores
    ## 656                                 Ayuque Rosario
    ## 657                                       Gabisson
    ## 658                                        Bendezú
    ## 659                                 Ramos Mestanza
    ## 660                                      Benavides
    ## 661                                   Chang Tejada
    ## 662                                          Monje
    ## 663                              Ccasani Velasquez
    ## 664                              Zegarra Malatesta
    ## 665                                        Ferrero
    ## 666                                  Quispe Quispe
    ## 667                                Herrera Cornejo
    ## 668                                         Garcia
    ## 669                             Portocarrero Quiñe
    ## 670                                  Garcia Haaker
    ## 671                                Montero Montoya
    ## 672                              Escribens Salinas
    ## 673                             Scerpella Manrique
    ## 674                                Hurtado Ramírez
    ## 675                                   Zegarra Blas
    ## 676                                       Chlimper
    ## 677                              Garmendia Mohanna
    ## 678                                           Kahn
    ## 679                                      Duranteau
    ## 680                                         Castro
    ## 681                                 Castillo Terán
    ## 682                                          Costa
    ## 683                                         Sardón
    ## 684                                       Leonhard
    ## 685                                          Laney
    ## 686                                 Acosta Murillo
    ## 687                                         Collas
    ## 688                                    Proaño Noel
    ## 689                              Herrero Bartolomé
    ## 690                                            Oré
    ## 691                               Beltrán Castañón
    ## 692                                   Taco Miranda
    ## 693                               Masabel Avendaño
    ## 694                                         Perkes
    ## 695                               Rocha de Andrade
    ## 696                                   Sambra Graña
    ## 697                                   Molina Félix
    ## 698                                       Palomino
    ## 699                                  Acuña Paredes
    ## 700                                        Aduviri
    ## 701                                        Linares
    ## 702                                         Méndez
    ## 703                                          Singh
    ## 704                                   Esteva Hache
    ## 705                                        Llerena
    ## 706                                   Vega Noriega
    ## 707                              Martínez Solimano
    ## 708                      Ortiz de Zevallos Rodrigo
    ## 709                                         Canosa
    ## 710                                        Neuhaus
    ## 711                                   Novoa Carpio
    ## 712                                     Ojeda Dejo
    ## 713                                         Bizama
    ## 714                                Céspedes Duffoo
    ## 715                                            Cam
    ## 716                              Cuneo Passalacqua
    ## 717                                   Chapilliquén
    ## 718                                          Rojas
    ## 719                                        Fonseca
    ## 720                                  Garrido Lecca
    ## 721                                    Brown Ph.D.
    ## 722                                          Pérez
    ## 723                                     Pumallihua
    ## 724                                    Sira Aponte
    ## 725                                        Vasquez
    ## 726                             el Kaliouby, Ph.D.
    ## 727                                       Nycander
    ## 728                                   Paredes, PhD
    ## 729                                  Schultz Rubio
    ## 730                                          Yzaga
    ## 731                                Dávila Castillo
    ## 732                                 Navarro García
    ## 733                                      Escribens
    ## 734                                        Jiménez
    ## 735                                          Rocca
    ## 736                                Cateriano Llosa
    ## 737                                 Quiros Herrera
    ## 738                                         Yazawa
    ## 739                                    Castiglioni
    ## 740                                        Alarcón
    ## 741                             Bustamante Escobar
    ## 742                                        Pacheco
    ## 743                                   Llanos Gallo
    ## 744                                          Bueno
    ## 745                              Zavaleta Martínez
    ## 746                                         Nandam
    ## 747                                       Mendiola
    ## 748                                         Collao
    ## 749                                          Singh
    ## 750                                  Ortiz Barriga
    ## 751                                        Sánchez
    ## 752                                     Cueva Luyo
    ## 753                                        Sánchez
    ## 754                                 Grados Salinas
    ## 755                                Mendoza Egoavil
    ## 756                                          Ortiz
    ## 757                           Montenegro Maldonado
    ## 758                                         Gamero
    ## 759                                        Velarde
    ## 760                                        Geitgey
    ## 761                                   Pérez Urbano
    ## 762                                         Smelan
    ## 763                            Bouroncle Hernández
    ## 764                                La Rosa Ferrero
    ## 765                                          Ponce
    ## 766                           Carrasco de Azambuja
    ## 767                                 Zelada Uriarte
    ## 768                                        Cabrera
    ## 769                                       Agapito 
    ## 770                                          Chion
    ## 771                                  Oliva Mesones
    ## 772                                           Roig
    ## 773                            Garcia Del Castillo
    ## 774                                Vinelli Becerra
    ## 775                                         Quiroz
    ## 776                                  Arias Montoya
    ## 777                              Barriga Alibrandi
    ## 778                                           Nima
    ## 779                                    Rubino Baña
    ## 780                                       Roca Rey
    ## 781                                       Reategui
    ## 782                                          Neira
    ## 783                                        Madueño
    ## 784                               Esposito Figari 
    ## 785                                        Peramás
    ## 786                                        Angosto
    ## 787                                   Luna Blondet
    ## 788                             Cornejo Albarracin
    ## 789                               Marcelo Mancilla
    ## 790                         Delgado Pérez Martinot
    ## 791                                         Veloso
    ## 792                               Escudero Ramírez
    ## 793                               Rebagliati Dibos
    ## 794                                          Mejia
    ## 795                                   Castillo Gil
    ## 796                            Sifuentes Sarmiento
    ## 797                                Alvarez Cordano
    ## 798                                  Martin Balboa
    ## 799                                         Vargas
    ## 800                                 Cabrera Rivera
    ## 801                              Valenzuela Phocco
    ## 802                                          Arana
    ## 803                                        MacLean
    ## 804                              Alvarado Martinez
    ## 805                                   García Perry
    ## 806                                      Echecopar
    ## 807                               Espinoza Zuloaga
    ## 808                                  Cabrera Zuazo
    ## 809                                    Lizarzaburu
    ## 810                              Miranda Sotomayor
    ## 811                            Feliubadalo Briceño
    ## 812                                      Vallejos 
    ## 813                              Corcuera Cisneros
    ## 814                                      Diaz Arca
    ## 815                                           Leon
    ## 816                              Ceballos Valencia
    ## 817                                         Cotter
    ## 818                                   Olano Romero
    ## 819                             Martinez Sotomayor
    ## 820                                         Garcia
    ## 821                         Gonzalez Iñiguez (OGI)
    ## 822                                         Campos
    ## 823                                Grados Marquina
    ## 824                                Castle Buraschi
    ## 825                                        Morales
    ## 826                                         Prieto
    ## 827                                        Diestra
    ## 828                                      Vega Vera
    ## 829                                        Sánchez
    ## 830                                         Lázaro
    ## 831                                        Duharte
    ## 832                                 Bruiget Mussio
    ## 833                                  Puelles Vella
    ## 834                                        Lickert
    ## 835                                         Kantor
    ## 836                                    Forti Rubio
    ## 837                                   Zavala Sulca
    ## 838                                      Cateriano
    ## 839                                        Moncada
    ## 840                                        Huiskes
    ## 841                                  Huillcas Pozo
    ## 842                                        Vasquez
    ## 843                              Perez Wicht Breña
    ## 844                                    Said García
    ## 845                                  Buse Visconti
    ## 846                                Portugal Torres
    ## 847                                          Armas
    ## 848                                     Del Aguila
    ## 849                                Narváez Del Rio
    ## 850                                          Vivar
    ## 851                                       Salvador
    ## 852                             y Economía de Lima
    ## 853                                    Vela Alfaro
    ## 854                                 Romero Clavijo
    ## 855                                       Cebulski
    ## 856                                 Salazar Llanos
    ## 857                                         De Col
    ## 858                                Briceño Bellomo
    ## 859                                          Rojas
    ## 860                                          Zagal
    ## 861                                Macher Figueroa
    ## 862                                         Calmet
    ## 863                         Mitterhofer Castellano
    ## 864                                        Salazar
    ## 865                                 Arbulú Barreda
    ## 866                                Calderon Candia
    ## 867                                Zamora Palomino
    ## 868                                Barra Santayana
    ## 869                                        Gopalan
    ## 870                                     Noel Madge
    ## 871                                   García Orams
    ## 872                              Maguina Reggiardo
    ## 873                                       Yrigoyen
    ## 874                                 Palacios Lopez
    ## 875                                        Malpica
    ## 876                                        Cogneau
    ## 877                                       Aramburu
    ## 878                               Jiménez Awuapara
    ## 879                               Ascencios Rondón
    ## 880                                          Muñoz
    ## 881                                       Aramburú
    ## 882                               Gutierrez Paseta
    ## 883                                 Albán Cigüeñas
    ## 884                                 Gil Juscamaita
    ## 885                                    Chambi Luna
    ## 886                          Polanco Valle Riestra
    ## 887                                   Vega Gamarra
    ## 888                                Palomino Vargas
    ## 889                                        Cabrera
    ## 890                              Chichizola Chaves
    ## 891                                         Cusman
    ## 892                                       Vizcardo
    ## 893                                      Kuncewicz
    ## 894                                         Lozada
    ## 895                                       Carrillo
    ## 896                                   Peña Guevara
    ## 897                               Cernicharo Ortiz
    ## 898                                          Barra
    ## 899                                          Nadal
    ## 900                                       Carrillo
    ## 901                                 Benettuce Mayo
    ## 902                                  Luna Queirolo
    ## 903                                        Binelli
    ## 904                              Carrion del Solar
    ## 905                                       Calderon
    ## 906                                    Gil Aguilar
    ## 907                                    Blas Garcia
    ## 908                                     De Vivanco
    ## 909                              Palomino Lanchipa
    ## 910                                       de Pablo
    ## 911                               Figari del Solar
    ## 912                                        Brandon
    ## 913                           Barthelmess Miletich
    ## 914                                          Hoyos
    ## 915                                  Voter Montejo
    ## 916                                     Requena C.
    ## 917                                   Gainza Llosa
    ## 918                              Bendezú Lizarraga
    ## 919                                         Romero
    ## 920                                Naveros Salazar
    ## 921                                         Oyague
    ## 922                                          Russo
    ## 923                              Cuicapuza Antonio
    ## 924                                        Delgado
    ## 925                                      Mischenko
    ## 926                                 Vargas Lapponi
    ## 927                                         Zárate
    ## 928                                   Rocano Ponce
    ## 929                                 Solano Morales
    ## 930                              Ruiz Conejo Neyra
    ## 931                                    Marzal Alva
    ## 932                                           Pila
    ## 933                                Osorio Gonzalez
    ## 934                                         Campos
    ## 935                                         Suarez
    ## 936                                      Arguelles
    ## 937                                    Davila Rios
    ## 938                                     Meza Roque
    ## 939                                          Cacha
    ## 940                                        Carrera
    ## 941                                 Charalla Olazo
    ## 942                              Saavedra Castillo
    ## 943                              Guerrero Martinez
    ## 944                                        Butrich
    ## 945                                       Aramburú
    ## 946                                          Valle
    ## 947                                Mansilla Garcia
    ## 948                                Fiol Villanueva
    ## 949                               Noriega Milligan
    ## 950                            Velaochaga González
    ## 951                          Ferreyros de la Borda
    ## 952                                   Luna Hidalgo
    ## 953                                     Carruitero
    ## 954                                         Vargas
    ## 955                                   Ravina Vidal
    ## 956                                        Ramella
    ## 957                                   Hidalgo Alta
    ## 958                                     Vega Ayala
    ## 959                                        C Jones
    ## 960                                          Assen
    ## 961                                           Roca
    ## 962                                      Beuermann
    ## 963                                  Jesús De Lama
    ## 964                                   Jara Almonte
    ## 965                                 Valdez del Mar
    ## 966                                 Ibáñez Marrese
    ## 967                            Torres del Castillo
    ## 968                                        Grandez
    ## 969                              Gutierrez Ayquipa
    ## 970                                       Ballesta
    ## 971                                         Quispe
    ## 972                                          Chuco
    ## 973                                        Honorio
    ## 974                              Huachaca Corrales
    ## 975                                     de la Flor
    ## 976                                           Nano
    ## 977                                   Moreno Reyes
    ## 978                                           Riva
    ## 979                                        Smaldon
    ## 980                                MOSCOSO NORIEGA
    ## 981                                        Alvarez
    ## 982                                          Muñoz
    ## 983                                  Soncco Sinchi
    ## 984                                        becerra
    ## 985                                          Velit
    ## 986                              Llosa De La Torre
    ## 987                                               
    ## 988                                Rodriguez Muñoz
    ## 989                                Fantozzi Freire
    ## 990                                 Mendoza Garcia
    ## 991                              Guevara Manosalva
    ## 992                                        Márquez
    ## 993                                     del Carpio
    ## 994                                      Crespo C.
    ## 995                                   Pérez Martín
    ## 996                                Ponce Sotomayor
    ## 997                                     Luque Lazo
    ## 998                                      Pavletich
    ## 999                                 Obregon Grillo
    ## 1000                                      Orellana
    ## 1001                                MBA, MSc, CIP.
    ## 1002                               Arróspide Mazzi
    ## 1003                                          Chuy
    ## 1004                                      Valverde
    ## 1005                                       Morillo
    ## 1006                              Cortés Jaramillo
    ## 1007                              Custódia de Lima
    ## 1008                                        Cóndor
    ## 1009                                 Grados Flores
    ## 1010                             Gutierrez Vasquez
    ## 1011                                 Alvarez Cueto
    ## 1012                                         Rivas
    ## 1013                                          Rodó
    ## 1014                                         Poggi
    ## 1015                                       Cadillo
    ## 1016                              Valdivia Velarde
    ## 1017                                   Verano León
    ## 1018                                           Gil
    ## 1019                                      Barbieri
    ## 1020                            Rodrigues Oliveira
    ## 1021                                       Praelli
    ## 1022                               Clarke Cantella
    ## 1023                                        Roncal
    ## 1024                                     Gutierrez
    ## 1025                              Guere Canchucaja
    ## 1026                               Suarez Mansilla
    ## 1027                               Castillo Romero
    ## 1028                                    H. Mireles
    ## 1029                              Seminario Moreno
    ## 1030                                 Montoya Gamio
    ## 1031                              Mendoza Tarrillo
    ## 1032                                     Parrales.
    ## 1033                             Collantes Montero
    ## 1034                                       Maguina
    ## 1035                                       Montero
    ## 1036                                        Cavero
    ## 1037                              Murciano Barrios
    ## 1038                                      Castillo
    ## 1039                                         Botti
    ## 1040                                     Brodersen
    ## 1041                                        Kumar 
    ## 1042                                Butrich Camino
    ## 1043                               Garrido - Lecca
    ## 1044                                          Rios
    ## 1045                                        Figari
    ## 1046                                Casado Morales
    ## 1047                           Cabanillas Gonzales
    ## 1048                                   Cuya Nizama
    ## 1049                              Ravichagua Vitor
    ## 1050                              Zuloaga Saavedra
    ## 1051                                Cortez Aguirre
    ## 1052                              Vasquez Teixeira
    ## 1053                                     Ferreccio
    ## 1054                                       Yarasca
    ## 1055                              Macher Ravettino
    ## 1056                                     Alcantara
    ## 1057                                       Ramirez
    ## 1058                                   Rubio Donet
    ## 1059    Terrones I Architect AWS I DevOps Engineer
    ## 1060                                       Ferraro
    ## 1061                              Gutierrez Tamayo
    ## 1062                                    Bacigalupo
    ## 1063                                         Vegas
    ## 1064                                        Astete
    ## 1065                              Hernández Borjas
    ## 1066                           Yzaguirre Seminario
    ## 1067                                     Cayo Arce
    ## 1068                                       Fox Koo
    ## 1069                             del Aguila Yovera
    ## 1070                             Aspillaga Voysest
    ## 1071                                Vargas Quevedo
    ## 1072                                       Murdoch
    ## 1073                              Echevarría Pérez
    ## 1074                              Zumaeta Figueroa
    ## 1075                               Abuid Majdalani
    ## 1076                                       Quedena
    ## 1077                               Castañeda Viale
    ## 1078 López Tenorio, PhD (Acreditación Aneca - PAD)
    ## 1079                                S. CAMPODONICO
    ## 1080                              Culqui Fernandez
    ## 1081                                       Naranjo
    ## 1082                                     Brancacho
    ## 1083                                   de Almenara
    ## 1084                               Espinosa Torres
    ## 1085                                Osores Beltrán
    ## 1086                                         Tapia
    ## 1087                                    Vivas Lago
    ## 1088                                       Salcedo
    ## 1089                                      Talavera
    ## 1090                                      Labarthe
    ## 1091                                       Moscoso
    ## 1092                                   Bado Espino
    ## 1093                                     Benzaquen
    ## 1094                                        Robles
    ## 1095                                         Tapia
    ## 1096                               Ramos Rodriguez
    ## 1097                                   Tello Benel
    ## 1098                                          Rico
    ## 1099                               Delgado Camacho
    ## 1100                                       Vasquez
    ## 1101                                       Delgado
    ## 1102                                  Garcia Ramos
    ## 1103                              Sanguineti Risco
    ## 1104                                Alarcon Flores
    ## 1105                             Huaman Salirrosas
    ## 1106                               Flores Enriquez
    ## 1107                                        Castle
    ## 1108                                         Román
    ## 1109                             Del Aguila Fiocco
    ## 1110                                           Pua
    ## 1111                                         Oliva
    ## 1112                                        Gamero
    ## 1113                                     Cocchella
    ## 1114                                  Díaz Appiani
    ## 1115                            Santillán Gordillo
    ## 1116                                Moreno Salinas
    ## 1117                              Vargas Fernandez
    ## 1118                                  García Auler
    ## 1119                                       Sabroso
    ## 1120                              Acostupa Ellisca
    ## 1121                                Huanca Huamaní
    ## 1122                                       Vásquez
    ## 1123                                        Flores
    ## 1124                                        Miyagi
    ## 1125                                   Penny Selem
    ## 1126                                 Macedo Naters
    ## 1127                                      Cardenas
    ## 1128                          VALDIVIA MANCHEGO L.
    ## 1129                                             T
    ## 1130                                    Paz Soldan
    ## 1131                                Fabian Arteaga
    ## 1132                            Velasquez Tupalaya
    ## 1133                             Anchiraico Orozco
    ## 1134                                        Chambi
    ## 1135                               Susanibar Sipan
    ## 1136                               Espinoza Busato
    ## 1137                                        Aguayo
    ## 1138                                       Velasco
    ## 1139                                       Basurto
    ## 1140                               Cateriano Llosa
    ## 1141                       Sanchez Gutierrez, Ing.
    ## 1142                                          Diaz
    ## 1143                                    COLLEMICHE
    ## 1144                                       Robles 
    ## 1145                              Nuñuvero Angeles
    ## 1146                            Cuba Villena, SMC\231
    ## 1147                               Figari Gonzalez
    ## 1148                                       Paredes
    ## 1149                            Shatwell Pittaluga
    ## 1150                                          Baba
    ## 1151                              Muñoz Villalobos
    ## 1152                                      Brownlee
    ## 1153                                    De la cruz
    ## 1154                                   Morin Zuazo
    ## 1155                               Chauca Saavedra
    ## 1156                                      Vexelman
    ## 1157                               Vinelli Becerra
    ## 1158                               Chávez González
    ## 1159                                Delgado Garcia
    ## 1160                                   Rivadeneira
    ## 1161                                    Alva Fossa
    ## 1162                                        Stuntz
    ## 1163                                Kouri Zacarias
    ## 1164                               Jiskra Elejalde
    ## 1165                                     Melgarejo
    ## 1166                               Cateriano Llosa
    ## 1167                          Burranca Barthelmess
    ## 1168                                          Abad
    ## 1169                                        Ganoza
    ## 1170                                         Soyer
    ## 1171                                Yaulli Herrera
    ## 1172                              Zevallos Munguia
    ## 1173                                       Jahnsen
    ## 1174                                  Merino Reyna
    ## 1175                                   Román Yseki
    ## 1176                                   Rey Noriega
    ## 1177                                      Valdivia
    ## 1178                                       Braschi
    ## 1179                                     Jaramillo
    ## 1180                         del Valle Consiglieri
    ## 1181                                      Chirinos
    ## 1182                                     Rodríguez
    ## 1183                                       Cordova
    ## 1184                                  de Goytisolo
    ## 1185                                     O'Connell
    ## 1186                                         Mayor
    ## 1187                             Barreto Velázquez
    ## 1188                                         Luque
    ## 1189                            Escudero Seminario
    ## 1190                                          Tito
    ## 1191                                 Jara Schenone
    ## 1192                             Aguirre Landázuri
    ## 1193                                       Almeyda
    ## 1194                                       Vergani
    ## 1195                                            UP
    ## 1196                                        Olcese
    ## 1197                                 Delgado P. M.
    ## 1198                         García Calderón Vidal
    ## 1199                                     Rosenberg
    ## 1200                                  Ghio Aspauza
    ## 1201                                         Chong
    ## 1202                                Barco Yriberry
    ## 1203                                Picasso Alarco
    ## 1204                          Ferreyros Bustamante
    ## 1205                                    Arias Mori
    ## 1206                                     Callirgos
    ## 1207                               Santillán Soler
    ## 1208                                 Mazuelos Beas
    ## 1209                           Aguilar Gargurevich
    ## 1210                                  Vidaurrazaga
    ## 1211                             Hernández Salazar
    ## 1212                                Cornejo Macedo
    ## 1213                               Sanguineti Hart
    ## 1214                                Mattos  Vinces
    ## 1215                              De Asín Alvariño
    ## 1216                                     Rodriguez
    ## 1217                                          Cano
    ## 1218                                       Deustua
    ## 1219                                         Chong
    ## 1220                                  Payet Castro
    ## 1221                                Ñañez Mouchard
    ## 1222                                 Aguedo Zuñiga
    ## 1223                                 Brescia Olsen
    ## 1224                        NUÑEZ DEL PRADO CORTEZ
    ## 1225                                        Olivos
    ## 1226                                       Documet
    ## 1227                                  Ortega Ariza
    ## 1228                             Ferreyros Kuppers
    ## 1229                                Herrera Medina
    ## 1230                                      Sangalli
    ## 1231                                     Fernández
    ## 1232                               Alatrista Salas
    ## 1233                                         Regal
    ## 1234                          Larraín Perez Albela
    ## 1235                                  Renzo Franco
    ## 1236                                 Cauvi Ferraro
    ## 1237                            Langschwager Pérez
    ## 1238                                Murdoch Fabbri
    ## 1239                                       Marcelo
    ## 1240                                Carranza Cueto
    ## 1241                                   Santa Maria
    ## 1242                                     Ferreyros
    ## 1243                                 Castro Gárate
    ## 1244                            Gastelumendi Lukis
    ## 1245                                     Ferreyros
    ## 1246                                      Hallinan
    ## 1247                              Garcia de Fabbri
    ## 1248                                        Molina
    ## 1249                                Loyer Makhlouf
    ## 1250                          Bettocchi Camogliano
    ## 1251                               Garcia Cantella
    ## 1252                            Herrera Eyzaguirre
    ## 1253                                        Morzán
    ## 1254                                       Jenkins
    ## 1255                                          Alva
    ## 1256                             Gomez de la Torre
    ## 1257                         Schwartzmann D`Angelo
    ## 1258                                       Murdoch
    ## 1259                                      Azabache
    ## 1260                                        Fabbri
    ## 1261                              Villafane Abregú
    ## 1262                          Fiorentino Ferreyros
    ## 1263                              Alvariño de Asín
    ## 1264                                 Libaque Saenz
    ## 1265                                          Hein
    ## 1266                                       Gamarra
    ## 1267                             Valenzuela García
    ## 1268                                 Ruiz Palomino
    ## 1269                                         Agois
    ## 1270                                       Ramirez
    ## 1271                                           Nin
    ## 1272                                   de Azambuja
    ## 1273                                       Urteaga
    ## 1274                                   Roncal Díaz
    ## 1275                               Fantozzi Freire
    ## 1276                                    Hemmenbach
    ## 1277                                      Calogero
    ## 1278                                     Callirgos
    ## 1279                                     Ferreyros
    ## 1280                                         Nadal
    ## 1281                               Cortés Cabieses
    ## 1282                                       Salazar
    ## 1283                                       Murdoch
    ## 1284                                      Berrospi
    ## 1285                              Ferreyros Fabbri
    ## 1286                          Pedraza Gastelumendi
    ## 1287      Transporte de personal agencia de viajes
    ## 1288                                  Soto Vásquez
    ##                                  Email.Address
    ## 1                                             
    ## 2                                             
    ## 3                                             
    ## 4                                             
    ## 5                                             
    ## 6                                             
    ## 7                     ale.rdz.vidrio@gmail.com
    ## 8                                             
    ## 9                                             
    ## 10                                            
    ## 11                                            
    ## 12                                            
    ## 13                                            
    ## 14                                            
    ## 15                                            
    ## 16                                            
    ## 17                                            
    ## 18                                            
    ## 19                                            
    ## 20                       cpchirinosc@gmail.com
    ## 21                                            
    ## 22                                            
    ## 23                                            
    ## 24                                            
    ## 25                                            
    ## 26                                            
    ## 27                                            
    ## 28                                            
    ## 29                                            
    ## 30                                            
    ## 31                                            
    ## 32                                            
    ## 33                                            
    ## 34                                            
    ## 35                                            
    ## 36                                            
    ## 37                                            
    ## 38                                            
    ## 39                                            
    ## 40                                            
    ## 41                                            
    ## 42                                            
    ## 43                                            
    ## 44                                            
    ## 45                                            
    ## 46                                            
    ## 47                                            
    ## 48                                            
    ## 49                                            
    ## 50                                            
    ## 51                                            
    ## 52                                            
    ## 53                                            
    ## 54                                            
    ## 55                                            
    ## 56                                            
    ## 57                                            
    ## 58                                            
    ## 59                                            
    ## 60                                            
    ## 61                                            
    ## 62                                            
    ## 63                                            
    ## 64                                            
    ## 65                                            
    ## 66                                            
    ## 67                                            
    ## 68                                            
    ## 69                                            
    ## 70                                            
    ## 71                                            
    ## 72                                            
    ## 73                                            
    ## 74                                            
    ## 75                                            
    ## 76                                            
    ## 77                                            
    ## 78                                            
    ## 79                                            
    ## 80                                            
    ## 81                                            
    ## 82                                            
    ## 83                                            
    ## 84                                            
    ## 85                                            
    ## 86                                            
    ## 87                                            
    ## 88                                            
    ## 89                                            
    ## 90                                            
    ## 91                                            
    ## 92                                            
    ## 93                                            
    ## 94               islem.saidani.1@ens.etsmtl.ca
    ## 95                                            
    ## 96                                            
    ## 97                                            
    ## 98                                            
    ## 99                                            
    ## 100                                           
    ## 101                                           
    ## 102                                           
    ## 103                                           
    ## 104                                           
    ## 105                                           
    ## 106                                           
    ## 107                                           
    ## 108                                           
    ## 109                                           
    ## 110                                           
    ## 111                                           
    ## 112                                           
    ## 113                                           
    ## 114                                           
    ## 115                                           
    ## 116                                           
    ## 117                                           
    ## 118                                           
    ## 119                                           
    ## 120                                           
    ## 121                                           
    ## 122                                           
    ## 123                                           
    ## 124                                           
    ## 125                                           
    ## 126                                           
    ## 127                                           
    ## 128                                           
    ## 129                                           
    ## 130                                           
    ## 131                                           
    ## 132                                           
    ## 133                                           
    ## 134                                           
    ## 135                                           
    ## 136                                           
    ## 137                                           
    ## 138                                           
    ## 139                                           
    ## 140                                           
    ## 141                                           
    ## 142                                           
    ## 143                                           
    ## 144                                           
    ## 145                                           
    ## 146                                           
    ## 147                                           
    ## 148                                           
    ## 149                                           
    ## 150                                           
    ## 151                                           
    ## 152                                           
    ## 153                                           
    ## 154                                           
    ## 155                                           
    ## 156                                           
    ## 157                                           
    ## 158                                           
    ## 159                                           
    ## 160                                           
    ## 161                                           
    ## 162                                           
    ## 163                                           
    ## 164                                           
    ## 165                                           
    ## 166                                           
    ## 167                                           
    ## 168                                           
    ## 169                                           
    ## 170                                           
    ## 171                                           
    ## 172                                           
    ## 173                                           
    ## 174                                           
    ## 175                  rociolizarragad@gmail.com
    ## 176                                           
    ## 177                                           
    ## 178                                           
    ## 179                                           
    ## 180                                           
    ## 181                                           
    ## 182                                           
    ## 183                                           
    ## 184                                           
    ## 185                                           
    ## 186                                           
    ## 187                                           
    ## 188                                           
    ## 189                                           
    ## 190              anukriti.yadav@mail.mcgill.ca
    ## 191                                           
    ## 192                                           
    ## 193                                           
    ## 194                                           
    ## 195                                           
    ## 196                                           
    ## 197                                           
    ## 198                                           
    ## 199                                           
    ## 200                                           
    ## 201                                           
    ## 202                                           
    ## 203                sebastianjsc_03@hotmail.com
    ## 204                                           
    ## 205                                           
    ## 206                                           
    ## 207                                           
    ## 208                                           
    ## 209                                           
    ## 210                                           
    ## 211                nicolaspenarandaf@gmail.com
    ## 212                                           
    ## 213                                           
    ## 214                                           
    ## 215                                           
    ## 216                                           
    ## 217                                           
    ## 218                                           
    ## 219                                           
    ## 220                                           
    ## 221                                           
    ## 222                                           
    ## 223                                           
    ## 224                                           
    ## 225                                           
    ## 226                                           
    ## 227                                           
    ## 228                                           
    ## 229                                           
    ## 230                                           
    ## 231                                           
    ## 232                                           
    ## 233                                           
    ## 234                                           
    ## 235                                           
    ## 236                                           
    ## 237                                           
    ## 238                                           
    ## 239                                           
    ## 240                                           
    ## 241                                           
    ## 242                                           
    ## 243                                           
    ## 244                                           
    ## 245                                           
    ## 246                                           
    ## 247                                           
    ## 248                                           
    ## 249                                           
    ## 250                                           
    ## 251                                           
    ## 252                                           
    ## 253                                           
    ## 254                                           
    ## 255                                           
    ## 256                                           
    ## 257                                           
    ## 258                                           
    ## 259                                           
    ## 260                                           
    ## 261                                           
    ## 262                                           
    ## 263                                           
    ## 264                                           
    ## 265                                           
    ## 266                                           
    ## 267                                           
    ## 268                                           
    ## 269                                           
    ## 270                                           
    ## 271                                           
    ## 272                                           
    ## 273                                           
    ## 274                                           
    ## 275                                           
    ## 276                                           
    ## 277                                           
    ## 278                                           
    ## 279                                           
    ## 280                                           
    ## 281                                           
    ## 282                                           
    ## 283                                           
    ## 284                                           
    ## 285                                           
    ## 286                                           
    ## 287                                           
    ## 288                                           
    ## 289                                           
    ## 290                                           
    ## 291                                           
    ## 292                                           
    ## 293                          jcasasq@gmail.com
    ## 294                                           
    ## 295                                           
    ## 296                 bermudezursula@hotmail.com
    ## 297                                           
    ## 298                                           
    ## 299                                           
    ## 300                                           
    ## 301                                           
    ## 302                                           
    ## 303                                           
    ## 304                  bautista.abanto@gmail.com
    ## 305                                           
    ## 306                                           
    ## 307                                           
    ## 308                                           
    ## 309                                           
    ## 310                                           
    ## 311                                           
    ## 312                                           
    ## 313                                           
    ## 314                                           
    ## 315                                           
    ## 316                                           
    ## 317                                           
    ## 318                                           
    ## 319                                           
    ## 320                                           
    ## 321                                           
    ## 322                                           
    ## 323                                           
    ## 324                                           
    ## 325                                           
    ## 326                                           
    ## 327                                           
    ## 328                                           
    ## 329                                           
    ## 330                                           
    ## 331                                           
    ## 332                                           
    ## 333                                           
    ## 334                                           
    ## 335                                           
    ## 336                                           
    ## 337                                           
    ## 338                                           
    ## 339                                           
    ## 340                                           
    ## 341                                           
    ## 342                                           
    ## 343                                           
    ## 344                                           
    ## 345                                           
    ## 346                                           
    ## 347                                           
    ## 348                                           
    ## 349                                           
    ## 350                                           
    ## 351                                           
    ## 352                                           
    ## 353              rubenrodriguezcoras@gmail.com
    ## 354                                           
    ## 355                                           
    ## 356                                           
    ## 357                                           
    ## 358                                           
    ## 359                                           
    ## 360                                           
    ## 361                                           
    ## 362                                           
    ## 363                                           
    ## 364                                           
    ## 365                                           
    ## 366                                           
    ## 367                                           
    ## 368                                           
    ## 369                                           
    ## 370                                           
    ## 371                                           
    ## 372                                           
    ## 373                                           
    ## 374                                           
    ## 375                                           
    ## 376                                           
    ## 377                                           
    ## 378                                           
    ## 379                     laurabcm1999@gmail.com
    ## 380                                           
    ## 381                                           
    ## 382                                           
    ## 383                                           
    ## 384                                           
    ## 385                                           
    ## 386                                           
    ## 387                                           
    ## 388                                           
    ## 389                                           
    ## 390                                           
    ## 391                                           
    ## 392                                           
    ## 393                                           
    ## 394                                           
    ## 395                                           
    ## 396                                           
    ## 397                                           
    ## 398                                           
    ## 399                                           
    ## 400                                           
    ## 401                                           
    ## 402                                           
    ## 403                                           
    ## 404                                           
    ## 405                                           
    ## 406                                           
    ## 407                                           
    ## 408                                           
    ## 409                                           
    ## 410                                           
    ## 411                                           
    ## 412                                           
    ## 413                                           
    ## 414                                           
    ## 415                                           
    ## 416                                           
    ## 417                                           
    ## 418                                           
    ## 419                                           
    ## 420                                           
    ## 421                                           
    ## 422                                           
    ## 423                                           
    ## 424                                           
    ## 425                                           
    ## 426                                           
    ## 427                                           
    ## 428                                           
    ## 429                    jasonlynchy@outlook.com
    ## 430                                           
    ## 431                                           
    ## 432                                           
    ## 433                                           
    ## 434                                           
    ## 435                                           
    ## 436                                           
    ## 437                         elullirl@gmail.com
    ## 438                                           
    ## 439                                           
    ## 440                                           
    ## 441                                           
    ## 442                                           
    ## 443                                           
    ## 444                                           
    ## 445                                           
    ## 446                                           
    ## 447                                           
    ## 448                                           
    ## 449                                           
    ## 450                                           
    ## 451                                           
    ## 452                                           
    ## 453                                           
    ## 454                                           
    ## 455                                           
    ## 456                                           
    ## 457                                           
    ## 458                                           
    ## 459                                           
    ## 460                                           
    ## 461                                           
    ## 462                                           
    ## 463                                           
    ## 464                                           
    ## 465                                           
    ## 466                                           
    ## 467                                           
    ## 468                                           
    ## 469                                           
    ## 470                                           
    ## 471                                           
    ## 472                                           
    ## 473                                           
    ## 474                                           
    ## 475                                           
    ## 476                                           
    ## 477                                           
    ## 478            noelia.avalosalvarado@gmail.com
    ## 479                                           
    ## 480                                           
    ## 481                                           
    ## 482                                           
    ## 483                                           
    ## 484                                           
    ## 485                                           
    ## 486                                           
    ## 487                                           
    ## 488                                           
    ## 489                        rodrigo@aiyuapp.com
    ## 490                                           
    ## 491                                           
    ## 492                                           
    ## 493                                           
    ## 494                                           
    ## 495                                           
    ## 496                                           
    ## 497                                           
    ## 498                                           
    ## 499                                           
    ## 500                                           
    ## 501                                           
    ## 502                                           
    ## 503                                           
    ## 504                                           
    ## 505                                           
    ## 506                                           
    ## 507                                           
    ## 508                                           
    ## 509                                           
    ## 510                                           
    ## 511                                           
    ## 512                         miich.qh@gmail.com
    ## 513                                           
    ## 514                                           
    ## 515                                           
    ## 516                                           
    ## 517                                           
    ## 518                                           
    ## 519                                           
    ## 520                                           
    ## 521                                           
    ## 522                                           
    ## 523                                           
    ## 524                                           
    ## 525                                           
    ## 526                                           
    ## 527                                           
    ## 528                                           
    ## 529                                           
    ## 530                                           
    ## 531                                           
    ## 532                                           
    ## 533                                           
    ## 534                                           
    ## 535                                           
    ## 536                                           
    ## 537                                           
    ## 538                                           
    ## 539                                           
    ## 540                                           
    ## 541                                           
    ## 542                                           
    ## 543                                           
    ## 544                                           
    ## 545                                           
    ## 546                                           
    ## 547                                           
    ## 548                                           
    ## 549                                           
    ## 550                                           
    ## 551                                           
    ## 552                                           
    ## 553                                           
    ## 554                                           
    ## 555                                           
    ## 556                                           
    ## 557                                           
    ## 558                                           
    ## 559                                           
    ## 560                                           
    ## 561                                           
    ## 562                                           
    ## 563                                           
    ## 564                     sebastiansm7@gmail.com
    ## 565                                           
    ## 566                                           
    ## 567                                           
    ## 568                                           
    ## 569                                           
    ## 570                                           
    ## 571                                           
    ## 572                                           
    ## 573                                           
    ## 574                                           
    ## 575                                           
    ## 576                                           
    ## 577                                           
    ## 578                                           
    ## 579                                           
    ## 580                                           
    ## 581                                           
    ## 582                                           
    ## 583                                           
    ## 584                                           
    ## 585                                           
    ## 586                                           
    ## 587                                           
    ## 588                   claudia_0720@hotmail.com
    ## 589                                           
    ## 590                                           
    ## 591                                           
    ## 592                                           
    ## 593                                           
    ## 594                                           
    ## 595                                           
    ## 596                                           
    ## 597                                           
    ## 598                                           
    ## 599                                           
    ## 600                                           
    ## 601                                           
    ## 602                                           
    ## 603                                           
    ## 604                                           
    ## 605                                           
    ## 606                     stuartbrown1@gmail.com
    ## 607                                           
    ## 608                                           
    ## 609                                           
    ## 610                                           
    ## 611                                           
    ## 612                                           
    ## 613                                           
    ## 614                                           
    ## 615                                           
    ## 616                                           
    ## 617                                           
    ## 618                                           
    ## 619                                           
    ## 620                                           
    ## 621                                           
    ## 622                                           
    ## 623                                           
    ## 624                                           
    ## 625                                           
    ## 626                                           
    ## 627                                           
    ## 628                                           
    ## 629                                           
    ## 630                                           
    ## 631                        vojedac16@gmail.com
    ## 632                                           
    ## 633                                           
    ## 634                                           
    ## 635                                           
    ## 636                                           
    ## 637                                           
    ## 638                                           
    ## 639                                           
    ## 640                                           
    ## 641                                           
    ## 642                                           
    ## 643                 andrecastrotafur@gmail.com
    ## 644                                           
    ## 645                                           
    ## 646                                           
    ## 647                                           
    ## 648                                           
    ## 649                                           
    ## 650                                           
    ## 651                                           
    ## 652                                           
    ## 653                                           
    ## 654                                           
    ## 655                                           
    ## 656                                           
    ## 657                                           
    ## 658                                           
    ## 659                                           
    ## 660                                           
    ## 661                       renzocht97@gmail.com
    ## 662                                           
    ## 663                                           
    ## 664                                           
    ## 665                                           
    ## 666                                           
    ## 667                                           
    ## 668                                           
    ## 669                                           
    ## 670                                           
    ## 671                                           
    ## 672               jaimeescribens1302@gmail.com
    ## 673                                           
    ## 674                                           
    ## 675                                           
    ## 676                                           
    ## 677                                           
    ## 678                                           
    ## 679                       mduranteau@gmail.com
    ## 680                                           
    ## 681                                           
    ## 682                       alisiaco97@gmail.com
    ## 683                                           
    ## 684                                           
    ## 685                                           
    ## 686                                           
    ## 687                alvaro@singularadvisors.com
    ## 688                                           
    ## 689                                           
    ## 690                                           
    ## 691                                           
    ## 692                                           
    ## 693                                           
    ## 694                                           
    ## 695                                           
    ## 696                                           
    ## 697                                           
    ## 698                                           
    ## 699                                           
    ## 700                                           
    ## 701                                           
    ## 702                                           
    ## 703                                           
    ## 704                                           
    ## 705                                           
    ## 706                                           
    ## 707                                           
    ## 708                                           
    ## 709                     martincanosa@gmail.com
    ## 710                                           
    ## 711                                           
    ## 712                    moshefabricio@gmail.com
    ## 713                                           
    ## 714                                           
    ## 715                                           
    ## 716                                           
    ## 717                                           
    ## 718                                           
    ## 719                                           
    ## 720                                           
    ## 721                                           
    ## 722                                           
    ## 723                                           
    ## 724                                           
    ## 725                                           
    ## 726                                           
    ## 727                                           
    ## 728                                           
    ## 729                                           
    ## 730                                           
    ## 731                                           
    ## 732                                           
    ## 733                                           
    ## 734                                           
    ## 735                                           
    ## 736                                           
    ## 737                                           
    ## 738                                           
    ## 739                                           
    ## 740                                           
    ## 741                                           
    ## 742                                           
    ## 743                        rllanos@hotmail.com
    ## 744                                           
    ## 745                                           
    ## 746                                           
    ## 747                                           
    ## 748                                           
    ## 749                                           
    ## 750                                           
    ## 751                                           
    ## 752                                           
    ## 753                                           
    ## 754                                           
    ## 755                                           
    ## 756                                           
    ## 757                                           
    ## 758                                           
    ## 759                                           
    ## 760                                           
    ## 761                                           
    ## 762                                           
    ## 763                                           
    ## 764                                           
    ## 765                                           
    ## 766                                           
    ## 767                                           
    ## 768                                           
    ## 769                                           
    ## 770                                           
    ## 771                                           
    ## 772                                           
    ## 773                                           
    ## 774                                           
    ## 775                                           
    ## 776                                           
    ## 777                                           
    ## 778                                           
    ## 779                                           
    ## 780                                           
    ## 781                                           
    ## 782                                           
    ## 783                                           
    ## 784                                           
    ## 785                                           
    ## 786                                           
    ## 787                                           
    ## 788                                           
    ## 789                                           
    ## 790                                           
    ## 791                                           
    ## 792                                           
    ## 793                                           
    ## 794                                           
    ## 795                                           
    ## 796                                           
    ## 797                                           
    ## 798                                           
    ## 799                                           
    ## 800                                           
    ## 801                                           
    ## 802                                           
    ## 803                                           
    ## 804                                           
    ## 805                                           
    ## 806                                           
    ## 807                                           
    ## 808                                           
    ## 809                                           
    ## 810                                           
    ## 811                                           
    ## 812                                           
    ## 813                                           
    ## 814                                           
    ## 815                                           
    ## 816                                           
    ## 817                                           
    ## 818                                           
    ## 819                                           
    ## 820                                           
    ## 821                                           
    ## 822                                           
    ## 823                                           
    ## 824                                           
    ## 825                                           
    ## 826                                           
    ## 827                                           
    ## 828                                           
    ## 829                                           
    ## 830                                           
    ## 831                                           
    ## 832                                           
    ## 833                                           
    ## 834                                           
    ## 835                                           
    ## 836                                           
    ## 837                                           
    ## 838                                           
    ## 839                                           
    ## 840                                           
    ## 841                                           
    ## 842                                           
    ## 843                                           
    ## 844                                           
    ## 845                                           
    ## 846                                           
    ## 847                                           
    ## 848                                           
    ## 849                                           
    ## 850                                           
    ## 851                                           
    ## 852                                           
    ## 853                                           
    ## 854  tomas.villanueva.romero.clavijo@gmail.com
    ## 855                                           
    ## 856                                           
    ## 857                                           
    ## 858                                           
    ## 859                                           
    ## 860                                           
    ## 861                                           
    ## 862                                           
    ## 863                                           
    ## 864                                           
    ## 865                                           
    ## 866                                           
    ## 867                                           
    ## 868                                           
    ## 869                                           
    ## 870                                           
    ## 871                     agarciao1965@gmail.com
    ## 872                                           
    ## 873                                           
    ## 874                                           
    ## 875                                           
    ## 876                                           
    ## 877                                           
    ## 878                                           
    ## 879                                           
    ## 880                                           
    ## 881                                           
    ## 882                                           
    ## 883                                           
    ## 884                                           
    ## 885                                           
    ## 886                                           
    ## 887                                           
    ## 888                                           
    ## 889                                           
    ## 890                                           
    ## 891                                           
    ## 892                                           
    ## 893                                           
    ## 894                                           
    ## 895                                           
    ## 896                                           
    ## 897                                           
    ## 898                                           
    ## 899                                           
    ## 900                                           
    ## 901                         daniel@velogig.com
    ## 902                                           
    ## 903                                           
    ## 904                                           
    ## 905                                           
    ## 906                                           
    ## 907                                           
    ## 908                                           
    ## 909                                           
    ## 910                                           
    ## 911                                           
    ## 912                                           
    ## 913                                           
    ## 914                                           
    ## 915                                           
    ## 916                                           
    ## 917                                           
    ## 918                                           
    ## 919                                           
    ## 920                                           
    ## 921                                           
    ## 922                                           
    ## 923                                           
    ## 924                                           
    ## 925                                           
    ## 926                                           
    ## 927                                           
    ## 928                                           
    ## 929                                           
    ## 930                                           
    ## 931                                           
    ## 932                                           
    ## 933                                           
    ## 934                                           
    ## 935                                           
    ## 936                                           
    ## 937                                           
    ## 938                                           
    ## 939                                           
    ## 940                                           
    ## 941                                           
    ## 942                                           
    ## 943                                           
    ## 944                                           
    ## 945                                           
    ## 946                                           
    ## 947                                           
    ## 948                                           
    ## 949                                           
    ## 950                                           
    ## 951                                           
    ## 952                                           
    ## 953                                           
    ## 954                                           
    ## 955                                           
    ## 956                                           
    ## 957                                           
    ## 958                                           
    ## 959                                           
    ## 960                                           
    ## 961                                           
    ## 962                                           
    ## 963                                           
    ## 964                                           
    ## 965                                           
    ## 966                                           
    ## 967                                           
    ## 968                                           
    ## 969                                           
    ## 970                                           
    ## 971                                           
    ## 972                                           
    ## 973                                           
    ## 974                                           
    ## 975                                           
    ## 976                                           
    ## 977                       rhmoreno@pucp.edu.pe
    ## 978                                           
    ## 979                                           
    ## 980                                           
    ## 981                                           
    ## 982                                           
    ## 983                                           
    ## 984                                           
    ## 985                                           
    ## 986                                           
    ## 987                                           
    ## 988                                           
    ## 989                                           
    ## 990                                           
    ## 991                                           
    ## 992                                           
    ## 993                                           
    ## 994                                           
    ## 995                                           
    ## 996                                           
    ## 997                                           
    ## 998                                           
    ## 999                                           
    ## 1000                                          
    ## 1001                                          
    ## 1002                                          
    ## 1003                       chi_mzt@hotmail.com
    ## 1004                                          
    ## 1005                                          
    ## 1006           carloscortesjaramillo@gmail.com
    ## 1007                                          
    ## 1008                                          
    ## 1009                                          
    ## 1010                                          
    ## 1011                                          
    ## 1012                                          
    ## 1013                                          
    ## 1014                                          
    ## 1015                                          
    ## 1016                                          
    ## 1017                                          
    ## 1018                                          
    ## 1019                                          
    ## 1020                                          
    ## 1021                                          
    ## 1022                                          
    ## 1023                                          
    ## 1024                                          
    ## 1025                                          
    ## 1026                                          
    ## 1027                                          
    ## 1028               carloshmireles@mskompas.com
    ## 1029                                          
    ## 1030                                          
    ## 1031                                          
    ## 1032                                          
    ## 1033                                          
    ## 1034                                          
    ## 1035                                          
    ## 1036                                          
    ## 1037                                          
    ## 1038                                          
    ## 1039                                          
    ## 1040                                          
    ## 1041                                          
    ## 1042                                          
    ## 1043                                          
    ## 1044                                          
    ## 1045                                          
    ## 1046                                          
    ## 1047                                          
    ## 1048                                          
    ## 1049                                          
    ## 1050                                          
    ## 1051                                          
    ## 1052                                          
    ## 1053                                          
    ## 1054                                          
    ## 1055                                          
    ## 1056                                          
    ## 1057                                          
    ## 1058                                          
    ## 1059                                          
    ## 1060                                          
    ## 1061              vgutierrez@hlmsoluciones.com
    ## 1062                                          
    ## 1063                                          
    ## 1064                                          
    ## 1065                                          
    ## 1066                                          
    ## 1067                                          
    ## 1068                                          
    ## 1069                                          
    ## 1070                                          
    ## 1071                                          
    ## 1072                                          
    ## 1073                                          
    ## 1074                                          
    ## 1075                                          
    ## 1076                                          
    ## 1077                                          
    ## 1078                                          
    ## 1079                                          
    ## 1080                                          
    ## 1081                                          
    ## 1082                                          
    ## 1083                                          
    ## 1084                                          
    ## 1085                                          
    ## 1086                                          
    ## 1087                hector.vivas@bairesdev.com
    ## 1088                                          
    ## 1089                                          
    ## 1090                                          
    ## 1091                                          
    ## 1092                                          
    ## 1093                                          
    ## 1094                                          
    ## 1095                                          
    ## 1096                                          
    ## 1097                                          
    ## 1098                                          
    ## 1099                                          
    ## 1100                                          
    ## 1101                                          
    ## 1102                                          
    ## 1103                                          
    ## 1104                                          
    ## 1105                                          
    ## 1106                                          
    ## 1107                                          
    ## 1108                                          
    ## 1109                                          
    ## 1110                                          
    ## 1111                                          
    ## 1112                                          
    ## 1113                                          
    ## 1114                                          
    ## 1115                                          
    ## 1116                                          
    ## 1117                                          
    ## 1118                                          
    ## 1119                                          
    ## 1120                                          
    ## 1121                                          
    ## 1122                                          
    ## 1123                                          
    ## 1124              andres.miyagi@student.ie.edu
    ## 1125                                          
    ## 1126                                          
    ## 1127                                          
    ## 1128                                          
    ## 1129                                          
    ## 1130                                          
    ## 1131                                          
    ## 1132                                          
    ## 1133                                          
    ## 1134                                          
    ## 1135                                          
    ## 1136                                          
    ## 1137                                          
    ## 1138                                          
    ## 1139                                          
    ## 1140                                          
    ## 1141                                          
    ## 1142                                          
    ## 1143                                          
    ## 1144                                          
    ## 1145                                          
    ## 1146                                          
    ## 1147                                          
    ## 1148                                          
    ## 1149                                          
    ## 1150                                          
    ## 1151                                          
    ## 1152                                          
    ## 1153                                          
    ## 1154                                          
    ## 1155                                          
    ## 1156                                          
    ## 1157                                          
    ## 1158                                          
    ## 1159                                          
    ## 1160                                          
    ## 1161                                          
    ## 1162                                          
    ## 1163                                          
    ## 1164                                          
    ## 1165                                          
    ## 1166                                          
    ## 1167                                          
    ## 1168                                          
    ## 1169                                          
    ## 1170                                          
    ## 1171                                          
    ## 1172                                          
    ## 1173                                          
    ## 1174                                          
    ## 1175                                          
    ## 1176                                          
    ## 1177                                          
    ## 1178                                          
    ## 1179                                          
    ## 1180                                          
    ## 1181                                          
    ## 1182                                          
    ## 1183                                          
    ## 1184                                          
    ## 1185                                          
    ## 1186                                          
    ## 1187                                          
    ## 1188                                          
    ## 1189                                          
    ## 1190                                          
    ## 1191                                          
    ## 1192                                          
    ## 1193                                          
    ## 1194                                          
    ## 1195                                          
    ## 1196                                          
    ## 1197                                          
    ## 1198                                          
    ## 1199                                          
    ## 1200                                          
    ## 1201                                          
    ## 1202                                          
    ## 1203                                          
    ## 1204                                          
    ## 1205                                          
    ## 1206                                          
    ## 1207                                          
    ## 1208                                          
    ## 1209                                          
    ## 1210                                          
    ## 1211                                          
    ## 1212                                          
    ## 1213                                          
    ## 1214                                          
    ## 1215                                          
    ## 1216                                          
    ## 1217                                          
    ## 1218                                          
    ## 1219                                          
    ## 1220                                          
    ## 1221                                          
    ## 1222                                          
    ## 1223                                          
    ## 1224                                          
    ## 1225                                          
    ## 1226                                          
    ## 1227                                          
    ## 1228                                          
    ## 1229                                          
    ## 1230                                          
    ## 1231                                          
    ## 1232                                          
    ## 1233                                          
    ## 1234                                          
    ## 1235                                          
    ## 1236                                          
    ## 1237                                          
    ## 1238                                          
    ## 1239                                          
    ## 1240                                          
    ## 1241                                          
    ## 1242                                          
    ## 1243                                          
    ## 1244                                          
    ## 1245                                          
    ## 1246                                          
    ## 1247                                          
    ## 1248                                          
    ## 1249                                          
    ## 1250                                          
    ## 1251                                          
    ## 1252                                          
    ## 1253                                          
    ## 1254                                          
    ## 1255                                          
    ## 1256                                          
    ## 1257                                          
    ## 1258                                          
    ## 1259                                          
    ## 1260                                          
    ## 1261                                          
    ## 1262                                          
    ## 1263                      lorena@imacom.com.pe
    ## 1264                                          
    ## 1265                                          
    ## 1266                                          
    ## 1267                                          
    ## 1268                                          
    ## 1269                                          
    ## 1270                                          
    ## 1271                                          
    ## 1272                                          
    ## 1273                                          
    ## 1274                                          
    ## 1275                                          
    ## 1276                                          
    ## 1277                                          
    ## 1278                                          
    ## 1279                                          
    ## 1280                                          
    ## 1281                                          
    ## 1282                                          
    ## 1283                                          
    ## 1284                                          
    ## 1285                                          
    ## 1286                                          
    ## 1287                                          
    ## 1288                                          
    ##                                                                                 Company
    ## 1                                                                   Maple (getmaple.ca)
    ## 2                                                                              Shared-X
    ## 3                                                                       Pratt & Whitney
    ## 4                                                                                      
    ## 5                                                                           Intelligems
    ## 6                                                                             Interbank
    ## 7                                                                   Investissements PSP
    ## 8                                                                               Dataiku
    ## 9                                                                Pratt & Whitney Canada
    ## 10                                                                                 HSBC
    ## 11                                                                              Transat
    ## 12                                                                                Ontop
    ## 13                                                                            Hootsuite
    ## 14                                                                            Interbank
    ## 15                                                                          WindTech AI
    ## 16                                                                       Rely On Dreams
    ## 17                                                                               Google
    ## 18                                                                           HelloFresh
    ## 19                                                                              Shopify
    ## 20                                                                     Bazar del Bosque
    ## 21                                                                                AMLUL
    ## 22                                                                            Starbucks
    ## 23                                                                           LAIVE S.A.
    ## 24                                                                      Lambton College
    ## 25                                                                           BOMBARDIER
    ## 26                                                              Pezer Investments Corp.
    ## 27                                                                         Sia Partners
    ## 28                                  McGill University - Desautels Faculty of Management
    ## 29                                  McGill University - Desautels Faculty of Management
    ## 30                                                                         AC Capitales
    ## 31                                                                 SIA Innovations Inc.
    ## 32                                                                               Frollo
    ## 33                                                                        SharpestMinds
    ## 34                                  McGill University - Desautels Faculty of Management
    ## 35                                                   Desautels Business Technology Club
    ## 36                                                                Keurig Dr Pepper Inc.
    ## 37                                                                    Luxaviation Group
    ## 38                                                        Boston Consulting Group (BCG)
    ## 39                                                                       Optima Energía
    ## 40                                                                                TELUS
    ## 41                                  McGill University - Desautels Faculty of Management
    ## 42                                                                             Novartis
    ## 43                                                                            Metrolinx
    ## 44                                                                        ArcelorMittal
    ## 45                                                                      Lens Technology
    ## 46                                                  Sociedad Era Contratistas Generales
    ## 47                                                           Banque Nationale du Canada
    ## 48                                                                         Sia Partners
    ## 49                                                              CFG Investment-Copeinca
    ## 50                                                                       Arshinkooh Co.
    ## 51                                                              NTT DATA Europe & LATAM
    ## 52                                  McGill University - Desautels Faculty of Management
    ## 53                                                                              Moov AI
    ## 54                                                                            wymaq.com
    ## 55                                                                 Overhaul Machineries
    ## 56                                                                              Hiraoka
    ## 57                                                                                Rappi
    ## 58                                                                        Pisco Huamaní
    ## 59                                                             Consultor Independiente.
    ## 60                                                                     aNumak & Company
    ## 61                                                                    APOYO Consultoría
    ## 62                                                                        Betsson Group
    ## 63                                                                                  CGI
    ## 64                                                                      McKesson Canada
    ## 65                                                                                 Laps
    ## 66                                                                                  DHL
    ## 67                                                                                     
    ## 68                                                                               Verint
    ## 69                                                                 Banco de Crédito BCP
    ## 70                                                                KPI Digital Solutions
    ## 71                                                                 Banco de Crédito BCP
    ## 72                                                                                  IBM
    ## 73                                                                            Grupo AJE
    ## 74                                                                             Arquinsa
    ## 75                                                           Rimac Seguros y Reaseguros
    ## 76                                                                        EFIC Partners
    ## 77                                                                    McGill University
    ## 78                                                                              Targray
    ## 79                                  McGill University - Desautels Faculty of Management
    ## 80                                                                            Kavak.com
    ## 81                                                                             Monithor
    ## 82                                                                                 KPMG
    ## 83                                                                            Rio Tinto
    ## 84                                                                             Deloitte
    ## 85                                                                                   EY
    ## 86                                                      École Polytechnique de Montréal
    ## 87                                                                               Twitch
    ## 88                                                                       Morgan Stanley
    ## 89                                                                              Moov AI
    ## 90                                                                              Moov AI
    ## 91                                                                          KPMG Canada
    ## 92                                                                              Moov AI
    ## 93                                                                          Air Transat
    ## 94                                                      École de technologie supérieure
    ## 95                                                                  Marsh Latinoamérica
    ## 96                                                                         LABOCER S.A.
    ## 97                                                                         HEC Montréal
    ## 98                                                           Wilfrid Laurier University
    ## 99                                                                               Abbott
    ## 100                                                                         Air Transat
    ## 101                                                                    Procter & Gamble
    ## 102                                                                        Sia Partners
    ## 103                                                          180 Degrees Consulting UP 
    ## 104                                                                                BBVA
    ## 105                                                                    Centro Gagliuffi
    ## 106                                                                Montebello Packaging
    ## 107                                 McGill University - Desautels Faculty of Management
    ## 108                                                              Kovacs & Asociados SAC
    ## 109                                 McGill University - Desautels Faculty of Management
    ## 110                                        SAP - Sports & Entertainment - North America
    ## 111                                                              Pratt & Whitney Canada
    ## 112                                                                                 CGI
    ## 113                                                                         Air Transat
    ## 114                                 McGill University - Desautels Faculty of Management
    ## 115                                                                   McGill University
    ## 116                                                                             PepsiCo
    ## 117                                           International Development Group LLC (IDG)
    ## 118                                                                          HOCHSCHILD
    ## 119                                                                           Interbank
    ## 120                                                              Pratt & Whitney Canada
    ## 121                                                                          Scotiabank
    ## 122                                                                       Héroux-Devtek
    ## 123                                                                            Mistplay
    ## 124  COVID-19 Immunity Task Force | Groupe de travail sur l’immunité face à la COVID-19
    ## 125                                                                   McGill University
    ## 126                                                             Keurig Dr Pepper Canada
    ## 127                                 McGill University - Desautels Faculty of Management
    ## 128                                                                                 PwC
    ## 129                                                                              Backus
    ## 130                                                                     Bernal Partners
    ## 131                                                                    XGIMI Technology
    ## 132                                                                     Banco Santander
    ## 133                                 McGill University - Desautels Faculty of Management
    ## 134                                                                     McKesson Canada
    ## 135                                                                                 CGI
    ## 136                                                                            Autodesk
    ## 137                                                            Resolute Forest Products
    ## 138                                                                 Robi Axiata Limited
    ## 139                                                                         Dora Desino
    ## 140                                                                                 CAE
    ## 141                                                                           Interbank
    ## 142                                                                                JOKR
    ## 143                                                               Rogers Communications
    ## 144                                                                          Millennial
    ## 145                                                                      Morgan Stanley
    ## 146                                 McGill University - Desautels Faculty of Management
    ## 147                                                               Rogers Communications
    ## 148                                                                    Ubisoft Montréal
    ## 149                                                                                KPMG
    ## 150                                                                                 RBC
    ## 151                                                                          Korn Ferry
    ## 152                                                                                 SAP
    ## 153                                                                                BGIS
    ## 154                                                                 Wall Street English
    ## 155                                                                       Atria Energía
    ## 156                                                                            Glencore
    ## 157                                                                        Polysistemas
    ## 158                                                                       Vikingo store
    ## 159                                                                   Agroved Fruit Sac
    ## 160                                                            <U+6B27><U+83B1><U+96C5>
    ## 161                                                                     McKesson Canada
    ## 162                                 McGill University - Desautels Faculty of Management
    ## 163                                 McGill University - Desautels Faculty of Management
    ## 164                                                                             Hotstar
    ## 165                                                                       D2V Analytics
    ## 166                                                                                    
    ## 167                                                                                  CN
    ## 168                                                                      Monarchy Build
    ## 169                                                                IPM World Properties
    ## 170                                                               Rogers Communications
    ## 171                                                                          ServiceNow
    ## 172                                                                          Consulting
    ## 173                                                                 BMO Commercial Bank
    ## 174                                 McGill University - Desautels Faculty of Management
    ## 175                                                                             Alicorp
    ## 176                                                                 Right Curly Bracket
    ## 177                                 McGill University - Desautels Faculty of Management
    ## 178                                                           AssetIO Wealth Management
    ## 179                                                                           FrienDuel
    ## 180                                                                           Metrolinx
    ## 181                                                                          Entel Perú
    ## 182                                                                              Sanofi
    ## 183                                                                            Autodesk
    ## 184                                                                                    
    ## 185                                                                             Mibanco
    ## 186                                                                         MAPFRE PERÚ
    ## 187                                                                            Deloitte
    ## 188                                                            Loblaw Companies Limited
    ## 189                                                                      Tempo Software
    ## 190                                                                                KPMG
    ## 191                                                     Bajaj Allianz General Insurance
    ## 192                                                                            MindGeek
    ## 193                                                              Pratt & Whitney Canada
    ## 194                                                                           IGA, INC.
    ## 195                                                                             Alicorp
    ## 196                                                                               TELUS
    ## 197                                                                              Aktana
    ## 198                                                                            Deloitte
    ## 199                                                                              Nasdaq
    ## 200                                                 Noon - The Social Learning Platform
    ## 201                                                                             Alicorp
    ## 202                                                                Banco de Crédito BCP
    ## 203                                                                        Hikari Group
    ## 204                                                                      Talent2Win USA
    ## 205                                                                              Adecco
    ## 206                                                     Banco de Crédito del Perú - BCP
    ## 207                                                                               Stori
    ## 208                                                                           Offeteria
    ## 209                                                                              CERTUS
    ## 210                                                          Wall Street English - Peru
    ## 211                                                                                    
    ## 212                                                                                    
    ## 213                                                                     SmartPrint Perú
    ## 214                                                                     McKesson Canada
    ## 215                                                           Odette School of Business
    ## 216                                                                      Brother Canada
    ## 217                                                                         BNP Paribas
    ## 218                                                                   McGill University
    ## 219                                                                              Slalom
    ## 220                                                                               Shell
    ## 221                                                                             Verizon
    ## 222                                                                     Bombonería Pons
    ## 223                                                                          Scotiabank
    ## 224                                                                            Autodesk
    ## 225                                                             DHL eCommerce Solutions
    ## 226                                                                            Novartis
    ## 227                                                                            McKesson
    ## 228                                                                            Antamina
    ## 229                                                                             Viatris
    ## 230                                                                            Novartis
    ## 231                                                  Macdonald Campus Students' Society
    ## 232                                                                          Scotiabank
    ## 233                                                                            Autodesk
    ## 234                                                                               Apple
    ## 235                                                                   McGill University
    ## 236                                 McGill University - Desautels Faculty of Management
    ## 237                                                                    Diners Club Perú
    ## 238                                                                                 IGT
    ## 239                                                                         Air Transat
    ## 240                                                                            Novartis
    ## 241                                                                          Scotiabank
    ## 242                                                                   McGill University
    ## 243                                                                                Bell
    ## 244                                 McGill University - Desautels Faculty of Management
    ## 245                                                                            Novartis
    ## 246                                                                           GRUPO DNA
    ## 247                                              McGill University - Faculty of Science
    ## 248                                                                         KPMG Canada
    ## 249                                                                       TOCA Football
    ## 250                                                                              CARS24
    ## 251                                                                          BOMBARDIER
    ## 252                                                             DHL eCommerce Solutions
    ## 253                                                                                Beat
    ## 254                                 McGill University - Desautels Faculty of Management
    ## 255                                                                        TD Insurance
    ## 256                                                             DHL eCommerce Solutions
    ## 257                                                               Rogers Communications
    ## 258                                                                             Belcorp
    ## 259                                                              Pentación Espectáculos
    ## 260                                                                             Belcorp
    ## 261                                                                            Deloitte
    ## 262                                 McGill University - Desautels Faculty of Management
    ## 263                                                                               Unity
    ## 264                                                                                  CN
    ## 265                                                              Waterborne Skateboards
    ## 266                                                                             Gorgias
    ## 267                                                                 Mosaic-HEC Montréal
    ## 268                                                                    Procter & Gamble
    ## 269                                                                          BOMBARDIER
    ## 270                                                                          Scotiabank
    ## 271                                 McGill University - Desautels Faculty of Management
    ## 272                                                                           Metrolinx
    ## 273                                                               Keurig Dr Pepper Inc.
    ## 274                                   Global Affairs Canada | Affaires mondiales Canada
    ## 275                                                                           Accenture
    ## 276                                                                            Plus 5XP
    ## 277                                                                             WeSpire
    ## 278                                                                       CAT-Barcelona
    ## 279                                                C-F Business Links (CFBL Consulting)
    ## 280                                                                         Air Transat
    ## 281                                 McGill University - Desautels Faculty of Management
    ## 282                                                                       Mercado Libre
    ## 283                                                                      MG gastronomia
    ## 284                                                                           APP GROUP
    ## 285                                                                              Selina
    ## 286                                                                       Endeavor Perú
    ## 287                                                                          Entel Perú
    ## 288                                                            Universidad del Pacifico
    ## 289                                                                              Amazon
    ## 290                                                                             Belcorp
    ## 291                                                                                BBVA
    ## 292                                                          Banco de la Nación de Perú
    ## 293                                                                                 IBM
    ## 294                                                                    Talent2Win Latam
    ## 295                                                                              Atento
    ## 296                                                                       Imdex Limited
    ## 297                                                                    Logitravel Group
    ## 298                                                                        Onapsis Inc.
    ## 299                                                         York Consulting Group (YCG)
    ## 300       Grupo CRES | Camet Real Estate Services (comercial, residencial e industrial)
    ## 301                                                                              3ERIZA
    ## 302                                                                   Colgate-Palmolive
    ## 303                                                                        Michael Page
    ## 304                                                                             Vooxell
    ## 305                      Neo Consulting - Consultora de Innovación y Estrategia Digital
    ## 306                                                              Data Engineering LATAM
    ## 307                                                                        Factorial HR
    ## 308                                                                           Grupo AJE
    ## 309                                                                           Interbank
    ## 310                                                                             Belcorp
    ## 311                                                                          Cheil Peru
    ## 312                                                               People Analytics Perú
    ## 313                                                                               QROMA
    ## 314                                                                              Keyrus
    ## 315                                                                   Credicorp Capital
    ## 316                                                                        Métrica Perú
    ## 317                                                              Doulton Drinking Water
    ## 318                                                                               Entel
    ## 319                                                                              Yanbal
    ## 320                                                                       Cencosud S.A.
    ## 321                                                                          Entel Perú
    ## 322                                                                 Entel Empresas Perú
    ## 323                                                                          Entel Perú
    ## 324                                                                          Entel Perú
    ## 325                                                              Mondelez International
    ## 326                                                                                    
    ## 327                                                                          Entel Perú
    ## 328                                                                    Pacífico Seguros
    ## 329                                                                    Huevos La Calera
    ## 330                                                                Banco de Crédito BCP
    ## 331                                                                    Applaudo Studios
    ## 332                                                                               Culqi
    ## 333                                                                            Red Bull
    ## 334                                                   Rodrigo, Elias & Medrano Abogados
    ## 335                                                                          PUMA Group
    ## 336                                                                                 SAP
    ## 337                                                                                Laps
    ## 338                                                           Winston Capital Advisors 
    ## 339                                                                Management Solutions
    ## 340                                                                          Salesforce
    ## 341                                                                             Belcorp
    ## 342                                                                           Dilat.arq
    ## 343                                                                               QROMA
    ## 344                                                                       Sapia Oficial
    ## 345                                                                               Rappi
    ## 346                                                                       Cencosud S.A.
    ## 347                                                                          Primax S.A
    ## 348                                                                              Juntas
    ## 349                                                   Universidad San Ignacio de Loyola
    ## 350                                                 Analytica Software and Technologies
    ## 351                                                                               BRECA
    ## 352                                                                        Igma Sports 
    ## 353                                                                          Scotiabank
    ## 354                                                         IDEM Organización Educativa
    ## 355                                                              Mondelez International
    ## 356                                                                        VNYSA Studio
    ## 357                                                              Cementos Pacasmayo SAA
    ## 358                                                                                 cbc
    ## 359                                                                             Belcorp
    ## 360                                                                           Garrigues
    ## 361                                                                             Alicorp
    ## 362                                                       MF Asesoría y Consultoría SAC
    ## 363                                                                      Ayni Educativo
    ## 364                                                                             Belcorp
    ## 365                                                                             Azzorti
    ## 366                                                                          Entel Perú
    ## 367                                                                               Paper
    ## 368                                                     Colegio Santa María Marianistas
    ## 369                                                                            DataKnow
    ## 370                                                                               Romex
    ## 371                                                                           Cognizant
    ## 372                                                                                    
    ## 373                                                                Banco de Crédito BCP
    ## 374                                                                          ALMA VITTA
    ## 375                                                                          Entel Perú
    ## 376                                                                   Colgate-Palmolive
    ## 377                                                                       CLUB NACIONAL
    ## 378                                                                        BBVA en Perú
    ## 379                                                                      Kimberly-Clark
    ## 380                                                          Falcon Management Partners
    ## 381                                 McGill University - Desautels Faculty of Management
    ## 382                                                                          Scotiabank
    ## 383                                                                            Autónomo
    ## 384                                                              Cementos Pacasmayo SAA
    ## 385                                                            Universidad del Pacifico
    ## 386                                                                Banco Santander Peru
    ## 387                                                               Volcan Cia Minera SAA
    ## 388                                                                            Autodesk
    ## 389                                                                   Baylor University
    ## 390                      Institute of Computing Technology, Chinese Academy of Sciences
    ## 391                                                                              Amazon
    ## 392                                                                        FLX AI, Inc.
    ## 393                                                      Soft group - Marketing y Trade
    ## 394                                                             University of Rochester
    ## 395                                                                         SKY Airline
    ## 396                                                                    Pacífico Seguros
    ## 397                                                                     Dive Consulting
    ## 398                                                       Rebaza Alcázar & De Las Casas
    ## 399                                                                             Untamed
    ## 400                                                                               Ontop
    ## 401                                                             Columbia Climate School
    ## 402                                                          University of Pennsylvania
    ## 403                                                                              Bilkom
    ## 404                                                          Columbia Economics Society
    ## 405                                                                           Park City
    ## 406                                                                            TGP Perú
    ## 407                                                                         Tienda Pago
    ## 408                                                                    Intercorp Retail
    ## 409                                                                    Pacífico Seguros
    ## 410                                                                          Entel Perú
    ## 411                                                                          HOCHSCHILD
    ## 412                                                                           Interbank
    ## 413                                                                     START Barcelona
    ## 414                                                                             Baufest
    ## 415                                                                            BHG CORP
    ## 416                                                                        Cedars-Sinai
    ## 417                                                                             Equifax
    ## 418                                                          University of Pennsylvania
    ## 419                                                                              Seidor
    ## 420                                       ASSOCIATION FOR COMPUTATIONAL LINGUISTICS INC
    ## 421                                                     Sociedad Nacional de Industrias
    ## 422                                                          ALEGREVO | Grupo Educativo
    ## 423                                                                            APD Perú
    ## 424                                                          University of Pennsylvania
    ## 425                                                                           Barchovia
    ## 426                                                                      Trade Republic
    ## 427                                                         Franco Ferraro Arquitectura
    ## 428                                                                    IA Collaborative
    ## 429                                   <U+5143><U+542F><U+8D44><U+672C> Thriving Capital
    ## 430                                                                       Haystack News
    ## 431                                                                          Entel Perú
    ## 432                                                                          Entel Perú
    ## 433                                                                          Entel Perú
    ## 434                                                                     Bloom Insurance
    ## 435                                                          University of Pennsylvania
    ## 436                                                                         Ripley Perú
    ## 437                                                                         Hidroponika
    ## 438                                                        The University of New Mexico
    ## 439                                                  México & Perú IT Business Services
    ## 440                                                             Shearman & Sterling LLP
    ## 441                                                                           Media Pro
    ## 442                                                Edinburgh University Consulting Club
    ## 443                                                                     Vodanovic Legal
    ## 444                                                       WWIN Planners by Wendy Wunder
    ## 445                                                             Bluetab, an IBM Company
    ## 446                                                                               Moovx
    ## 447                                                                               Manya
    ## 448                                                                              Inetum
    ## 449                                                                        WOM Colombia
    ## 450                                                                     Cambridge Spark
    ## 451                                                                       Goldman Sachs
    ## 452                                                                         Wells Fargo
    ## 453                                                                               WePay
    ## 454                                                                                  EY
    ## 455                                                     Barclay & Crousse Architecture 
    ## 456                                                                            Marcobre
    ## 457                                                          University of Pennsylvania
    ## 458                                                                        RecoveryLink
    ## 459                                                                               AzLab
    ## 460                                                                           Gallagher
    ## 461                                                                      A.G.S INT LLC 
    ## 462                                                              Mondelez International
    ## 463                                                          Sealand – A Maersk Company
    ## 464                                                                              Nestlé
    ## 465                                                                          Prestamype
    ## 466                                                                     Banco Santander
    ## 467                                                Libero Esports - grupo La República 
    ## 468                                                                          Scotiabank
    ## 469                                                                           INNSPIRAL
    ## 470                                                                               Rappi
    ## 471                                                               NewCapital Securities
    ## 472                                 Servicio de Administración Tributaria de Lima - SAT
    ## 473                                                                           Kavak.com
    ## 474                                                                               Cafin
    ## 475                                                                                  EY
    ## 476                                 Una Solutions - Innovación & Transformación Digital
    ## 477                                                       Rehabilitation Enables Dreams
    ## 478                                                                   Servientrega Perú
    ## 479                                                           Profesional independiente
    ## 480                                                                             KIACORP
    ## 481                                                                             R COORP
    ## 482                                                                 Arquinfo SAC - Perú
    ## 483                                                                      Pas Une Marque
    ## 484                                              Comunidad de Analytics Translators LAC
    ## 485                                                                            Voyantic
    ## 486                                                                Banco de Crédito BCP
    ## 487                                                                       Atria Energía
    ## 488                                                         Capitalismo Consciente Peru
    ## 489                                                                                Favo
    ## 490                                                              Cementos Pacasmayo SAA
    ## 491                                                                              CERTUS
    ## 492                                                                             Belcorp
    ## 493                                                                          Entel Perú
    ## 494                                                                             Belcorp
    ## 495                                                                           SURA Perú
    ## 496                                                            Universidad del Pacifico
    ## 497                                                                               Culqi
    ## 498                                                                                    
    ## 499                                          Ministerio de Relaciones Exteriores - Peru
    ## 500                                                                Anheuser-Busch InBev
    ## 501                                                                           Grupo AJE
    ## 502                                                                               BREIN
    ## 503                                                                       Consersa Perú
    ## 504                                                                                 IBM
    ## 505                                                                         Oh Zsa Zsa 
    ## 506                                                                               Ookla
    ## 507                                                                          Entel Perú
    ## 508                                                                        BBVA en Perú
    ## 509                                                                          Entel Perú
    ## 510                                                                      Inteligo Group
    ## 511                                                                          Scotiabank
    ## 512                                                            Arca Continental Lindley
    ## 513                                                                             Alicorp
    ## 514                                                                           Credicorp
    ## 515                                                                                Auna
    ## 516                                                                     Grupo Intercorp
    ## 517                                                   Rodrigo, Elias & Medrano Abogados
    ## 518                                                                                  EY
    ## 519                                                                              Natura
    ## 520                                                            Corporación Antezana SAC
    ## 521                                                          Rimac Seguros y Reaseguros
    ## 522                                                         Supermercados Peruanos S.A.
    ## 523                                                                                  HP
    ## 524                                             ZINC INDUSTRIAS NACIONALES S.A. (ZINSA)
    ## 525                                                                                  3M
    ## 526                                                                             Entelgy
    ## 527                                                                                  EY
    ## 528                                                                             Alicorp
    ## 529                                                                    Hunt Oil Company
    ## 530                                                                            Ghanimah
    ## 531                                                                      Perufarma S.A.
    ## 532                                                                    Mercedes-Benz AG
    ## 533                                                              Cementos Pacasmayo SAA
    ## 534                                                                         Consultoría
    ## 535                                                                         IT Company 
    ## 536                                                                               BREIN
    ## 537                                                                        Grupo Plenum
    ## 538                                                                              Phenom
    ## 539                                                                        Alfil Sports
    ## 540                                                  The University of Adelaide College
    ## 541                                                                    Mevoydeviaje.com
    ## 542                                                                Banco de Crédito BCP
    ## 543                                                                             Workday
    ## 544                                                                         Encora Inc.
    ## 545                                                                Innova Hunting Group
    ## 546                                                                          Bitel Perú
    ## 547                                                                           IBservice
    ## 548                                                                          FORCECLOSE
    ## 549                                                                           PedidosYa
    ## 550                                                                The HEINEKEN Company
    ## 551                                                                          Cool Earth
    ## 552                                                                                BBVA
    ## 553                                                                              Amazon
    ## 554                                                                    Uno Salud Dental
    ## 555                                                DSV - Global Transport and Logistics
    ## 556                                                                                JOKR
    ## 557                                                                 Best selection Peru
    ## 558                        Escuela de Postgrado de la Universidad San Ignacio de Loyola
    ## 559                                                                              Odisea
    ## 560                                                                   Fundación Capital
    ## 561                                                                        BBVA en Perú
    ## 562                                                      Centro Odontológico Francesqui
    ## 563                                                                        DPP Abogados
    ## 564                                                                            Coopeuch
    ## 565                                                                   Independiente SAF
    ## 566                                                              El Roble Cava y Quesos
    ## 567                                                                               Rappi
    ## 568                                                                                    
    ## 569                                                                           IBservice
    ## 570                                                                   APOYO Consultoría
    ## 571                                           Asociación Peruana de Facility Management
    ## 572                                                                            PwC Perú
    ## 573                                                                  Banco Ripley Chile
    ## 574                                                             Matemáticamente posible
    ## 575                                                                      LATAM Airlines
    ## 576                                                                             PepsiCo
    ## 577                                                                              Amazon
    ## 578                                                                             Belcorp
    ## 579                                                                          Cool Earth
    ## 580                                                                     Grupo Intercorp
    ## 581                                                                   DMB Sports Agency
    ## 582                                                                   Ecommerce Medical
    ## 583                                                                             Belcorp
    ## 584                                                           Gourmet Logistics Company
    ## 585                                                         Seaboard Overseas Perú S.A.
    ## 586                                                     Ministry of Economy and Finance
    ## 587                                                          Banco de la Nación de Perú
    ## 588                                                                         FILTROS LYS
    ## 589                                                                   Dell Technologies
    ## 590                                                            Clairfield International
    ## 591                                                      San Miguel Industrias PET S.A.
    ## 592                                                                               Chubb
    ## 593                                                                     Banco Santander
    ## 594                                                                            MegaNext
    ## 595                                                                       Pernod Ricard
    ## 596                                                                             Aldeamo
    ## 597                                                                          Reviur Inc
    ## 598                                                                               RITMO
    ## 599                                                                           Credicorp
    ## 600                                                                                VTEX
    ## 601                                                                 Laboratorios Smasac
    ## 602                                                                        Macroconsult
    ## 603                                                                   APOYO Consultoría
    ## 604                                                                Banco de Crédito BCP
    ## 605                                                                          Scotiabank
    ## 606                                                                     Macquarie Group
    ## 607                                                                               Clara
    ## 608                                                                                  EY
    ## 609                                                                         Ripley Perú
    ## 610                                                                 Datum Internacional
    ## 611                                                                           DataRobot
    ## 612                                                                              Oracle
    ## 613                                                                                Beat
    ## 614                                                                       Endeavor Perú
    ## 615                                                                 NG Restaurants S.A.
    ## 616                                                             Bluetab, an IBM Company
    ## 617                                               Center for Brains, Minds and Machines
    ## 618                                                                       Manuchar Perú
    ## 619                                                                            AB InBev
    ## 620                                                                           Interbank
    ## 621                                                           Profesional independiente
    ## 622                                                                            Ericsson
    ## 623                                                                          Desjardins
    ## 624                                                                  Gestión y Sistemas
    ## 625                                                                Anheuser-Busch InBev
    ## 626                                                                               Adobe
    ## 627                                                                              Minsky
    ## 628                                                                                 EFC
    ## 629                                      Tuxpas - Workplace from Facebook & AWS Partner
    ## 630                                                                             Globant
    ## 631                                                                            Listopro
    ## 632                                                                             Belcorp
    ## 633                                                                               BRECA
    ## 634                                                                         SKY Airline
    ## 635                                                                                Citi
    ## 636                                                                               Roche
    ## 637                                           Universidad Peruana de Ciencias Aplicadas
    ## 638                                                                                Auna
    ## 639                                        Humanistische Kindertagesstätte Wilde Hummel
    ## 640                                                                Stealth Mode Startup
    ## 641                                                                             Alicorp
    ## 642                                                                           Qbiz Inc.
    ## 643                                                                             Belcorp
    ## 644                                                     Interseguro Compañía de Seguros
    ## 645                                                                      Future Visions
    ## 646                                                                             Belcorp
    ## 647                                                                             Belcorp
    ## 648                                                                     Primal Instinct
    ## 649                                                                                Uber
    ## 650                                                                 ERA PR + NETWORKING
    ## 651                                                                  Zone Nine Survival
    ## 652                                                                              Tottus
    ## 653                                                                           MyPay App
    ## 654                                                                             Belcorp
    ## 655                                                                         Nexus Group
    ## 656                                                                              Kantar
    ## 657                                                                            Ironhack
    ## 658                                                                            Talently
    ## 659                                                                            Talently
    ## 660                                                                              Niubiz
    ## 661                                                                             Belcorp
    ## 662                                                          Rimac Seguros y Reaseguros
    ## 663                                                                              Atento
    ## 664                                                                 JZM & Asociados SAC
    ## 665                                                                              Backus
    ## 666                                                                       Caja Arequipa
    ## 667                                                          UTEC - Educación Ejecutiva
    ## 668                                                                             Belcorp
    ## 669                                                                         Havas Group
    ## 670                                                                           SURA Perú
    ## 671                                                           DINET, Operador Logístico
    ## 672                                                                               AGREF
    ## 673                                                                     Pacific Control
    ## 674                                                                             Caylent
    ## 675                                                                             Tismart
    ## 676                                                                Lucha Startup Studio
    ## 677                                                                  APOYO Comunicación
    ## 678                                                                              Backus
    ## 679                                                                                Aimo
    ## 680                                                                             Belcorp
    ## 681                                                                             Belcorp
    ## 682                                                                         Razor Group
    ## 683                                                                       Profuturo AFP
    ## 684                                                              Stadtverwaltung Zürich
    ## 685                                                                         West Monroe
    ## 686                                                                             Belcorp
    ## 687                                                                   Singular Advisors
    ## 688                                              GRIO - Grupo Romero Investment Office 
    ## 689                                                                     Grupo Intercorp
    ## 690                                                                   Credicorp Capital
    ## 691                                            Pontificia Universidad Católica del Perú
    ## 692                                                                             Belcorp
    ## 693                                                                               Tsoft
    ## 694                                                                        AlixPartners
    ## 695                                                                Banco de Crédito BCP
    ## 696                    DCH - Organización Internacional de Directivos de Capital Humano
    ## 697                                                      Laboratorio de Big Data México
    ## 698                                                                             Belcorp
    ## 699                                                                    BBVA Continental
    ## 700                                                                               Kanto
    ## 701                                                                              Amazon
    ## 702                                                                               Rappi
    ## 703                                                                             Sigmoid
    ## 704                                                                      Partido Morado
    ## 705                                                                AGRICOLA SANTA AZUL 
    ## 706                                                                         J.P. Morgan
    ## 707                                                                         Encora Inc.
    ## 708                                                                     La Victoria Lab
    ## 709                                                                           Interbank
    ## 710                                                                Anheuser-Busch InBev
    ## 711                                                                                Favo
    ## 712                                                                               Rappi
    ## 713                                                              Desarrollo Digital SpA
    ## 714                                                                             L'Oréal
    ## 715                                                             CloudSystems.ES en Perú
    ## 716                                                               La Fornaia Pastificio
    ## 717                                                                             Belcorp
    ## 718                                                                    Pacífico Seguros
    ## 719                                                                        BBVA en Perú
    ## 720                                                                     Surf Place Perú
    ## 721                                                                                 SAS
    ## 722                                                                             Devlane
    ## 723                                                                        Experis Perú
    ## 724                                                                      BFA Industries
    ## 725                                                                          HelloFresh
    ## 726                                                                           Smart Eye
    ## 727                                                              Cementos Pacasmayo SAA
    ## 728                                                                Albertsons Companies
    ## 729                                                                        HEMAGGI EIRL
    ## 730                                                                      Morgan Stanley
    ## 731                                                                             Mibanco
    ## 732                                                   Payet, Rey, Cauvi, Pérez Abogados
    ## 733                                                                                Favo
    ## 734                                           Executive Insight, Healthcare Consultants
    ## 735                                                                  McKinsey & Company
    ## 736                                                                 Universidad de Lima
    ## 737                                                                             Belcorp
    ## 738                                                                    Intercorp Retail
    ## 739                                                                            Global66
    ## 740                                                                     Sedapal Oficial
    ## 741                                                                        Equifax Perú
    ## 742                                                                             Belcorp
    ## 743                                                             Santander Consumer Peru
    ## 744                                                                             Queloco
    ## 745                                                                             Belcorp
    ## 746                                                                             Sigmoid
    ## 747                                                                                BJSS
    ## 748                                                                   NTT DATA Services
    ## 749                                                                                  EY
    ## 750                                                                             WOWPERÚ
    ## 751                                                                            WITZ SAC
    ## 752                                                                       CAJA TRUJILLO
    ## 753                                                                     Cocinas Ocultas
    ## 754                                                                               BREIN
    ## 755                                                                             Belcorp
    ## 756                                                                   Polymath Ventures
    ## 757                                                                             Belcorp
    ## 758                                                                              Yanbal
    ## 759                                                           Pan American Silver Corp.
    ## 760                                                                    Turquoise Health
    ## 761                                                                              Kushki
    ## 762                                                                        Compra Agora
    ## 763                                                                          AGP eGlass
    ## 764                                                                    Amaru Superfoods
    ## 765                                                                                Favo
    ## 766                                                               Séntisis Intelligence
    ## 767                                                                       IGNIS Energía
    ## 768                                                                           Modo Beta
    ## 769                                                                            Deloitte
    ## 770                                                                             Belcorp
    ## 771                                                                               Culqi
    ## 772                                                                             Globant
    ## 773                                                                             Alicorp
    ## 774                                                                  Almer Technologies
    ## 775                                                                             Belcorp
    ## 776                                                                    Armo's & Company
    ## 777                                                                      Chaccu Trading
    ## 778                                                                                Auna
    ## 779                                                                          TyC Sports
    ## 780                                                                Banco de Crédito BCP
    ## 781                                                                       Betsson Group
    ## 782                                                                                 B89
    ## 783                                                                               Culqi
    ## 784                                                                               Ontop
    ## 785                                                                Instituto del Futuro
    ## 786                                                                          Jellysmack
    ## 787                                                                     PromoInvest SAF
    ## 788                                                                   Credicorp Capital
    ## 789                                                                             Belcorp
    ## 790                                                              Cementos Pacasmayo SAA
    ## 791                                                           Amazon Web Services (AWS)
    ## 792                                                                          Tebca Perú
    ## 793                                                                             Belcorp
    ## 794                                                                             Belcorp
    ## 795                                                          Business Agility Institute
    ## 796                                                                              Es Hoy
    ## 797                                                                           Interbank
    ## 798                                                                                 B89
    ## 799                                                                             Belcorp
    ## 800                                                                             Belcorp
    ## 801                                                           Amazon Web Services (AWS)
    ## 802                                                                                Auna
    ## 803                                                                             Belcorp
    ## 804                                                                             Belcorp
    ## 805                                                                          DRA Global
    ## 806                                                                     Stealth Startup
    ## 807                                                           Centria - CSC Grupo Breca
    ## 808                                                                           MAB Perú 
    ## 809                                                                             Alicorp
    ## 810                                                         Supermercados Peruanos S.A.
    ## 811                                                               Capgemini Engineering
    ## 812                                                                     AVC Real Estate
    ## 813                                                                              Sunarp
    ## 814                                                                             Belcorp
    ## 815                                                                      Maygel Coronel
    ## 816                                                       Universidad del Pacífico (PE)
    ## 817                                                     North Carolina State University
    ## 818                                                              Cementos Pacasmayo SAA
    ## 819                                                                          PUMA Group
    ## 820                                                          Wall Street English - Peru
    ## 821                                                                             Accéder
    ## 822                                                                             Belcorp
    ## 823                                                                 BPC Business School
    ## 824                                                                               Mandü
    ## 825                                                                          BOMBARDIER
    ## 826                                                                      eTeacher Group
    ## 827                                                                           Interbank
    ## 828                                                                             Belcorp
    ## 829                                                                    Jaguar Plásticos
    ## 830                                                                        Accenture AI
    ## 831                                                                               Rappi
    ## 832                                                                             Belcorp
    ## 833                                                                             Belcorp
    ## 834                                                                                 UBS
    ## 835                                                                      Quantum Talent
    ## 836                                                                                  hp
    ## 837                                                                               Orión
    ## 838                                                                               BRECA
    ## 839                                                                              Inetum
    ## 840                                                                              Magnus
    ## 841                                   Universidad Nacional Micaela Bastidas de Apurimac
    ## 842                                                                                 BAT
    ## 843                                                                              Backus
    ## 844                                                                             Belcorp
    ## 845                                                        Acero-Deck Placa Colaborante
    ## 846                                                                                Wabu
    ## 847                                                                       Postgrado UPC
    ## 848                                             ISA Interconexión Eléctrica S.A. E.S.P.
    ## 849                                                                             Belcorp
    ## 850                                                           Applying Consulting Latam
    ## 851                                                                                ISIL
    ## 852                                                                                    
    ## 853                                                                   Matrix Consulting
    ## 854                                                                          Clarity AI
    ## 855                                                                      Cape Analytics
    ## 856                                                                Banco de Crédito BCP
    ## 857                                                                      Delta Partners
    ## 858                                                                            Antamina
    ## 859                                                                    Procter & Gamble
    ## 860                                                                        EY-Parthenon
    ## 861                                                                                  EY
    ## 862                                                                             Belcorp
    ## 863                                                                       Pernod Ricard
    ## 864                                                                   A. E. LUMINUS DEI
    ## 865                                                                      GHL PUBLICIDAD
    ## 866                                                                           CSTI Corp
    ## 867                                                                              izipay
    ## 868                                                                         Encora Inc.
    ## 869                                                                             Belcorp
    ## 870                                                                           Credicorp
    ## 871                                                                    Ferreycorp S.A.A
    ## 872                                                                GRETEL INTERNATIONAL
    ## 873                                                                                Beat
    ## 874                                                                    Intercorp Retail
    ## 875                                                                        Voltron Data
    ## 876                                                         Business & Decision Belgium
    ## 877                                                                        Voltron Data
    ## 878                                                                         Cuatrecasas
    ## 879                                                          Rimac Seguros y Reaseguros
    ## 880                                                      CIUP, Universidad del Pacífico
    ## 881                                                                    Pacífico Seguros
    ## 882                                                                            AB InBev
    ## 883                                                                Anheuser-Busch InBev
    ## 884                                                          Rimac Seguros y Reaseguros
    ## 885                                                                       Gruas del sur
    ## 886                                                                             Belcorp
    ## 887                                                                               Cisco
    ## 888                                                                          Platanitos
    ## 889                                                          Marsh & McLennan Companies
    ## 890                                                                             Belcorp
    ## 891                                                                    Procter & Gamble
    ## 892                                                                               Pulso
    ## 893                                                                              Digica
    ## 894                                                                             Belcorp
    ## 895                                                     Interseguro Compañía de Seguros
    ## 896                                                                              Inetum
    ## 897                                                                              AdJinn
    ## 898                                                                                    
    ## 899                                                                                Yape
    ## 900                                                                         Anida Latam
    ## 901                                                                             Velogig
    ## 902                                                                   Johnson & Johnson
    ## 903                                                                                 IBM
    ## 904                                                                          Lava Quick
    ## 905                                                               Casino Atlantic City 
    ## 906                                                                              LINKIT
    ## 907                                       UTEC - Universidad de Ingeniería y Tecnología
    ## 908                                                                            Space AG
    ## 909                                                                   Banco Ripley Perú
    ## 910                                                                     BBVA AI Factory
    ## 911                                                                    Vinatea & Toyama
    ## 912                                                                             BP Perú
    ## 913                                                                                Favo
    ## 914                                                                Banco de Crédito BCP
    ## 915                                                                          Claro Perú
    ## 916                                                                            Labofta 
    ## 917                                                                            COPEINCA
    ## 918                                                                             RESEMIN
    ## 919                                                                       falabella.com
    ## 920                                                                             Belcorp
    ## 921                                                                  Salkantay Ventures
    ## 922                                                                           Cognizant
    ## 923                                                          Data Science Research Perú
    ## 924                                                                Banco de Crédito BCP
    ## 925                                                                       Leader Talent
    ## 926                                                                        BBVA en Perú
    ## 927                                                                               BREIN
    ## 928                                                           Profesional independiente
    ## 929                                          Promotora Inmobiliaria Industrial de Piura
    ## 930                                                                               Culqi
    ## 931                                                                         innova Pucp
    ## 932                                                                               Rappi
    ## 933                                                                              Yanbal
    ## 934                                                                            Cloudera
    ## 935                                                                       Beliv Company
    ## 936                                                                    Nitron Group LLC
    ## 937                                                                           Interbank
    ## 938                                                                  América Televisión
    ## 939                                                              America Movil Peru SAC
    ## 940                                                                    Procter & Gamble
    ## 941                                                                               Rappi
    ## 942                                                                           Swissport
    ## 943                                                       Boston Consulting Group (BCG)
    ## 944                                                                           Grupo AJE
    ## 945                                                              Cementos Pacasmayo SAA
    ## 946                                                                             Belcorp
    ## 947                                                                             Belcorp
    ## 948                                                                   APOYO Consultoría
    ## 949                                                                           Interbank
    ## 950                                              GRIO - Grupo Romero Investment Office 
    ## 951                                                                             Alicorp
    ## 952                                                                Banco Santander Perú
    ## 953                                                                      TechStart Perú
    ## 954                                                                      Andino Capital
    ## 955                                                                      Falabella Perú
    ## 956                                                                              Amazon
    ## 957                                                                                BBVA
    ## 958                                                                               Mandü
    ## 959                                                                  Cornershop by Uber
    ## 960                                                                         Consultora 
    ## 961                                                                Banco de Crédito BCP
    ## 962                                                                        Michael Page
    ## 963                                                       Ministerio de Energía y Minas
    ## 964                                                                                Favo
    ## 965                                                                Anheuser-Busch InBev
    ## 966                                                                                BBVA
    ## 967                                                                   Johnson & Johnson
    ## 968                                                                               SONDA
    ## 969                                                                 BPC Business School
    ## 970                                                                    Stefanini Brasil
    ## 971                                                                           Interbank
    ## 972                                                                         Farmaniacos
    ## 973                                                       Selectum Professional Hunting
    ## 974                         Registro Nacional de Identificación y Estado Civil - RENIEC
    ## 975                                                            Athenea Dental Institute
    ## 976                                                                  Farmacias Peruanas
    ## 977                                            Pontificia Universidad Catolica del Peru
    ## 978                                  Hospital Nacional Docente Madre Niño San Bartolomé
    ## 979                                                                               Infor
    ## 980                                             UPT - LIMA UNIVERSIDAD PRIVADA TELESUP”
    ## 981                                                                             Crehana
    ## 982                                           Universidad Peruana de Ciencias Aplicadas
    ## 983                                           Universidad Peruana de Ciencias Aplicadas
    ## 984                                                                    Cooperativa BCRP
    ## 985                                                              Instituto Ayrton Senna
    ## 986                                                                           Kavak.com
    ## 987                                                                                    
    ## 988                                                                      Kimberly-Clark
    ## 989                                                                    Procter & Gamble
    ## 990                                                                         GRUPO AUREN
    ## 991                                                                              Fitesa
    ## 992                                                           Asociación de Internet MX
    ## 993                                                                               Valia
    ## 994                                                                        CENTRUM PUCP
    ## 995                                                                               Indra
    ## 996                                                    PROSERVICES GESTION INMOBILIARIA
    ## 997                                                                             Equifax
    ## 998                                                       Real Plaza - Intercorp Retail
    ## 999                                                               Courier Kunan Express
    ## 1000                                                                            GesNext
    ## 1001                                                                      La Llave S.A.
    ## 1002                                                                            Belcorp
    ## 1003                                                                           Autónomo
    ## 1004                                                            NTT DATA Europe & LATAM
    ## 1005                                                                       Afore Coppel
    ## 1006                                                             GMF S.A.C. - AnphiCorp
    ## 1007                                                       casa de família ou Hospital 
    ## 1008                                                             HR Business Consultant
    ## 1009                                                                 TEST & CONTROL SAC
    ## 1010                                                                             Adecco
    ## 1011                                                             Mondelez International
    ## 1012                                                                      Condor Agency
    ## 1013                                                                             Suscri
    ## 1014                                                                        Grupo INMAC
    ## 1015                                          Universidad Peruana de Ciencias Aplicadas
    ## 1016                                                                           INTELIGO
    ## 1017                                                                            Belcorp
    ## 1018                                                                Universidad de Lima
    ## 1019                                                                                 EY
    ## 1020                                                                 Banco Ripley Chile
    ## 1021                                                                            Accéder
    ## 1022                                                                          Verde&Más
    ## 1023                                                                           Altozano
    ## 1024                                                                        Voxiva Perú
    ## 1025                                                        Sociedad Agrícola Rapel SAC
    ## 1026                                                                            Globant
    ## 1027                                                                                 EY
    ## 1028                                                                           msKompas
    ## 1029                                                                            Alicorp
    ## 1030                                                                            Crehana
    ## 1031                                                                            L'Oréal
    ## 1032                                                                         OlamFX Ltd
    ## 1033                                                                            Comunal
    ## 1034                                                                Crédit Agricole CIB
    ## 1035                                                                           Libélula
    ## 1036                                                                           Seequent
    ## 1037                                                                   Grupo Pucón Perú
    ## 1038                                                                     Spencer Stuart
    ## 1039                                                                 Farmacias Peruanas
    ## 1040                                                                  Almendra Software
    ## 1041                                                                            Sigmoid
    ## 1042                                                               Banco de Crédito BCP
    ## 1043                                                                          Immunotec
    ## 1044                                                                       Proarándanos
    ## 1045                                                                              QROMA
    ## 1046                                                                                   
    ## 1047                                                    Clinica San Juan de Dios - Lima
    ## 1048                                                              Black Andes Analytics
    ## 1049                                                                             Tandia
    ## 1050                                                                   Club De La Union
    ## 1051                                                                        Magistragos
    ## 1052                                                                             Attach
    ## 1053                                                                            BP Perú
    ## 1054                                                                              Rappi
    ## 1055                                                                            EA Corp
    ## 1056                                                                                IBM
    ## 1057                                                                            Globant
    ## 1058                                                           Universidad del Pacifico
    ## 1059                                                              Santander Global Tech
    ## 1060                                                                    brownie express
    ## 1061                                     HLM Soluciones en Tecnología de la Información
    ## 1062                                                                              BRECA
    ## 1063                                                                          Interbank
    ## 1064                                                                               LLYC
    ## 1065                                                                              Rappi
    ## 1066                                                           JFV CONSTRUCCIONES E ING
    ## 1067                                                                              Cisco
    ## 1068                                                                          Interbank
    ## 1069                                                                          Interbank
    ## 1070                                                                            Belcorp
    ## 1071                                                                           AB InBev
    ## 1072                                                                 Perfumerías Unidas
    ## 1073                                                                     Falabella Perú
    ## 1074                                                                      Agata Zumaeta
    ## 1075                                                                               JOKR
    ## 1076                                                                              Mandü
    ## 1077                                                                         Scotiabank
    ## 1078                                                   Universidad Carlos III de Madrid
    ## 1079                                 PRECISA Laboratorios - Subsidiaria de Pacifico EPS
    ## 1080                                                               Prediqt - Data to AI
    ## 1081                                                                              BREIN
    ## 1082                                                                           GRUPORPP
    ## 1083                                                               Banco de Crédito BCP
    ## 1084                                                                  Performing Brands
    ## 1085                                                                      Apuesta Total
    ## 1086                                                                              Culqi
    ## 1087                                                                          BairesDev
    ## 1088                                                                       EY-Parthenon
    ## 1089                                                      Universidad del Pacífico (PE)
    ## 1090                                                         Rimac Seguros y Reaseguros
    ## 1091                                                                       EVOL (TSnet)
    ## 1092                                                                       Mapsalud SAC
    ## 1093                                                                               JOKR
    ## 1094                                                                     Anglo American
    ## 1095                                                                             Ventas
    ## 1096                                        Ministerio de Desarrollo e Inclusión Social
    ## 1097                                                                      Grupo Medixon
    ## 1098                                                                            Belcorp
    ## 1099                                                                            Belcorp
    ## 1100                                                                            Belcorp
    ## 1101                                                                            Belcorp
    ## 1102                                                                            Sigmoid
    ## 1103                                                               Banco de Crédito BCP
    ## 1104                                                                              Rappi
    ## 1105                                                                           Marcobre
    ## 1106                                                                             Sunarp
    ## 1107                                                                        Ripley Perú
    ## 1108                                                                            Globant
    ## 1109                                                                             Twilio
    ## 1110                                                                             Tottus
    ## 1111                                                                         Scotiabank
    ## 1112                                                                     Falabella Perú
    ## 1113                                                                            Belcorp
    ## 1114                                                                             Diageo
    ## 1115                                                                            Crehana
    ## 1116                                                             Grupo Hinode - Oficial
    ## 1117                                                  Global Reporting Initiative (GRI)
    ## 1118                                                                 CLUSTER CONSULTING
    ## 1119                                                                         Scotiabank
    ## 1120                                                                       BBVA en Perú
    ## 1121                                                                            Mibanco
    ## 1122                                                                              Rappi
    ## 1123                                                                 Farmacias Peruanas
    ## 1124                                                                   Grünenthal Group
    ## 1125                                                                     Kimberly-Clark
    ## 1126                                                               Anheuser-Busch InBev
    ## 1127                                                              SURA Asset Management
    ## 1128                                                                               MGM 
    ## 1129                                                                           TC1 Labs
    ## 1130                                                                   Procter & Gamble
    ## 1131                                                       State University of Campinas
    ## 1132                                                                         Derco Perú
    ## 1133                                                               Banco de Crédito BCP
    ## 1134                                                                          Prima AFP
    ## 1135                                                                            Udacity
    ## 1136                                                                         Scotiabank
    ## 1137                                                                            Belcorp
    ## 1138                                                                     Bain & Company
    ## 1139                                                               Pacifica Continental
    ## 1140                                                               Banco de Crédito BCP
    ## 1141                                                                      INDEPENDIENTE
    ## 1142                                                                             Google
    ## 1143                                                                      Grupo Salinas
    ## 1144                                                                           Talently
    ## 1145                                                                           DMC Perú
    ## 1146                                                                          Interbank
    ## 1147                                                        Remax Platinum Miguel Dasso
    ## 1148                                                                   Pacífico Seguros
    ## 1149                                                                         HOCHSCHILD
    ## 1150                                                                        FITCO, Inc.
    ## 1151                                                                      CCE - PUC-Rio
    ## 1152                                                                  Super Fast Python
    ## 1153                                                        Peruvian Sourcing Group SAC
    ## 1154                                                                  Independiente SAF
    ## 1155                                                                     SERVIFASTPERU 
    ## 1156                                                                     Falabella Perú
    ## 1157                                                                      Marco Vinelli
    ## 1158                                                                        Nexus Group
    ## 1159                                                                            Afilnet
    ## 1160                                                                               Favo
    ## 1161                                                                 Hult Workshop Club
    ## 1162                                                                            Citadel
    ## 1163                                                                  Almendra Software
    ## 1164                                                                          WeHunterz
    ## 1165                                                                   Big Data Academy
    ## 1166                                                                       Métrica Perú
    ## 1167                                         Caterpillar Financial Services Corporation
    ## 1168                                                                              Tenpo
    ## 1169                                                                     Quantum Talent
    ## 1170                                                                            Mibanco
    ## 1171                                                                              Ontop
    ## 1172                                                                   Intercorp Retail
    ## 1173                                                                        Grupo Sypsa
    ## 1174                                                                 G.W. Yichang & Cia
    ## 1175                                                                   Beta Gamma Sigma
    ## 1176                                                                           torre.co
    ## 1177                                                                      Caja Arequipa
    ## 1178                                                                            Belcorp
    ## 1179                                                                         Scotiabank
    ## 1180                                                                   AFP Habitat Perú
    ## 1181                                                                         POTRO Lima
    ## 1182                                                                            Belcorp
    ## 1183                                                                           Invertir
    ## 1184                                                                           CreaCode
    ## 1185                                                           Surfline\\Wavetrak, Inc.
    ## 1186                                                                        FITCO, Inc.
    ## 1187                                                           Universidad del Pacifico
    ## 1188                                                                          Interbank
    ## 1189                                                                                 EY
    ## 1190                                                                       Michael Page
    ## 1191                                                               Arimathea Konsulting
    ## 1192                                                       Consorcio Aulas para el Perú
    ## 1193                                                                               Auna
    ## 1194                                                         Falabella Corporativo Perú
    ## 1195                                                           Universidad del Pacifico
    ## 1196                                                                              Bauen
    ## 1197                                                                  Credicorp Capital
    ## 1198                                              Northwestern University Medill School
    ## 1199                                                                    Bank of America
    ## 1200                                                                        J.P. Morgan
    ## 1201                                                                              CGIAR
    ## 1202                                                                          AGP Group
    ## 1203                                                                       EY-Parthenon
    ## 1204                                                                  APOYO Consultoría
    ## 1205                                                                     Giovanni Arias
    ## 1206                                                                      Grupo Grameco
    ## 1207                                                   Casas Colonia Inmobiliaria y Más
    ## 1208                                                               The HEINEKEN Company
    ## 1209                                                                        Ripley Perú
    ## 1210                                                                      CreaCode Peru
    ## 1211                                                                           ucrop.it
    ## 1212                                                                             Amazon
    ## 1213                                                                       Wait N' Rest
    ## 1214                                                          Policía Nacional del Perú
    ## 1215                                                                                 EY
    ## 1216                                                      Universidad del Pacífico (PE)
    ## 1217                                                         Rimac Seguros y Reaseguros
    ## 1218                                      Universidad de Ingeniería & Tecnología - UTEC
    ## 1219                                                           Universidad del Pacífico
    ## 1220                                                                              Mandü
    ## 1221                                                               Cervecería Barbarian
    ## 1222                                                      responsAbility Investments AG
    ## 1223                                                                 Core Partners Perú
    ## 1224                                      UTEC - Universidad de Ingeniería y Tecnología
    ## 1225                                                                                   
    ## 1226                                                          Café con Leche Comfy Wear
    ## 1227                                                      Universidad del Pacífico (PE)
    ## 1228                                                          Profesional independiente
    ## 1229                                                                      ebombo events
    ## 1230                                                                        J.P. Morgan
    ## 1231                                                                           NFTicket
    ## 1232                                    Pontificia Universidad Católica del Peru - PUCP
    ## 1233                                                      Universidad del Pacífico (PE)
    ## 1234                                                                  LIFT - smart eats
    ## 1235                                                                     AYNITECH GROUP
    ## 1236                                                                              Koopa
    ## 1237                                                                              FITCO
    ## 1238                                                                          Interbank
    ## 1239                                              The Main Millennial Advisory - THEMMA
    ## 1240                                                    Colegio Santa Maria Marianistas
    ## 1241                                                                            Ocucaje
    ## 1242                                                                         Prestamype
    ## 1243                                                                         Scotiabank
    ## 1244                                                                     FERREYCORP SAA
    ## 1245                                                                   Procter & Gamble
    ## 1246                                                       JCM Management Company, Inc.
    ## 1247                                                                     Ferreycorp SAA
    ## 1248                                                              Solidaridad en Marcha
    ## 1249                                                               Anheuser-Busch InBev
    ## 1250                                                                              BRECA
    ## 1251                                                                  Outbound Ventures
    ## 1252                                                                    Banco Santander
    ## 1253                                                         Rimac Seguros y Reaseguros
    ## 1254                                                                            Pear VC
    ## 1255                                                        Samsung Electronics America
    ## 1256                                                                             izipay
    ## 1257                                                                            Katari 
    ## 1258                                                              The Coca-Cola Company
    ## 1259                                                         Rimac Seguros y Reaseguros
    ## 1260                                                                   Intercorp Retail
    ## 1261                                                    Colegio Santa Maria Marianistas
    ## 1262                                                                               Meta
    ## 1263                                                                        Imacom EIRL
    ## 1264                                                           Universidad del Pacifico
    ## 1265                                                               IESE Business School
    ## 1266                                                                                   
    ## 1267                                                                      Condor Travel
    ## 1268                                                      Universidad del Pacífico (PE)
    ## 1269                                                               La Purita Verdad SAC
    ## 1270                                                                             Zillow
    ## 1271                                                        ESADE Business & Law School
    ## 1272                                                      Universidad del Pacífico (PE)
    ## 1273                                                                        J.P. Morgan
    ## 1274                                                        Automotores Gildemeister SA
    ## 1275                                                                              Mandü
    ## 1276                                                               University of Guelph
    ## 1277                                                                Infotek Perú S.A.C.
    ## 1278                                                                          MESA 24/7
    ## 1279                                                               Anheuser-Busch InBev
    ## 1280                                                                              Mandü
    ## 1281                                                                              Mandü
    ## 1282                                                                            Globant
    ## 1283                                                                Murdoch Sistemas SA
    ## 1284                                                                             Fluyez
    ## 1285                                                                    Markham College
    ## 1286                                                                            Alicorp
    ## 1287                                                                                   
    ## 1288                                                                                   
    ##                                                                                                                                                 Position
    ## 1                                                                                                                                   General Practitioner
    ## 2                                                                                                                             Head Of Financial Planning
    ## 3                                                                                                                              Product Lifecycle Analyst
    ## 4                                                                                                                                                       
    ## 5                                                                                                                                             Researcher
    ## 6                                                                                                                             Analista de Información Jr
    ## 7                                                                                                                               Intern, Transversal Risk
    ## 8                                                                                                                            Academic Program Specialist
    ## 9                                                                                                                     Project Lead, Accesories Lifecycle
    ## 10                                                                                                                            Investment Banking Analyst
    ## 11                                                                                                       Network Planning Analyst (Strategy & Analytics)
    ## 12                                                                                                                                     Account Executive
    ## 13                                                                                                                            Senior Technical Recruiter
    ## 14                                                                                                                                          Data Analyst
    ## 15                                                                                                                                          Entrepreneur
    ## 16                                                                                                                                        Business Owner
    ## 17                                                                                                                                       Product Manager
    ## 18                                                                                                                   Associate Director, Data & Insights
    ## 19                                                                                                                                        Data Scientist
    ## 20                                                                                                             Dueña del emprendimiento Bazar del Bosque
    ## 21                                                                                                                                  Social Media Manager
    ## 22                                                                                                                                    Starbucks Barista 
    ## 23                                                                                                                                      Marketing Intern
    ## 24                                                                                                                                          Data Analyst
    ## 25                                                                                                                                     Developer Analyst
    ## 26                                                                                                                                             President
    ## 27                                                                                                                                     Managing Director
    ## 28                                                                                                                       Research And Teaching Assistant
    ## 29                                                                                                                                James McGill Professor
    ## 30                                                                                                            Infrastructure Private Equity Funds Intern
    ## 31                                                                                     Gestionnaire, Expérience Candidat / Manager, Candidate Experience
    ## 32                                                                                                                                   Lead Data Scientist
    ## 33                                                                                                                                   Data Science Fellow
    ## 34                                                                                                                                         PHD Candidate
    ## 35                                                                                                                                        Vice President
    ## 36                                                                                                 Analytics Academic Consulting Project, Data Scientist
    ## 37                                                                                                                                                   CEO
    ## 38                                                                                                                      Global Marketing and Media Co-op
    ## 39                                                                                                                          Business Development Manager
    ## 40                                                                                                 Director Artificial Intelligence & Advanced Analytics
    ## 41                                                                                                                                   Master Career Coach
    ## 42                                                                                                        Data Scientist (Academic Analytics Consultant)
    ## 43                                                                                        Data Analyst | UX/UI Specialist | Academic Consulting Project 
    ## 44                                                                                                       Consultant, Academic Analytics Capstone Project
    ## 45                                                                                                                                         Summer Intern
    ## 46                                                                                                                                   Asistente comercial
    ## 47                                                                                              Senior Data Scientist - Valorisation des Données Clients
    ## 48                                                                                                                               Data Science Consultant
    ## 49                                                                                  Jefe de Responsabilidad Social Corporativa y Relaciones Comunitarias
    ## 50                                                                                                                                   Procurement Manager
    ## 51                                                                                                                  SAP Business Intelligence Consultant
    ## 52                                                                                                                                      <U+52A9><U+6559>
    ## 53                                                                                                                 Spécialiste en acquisition de talents
    ## 54                                                                                                                                            Co Founder
    ## 55                                                                                                                                                ovemac
    ## 56                                                                                                                                          Data Analyst
    ## 57                                                                                                                  Prime & Pricing Intern - South Latam
    ## 58                                                                                                                          Pisco Huamaní Export Manager
    ## 59                                                                                               Facilitador y consultor de soluciones digitales y de TI
    ## 60                                                                                                                                     Board Of Advisors
    ## 61                                                                                                                                             Consultor
    ## 62                                                                                                                        Managing Director Peru & Chile
    ## 63                                                                                                                           Consultant - Data Scientist
    ## 64                                                                                                                                Data Analytics Modeler
    ## 65                                                                                                                                 Data Science Director
    ## 66                                                               Global Head of Product Strategy & Key Customer Management at DSC Real Estate Solutions 
    ## 67                                                                                                                                                      
    ## 68                                                                                                                               Implementation Engineer
    ## 69                                                                                                                                 Junior Data Scientist
    ## 70                                                                                                                                     President and CEO
    ## 71                                                                                                                     Practicante Centro de InnovaCXión
    ## 72                                                                                                                                      Data & AI intern
    ## 73                                                                                                                   Coordinadora de Proyectos Digitales
    ## 74                                                                                                                                     Project Assistant
    ## 75                                                                                                                             Machine Learning Engineer
    ## 76                                                                                                                            Investment Banking Analyst
    ## 77                                                                                                                            Senior Development Officer
    ## 78                                                                                                                                       IT Data Analyst
    ## 79                                                           Analytics Academic Consulting Practicum, McKesson Canada, Strategy Consultant, Data Analyst
    ## 80                                                                                                                                      Launcher Trainee
    ## 81                                                                                                                                            Consultant
    ## 82                                                                                                                          Consultant - People & Change
    ## 83                                                                                                                          Strategy & Business Analysis
    ## 84                                                                                                                                     Consultant Intern
    ## 85                                                                                                                                    Data Science Staff
    ## 86                                                                                                                                   Associate Professor
    ## 87                                                                                                                             Data Scientist, Analytics
    ## 88                                                                                                                             Wealth Management Analyst
    ## 89                                                                                                                                        Data Scientist
    ## 90                                                                                                                                        Data scientist
    ## 91                                                                                                                                        Data Scientist
    ## 92                                                                                                                                        Data Scientist
    ## 93                                                                                           Analytics Consultant - Capstone Academic Consulting Project
    ## 94                                                                                                                                        Student Mentor
    ## 95                                                                                                                               Practicante pre de risk
    ## 96                                                                                                                                                Intern
    ## 97                                                                                                                           Graduate Research Assistant
    ## 98                                                                                                                                     Marking Assistant
    ## 99                                                                                                                                  Analytical Scientist
    ## 100                                                                                         Analytics Consulting Project with Air Transat, Data Modeler\t
    ## 101                                                                                                                       MBA Intern- Digital Technology
    ## 102                                                                                                                Consultant/Consultante - Data Science
    ## 103                                                                                                                                           Consultant
    ## 104                                                                                                     Practicante de Strategy & Solutions Development 
    ## 105                                                                                                                    Practicante de Psicología Clínica
    ## 106                                                                                                                 The worker of a station of packaging
    ## 107                                                                                         Analytics Academic Consulting Project with DHL, Data Analyst
    ## 108                                                                                                                                     Consultor Senior
    ## 109                                                                             Industry Liaison - Experiential Learning, Marketing and Career Placement
    ## 110                                                                                                      Head of Sports Analytics & Business Development
    ## 111                                                                                                                 Analytics and Information Management
    ## 112                                                                                                            Consultant, Business Analysis & Analytics
    ## 113                                                                                  Analytics Consultant - McGill Capstone Academic Consulting Project 
    ## 114                                                                                                                                  Associate Professor
    ## 115                                                                                                                                  Associate Professor
    ## 116                                                                                                      Talent Acquisition Coordinator - Eastern Canada
    ## 117                                                                                                                                           Consultant
    ## 118                                                                                                                                      Asistente Legal
    ## 119                                                                                                       Digital Transformation Trainee - Programa TRBK
    ## 120                                                                                                                    Principal Specialist Procurement 
    ## 121                                                                                                        Audit Credit Risk Associate, Activate Program
    ## 122                                                                                                                                    Test Jr. Engineer
    ## 123                                                                                                                                      Data Analyst II
    ## 124                                                                                                                                   Research Assistant
    ## 125                                                                                                                             Scale AI Chair Professor
    ## 126                                                                                                          Data Scientist Team Lead (Academic Project)
    ## 127                                                                                  Analytics Acedemic Consulting Project with L'Oréal, UIUX Specialist
    ## 128                                                                                                                           Manager, Advisory Services
    ## 129                                                                                                             Practicante Pre-Profesional de Marketing
    ## 130                                                                                                                                     Asociada Junior 
    ## 131                                                                                                                                     Marketing Intern
    ## 132                                                                                                                                          M&A Analyst
    ## 133                                                                                      Analytics Academic Consulting Project with Pratt&Whitney Canada
    ## 134                                                                                                                  Data Scientist - Student Consultant
    ## 135                                                                                                 Data Analyst ( Academic Analytics Consultant) at CGI
    ## 136                                                                                                                                        Data Engineer
    ## 137                                                                                                                 Business Process Optimization Intern
    ## 138                                                                                                                                              Manager
    ## 139                                                                                                                              Chief Executive Officer
    ## 140                                                                                                                  Civil Business Intelligence Analyst
    ## 141                                                                                                                       Product Owner de Venta Digital
    ## 142                                                                                                                                  Peru Pre MBA Intern
    ## 143                                                                                                       Data Analyst (Academic Analytics Consultant)  
    ## 144                                                                                                                                     Brand Supervisor
    ## 145                                                                                                                                 Technology Associate
    ## 146                                                                                                           Assistant Professor of Information Systems
    ## 147                                                                                                  Analytics Academic Consulting Project, Data Analyst
    ## 148                                                                                                                   Data Analyst, Subscription Service
    ## 149                                                                                                                                       Data Scientist
    ## 150                                                                                                                                       Data Scientist
    ## 151                                                                                                                                            Associate
    ## 152                                                                                                                          Central Product Manager, CX
    ## 153                                                                                                                        Business Intelligence Analyst
    ## 154                                                                                                                 Supervisor de Marketing y Publicidad
    ## 155                                                                                                                        Atracción de Talento Regional
    ## 156                                                                                                                                     Graduate Trainee
    ## 157                                                                                                                                       Senior Analyst
    ## 158                                                                                                              Administrador del local "Vikingo Store"
    ## 159                                                                                                                                      Gerente general
    ## 160  <U+6570><U+636E><U+5206><U+6790>&<U+7528><U+6237><U+4ECB><U+9762><U+548C><U+4F53><U+9A8C><U+5206><U+6790><U+5E08>  Data Modeling & UIUX Consultant 
    ## 161                                                                                                 Data Analyst Team Lead (Academic Consulting Project)
    ## 162                                                                                                                           Marketing Area Coordinator
    ## 163                                                                                                                                 Master Career Coach 
    ## 164                                                                                                                            Executive - Hotstar Sales
    ## 165                                                                                                                    Co-Founder & Analytics Consultant
    ## 166                                                                                                                                                     
    ## 167                                                                                                                Data Governance & Quality Coordinator
    ## 168                                                                                                                                     Office Assistant
    ## 169                                                                                                                                     Property Manager
    ## 170                                                                                      Analytics Academic Consulting Project with Rogers, Data Analyst
    ## 171                                                                                                                                         AI Developer
    ## 172                                                                                                       Consultant, Strategist - AI/Data/Finance/Sales
    ## 173                                                                                                                   Senior Analyst, Business Analytics
    ## 174                                                                                                           Data Analyst - Academic Consultant for CGI
    ## 175                                                                                   Practicante Comercial, Vicepresidencia de Alicorp Soluciones (B2B)
    ## 176                                                                                                                                                Owner
    ## 177                                                                             Analytics Academic Consulting Project with McKesson Canada, Data Analyst
    ## 178                                                                                                                  Video Game Financial Advisor Intern
    ## 179                                                                                                                                     CFO & Co-Founder
    ## 180                                                                                         Data Analytics Consultant with Metrolinx - Academic Capstone
    ## 181                                                                                                                     Analista de Soluciones  Big Data
    ## 182                                                                                                                                     Marketing Intern
    ## 183                                                                                                                                Digital Sales Analyst
    ## 184                                                                                                                                                     
    ## 185                                                                                                                 Consulting and Value Capture Analyst
    ## 186                                                                                                                   Actuarial & Risk Management Intern
    ## 187                                                                                                                               Junior Financial Audit
    ## 188                                                                                                                                       Data Scientist
    ## 189                                                                                                                                       Data Scientist
    ## 190                                                                                                                                      Data Consultant
    ## 191                                                                                                                             Digital Marketing Intern
    ## 192                                                                                                                                         Data Analyst
    ## 193                                                                                            Analytics Consultant - McGill Capstone Consulting Project
    ## 194                                                                                                                                                Clerk
    ## 195                                                                                                                                      Trade Marketing
    ## 196                                                                                                                      Sr ML Engineer & Data Scientist
    ## 197                                                                                                                       Adavanced Analytics Consultant
    ## 198                                                                                                                                 Consultant, Omnia AI
    ## 199                                                                                                                            Market Advisory - Analyst
    ## 200                                                                                                                       Business Development Associate
    ## 201                                                                                                                  Practicante de Negocio Restaurantes
    ## 202                                                                                               Subgerente Adjunto de Estrategia de Soluciones de Pago
    ## 203                                                                                                                            SUPERVISOR DE OPERACIONES
    ## 204                                                                                                                           IT Talent Planning Partner
    ## 205                                                                                                               Consultor Senior deSelección - RPO BCP
    ## 206                                                                                               Gerente Adj Auditoría de Modelos de Riesgo - Credicorp
    ## 207                                                                                                                                              Analyst
    ## 208                                                                                                                                          Co-Founder 
    ## 209                                                                                                                                             Docencia
    ## 210                                                                                                                  Ejecutiva de Marketing y Publicidad
    ## 211                                                                                                                                                     
    ## 212                                                                                                                                                     
    ## 213                                                                                                                                               C.O.O.
    ## 214                                                                                                                Senior Analyst, Business Intelligence
    ## 215                                                                                                                     Undergraduate Teaching Assistant
    ## 216                                                                                                                                         Data Analyst
    ## 217                                                                                                        Enterprise Database Management - Data Analyst
    ## 218                                                                                                                                   Teaching Assistant
    ## 219                                                                                                                                 Associate Consultant
    ## 220                                                                                                                                    Software Engineer
    ## 221                                                                                                                    Engineer 1 - Software Development
    ## 222                                                                                                                                            Marketing
    ## 223                                                                                           Data Science Consultant and Team Lead (Analytics Capstone)
    ## 224                                                                                                           Business Analyst, Global Demand Generation
    ## 225                                                                                                    Data Analyst-Academic Capstone Consulting Project
    ## 226                                                                                    Business Analyst & UI/UX Specialist (Academic Consulting Project)
    ## 227                                                                           Business Intelligence Analyst/Data Scientist (Academic Consulting Project)
    ## 228                                                                                                                       Sustainable Development Intern
    ## 229                                                                                                           Pharmaceutical Sales Representative Intern
    ## 230                                                                                     Analytics Academic Consulting Project - Data Science Consultant 
    ## 231                                                                                                                                        VP of Finance
    ## 232                                                                                                                              Data Science Consultant
    ## 233                                                                                                                     Senior Product Manager, Platform
    ## 234                                                                                                                                     Technical Expert
    ## 235                                                                                                       Academic Consulting Project with ArcelorMittal
    ## 236                                                                                         Analytics Academic Consulting Project with CGI, Data Analyst
    ## 237                                                                                                                                     Category Manager
    ## 238                                                                                                                            Talent Acquisition Intern
    ## 239                                                                                 Business Analytics Consultant - Academic Capstone Consulting Project
    ## 240                                                                                                         Data Scientist (Academic Consulting Project)
    ## 241                                                                                                                                       Data Scientist
    ## 242                                                               Program Administrator-Global Manufacturing and Supply Chain Management (GMSCM) Program
    ## 243                                                                                                               Business Intelligence Developer Intern
    ## 244                                                                                      Academic Consulting Project with ArcelorMittal | Data Scientist
    ## 245                                                                                                                 Academic consultant - Data Architect
    ## 246                                                                                                                                  Delivery Consultant
    ## 247                                                                                                                           Graduate Student Assistant
    ## 248                                                                                                                                         Data Analyst
    ## 249                                                                                                                            Data Analytics Consultant
    ## 250                                                                                                                                   Senior Coordinator
    ## 251                                                                                                                           AI & Data Scientist Intern
    ## 252                                                                                                Data Analytics Consultant - Academic Capstone Project
    ## 253                                                                                                                                      Data Specialist
    ## 254                                                                         Analytics Academic Consulting Practicum, Data Scientist/Architect, Team Lead
    ## 255                                                                                                                    Data Science and Analytics Intern
    ## 256                                                                                    Team Lead & Data Analyst (Academic Analytics Consulting Capstone)
    ## 257                                                                            Analytics Academic Consulting Project, Data Architect and Project Manager
    ## 258                                                                                                                           Consumer Engagement Intern
    ## 259                                                                                                                     Becario de Prensa y Comunicación
    ## 260                                                                                                          Consumer Innovation Analyst - Personal Care
    ## 261                                                                                                                                              Analyst
    ## 262                                                                             Analytics Academic Consulting Project with McKesson Canada, Data Analyst
    ## 263                                                                                                                      Business Intelligence Developer
    ## 264                                                                                                                  Data Governance & Management Intern
    ## 265                                                                                                                           Co-Founder Waterborne Perú
    ## 266                                                                                                                             Growth Marketing Analyst
    ## 267                                                                                                                      Logistics and Technology Intern
    ## 268                                                                                                                Key Account Manager Emerging Channels
    ## 269                                                                                        Analyst, Strategic Projects and Governance – Global Expansion
    ## 270                                                                                                       International Banking, Enterprise Productivity
    ## 271                                                                             Analytics Academic Consulting Project with McKesson Canada, Data Analyst
    ## 272                                                                                                                                         Data Analyst
    ## 273                                                                                      Business Strategist & Data Analyst (Academic Analytics Project)
    ## 274                                                                                                                             Data Scientist - Student
    ## 275                                                                                               Management Consulting Manager, Strategy and Consulting
    ## 276                                                                                                                                           Co-Founder
    ## 277                                                                                                                                       Data Engineer 
    ## 278                                                                                                                          Clinical Psychologist Guard
    ## 279                                                                                                                                Consultant Internship
    ## 280                                                                                     Lead Analytics Consultant - Capstone Academic Consulting Project
    ## 281                                                                                                               Full-time Graduate Student (Analytics)
    ## 282                                                                                                              Business Intelligence & Ops Ssr Analyst
    ## 283                                                                                                                                   Director ejecutivo
    ## 284                                                                                                                                      Gerente general
    ## 285                                                                                                                              Marketing Design Intern
    ## 286                                                                                                 Practicante de Búsqueda y Selección de Emprendedores
    ## 287                                                                                                                                  HR Business Partner
    ## 288                                                                                                           Directora de Red Alumni y Bolsa de Trabajo
    ## 289                                                                                                               Workplace Health and Safety Specialist
    ## 290                                                                                                                         Cathegory Innovation Analyst
    ## 291                                                                                                    Associate Data Scientist - CoE Advanced Analytics
    ## 292                                                                                                                          Data Scientist | Consultant
    ## 293                                                                                                                   Customer Success Manager Architect
    ## 294                                                                                                                  Talent Acquisition Business Partner
    ## 295                                                                                                                          Regional Talent Acquisition
    ## 296                                                                                           Senior HR Business Partner – South América (PER-CL-BR-ARG)
    ## 297                                                                                                               Director Business Intelligence Hoteles
    ## 298                                                                                                                                       Data Scientist
    ## 299                                                                                                                    International Business Consultant
    ## 300                                                                                                                                        Founder | CEO
    ## 301                                                                                                                    Jefe de Reclutamiento y Selección
    ## 302                                                                                                                         Practicante Retail Marketing
    ## 303                                                                                                                   Consultant - Finance & Accounting 
    ## 304                                                                                           Consultor Externo Senior de Business Intelligence - Tottus
    ## 305                                                                                                                            Head de Talento y Cultura
    ## 306                                                                                                                                           Co-Founder
    ## 307                                                                                                                      Marketing Operations Specialist
    ## 308                                                                                                                 Practicante Global de Talento Humano
    ## 309                                                                                                                         Analista Jr. Clima y Cultura
    ## 310                                                                                                                          Territorial and GIS Analyst
    ## 311                                                                                                                        Talent Administration Manager
    ## 312                                                                                                                                Investigador de campo
    ## 313                                                                                                            Analista de Atracción de Talento Regional
    ## 314                                                                                            Enabling Organizations to Make Data Matter - VP Data NOLA
    ## 315                                                                                                                           Investment Banking Analyst
    ## 316                                                                                                                                 Asistente de cuentas
    ## 317                                                                                                                                               Asesor
    ## 318                                                                                                                                       Data Scientist
    ## 319                                                                                                         Jefe Corporativo de Data Science & Analytics
    ## 320                                                                                                                             Practicante de Marketing
    ## 321                                                                                                                   Coordinador de Admisión y Métricas
    ## 322                                                                                                                 Analista de Inteligencia de Negocios
    ## 323                                                                                                                                       Data Scientist
    ## 324                                                                                                                             coordinador de cobranzas
    ## 325                                                                                                                          Sales Intern - Food Service
    ## 326                                                                                                                                                     
    ## 327                                                                                                               Coordinadora Customer Value Management
    ## 328                                                                                                                  Analista de Inversiones Sostenibles
    ## 329                                                                                                                                Administrative Intern
    ## 330                                                                                                                              Gestor de Productividad
    ## 331                                                                                                                              React Developer Trainee
    ## 332                                                                                                                 Chief Data, Analytics & Risk Officer
    ## 333                                                                                                                                        Red Bull Wing
    ## 334                                                                                                    Practicante del Despacho de Propiedad Intelectual
    ## 335                                                                                                                                      Marketing Co-op
    ## 336                                                                                                                             Local HR Services Intern
    ## 337                                                                                                                                       Data Scientist
    ## 338                                                                                                                          Client & Product Management
    ## 339                                                                                                                                            Assistant
    ## 340                                                                                                                 Analyst, Sales Strategy & Operations
    ## 341                                                                                                                         Consumer Marketing Associate
    ## 342                                                                                                                     Directora de relaciones públicas
    ## 343                                                                                                                       Analista de Marca Color Centro
    ## 344                                                                                                                            Analista Datos de Negocio
    ## 345                                                                                                                                        Design Intern
    ## 346                                                                                                                               Asistente de Marketing
    ## 347                                                                                                             Strategy & Transformation Senior Analyst
    ## 348                                                                                                                            Coordinadora de proyectos
    ## 349                                                                                     Coordinador de Emprendimiento / Experiencia del emprendedor (CX)
    ## 350                                                                                                                          Cofounder / Chief Scientist
    ## 351                                                                                                                              People Analytics Senior
    ## 352                                                                                                                               Jefe de comunicaciones
    ## 353                                                                                                                              Especialista de Modelos
    ## 354                                                                                                                                     Co-founder & CEO
    ## 355                                                                                                                 Key Account Executive - Modern Trade
    ## 356                                                                                                                Social Media and Community Management
    ## 357                                                                                                                    Practicante de Control de Gestión
    ## 358                                                                                                                       Financial Planning Coordinator
    ## 359                                                                                                                       Analista de Marketing al Canal
    ## 360                                                                                                                Associate | Corporate & Financial Law
    ## 361                                                                                                                  Practicante de Marketing Industrias
    ## 362                                                                                                                          Puestos de recursos humanos
    ## 363                                                                                                                      Coordinador Relaciones Públicas
    ## 364                                                                                                          Experience Delivery Director (Engineering) 
    ## 365                                                                                                                                 Head of Data Science
    ## 366                                                                                                                  Data Scientist Especialista Riesgos
    ## 367                                                                                                                                     Mobile Developer
    ## 368                                                                                                                                            Directivo
    ## 369                                                                                                                                        CEO & Founder
    ## 370                                                                                                                                Practicante Comercial
    ## 371                                                                                                                 Sr. Manager, Consulting - Insurance 
    ## 372                                                                                                                                                     
    ## 373                                                                                                                                Senior Data Scientist
    ## 374                                                                                                      Cofundadora y Diseñadora de la marca Alma Vitta
    ## 375                                                                                                                                   Asistente contable
    ## 376                                                                                              Customer Development Executive - Indirect Trade Norte 2
    ## 377                                                                                                                     GERENTE GENERAL & CHEF EJECUTIVO
    ## 378                                                                                                       Head of investment operations - BBVA BOLSA SAB
    ## 379                                                                                                            Practicante de Ventas - Canal Tradicional
    ## 380                                                                                                                                              Analyst
    ## 381                                                                                                                      Director – Masters of Analytics
    ## 382                                                                                  Senior Manager, International Banking Analytics - Customer Insights
    ## 383                                                                                                                                    Advisory Services
    ## 384                                                                                                                                     Data Performance
    ## 385                                                                                                                               Facultad de Ingeniería
    ## 386                                                                                                                           Jefe de Riesgos de Mercado
    ## 387                                                                                                                Practicante Pre Profesional Comercial
    ## 388                                                                                                                            Machine Learning Engineer
    ## 389                                                                                                                                      Research Intern
    ## 390                                                                                                                              Machine Learning Intern
    ## 391                                                                                Senior Manager, Analytics & Operations Technology Integration, ATS EU
    ## 392                                                                                                                                       Data Scientist
    ## 393                                                                                                                        Practicante de diseño gráfico
    ## 394                                                                                               Program Coordinator, Goergen Institute of Data Science
    ## 395                                                                                                                       Analista de Control de Gestión
    ## 396                                                                                                              Practicante de Planeamiento Estratégico
    ## 397                                                                                                                                          Co-Founder 
    ## 398                                                                                                                                          Practicante
    ## 399                                                                                                                             Lead Creative Strategist
    ## 400                                                                                                                                    Account Executive
    ## 401                                                                                                                                        Founding Dean
    ## 402                                                                                                                 Associate Dean for Graduate Programs
    ## 403                                                                                                                        Senior Data Analytics Manager
    ## 404                                                                                                                                            President
    ## 405                                                                                                                                 Ski School Team Lead
    ## 406                                                                                                                           Financial Planning Analyst
    ## 407                                                                                                                                         Product Lead
    ## 408                                                                                        Data Analytics Specialist - Digital Payments & Data Analytics
    ## 409                                                                                                                   Jefe de Automatización de Procesos
    ## 410                                                                                                                                Data Scientist @Entel
    ## 411                                                                                                                                         Law Practice
    ## 412                                                                                                                  Practicante de Procesos y Proyectos
    ## 413                                                                                                                  Strategic Relations | Partnerships 
    ## 414                                                                                                                                        Data Engineer
    ## 415                                                                                                                              Analista de operaciones
    ## 416                                                                                                       Chair, Department of Computational Biomedicine
    ## 417                                                                                                      Sales Manager - Telco, Bank, Insurance & Retail
    ## 418                                                                                                                                       Data Scientist
    ## 419                                                                                                                                       Data Scientist
    ## 420                                                                                                                                 Sponsorship Director
    ## 421                                                                                                                      Practicante de Gerencia General
    ## 422                                                                                                                                                  CEO
    ## 423                                                                                                                                      Gerente general
    ## 424                                                                                                                  Full Professor (endowed chair, PIK)
    ## 425                                                                                                                                             Fundador
    ## 426                                                                                                            Engineering Manager - Data Infrastructure
    ## 427                                                                                                          Practicante Pre Profesional de Arquitectura
    ## 428                                                                                                                  Research and Design Strategy Intern
    ## 429                                                                                                                                  Analyst - Hard Tech
    ## 430                                                                                                                                        Data Engineer
    ## 431                                                                                                                   Vicepresidente de TI y Operaciones
    ## 432                                                                                                                   Vicepresidente de Mercado Empresas
    ## 433                                                                                                                                  Gerente de Whosales
    ## 434                                                                                                                                        Data Engineer
    ## 435                                                                                                                Visiting Scholar - Research Assistant
    ## 436                                                                                                                            Seller Perfomance Analyst
    ## 437                                                                                                                                   Director comercial
    ## 438                                                                                                          Research Assistant - Electrical Engineering
    ## 439                                                                                                                   Latin America Business Development
    ## 440                                                                                                                                    Visiting Attorney
    ## 441                                                                                          Analista de logística en los Juegos Panamericanos Lima 2019
    ## 442                                                                                                                                   Marketing Director
    ## 443                                                                                                                                          Practicante
    ## 444                                                                                                                     Fundadora y CEO de WWIN Planners
    ## 445                                                                                                                             Data & Big Data Modeler 
    ## 446                                                                                                                             Senior Software Engineer
    ## 447                                                                                                                                   Director de medios
    ## 448                                                                                                                                        Data Engineer
    ## 449                                                                                                                                                  CEO
    ## 450                                                                                                                                                  CTO
    ## 451                                                                                                                                            Associate
    ## 452                                                                                                                     Quantitative Analytics Associate
    ## 453                                                                                                                                    Software Engineer
    ## 454                                                                                               Associate - Planning, Budgeting and Financial Analysis
    ## 455                                                                                                                                          Practicante
    ## 456                                                                                                                                    Practicante Legal
    ## 457                                                                                               Machine Learning, NLP, Data Science Research Assistant
    ## 458                                                                                                                                       Data Scientist
    ## 459                                                                                                                               Gerente de operaciones
    ## 460                                                                                                                     Practicante en el Area comercial
    ## 461                                                                                                                                       President -CEO
    ## 462                                                                                                                             Key Account Executive MT
    ## 463                                                                                                            Customer Success Partner - Fruit & Retail
    ## 464                                                                                                                          Factory Controlling Trainee
    ## 465                                                                                                                                       Data Scientist
    ## 466                                                                                                    Coverage Analyst - Corporate & Investment Banking
    ## 467                                                                                                                                 Ejecutivo de cuentas
    ## 468                                                                                                                Especialista de validación de modelos
    ## 469                                                                                                                                                Socio
    ## 470                                                                                                                  RappiPay - TA Lead Tech and Product
    ## 471                                                                                                                                 Ejecutiva Financiera
    ## 472                                                                                                     Gerente  de Planificación y Estudios Económicos 
    ## 473                                                                                                                   General Manager Kavak Capital Perú
    ## 474                                                                                                                          CEO Chief Executive Officer
    ## 475                                                                                                                   Senior | Financial Services Office
    ## 476                                                                                                                                      Gerente General
    ## 477                                                                                                                              Director Of Engineering
    ## 478                                                                                                    Facilitadora Comercial de Soluciones Corporativas
    ## 479                                                                                                                            Asesor superior de ventas
    ## 480                                                                                                              Jefe de Finanzas y Proyectos Especiales
    ## 481                                                                                                                                     Asesor comercial
    ## 482                                                                                                                             Chief Technology Officer
    ## 483                                                                                                                                        Design Intern
    ## 484                                                                                                                                 Analytics Translator
    ## 485                                                                                                                                    Logistics Trainee
    ## 486                                                                                                       Subgerente Adjunto de Analytics y Cumplimiento
    ## 487                                                                                                                                   Director Ejecutivo
    ## 488                                                                                                                                President & cofounder
    ## 489                                                                                                     Head of Strategy, Planning, and Special Projects
    ## 490                                                                                                                       Analista de Control de Gestion
    ## 491                                                                                                                                 Docente de marketing
    ## 492                                                                         Planning & Merchandising Analyst (República Dominicana Fashion & Accesories)
    ## 493                                                                                        Gerente Central de Planificación, Riesgos y Negocio Mayorista
    ## 494                                                                                                                     Jefe de Inteligencia de Negocios
    ## 495                                                                                                      Gerente de Inversiones y Productos en SURA Perú
    ## 496                                                                                                                                            Professor
    ## 497                                                                                                                                Data & Analytics Lead
    ## 498                                                                                                                                                     
    ## 499                                                                                                                                    Tercer Secretario
    ## 500                                                                                                                                Commercial Supervisor
    ## 501                                                                                                                       Talent Acquisition Analyst Sr.
    ## 502                                                                                                                     Data & Analytics Product Manager
    ## 503                                                                                                                                        Administrator
    ## 504                                                                           Associate Client Engineering Data Scientist, IBM Technology, Latin America
    ## 505                                                                                                                                    Marketing Analyst
    ## 506                                                                                                                        Business Intelligence Analyst
    ## 507                                                                                                                          Data Scientist Especialista
    ## 508                                                                                                                               Manager Data Scientist
    ## 509                                                                                                                           Advanced Analytics Manager
    ## 510                                                                                                                                Senior Data Scientist
    ## 511                                                                                                                  Business Analyst - Digital Channels
    ## 512                                                                                                                                Senior Data Scientist
    ## 513                                                                                                                    Analista de Mediciones de Mercado
    ## 514                                                                                                                       Corporate M&A Junior Associate
    ## 515                                                                                                                           Strategy Manager @Farmauna
    ## 516                                                                                                                     Machine Learning Engineer Junior
    ## 517                                                                                                                    Practicante de Derecho Financiero
    ## 518                                                                                      Staff/Assistant in Audit Analytics | DnA Perú - 10x Accelerator
    ## 519                                                                                                                  Practicante de Campañas Comerciales
    ## 520                                                                                                                                      gerente general
    ## 521                                                                                                                      Product Owner of Revenue Growth
    ## 522                                                                                                                              Digital Product Analyst
    ## 523                                                                                                              Director of Data Privacy and Governance
    ## 524                                                                                                                                       Growth Analyst
    ## 525                                                                                                                           Talent Acquisition Trainee
    ## 526                                                                                                                                 Data Engineer Senior
    ## 527                                                                                                                                     Staff consultant
    ## 528                                                                                                                      Analista Gestión Punto de Venta
    ## 529                                                                                                                                    Practicante legal
    ## 530                                                                                                                Chief Technology Officer & Co-founder
    ## 531                                                                                                            Sales Representative - Bebidas On Premise
    ## 532                                                                                                                Product Manager Digital Vehicle Sales
    ## 533                                                                                                                         Business Development Analyst
    ## 534                                                        Análisis de datos y asesorías en aplicaciones de Machine learning, Psicometría y Estadística.
    ## 535                                                                                                                            Machine Learning Engineer
    ## 536                                                                                                                                      Data Scientist 
    ## 537                                                                                                                                           IT Manager
    ## 538                                                                                                                 Associate Product Excellency Manager
    ## 539                                                                                                                Socio - Gerente Comercial & Marketing
    ## 540                                                                                                                                             Lecturer
    ## 541                                                                                                                                Co-Founder & manager 
    ## 542                                                                                      Chapter Lead - Data Science Manager (COE of Advanced Analytics)
    ## 543                                                                                                                 Associate Data Conversion Consultant
    ## 544                                                                                                                                  Technical Recruiter
    ## 545                                                                                        Asistente de Reclutamiento y Selección - Recolocación Laboral
    ## 546                                                                                                                                    Commercial Intern
    ## 547                                                                                                                                                 CIO 
    ## 548                                                                                                                 Analista de Talento, Cultura y Clima
    ## 549                                                                                                                     Logistics Performance Sr Analyst
    ## 550                                                                                                                             Practicante de Marketing
    ## 551                                                                                                                      Programme Manager - Cash Giving
    ## 552                                                                                                                    Business Transformation Associate
    ## 553                                                                                                                          Incoming UX Designer Intern
    ## 554                                                                                                                                       Data Scientist
    ## 555                                                                                                                      Business Controlling Specialist
    ## 556                                                                                                                                      Finance Analyst
    ## 557                                                                                                                  Director general y consultor senior
    ## 558                                                                                   Docente del Programa Online de Innovación y Transformación Digital
    ## 559                                                                                                               Jefe de Operaciones e Investigaciones.
    ## 560                                                                                                                                         Data Analyst
    ## 561                                                                                                                    Retail Business Execution Analyst
    ## 562                                                                                                                                          Odontología
    ## 563                                                                                                         Practicante del área de litigios y arbitraje
    ## 564                                                                                                                                       Data Scientist
    ## 565                                                                                                                                  Head de Operaciones
    ## 566                                                                                                                                  Analista de Compras
    ## 567                                                                                                           Groceries Operations Lead | Pacific Region
    ## 568                                                                                                                                                     
    ## 569                                                                                                                                   Head Of Operations
    ## 570                                                                                                                           Investment Banking Analyst
    ## 571                                                                                                                                     Facility Manager
    ## 572                                                                                                                     Senior Cyber Security Consultant
    ## 573                                                                                                                       Product Owner - Chile and Peru
    ## 574                                                                                                             Chief Data Officer | Football Analytics 
    ## 575                                                                                                                                Key Account Executive
    ## 576                                                                                                                    Brand Marketing Assistant Analyst
    ## 577                                                                                                                        Applied Scientist - Prime Air
    ## 578                                                                                                                           Talent Acquisition Analyst
    ## 579                                                                                                                              Directora Programa Peru
    ## 580                                                                                                                          Practicante de Data Science
    ## 581                                                                                                                                           Co-Founder
    ## 582                                                                                                                                        SEO – Founder
    ## 583                                                                                                                        Business Intelligence Analyst
    ## 584                                                                                                                                 Logistics Supervisor
    ## 585                                                                                                                                Junior Credit Analyst
    ## 586                                                      Data Architect for the Development  of the "Nuevo Sistemas de Recaudación Tributaria Municipal"
    ## 587                                                                                                                  Advanced Analytics - Data Scientist
    ## 588                                                                                                                                             Tesorera
    ## 589                                                                                                                         Inside Sales Account Manager
    ## 590                                                                                                             Investment Banking M&A Off-Cycle Analyst
    ## 591                                                                                                                                               Ventas
    ## 592                                                                                                               Property & Casualty Commercial Trainee
    ## 593                                                                                                                            Corporate Banking Analyst
    ## 594                                                                                                                            Asesor de ventas de campo
    ## 595                                                                                                                Commercial Development On Core Intern
    ## 596                                                                                                                                           Analyst BO
    ## 597                                                                                                                                              Analyst
    ## 598                                                                                                                               Product & Partnerships
    ## 599                                                                                                                               Practicante de Talento
    ## 600                                                                                                                          Customer Excellence Manager
    ## 601                                                                                                                        PMO (Project Manager Officer)
    ## 602                                                                                                                                            Economist
    ## 603                                                                                                                                 Gerente de Analytics
    ## 604                                                                                                          Business Innovator en Centro de Innovacxión
    ## 605                                                                                                                        Funcionario Banca de Negocios
    ## 606                                                                                     Group Data Officer | Head of Data & Analytics, Macquarie Capital
    ## 607                                                                                                                          Strategic Finance Associate
    ## 608                                                                                                                                  Business Consultant
    ## 609                                                                                                                           Seller Performance Analyst
    ## 610                                                                                                              Director de Estadistica y Procesamiento
    ## 611                                                                                                                                     Director - LATAM
    ## 612                                                                                                                Business Architect -Public Sector-MCR
    ## 613                                                                                                              User Acquisition and Activation Analyst
    ## 614                                                                                                   Entrepreneur Selection and Growth Senior Associate
    ## 615                                                                                                                              Oficial de Cumplimiento
    ## 616                                                                                                                               Experienced Technician
    ## 617                                                                                                                                      Research Intern
    ## 618                                                                                                                             Jefe de recursos humanos
    ## 619                                                                                                          Brand Development Representative - E-Retail
    ## 620                                                                                                                           Big Data Software Engineer
    ## 621                                                                                                          Coach y experta en desarrollo de personas. 
    ## 622                                                                                                                                Senior Data Scientist
    ## 623                                                                                                                                Conseillier principal
    ## 624                                                                                                                             Jefe de Recursos Humanos
    ## 625                                                                                                                                    Talento Logistica
    ## 626                                                                                                                                       Talent Partner
    ## 627                                                                                                                                           Co-Founder
    ## 628                                                                                                 Coordinador Comercial - Desarollo de Nuevos Negocios
    ## 629                                                                                                                                       Growth Manager
    ## 630                                                                                                                                    Software engineer
    ## 631                                                                                                                                     Customer Success
    ## 632                                                                                                                        Business Intelligence Analyst
    ## 633                                                                                                                               Analista Sr de Talento
    ## 634                                                                                                                           Revenue Management Analyst
    ## 635                                                                                                           Associate | Corporate & Investment Banking
    ## 636                                                                                                                        Commercial Excellence Analyst
    ## 637                                                                                                    Interna en el área de Orientación Psicopedagógica
    ## 638                                                                                                                            Site Reliability Engineer
    ## 639                                                                                                                                       Gruppenleitung
    ## 640                                                                                                                                              Founder
    ## 641                                                                                                                  Analista Jr. Gestión Punto de Venta
    ## 642                                                                                                                                       VP of Delivery
    ## 643                                                                                                                        Planning Optimization Analyst
    ## 644                                                                                                                               Growth Lead Specialist
    ## 645                                                                                                                                            Marketing
    ## 646                                                                                                                     Corporate Affairs Senior Analyst
    ## 647                                                                                                       Corporate Cash Management & Collection Manager
    ## 648                                                                                                                                           Cofundador
    ## 649                                                                                                                               Operations Coordinator
    ## 650                                                                                                                                  Project Coordinator
    ## 651                                                                                                                          Community Relations Manager
    ## 652                                                                                                                        Customer Intelligence Analyst
    ## 653                                                                                                                                     Co-Founder / CEO
    ## 654                                                                                                      Analista de Data Governance (DMBOK MDM CATALOG)
    ## 655                                                                                                                               Private Equity Analyst
    ## 656                                                                                                                          Analista Estadístico Junior
    ## 657                                                                                                                       Lead Instructor - Data Science
    ## 658                                                                                                                                 Senior Data Engineer
    ## 659                                                                                                                                      Mentorship Lead
    ## 660                                                                                                 Coordinadora de canales de autogestión y Eficiencias
    ## 661                                                                                                       Data Analyst -- Analytics Center of Excellence
    ## 662                                                                                                                                Practicante Actuarial
    ## 663                                                                                                                                   Selectora Bilingüe
    ## 664                                                                                                                                      Gerente General
    ## 665                                                                                                                             Asistente de Revenue PPM
    ## 666                                                                                                                                  Data Science Junior
    ## 667                                                                                                                               Coordinador Académico 
    ## 668                                                                                                                                   Commercial Analyst
    ## 669                                                                                                                                  Research Strategist
    ## 670                                                                                    Vicepresidente de Gestión Humana, Sostenibilidad y Administración
    ## 671                                                                                                                                      Legal Assistant
    ## 672                                                                                             Jefe de Scouting y coordinación de soporte al futbolista
    ## 673                                                                                                                                  Asistente Comercial
    ## 674                                                                                                                               Senior DevOps Engineer
    ## 675                                                                                                                                 Lead Cloud Architect
    ## 676                                                                                                                                    Co-fundador y CEO
    ## 677                                                                                                                              Consultora de proyectos
    ## 678                                                                                                                              Command Center Manager 
    ## 679                                                                                                                                           Co-Founder
    ## 680                                                                                                                             Customer Support Manager
    ## 681                                                                                                                                 Brand Growth Analyst
    ## 682                                                                                                                                  Venture Development
    ## 683                                                                                                                                   Investment Analyst
    ## 684                                                                                                                         Assistentin Stadtpräsidentin
    ## 685                                                                                                         Innovation Fellow, Data & Analytics Strategy
    ## 686                                                                                                               Innovation Data Analyst Senior Analyst
    ## 687                                                                                                                                     Managing Partner
    ## 688                                                                                                                    M&A and Business Strategy Analyst
    ## 689                                                                                                                                   Chief Data Officer
    ## 690                                                                                                                             Chief Data Officer (CDO)
    ## 691                                                                  Profesor Principal, Investigador Senior en Pontificia Universidad Catolica del Peru
    ## 692                                                                                                                                    Big Data Engineer
    ## 693                                                                                                                             Senior DevOps Consultant
    ## 694                                                                                                                                  Data Scientist - VP
    ## 695                                                                                                                       Chief Data & Analytics Officer
    ## 696                                                                                                 Embajador y Miembro del Consejo Asesor Internacional
    ## 697                                                                                                     Director responsable del laboratorio de Big Data
    ## 698                                                                                                                            Director of Analytics COE
    ## 699                                                                             Especialista de Control de Gestion - Banca Minorista/ Revenue Management
    ## 700                                                                                                                                       Data Scientist
    ## 701                                                                                                                       Business Intelligence Engineer
    ## 702                                                                                                                                   Operations Analyst
    ## 703                                                                                                                                             Director
    ## 704                                                                                                                           Assistant To The President
    ## 705                                                                                                                        Analista de Comercio Exterior
    ## 706                                                                                                                                      EM Sales Intern
    ## 707                                                                                                                               IT Technical Recruiter
    ## 708                                                                                                                                    Business Designer
    ## 709                                                                                                                          Business Analytics Manager 
    ## 710                                                                                                          High end - Brand Development Representative
    ## 711                                                                                                                      Strategy & Planning Coordinator
    ## 712                                                                                                                            Machine Learning Engineer
    ## 713                                                                                                                           Independent Business Owner
    ## 714                                                                                                                    Trade Marketing Leader Hair Color
    ## 715                                                                                                                                      Country Manager
    ## 716                                                                                                                                           Co-Founder
    ## 717                                                                                                                     Practicante de Data Architecture
    ## 718                                                                                                                                       Data Architect
    ## 719                                                                                                                            Data Portfolio Managment 
    ## 720                                                                                                                                           Cofundador
    ## 721                                                                                                                                 Head of Data Science
    ## 722                                                                                                                                        Data Engineer
    ## 723                                                                                                                                 Analista business BI
    ## 724                                                                                                                        Senior Product Manager (Data)
    ## 725                                                                                                                                          SEO Manager
    ## 726                                                                                                                                           Deputy CEO
    ## 727                                                                                                          Practicante Pro de Supply Chain & Logística
    ## 728                                                                                                                       Vice President of Data Science
    ## 729                                                                                                                                  Asistente Comercial
    ## 730                                                                                                                           Investment Banking Analyst
    ## 731                                                                                                    Especialista de Inteligencia y Analitica Avanzada
    ## 732                                                                                                                                      Legal Assistant
    ## 733                                                                                                                                        Growth Intern
    ## 734                                                                                                                                    Senior Consultant
    ## 735                                                                                                                                     Business Analyst
    ## 736                                                                                                          Profesor de Imagen Corporativa y Reputación
    ## 737                                                                                                                         Market Places Senior Analyst
    ## 738                                                                                                                                   Business Developer
    ## 739                                                                                                                             Head of Operations & SLA
    ## 740                                                                                                                                      Head Equipo TIC
    ## 741                                                                                                                                  Statistical Analyst
    ## 742                                                                                                          Focal Point AMS - Data & Analytics Products
    ## 743                                                                                                                            Gerente de Sistemas - CIO
    ## 744                                                                                                                                             Fundador
    ## 745                                                                                                                      Ecommerce Digital Media Analyst
    ## 746                                                                                                                                  Engineering Manager
    ## 747                                                                                                                                         Data Analyst
    ## 748                                                                                                                      Data & Analytics Expert Analyst
    ## 749                                                                                                                                  Solutions Architect
    ## 750                                                                                                                                       Reclutador Sr.
    ## 751                                                                                                                                      GERENTE GENERAL
    ## 752                                                                                                                     Jefe de Inteligencia de Negocios
    ## 753                                                                                                                      Account Executive Andean Region
    ## 754                                                                                                                                  Data Managment Lead
    ## 755                                                                                                                                       Data Scientist
    ## 756                                                                                                                               Chief Business Officer
    ## 757                                                                                                                 Analista de Experimentación y Growth
    ## 758                                                                                                                  CDO - Data, BI & Advanced Analytics
    ## 759                                                                                                                             Practicante de Logística
    ## 760                                                                                                                                           Co-Founder
    ## 761                                                                                                                                         Data Analyst
    ## 762                                                                                                                Head of Digital and Technology, LATAM
    ## 763                                                                                                                                 Design & UX Sr. Lead
    ## 764                                                                                                                                           Co-Founder
    ## 765                                                                                                                                        Founder - CEO
    ## 766                                                                                                             Head of Sales Development Representative
    ## 767                                                                                                                                    Financial Analyst
    ## 768                                                                                                                       CTO - Chief Technology Officer
    ## 769                                                                                              Senior Data Consultant - Artificial Intelligence & Data
    ## 770                                                            Corporate Director - Commercial Planning, Sales, Retail, Marketing & HR Platform Services
    ## 771                                                                                                                                  Business Specialist
    ## 772                                                                                                             Senior Subject Matter Expert - Data & AI
    ## 773                                                                                                              Practicante de Trade Marketing - Salsas
    ## 774                                                                                                                           Marketing and Sales Intern
    ## 775                                                                                                                                  Senior Data Analyst
    ## 776                                                                                                             Co-Founder & Marketing and Sales Manager
    ## 777                                                                                                                                      Product Manager
    ## 778                                                                                                                                  Solutions Architect
    ## 779                                                                                                                     Subjefe de Programación TV y OTT
    ## 780                                                                                          Practicante Pre Profesional de Inclusión financiera en Yape
    ## 781                                                                                                                                  Content Coordinator
    ## 782                                                                                                                              Chief Operating Officer
    ## 783                                                                                                                                        QA Automation
    ## 784                                                                                                                                    Account Executive
    ## 785                                                                                                                             Investigador practicante
    ## 786                                                                                                                                         Video Editor
    ## 787                                                                                                                          Investment Advisory Analyst
    ## 788                                                                                                                                 Private Debt Analyst
    ## 789                                                                                                                 Treasury & Collection Senior Analyst
    ## 790                                                                                                                       Analista de Control de Gestión
    ## 791                                                                                                                           Senior Solutions Architect
    ## 792                                                                                                                                     Analista de Data
    ## 793                                                                                                                                   Commercial Manager
    ## 794                                                                                                                             Managing Director Mexico
    ## 795                                                                                             Buiness Leader - Business Agility Institute Chapter Perú
    ## 796                                                                                                                                      Gerente general
    ## 797                                                                                                                                    Service Owner GDH
    ## 798                                                                                                                         Data Platform Technical Lead
    ## 799                                                                                                                   Talent & Culture Manager (CO & EC)
    ## 800                                                                                                                               Innovation Lab Manager
    ## 801                                                                                                                Data Architect, Data Lake & Analytics
    ## 802                                                                                                                                        Growth Hacker
    ## 803                                                                                                                     Planning & Merchandising Analyst
    ## 804                                                                                            Data & Analytics Manager - Analytics Center of Excellence
    ## 805                                                                                                                               Recruitment Specialist
    ## 806                                                                                                                                      General Manager
    ## 807                                                                                                    Business Partner Senior - Experiencia del Cliente
    ## 808                                                                                                                                      General Manager
    ## 809                                                                                                                                      Project Analyst
    ## 810                                                                                           Gerente de Gestion de clientes e investigación de mercados
    ## 811                                                                                                                            Analista Programador JAVA
    ## 812                                                                                                                    Founder & Chief Executive Officer
    ## 813                                                                                                                          Practicante profesional UTI
    ## 814                                                                                                                                        Data Enginner
    ## 815                                                                                                                                    Sales Coordinator
    ## 816                                                                                                                                    Jefe de prácticas
    ## 817                                                                                                                                   Teaching Assistant
    ## 818                                                                                                                       Analista de Control de Gestión
    ## 819                                                                                                                            Sales Planning Analyst Jr
    ## 820                                                                                                                                     Gerente regional
    ## 821                                                                                                                             Founder & Team Principal
    ## 822                                                                                                                              Social Commerce Analyst
    ## 823                                                                                         Profesor a tiempo parcial - Machine Learning & Deep Learning
    ## 824                                                                                                                                     Product Designer
    ## 825                                                                                                                                Digital Product Owner
    ## 826                                                                                                                                 Sales Representative
    ## 827                                                                                                                                       Data Scientist
    ## 828                                                                                                                                  Senior Data Analyst
    ## 829                                                                                                                                Representante en Perú
    ## 830                                                                                                  Applied Intelligence Network Lead for Latin America
    ## 831                                                                                                                           Brand Marketing Specialist
    ## 832                                                                                          Analista de Transformación Digital - PMO & Results Delivery
    ## 833                                                                                                                            Manager Talent Management
    ## 834                                                                                                                                     Project Officer 
    ## 835                                                                                                                                 Chief Data Scientist
    ## 836                                                                                                        Home Printing Category Manager Perú & Bolivia
    ## 837                                                                                                                          Cloud Service Delivery Lead
    ## 838                                                                                                                               Value Creation Analyst
    ## 839                                                                                                                                      Consultor pleno
    ## 840                                                                                                             Junior Consultant Digital Transformation
    ## 841                                                  Asistente administrativo de la Oficina de Contabilidad                                             
    ## 842                                                                                                                             Practicante de Marketing
    ## 843                                                                                                         Trade Marketing Execution Analyst - High End
    ## 844                                                                                                              Skin & Care Category Innovation Analyst
    ## 845                                                                                                                                    Gerente Comercial
    ## 846                                                                                                                                           Co-Founder
    ## 847                                                                                Director de la Maestría en Ciberseguridad y Gestión de la Información
    ## 848                                                                                                                            Coordinadora de marketing
    ## 849                                                                                                                                 Data Product Manager
    ## 850                                                                                                                              Chief Executive Officer
    ## 851                                                                                                                      Docente de Diseño de Interiores
    ## 852                                                                                                                                                     
    ## 853                                                                                                                                           Consultant
    ## 854                                                                                                                            Ingeniero de Datos Senior
    ## 855                                                                                                                                Senior Data Scientist
    ## 856                                                                                                    Gerente Adj. Arq. de Tecnologías - Tech Architect
    ## 857                                                                                                                                 Analytics Specialist
    ## 858                                                                                                               Practicante de Excelencia Operacional 
    ## 859                                                                                                                                         Data Analyst
    ## 860                                                                                                                                            Associate
    ## 861                                                                                                                 Incharge - Financial Services Office
    ## 862                                                                                                       Senior Business Analyst - Analytics & Big Data
    ## 863                                                                                                                          Sales Executive Wholesalers
    ## 864                                                                                                                                 PRESIDENTE EJECUTIVO
    ## 865                                                                                                        Practicante Pre-Profesional de Diseño Gráfico
    ## 866                                                                                                                             IT Recruitment Associate
    ## 867                                                                                                                      Pre sales E-commerce Consultant
    ## 868                                                                                                       IT Head Hunter / Talent Acquisition Specialist
    ## 869                                                              Chief Digital Officer (CDO) & Chief Technology Officer (CTO) & Chief Data Officer (CDO)
    ## 870                                                                                                                         Corporate M&A Senior Analyst
    ## 871                                                                                                                            Chief Information Officer
    ## 872                                                                                                                         Analista de recursos humanos
    ## 873                                                                                                                     Operations and Growth Specialist
    ## 874                                                                                                                      Gerente de Transformación Agile
    ## 875                                                                                                                                    VP of Engineering
    ## 876                                                                                             Senior consultant in risk management, accounting and P&L
    ## 877                                                                                                                                   COO and Co-Founder
    ## 878                                                                                                                                        Summer Intern
    ## 879                                                                                                                            Machine Learning Engineer
    ## 880                                                                                                                            Profesora e Investigadora
    ## 881                                                                                                         Key Account Executive - Brokers Corporativos
    ## 882                                                                                                                     Brand Development Representative
    ## 883                                                                                                                                                  BDR
    ## 884                                                                                                                  Analista de Inteligencia de Negocio
    ## 885                                                                                                                                 Gerente de proyectos
    ## 886                                                                                                                          Consumer Engagement Analyst
    ## 887                                                                                                                                    Marketing Manager
    ## 888                                                                                                                                         Data Analyst
    ## 889                                                                                                                                  FP&A Senior Analyst
    ## 890                                                                                                                          Consumer Innovation Analyst
    ## 891                                                                                                                                         Legal Intern
    ## 892                                                                                                                                         Data Analyst
    ## 893                                                                                                                                 Head of Data Science
    ## 894                                                                                                                 Consumer Engagement Manager - Cyzone
    ## 895                                                                                                                       Operations & Processes Manager
    ## 896                                                                                                 Digital Transformation & Innovation Delivery Manager
    ## 897                                                                                                                                         Data Analyst
    ## 898                                                                                                                                                     
    ## 899                                                                                                                           Senior Business Specialist
    ## 900                                                                                                                                          Líder Cloud
    ## 901                                                                                                                          Founding Executive Director
    ## 902                                                                                                                       Category Management Specialist
    ## 903                                                                                                                                   Arquiteto de dados
    ## 904                                                                                                                                                  CEO
    ## 905                                                                                                                                      Analytical Lead
    ## 906                                                                                                                                        Data Engineer
    ## 907                                                                                                                       Analista Business intelligence
    ## 908                                                                                                                                     Co-Founder & CEO
    ## 909                                                                                                                                       Data Architect
    ## 910                                                                                                                                Senior Data Scientist
    ## 911                                                                                                                        Business Intelligence Analyst
    ## 912                                                                                                               Product Manager - William Grant & Sons
    ## 913                                                                                                                                   Product Manager Sr
    ## 914                                                                                                                                Senior Data Scientist
    ## 915                                                                                                        Analista de Atracción y Selección del Talento
    ## 916                                                                                                                                            Lead Data
    ## 917                                                                                                                                  Analista de compras
    ## 918                                                                                                     Practicante Profesional Comercial | Aftermarket 
    ## 919                                                                                                          Subgerente de Planificación y Red Logística
    ## 920                                                                                                                          Consumer Engagement Manager
    ## 921                                                                                                                                            VC Intern
    ## 922                                                                                                         Machine Learning Engineer & Big Data Analyst
    ## 923                                                                                                                    Founder & Chief Executive Officer
    ## 924                                                                                                    Business Specialist Advanced - Clientes Digitales
    ## 925                                                                                                                                     Managing Partner
    ## 926                                                                                                                         Senior Business Intelligence
    ## 927                                                                                                                                Senior Data Scientist
    ## 928                                                                                                                    Desarrollador de aplicaciones web
    ## 929                                                                                                                               Director independiente
    ## 930                                                                                                                                  Business Specialist
    ## 931                                                                                            Especialista y Consultor de Innovación y Design Thinking 
    ## 932                                                                                                                                  Lead Data Scientist
    ## 933                                                                                                      Director TI - Tecnología y Soluciones Digitales
    ## 934                                                                                                           Senior Solutions Engineer - Spain/Portugal
    ## 935                                                                                                                                Data & Analytics Head
    ## 936                                                                                                                             Financial Market Analyst
    ## 937                                                                                                                                         Lead Bot AVI
    ## 938                                                                                                                    Data Analyst Specialist - Digital
    ## 939                                                                                                                 SAP Business Intelligence Consultant
    ## 940                                                                                                                              Sales Manager HFS North
    ## 941                                                                                                                         Sr Machine Learning Engineer
    ## 942                                                                                                                                         Head of QHSE
    ## 943                                                                                                                                            Associate
    ## 944                                                                                                         Global Coordinator - D2C & Digital Platforms
    ## 945                                                                                                                                Analista de categoría
    ## 946                                                                                                                                   Commercial Manager
    ## 947                                                                                                                          Commercial Strategy Analyst
    ## 948                                                                                                                                  Business Consultant
    ## 949                                                                                                                                     Business Analyst
    ## 950                                                                                                                         Investments Junior Associate
    ## 951                                                                                                                             Practicante de Categoría
    ## 952                                                                                                       Practicante Comercial del área de Multilatinas
    ## 953                                                                                                                Coordinadora de selección & marketing
    ## 954                                                                                                                                    Financial Analyst
    ## 955                                                                                                                          Category Manager Accesorios
    ## 956                                                                                                                                 Supply Chain Analyst
    ## 957                                                                                                    Associate Data Scientist - CoE Advanced Analytics
    ## 958                                                                                                                                  Full Stack Engineer
    ## 959                                                                                                           Head of Shopper Integrations - Central Ops
    ## 960                                                                                                                             Consultora independiente
    ## 961                                                                                                                           Data Consulting - COE Data
    ## 962                                                                                                                          Manager | Sales & Marketing
    ## 963                                                                                                              Experto Ambiental en Asesoría Jurídica 
    ## 964                                                                                                                     Marketing & Trade Specialist SR.
    ## 965                                                                                                          Brand Development Representative - High End
    ## 966                                                                                                                                         OPEN BANKING
    ## 967                                                                                                 Sales Executive | Traditional Trade - Centro Oriente
    ## 968                                                                            Business Unit Manager - Data Center, Cloud, IT Consulting & Cybersecurity
    ## 969                                                                                                                                Gerente de Desarrollo
    ## 970                                                                                                        Global Innovation & Digital Business Director
    ## 971                                                                                                                            Lead Analytics & Big Data
    ## 972                                                                                                                                      Gerente general
    ## 973                                                                                                       Coordinador de Gestión Humana y Capacitaciones
    ## 974                                                                                                                                       Administrativo
    ## 975                                                                                                                                    Profesor Invitado
    ## 976                                                                                                         Coordinadora de marca empleadora y proyectos
    ## 977                                                                                                               Líder Técnico de Business Intelligence
    ## 978                                                                     Especialista en Gestión en Salud - Oficina Ejecutiva de Planeamiento Estrategico
    ## 979                                                                                                                  Business Consultant - EMEA Services
    ## 980                                                                                                                                     Docente invitado
    ## 981                                                                                                           Senior Business Development Representative
    ## 982                                                                                                                            Docente a Tiempo Completo
    ## 983                                                                                                                              Científico investigador
    ## 984                                                                                                                                      Gerente General
    ## 985                                                                                                         Analista de Negocios y Alianzas Estratégicas
    ## 986                                                                                                                                             Launcher
    ## 987                                                                                                                                                     
    ## 988                                                                                                                          MRO Buyer Cluster South LAO
    ## 989                                                                                                                 Market Strategy and Planning Manager
    ## 990                                                                                                                        Jefe de selección de personal
    ## 991                                                                                                                                    Sales & Solutions
    ## 992                                                                                                      VP Capital Humano  y Miembro del Consejo (2022)
    ## 993                                                                                                                                   Co-founder and CEO
    ## 994                                                                                                                                              Docente
    ## 995                                                                                                                                       Senior Manager
    ## 996                                                                                                                                  Asistente comercial
    ## 997                                                                                                                           Regional Territory Manager
    ## 998                                                                                                                      Director de Operaciones y Malls
    ## 999                                                                                                                             Coordinador de logística
    ## 1000                                                                                                             Senior de Gestión del Talento y Cultura
    ## 1001                                                                                                                        BUSINESS DEVELOPMENT MANAGER
    ## 1002                                                                                                                             Social commerce Analyst
    ## 1003                                                          Hipnoterapeuta Certificado por la National Guild of Hypnotists  USA (Miami, México y Perú)
    ## 1004                                                                                                                                        Scrum Master
    ## 1005                                                                                                                        Desarrollador Web Full Stack
    ## 1006                                                                                                                                  Director Comercial
    ## 1007                                                                                                                                            Cuidador
    ## 1008                                                                                  Human Resources Senior Consultant // Talent Acquisition Specialist
    ## 1009                                                                                                                      ACCOUNT MANAGER TEST & CONTROL
    ## 1010                                                                                                                   Operations Supervisor Sales & MKT
    ## 1011                                                                                                                            Key Account Cash & Carry
    ## 1012                                                                                                                                   Analytics Analyst
    ## 1013                                                                                                                                    Co-Founder & CCO
    ## 1014                                                                                                                          Senior Logistikkoordinator
    ## 1015                                                                                                                                           Professor
    ## 1016                                                                                              Fixed Income & Equity Jr. Analyst - Latin America Team
    ## 1017                                                                                                                Senior Manager Business Intelligence
    ## 1018                                                                                                                     Business & Management Professor
    ## 1019                                                                                                                    Senior Analyst Corporate Finance
    ## 1020                                                                                                                                  Head Of Technology
    ## 1021                                                                                              Director of AI & Quantum Computing Solutions – Partner
    ## 1022                                                                                                                                                 CEO
    ## 1023                                                                                                                        Corporate Compliance Officer
    ## 1024                                                                                                                                      Data Scientist
    ## 1025                                                                                                                                 Analista de gestión
    ## 1026                                                                                                                        Product analyst Ssr Advanced
    ## 1027                                                                                                                                    Staff Consultant
    ## 1028                                                                                                                                           Economist
    ## 1029                                                                                                                                     Project Manager
    ## 1030                                                                                                             Mentor en MicroDegree en Data Analytics
    ## 1031                                                                                                                          Admistradora Comercial ACD
    ## 1032                                                                                                                            Chief Executive Director
    ## 1033                                                                                                                         Strategic Account Executive
    ## 1034                                                                                                  Associate | Structured Finance Advisory - Americas
    ## 1035                                                                                                      Jefe de Administracion y finanzas Libelula ONG
    ## 1036                                                                    Global Key Account Manager Mining and Minerals (Perú Colombia Bolivia y Surinam)
    ## 1037                                                                                                                                 Ejecutivo comercial
    ## 1038                                                                                                            Consultant & Head of Leadership Advisory
    ## 1039                                                                                                                              Analytics Tribe Leader
    ## 1040                                                                                                                                  Co-Founder and COO
    ## 1041                                                                                                                CGO- Data Science & Data Engineering
    ## 1042                                                                                                                     Sub Gerente Adjunto de Negocios
    ## 1043                                                                                                                                   Marketing Trainee
    ## 1044                                                                                                                   Analista de Información y Gestión
    ## 1045                                                                                                                                Strategy Coordinator
    ## 1046                                                                                                                                                    
    ## 1047                                                                                                                                     Director Médico
    ## 1048                                                                                                                                            Asociado
    ## 1049                                                                                                                                     Gerente General
    ## 1050                                                                                                                       Miembro de la Junta Directiva
    ## 1051                                                                                                                                         Co Founder 
    ## 1052                                                                                                                     Practicante de Recursos Humanos
    ## 1053                                                                                                                 Key Account Manager - Canal Moderno
    ## 1054                                                                                                                                      Data Scientist
    ## 1055                                                                                                                               Asesor de Post -Venta
    ## 1056                                                                                                                                  IBM Data Scientist
    ## 1057                                                                                                                              Data Scientist Senior 
    ## 1058                                                                                                                                  Profesor Principal
    ## 1059                                                                                                                             DevOps / Cloud Delivery
    ## 1060                                                                                                                                         propietaria
    ## 1061                                                                                                                                     General Manager
    ## 1062                                                                                                                            Senior Financial Analyst
    ## 1063                                                                                                                            Digital Strategy Manager
    ## 1064                                                                                                                          Consultor Junior de Crisis
    ## 1065                                                                                                           Data Scientist | Search & Personalization
    ## 1066                                                                                                                              Asistente de Ingeniero
    ## 1067                                                                                              Strategy & Planning LatAm Partner Org Business Analyst
    ## 1068                                                                                                        Business Designer - Labentana Innovation Lab
    ## 1069                                                                                                                                 Lead Data Scientist
    ## 1070                                                                                                                                Brand Growth Analyst
    ## 1071                                                                                                                                  Packaging Engineer
    ## 1072                                                                                                                 Brand Manager Senior Christian Dior
    ## 1073                                                                                                                       Category Manager - Deco Hogar
    ## 1074                                                                                                                             Consultor independiente
    ## 1075                                                                                                                     On-Site Specialist | Commercial
    ## 1076                                                                                                                                    Head of Strategy
    ## 1077                                                                                                                           Wealth Management Analyst
    ## 1078                                                                                                               Profesor de Investigación de Mercados
    ## 1079                                                                                                                Molecular Biology & Genetics Analyst
    ## 1080                                                                                                                                      Data Scientist
    ## 1081                                                                                                                   Data & Analytics Strategy Manager
    ## 1082                                                                                                                    Human Resources Business Partner
    ## 1083                                                                                                           Analista Senior de Negocios Banca Empresa
    ## 1084                                                                                                                                Commercial Executive
    ## 1085                                                                                                                             Jefe de trade marketing
    ## 1086                                                                                                                                 Recruiter of People
    ## 1087                                                                                                                          Staffing Manager Associate
    ## 1088                                                                                                                                           Associate
    ## 1089                                                                                                                                 Associate Professor
    ## 1090                                                                                                                            Digital Strategy Manager
    ## 1091                                                                                                                                Jefe de proyectos BI
    ## 1092                                                                                                                                   Co-Fundador & CEO
    ## 1093                                                                                                                   Launch Manager LATAM - Commercial
    ## 1094                                                                                                             Talent Acquisition Operations Recruiter
    ## 1095                                                                                                                                  Director de ventas
    ## 1096                                                                                                            Especialista en Inteligencia de Negocios
    ## 1097                                                                                                                             Chief Executive Officer
    ## 1098                                                                                                     Corporate Data Architecture Director at Belcorp
    ## 1099                                                                                                                                Senior Data Engineer
    ## 1100                                                                                                                                     Jefe de Bigdata
    ## 1101                                                                                                                        Product Owner E-commerce B2B
    ## 1102                                                                                                              Sr. Director Strategy & Growth - LATAM
    ## 1103                                                                                                                 Subgerente Adjunto Pricing Strategy
    ## 1104                                                                                                       Data Science Manager - Global Growth Vertical
    ## 1105                                                                                                             Supervisor Senior de Mantenimiento Mina
    ## 1106                                                                                                                                SIGM Project Analyst
    ## 1107                                                                                                                    Project Manager - Customer Focus
    ## 1108                                                                                                                                    NodeJS Developer
    ## 1109                                                                                                                                   Product Marketing
    ## 1110                                                                                                           Lead CoE Data & Corporate Data Governance
    ## 1111                                                                                                                  Senior Manager Customer Experience
    ## 1112                                                                                                                         Category Manager - Lencería
    ## 1113                                                                                                                    Analista de Analytics & Big Data
    ## 1114                                                                                                         Business Intelligence EDGE Specialist PEBAC
    ## 1115                                                                                                                                 Product Manager B2B
    ## 1116                                                                                                                    Manager of Business Intelligence
    ## 1117                                                                                                                Regional Manager in Hispanic America
    ## 1118                                                                                                                                          Consultant
    ## 1119                                                                                                                                   Design Researcher
    ## 1120                                                                                                                            Analytics Senior Manager
    ## 1121                                                                                                   Especialista de inteligencia y analítica avanzada
    ## 1122                                                                                                                             Product Lead - RappiAds
    ## 1123                                                                                                                     Lead de proyectos de innovación
    ## 1124                                                                                             Marketing Intern | Sales Operations & Events Management
    ## 1125                                                                                                                           Territory Sales Executive
    ## 1126                                                                                                                   Channel Digitalization Specialist
    ## 1127                                                                                                                   Practicante de Publicidad y Marca
    ## 1128                                                                                                                                   Gerente comercial
    ## 1129                                                                                                                          Marketing y Comunicaciones
    ## 1130                                                                                                                                             Manager
    ## 1131                                                                                                                                   Teacher Assistant
    ## 1132                                                                                                               Sub Gerente de Inteligencia Comercial
    ## 1133                                                                                                                              Data Science Architect
    ## 1134                                                                                                                           Gerente de Data Analytics
    ## 1135                                                                                                                                              Mentor
    ## 1136                                                                                                                                         KYC Analyst
    ## 1137                                                                                                                                Brand Growth Analyst
    ## 1138                                                                                                                                          Consultant
    ## 1139                                                                                                                           Global Business Developer
    ## 1140                                                                                                           Analista de Negocios - Cuentas Especiales
    ## 1141                                                                                                                                           CONSULTOR
    ## 1142                                                                                                                  Field Sales Manager - Google Cloud
    ## 1143                                                                                                                      Data & Analytics Grupo Elektra
    ## 1144                                                                                                                            Data & Analytics Manager
    ## 1145                                                                                                                       Teacher in Advanced Analytics
    ## 1146                                                                                                                                       Data Engineer
    ## 1147                                                                                                                                              Broker
    ## 1148                                                                                                                       CDO, Head of Data & Analytics
    ## 1149                                                                                                                             Ingeniero de Innovación
    ## 1150                                                                                                                                      Socio Fundador
    ## 1151                                                                                                                                           Professor
    ## 1152                                                                                                                                     Founding Writer
    ## 1153                                                                                                                            Jefe de Recursos Humanos
    ## 1154                                                                                                                  Analista de Inteligencia Comercial
    ## 1155                                                                                                                                  GERENTE COMERCIAL 
    ## 1156                                                                                            Category Manager Calzado Hombres y Zapatillas Deportivas
    ## 1157                                                                                                                                              Artist
    ## 1158                                                                                                                              Private Equity Analyst
    ## 1159                                                                                                                               CTO / Project Manager
    ## 1160                                                                                                                               Product Manager Pleno
    ## 1161                                                                                                                                      Head of Events
    ## 1162                                                                                                                               Sector Data Associate
    ## 1163                                                                                                                               Commercial Consultant
    ## 1164                                                                                                                                         Head Hunter
    ## 1165                                                                                                                                     Gerente General
    ## 1166                                                                                                                               Supervisor de cuentas
    ## 1167                                                                                                                        Sales Support Representative
    ## 1168                                                                                                                                  Analytics Engineer
    ## 1169                                                                                                                                   Cofounder and CEO
    ## 1170                                                                                                               Especialista de parámetros de riesgos
    ## 1171                                                                                                                                      Data Scientist
    ## 1172                                                                                                                               Senior Data Scientist
    ## 1173                                                                                                                                Ejecutivo de cuentas
    ## 1174                                                                                                                                Independent Director
    ## 1175                                                                                                                        Member - Peru Alumni Chapter
    ## 1176                                                                                                        Inside Sales Manager | LATAM & North America
    ## 1177                                                                                                                  Gerente COE Data & Analytics (CDO)
    ## 1178                                                                    Director Corporativo de Transformación Digital y transformación Agil en  Belcorp
    ## 1179                                                                                                          Director, Head of Digital Data & Analytics
    ## 1180                                                                                                                       Analista de Riesgo de Crédito
    ## 1181                                                                                                                                Ejecutiva de Cuentas
    ## 1182                                                                                                                               Senior Data Scientist
    ## 1183                                                                                                                                            Chairman
    ## 1184                                                                                                                                          Co-Founder
    ## 1185                                                                                                                                    Strategy Analyst
    ## 1186                                                                                                                                          Co Founder
    ## 1187                                                                                                                                 Profesor contratado
    ## 1188                                                                                          Relationship Manager- International Financial Institutions
    ## 1189                                                                                    Consulting Associate Partner - Digital and Emerging Technologies
    ## 1190                                                                                                                              React Native Developer
    ## 1191                                                                                                                             Consultor Independiente
    ## 1192                                                                                                                                          Supervisor
    ## 1193                                                                                                                                  Digital Tribe Lead
    ## 1194                                                                                                          Marketing Strategy and Data Senior Analyst
    ## 1195                                                                                                                           Centro de Emprendimiento 
    ## 1196                                                                                                                        Business Development Manager
    ## 1197                                                                                                                  Asociado Sr. Business Partner FP&A
    ## 1198                                                                                               M.S. Candidate in Integrated Marketing Communications
    ## 1199                                                                                                                           Corporate Banking Analyst
    ## 1200                                                                                                                                             Analyst
    ## 1201                                                                                                     Member of the Audit, Finance and Risk Committee
    ## 1202                                                                                                                        Product Development Engineer
    ## 1203                                                                                                                                           Associate
    ## 1204                                                                                                                                 Business Consultant
    ## 1205                                                                                                                Consultor Internacional de Educacion
    ## 1206                                                                                                              Gerente de Franquicias Internacionales
    ## 1207                                                                                                                                     Gerente general
    ## 1208                                                                                                                        Key Account Manager C-Stores
    ## 1209                                                                                         Analista de Desarrollo Organizacional - Gestión de Personas
    ## 1210                                                                                                                                         Cofundador 
    ## 1211                                                                                                                              Programador full stack
    ## 1212                                                                                                                                    Business Analyst
    ## 1213                                                                                                                                       CEO & Founder
    ## 1214                                                                                    Gral. PNP (R) con 35 años de servicio a su Institución Policial.
    ## 1215                                                                                                                                          Consultant
    ## 1216                                                                                                                           Profesora e investigadora
    ## 1217                                                                                                                                      Data Scientist
    ## 1218                                                                                                                      Director Ventures & Innovation
    ## 1219                                                                                                                                           Professor
    ## 1220                                                                                                                                                CCO 
    ## 1221                                                                                                                                 Brewing Coordinator
    ## 1222                                                                                                                     Sustainable Food Debt Assistant
    ## 1223                                                                                                               Coordinador de Inversiones y Procesos
    ## 1224                                                                                                                        Research Associate Professor
    ## 1225                                                                                                                                                    
    ## 1226                                                                                                                                     General Manager
    ## 1227                                                                                                                                    Research Analyst
    ## 1228                                                                                                                       Pediatra en Pediatras El Golf
    ## 1229                                                                                                                   Co Founder - CPO & Games Director
    ## 1230                                                                                                              Corporate & Investment Banking Analyst
    ## 1231                                                                                                                                    Co-Founder & CEO
    ## 1232                                                                                                                                 Assistant professor
    ## 1233                                                                                                                                     Project Analyst
    ## 1234                                                                                                                          Practicante VD & Marketing
    ## 1235                                                                                       Politics & Economics ADVISE Manager| ADVISE Training Director
    ## 1236                                                                                                                                       CEO & Founder
    ## 1237                                                                                                                                       Sales Manager
    ## 1238                                                                                                  Gerente de Planeamiento e Inteligencia de Negocios
    ## 1239                                                                                                                          Fundador y Gerente General
    ## 1240                                                                                                                                            Profesor
    ## 1241                                                                                                                      Executive Sales Representative
    ## 1242                                                                                                                                                 CEO
    ## 1243                                                                                                                          Strategic Sourcing Analyst
    ## 1244                                                                                                    Gerente Corporativo de Administración y Finanzas
    ## 1245                                                                                             Brand Director - Global Hair Care Disruptive Innovation
    ## 1246                                                                                                                                      Office Manager
    ## 1247                                                                                                                                     Gerente General
    ## 1248                                                                                                                            Director de voluntariado
    ## 1249                                                                                                                      Key Account Manager - C-Stores
    ## 1250                                                                                                      Corporate Affairs and Sustainability Associate
    ## 1251                                                                                                                             Venture Capital Analyst
    ## 1252                                                                                                                           Corporate Banking Analyst
    ## 1253                                                                                                                                      Data Scientist
    ## 1254                                                                                                                                           VC Fellow
    ## 1255                                                                                                                                 GTM Project Manager
    ## 1256                                                                                                                                 Key Account Manager
    ## 1257                                                                                                                          CEO & Co-founder in Katari
    ## 1258                                                                                                                          Brand Manager Fanta LATAM 
    ## 1259                                                                                                                       Desarrollador FrontEnd Expert
    ## 1260                                                                                                                Sub-Gerenta de Finanzas Corporativas
    ## 1261                                                                                                                Coordinador de Gestión de la Calidad
    ## 1262                                                                                                                                 External Consultant
    ## 1263                                                                                                                          Fundador - Gerente General
    ## 1264                                                                                                                                 Associate Professor
    ## 1265                                                                                                                                       MBA Candidate
    ## 1266                                                                                                                                                    
    ## 1267                                                                                                                 Sub Gerenta de Marketing y Producto
    ## 1268                                                                                                                                Director de Admisión
    ## 1269                                                                                                                                  Director comercial
    ## 1270                                                                                                                             Product Manager, Growth
    ## 1271                                                         Assistant Professor at ESADE, Contracted Doctoral Professor at Ramon Llull University (URL)
    ## 1272                                                                                                                 Decano de la Facultad de Ingeniería
    ## 1273                                                                                            Executive Director - Corporate & Investment Banking Perú
    ## 1274                                                                                                                                  Commercial Advisor
    ## 1275                                                                                                                            Head of Customer Success
    ## 1276                                                                                             Regional Operations Manager, Middle East and South Asia
    ## 1277                                                                                                                                     Gerente General
    ## 1278                                                                                                                                       Founder & CEO
    ## 1279                                                                                                                               Brand Manager Cristal
    ## 1280                                                                                                                                                 CEO
    ## 1281                                                                                                                                          Co-founder
    ## 1282                                                                                                                                Web UI Developer SSr
    ## 1283                                                                                                                                     General Manager
    ## 1284                                                                                                                                       CEO & FOUNDER
    ## 1285                                                                                                                                   Teacher Assistant
    ## 1286                                                                                                                       Digital Product Strategy Lead
    ## 1287                                                                                                                                                    
    ## 1288                                                                                                                                Senior Web Developer
    ##      Connected.On
    ## 1     28 Apr 2022
    ## 2     27 Apr 2022
    ## 3     22 Apr 2022
    ## 4     22 Apr 2022
    ## 5     22 Apr 2022
    ## 6     20 Apr 2022
    ## 7     01 Apr 2022
    ## 8     01 Apr 2022
    ## 9       30-Mar-22
    ## 10      18-Mar-22
    ## 11      13-Mar-22
    ## 12      10-Mar-22
    ## 13       9-Mar-22
    ## 14       9-Mar-22
    ## 15       9-Mar-22
    ## 16       9-Mar-22
    ## 17       9-Mar-22
    ## 18       9-Mar-22
    ## 19       4-Mar-22
    ## 20       4-Mar-22
    ## 21       4-Mar-22
    ## 22       3-Mar-22
    ## 23       3-Mar-22
    ## 24       2-Mar-22
    ## 25      28-Feb-22
    ## 26      25-Feb-22
    ## 27      18-Feb-22
    ## 28      18-Feb-22
    ## 29      17-Feb-22
    ## 30      16-Feb-22
    ## 31      16-Feb-22
    ## 32      16-Feb-22
    ## 33       8-Feb-22
    ## 34       1-Feb-22
    ## 35    31 Jan 2022
    ## 36    27 Jan 2022
    ## 37    21 Jan 2022
    ## 38    20 Jan 2022
    ## 39    20 Jan 2022
    ## 40    20 Jan 2022
    ## 41    19 Jan 2022
    ## 42    19 Jan 2022
    ## 43    19 Jan 2022
    ## 44    13 Jan 2022
    ## 45    13 Jan 2022
    ## 46    13 Jan 2022
    ## 47    13 Jan 2022
    ## 48    13 Jan 2022
    ## 49    06 Jan 2022
    ## 50    06 Jan 2022
    ## 51    06 Jan 2022
    ## 52    05 Jan 2022
    ## 53    04 Jan 2022
    ## 54    30 Dec 2021
    ## 55    30 Dec 2021
    ## 56    30 Dec 2021
    ## 57    29 Dec 2021
    ## 58    29 Dec 2021
    ## 59    29 Dec 2021
    ## 60    29 Dec 2021
    ## 61    29 Dec 2021
    ## 62    28 Dec 2021
    ## 63    27 Dec 2021
    ## 64    27 Dec 2021
    ## 65    27 Dec 2021
    ## 66    26 Dec 2021
    ## 67    25 Dec 2021
    ## 68    24 Dec 2021
    ## 69    24 Dec 2021
    ## 70    23 Dec 2021
    ## 71    23 Dec 2021
    ## 72    23 Dec 2021
    ## 73    23 Dec 2021
    ## 74    23 Dec 2021
    ## 75    23 Dec 2021
    ## 76    23 Dec 2021
    ## 77    23 Dec 2021
    ## 78    23 Dec 2021
    ## 79    20 Dec 2021
    ## 80    17 Dec 2021
    ## 81    16 Dec 2021
    ## 82    14 Dec 2021
    ## 83    10 Dec 2021
    ## 84    09 Dec 2021
    ## 85    09 Dec 2021
    ## 86    09 Dec 2021
    ## 87    09 Dec 2021
    ## 88    08 Dec 2021
    ## 89    08 Dec 2021
    ## 90    08 Dec 2021
    ## 91    07 Dec 2021
    ## 92    07 Dec 2021
    ## 93      29-Nov-21
    ## 94      29-Nov-21
    ## 95      29-Nov-21
    ## 96      26-Nov-21
    ## 97      25-Nov-21
    ## 98      23-Nov-21
    ## 99      19-Nov-21
    ## 100     19-Nov-21
    ## 101     19-Nov-21
    ## 102     19-Nov-21
    ## 103     19-Nov-21
    ## 104     19-Nov-21
    ## 105     19-Nov-21
    ## 106     19-Nov-21
    ## 107     16-Nov-21
    ## 108      4-Nov-21
    ## 109      4-Nov-21
    ## 110      4-Nov-21
    ## 111      4-Nov-21
    ## 112      3-Nov-21
    ## 113      3-Nov-21
    ## 114      1-Nov-21
    ## 115     30-Oct-21
    ## 116     29-Oct-21
    ## 117     29-Oct-21
    ## 118     29-Oct-21
    ## 119     29-Oct-21
    ## 120     28-Oct-21
    ## 121     28-Oct-21
    ## 122     28-Oct-21
    ## 123     28-Oct-21
    ## 124     28-Oct-21
    ## 125     28-Oct-21
    ## 126     28-Oct-21
    ## 127     27-Oct-21
    ## 128     27-Oct-21
    ## 129     27-Oct-21
    ## 130     27-Oct-21
    ## 131     27-Oct-21
    ## 132     26-Oct-21
    ## 133     25-Oct-21
    ## 134     24-Oct-21
    ## 135     24-Oct-21
    ## 136     24-Oct-21
    ## 137     21-Oct-21
    ## 138     18-Oct-21
    ## 139     18-Oct-21
    ## 140     18-Oct-21
    ## 141     18-Oct-21
    ## 142     18-Oct-21
    ## 143     14-Oct-21
    ## 144     14-Oct-21
    ## 145     14-Oct-21
    ## 146     13-Oct-21
    ## 147     12-Oct-21
    ## 148     12-Oct-21
    ## 149     12-Oct-21
    ## 150     12-Oct-21
    ## 151     12-Oct-21
    ## 152     12-Oct-21
    ## 153     12-Oct-21
    ## 154     11-Oct-21
    ## 155     11-Oct-21
    ## 156     11-Oct-21
    ## 157     11-Oct-21
    ## 158     11-Oct-21
    ## 159     11-Oct-21
    ## 160     11-Oct-21
    ## 161     11-Oct-21
    ## 162     11-Oct-21
    ## 163      9-Oct-21
    ## 164      8-Oct-21
    ## 165      7-Oct-21
    ## 166      7-Oct-21
    ## 167      6-Oct-21
    ## 168      6-Oct-21
    ## 169      6-Oct-21
    ## 170      6-Oct-21
    ## 171      1-Oct-21
    ## 172   30 Sep 2021
    ## 173   29 Sep 2021
    ## 174   28 Sep 2021
    ## 175   26 Sep 2021
    ## 176   24 Sep 2021
    ## 177   24 Sep 2021
    ## 178   24 Sep 2021
    ## 179   23 Sep 2021
    ## 180   23 Sep 2021
    ## 181   21 Sep 2021
    ## 182   21 Sep 2021
    ## 183   20 Sep 2021
    ## 184   16 Sep 2021
    ## 185   16 Sep 2021
    ## 186   15 Sep 2021
    ## 187   15 Sep 2021
    ## 188   13 Sep 2021
    ## 189   13 Sep 2021
    ## 190   13 Sep 2021
    ## 191   13 Sep 2021
    ## 192   13 Sep 2021
    ## 193   13 Sep 2021
    ## 194   13 Sep 2021
    ## 195   13 Sep 2021
    ## 196   11 Sep 2021
    ## 197   11 Sep 2021
    ## 198   10 Sep 2021
    ## 199   10 Sep 2021
    ## 200   09 Sep 2021
    ## 201   09 Sep 2021
    ## 202   09 Sep 2021
    ## 203   09 Sep 2021
    ## 204   09 Sep 2021
    ## 205   09 Sep 2021
    ## 206   09 Sep 2021
    ## 207   09 Sep 2021
    ## 208   09 Sep 2021
    ## 209   09 Sep 2021
    ## 210   09 Sep 2021
    ## 211   09 Sep 2021
    ## 212   09 Sep 2021
    ## 213   09 Sep 2021
    ## 214   09 Sep 2021
    ## 215   09 Sep 2021
    ## 216   09 Sep 2021
    ## 217   09 Sep 2021
    ## 218   09 Sep 2021
    ## 219   09 Sep 2021
    ## 220   09 Sep 2021
    ## 221   09 Sep 2021
    ## 222   09 Sep 2021
    ## 223   09 Sep 2021
    ## 224   09 Sep 2021
    ## 225   04 Sep 2021
    ## 226   03 Sep 2021
    ## 227   03 Sep 2021
    ## 228   02 Sep 2021
    ## 229   31 Aug 2021
    ## 230   27 Aug 2021
    ## 231   27 Aug 2021
    ## 232   27 Aug 2021
    ## 233   25 Aug 2021
    ## 234   25 Aug 2021
    ## 235   25 Aug 2021
    ## 236   24 Aug 2021
    ## 237   23 Aug 2021
    ## 238   23 Aug 2021
    ## 239   23 Aug 2021
    ## 240   21 Aug 2021
    ## 241   21 Aug 2021
    ## 242   21 Aug 2021
    ## 243   21 Aug 2021
    ## 244   21 Aug 2021
    ## 245   21 Aug 2021
    ## 246   17 Aug 2021
    ## 247   15 Aug 2021
    ## 248   15 Aug 2021
    ## 249   15 Aug 2021
    ## 250   15 Aug 2021
    ## 251   12 Aug 2021
    ## 252   10 Aug 2021
    ## 253   10 Aug 2021
    ## 254   10 Aug 2021
    ## 255   09 Aug 2021
    ## 256   08 Aug 2021
    ## 257   06 Aug 2021
    ## 258   06 Aug 2021
    ## 259   06 Aug 2021
    ## 260   06 Aug 2021
    ## 261   06 Aug 2021
    ## 262   04 Aug 2021
    ## 263   04 Aug 2021
    ## 264   04 Aug 2021
    ## 265   04 Aug 2021
    ## 266   04 Aug 2021
    ## 267   03 Aug 2021
    ## 268   03 Aug 2021
    ## 269   02 Aug 2021
    ## 270   01 Aug 2021
    ## 271     31-Jul-21
    ## 272     31-Jul-21
    ## 273     31-Jul-21
    ## 274     31-Jul-21
    ## 275     31-Jul-21
    ## 276     30-Jul-21
    ## 277     30-Jul-21
    ## 278     27-Jul-21
    ## 279     23-Jul-21
    ## 280     21-Jul-21
    ## 281     18-Jul-21
    ## 282     12-Jul-21
    ## 283     11-Jul-21
    ## 284      8-Jul-21
    ## 285      7-Jul-21
    ## 286     29-Jun-21
    ## 287     26-Jun-21
    ## 288     25-Jun-21
    ## 289     23-Jun-21
    ## 290     22-Jun-21
    ## 291     17-Jun-21
    ## 292     15-Jun-21
    ## 293     15-Jun-21
    ## 294     15-Jun-21
    ## 295     15-Jun-21
    ## 296     15-Jun-21
    ## 297     15-Jun-21
    ## 298     15-Jun-21
    ## 299     15-Jun-21
    ## 300     15-Jun-21
    ## 301     15-Jun-21
    ## 302     15-Jun-21
    ## 303     15-Jun-21
    ## 304     15-Jun-21
    ## 305     15-Jun-21
    ## 306     15-Jun-21
    ## 307     15-Jun-21
    ## 308     15-Jun-21
    ## 309     15-Jun-21
    ## 310     15-Jun-21
    ## 311     19-May-21
    ## 312     19-May-21
    ## 313     12-May-21
    ## 314     10-May-21
    ## 315      4-May-21
    ## 316      3-May-21
    ## 317      1-May-21
    ## 318      1-May-21
    ## 319   29 Apr 2021
    ## 320   24 Apr 2021
    ## 321   16 Apr 2021
    ## 322   16 Apr 2021
    ## 323   16 Apr 2021
    ## 324   15 Apr 2021
    ## 325   15 Apr 2021
    ## 326   15 Apr 2021
    ## 327   10 Apr 2021
    ## 328     31-Mar-21
    ## 329     30-Mar-21
    ## 330     30-Mar-21
    ## 331     30-Mar-21
    ## 332     26-Mar-21
    ## 333     26-Mar-21
    ## 334     25-Mar-21
    ## 335     18-Mar-21
    ## 336     17-Mar-21
    ## 337     17-Mar-21
    ## 338     16-Mar-21
    ## 339     12-Mar-21
    ## 340      7-Mar-21
    ## 341      5-Mar-21
    ## 342      5-Mar-21
    ## 343      5-Mar-21
    ## 344      5-Mar-21
    ## 345      5-Mar-21
    ## 346      5-Mar-21
    ## 347      5-Mar-21
    ## 348      5-Mar-21
    ## 349     25-Feb-21
    ## 350     25-Feb-21
    ## 351     20-Feb-21
    ## 352     18-Feb-21
    ## 353     18-Feb-21
    ## 354     18-Feb-21
    ## 355     10-Feb-21
    ## 356     10-Feb-21
    ## 357      5-Feb-21
    ## 358      5-Feb-21
    ## 359      2-Feb-21
    ## 360   31 Jan 2021
    ## 361   28 Jan 2021
    ## 362   21 Jan 2021
    ## 363   21 Jan 2021
    ## 364   19 Jan 2021
    ## 365   17 Jan 2021
    ## 366   17 Jan 2021
    ## 367   17 Jan 2021
    ## 368   14 Jan 2021
    ## 369   14 Jan 2021
    ## 370   09 Jan 2021
    ## 371   04 Jan 2021
    ## 372   31 Dec 2020
    ## 373   29 Dec 2020
    ## 374   23 Dec 2020
    ## 375   23 Dec 2020
    ## 376   20 Dec 2020
    ## 377   16 Dec 2020
    ## 378   14 Dec 2020
    ## 379   05 Dec 2020
    ## 380   01 Dec 2020
    ## 381     27-Nov-20
    ## 382     27-Nov-20
    ## 383     27-Nov-20
    ## 384     24-Nov-20
    ## 385     19-Nov-20
    ## 386     19-Nov-20
    ## 387     16-Nov-20
    ## 388     10-Nov-20
    ## 389      9-Nov-20
    ## 390      7-Nov-20
    ## 391      6-Nov-20
    ## 392      5-Nov-20
    ## 393      4-Nov-20
    ## 394      3-Nov-20
    ## 395      2-Nov-20
    ## 396      2-Nov-20
    ## 397      2-Nov-20
    ## 398     30-Oct-20
    ## 399     29-Oct-20
    ## 400     28-Oct-20
    ## 401     27-Oct-20
    ## 402     23-Oct-20
    ## 403     20-Oct-20
    ## 404     16-Oct-20
    ## 405     16-Oct-20
    ## 406     15-Oct-20
    ## 407     14-Oct-20
    ## 408     14-Oct-20
    ## 409     14-Oct-20
    ## 410     14-Oct-20
    ## 411     11-Oct-20
    ## 412      7-Oct-20
    ## 413      6-Oct-20
    ## 414      5-Oct-20
    ## 415      4-Oct-20
    ## 416      1-Oct-20
    ## 417      1-Oct-20
    ## 418   29 Sep 2020
    ## 419   28 Sep 2020
    ## 420   25 Sep 2020
    ## 421   17 Sep 2020
    ## 422   17 Sep 2020
    ## 423   16 Sep 2020
    ## 424   16 Sep 2020
    ## 425   15 Sep 2020
    ## 426   15 Sep 2020
    ## 427   14 Sep 2020
    ## 428   14 Sep 2020
    ## 429   14 Sep 2020
    ## 430   12 Sep 2020
    ## 431   12 Sep 2020
    ## 432   11 Sep 2020
    ## 433   11 Sep 2020
    ## 434   11 Sep 2020
    ## 435   10 Sep 2020
    ## 436   09 Sep 2020
    ## 437   09 Sep 2020
    ## 438   09 Sep 2020
    ## 439   09 Sep 2020
    ## 440   09 Sep 2020
    ## 441   07 Sep 2020
    ## 442   07 Sep 2020
    ## 443   05 Sep 2020
    ## 444   04 Sep 2020
    ## 445   04 Sep 2020
    ## 446   04 Sep 2020
    ## 447   04 Sep 2020
    ## 448   04 Sep 2020
    ## 449   04 Sep 2020
    ## 450   03 Sep 2020
    ## 451   02 Sep 2020
    ## 452   02 Sep 2020
    ## 453   02 Sep 2020
    ## 454   02 Sep 2020
    ## 455   02 Sep 2020
    ## 456   01 Sep 2020
    ## 457   01 Sep 2020
    ## 458   01 Sep 2020
    ## 459   31 Aug 2020
    ## 460   28 Aug 2020
    ## 461   28 Aug 2020
    ## 462   28 Aug 2020
    ## 463   27 Aug 2020
    ## 464   27 Aug 2020
    ## 465   25 Aug 2020
    ## 466   25 Aug 2020
    ## 467   25 Aug 2020
    ## 468   24 Aug 2020
    ## 469   24 Aug 2020
    ## 470   24 Aug 2020
    ## 471   24 Aug 2020
    ## 472   24 Aug 2020
    ## 473   24 Aug 2020
    ## 474   24 Aug 2020
    ## 475   24 Aug 2020
    ## 476   24 Aug 2020
    ## 477   24 Aug 2020
    ## 478   24 Aug 2020
    ## 479   24 Aug 2020
    ## 480   24 Aug 2020
    ## 481   24 Aug 2020
    ## 482   24 Aug 2020
    ## 483   24 Aug 2020
    ## 484   20 Aug 2020
    ## 485   19 Aug 2020
    ## 486   18 Aug 2020
    ## 487   18 Aug 2020
    ## 488   17 Aug 2020
    ## 489   15 Aug 2020
    ## 490   11 Aug 2020
    ## 491   11 Aug 2020
    ## 492   11 Aug 2020
    ## 493   08 Aug 2020
    ## 494   08 Aug 2020
    ## 495   05 Aug 2020
    ## 496   05 Aug 2020
    ## 497   01 Aug 2020
    ## 498     30-Jul-20
    ## 499     30-Jul-20
    ## 500     30-Jul-20
    ## 501     25-Jul-20
    ## 502     25-Jul-20
    ## 503     24-Jul-20
    ## 504     23-Jul-20
    ## 505     23-Jul-20
    ## 506     23-Jul-20
    ## 507     23-Jul-20
    ## 508     22-Jul-20
    ## 509     22-Jul-20
    ## 510     22-Jul-20
    ## 511     22-Jul-20
    ## 512     21-Jul-20
    ## 513     21-Jul-20
    ## 514     21-Jul-20
    ## 515     20-Jul-20
    ## 516     20-Jul-20
    ## 517     17-Jul-20
    ## 518     16-Jul-20
    ## 519     16-Jul-20
    ## 520     15-Jul-20
    ## 521     15-Jul-20
    ## 522     15-Jul-20
    ## 523     15-Jul-20
    ## 524      3-Jul-20
    ## 525      3-Jul-20
    ## 526      2-Jul-20
    ## 527      2-Jul-20
    ## 528      1-Jul-20
    ## 529     30-Jun-20
    ## 530     30-Jun-20
    ## 531     29-Jun-20
    ## 532     27-Jun-20
    ## 533     25-Jun-20
    ## 534     24-Jun-20
    ## 535     22-Jun-20
    ## 536     22-Jun-20
    ## 537     15-Jun-20
    ## 538     14-Jun-20
    ## 539     14-Jun-20
    ## 540     13-Jun-20
    ## 541     11-Jun-20
    ## 542     11-Jun-20
    ## 543     10-Jun-20
    ## 544     10-Jun-20
    ## 545      8-Jun-20
    ## 546      8-Jun-20
    ## 547      8-Jun-20
    ## 548      5-Jun-20
    ## 549      3-Jun-20
    ## 550     31-May-20
    ## 551     31-May-20
    ## 552     30-May-20
    ## 553     29-May-20
    ## 554     27-May-20
    ## 555     27-May-20
    ## 556     26-May-20
    ## 557     24-May-20
    ## 558     24-May-20
    ## 559     24-May-20
    ## 560     24-May-20
    ## 561     24-May-20
    ## 562     24-May-20
    ## 563     24-May-20
    ## 564     24-May-20
    ## 565     24-May-20
    ## 566     24-May-20
    ## 567     24-May-20
    ## 568     24-May-20
    ## 569     24-May-20
    ## 570     16-May-20
    ## 571     15-May-20
    ## 572     15-May-20
    ## 573     15-May-20
    ## 574     12-May-20
    ## 575     12-May-20
    ## 576     11-May-20
    ## 577      9-May-20
    ## 578      8-May-20
    ## 579      4-May-20
    ## 580   27 Apr 2020
    ## 581   27 Apr 2020
    ## 582   23 Apr 2020
    ## 583   22 Apr 2020
    ## 584   22 Apr 2020
    ## 585   22 Apr 2020
    ## 586   16 Apr 2020
    ## 587   15 Apr 2020
    ## 588   15 Apr 2020
    ## 589   15 Apr 2020
    ## 590   15 Apr 2020
    ## 591   14 Apr 2020
    ## 592   14 Apr 2020
    ## 593   13 Apr 2020
    ## 594   13 Apr 2020
    ## 595   13 Apr 2020
    ## 596   11 Apr 2020
    ## 597   06 Apr 2020
    ## 598   06 Apr 2020
    ## 599   06 Apr 2020
    ## 600   05 Apr 2020
    ## 601   03 Apr 2020
    ## 602   02 Apr 2020
    ## 603   02 Apr 2020
    ## 604   01 Apr 2020
    ## 605   01 Apr 2020
    ## 606   01 Apr 2020
    ## 607     31-Mar-20
    ## 608     31-Mar-20
    ## 609     31-Mar-20
    ## 610     31-Mar-20
    ## 611     31-Mar-20
    ## 612     31-Mar-20
    ## 613     31-Mar-20
    ## 614     31-Mar-20
    ## 615     31-Mar-20
    ## 616     31-Mar-20
    ## 617     31-Mar-20
    ## 618     29-Mar-20
    ## 619     28-Mar-20
    ## 620     28-Mar-20
    ## 621     28-Mar-20
    ## 622     27-Mar-20
    ## 623     20-Mar-20
    ## 624      3-Mar-20
    ## 625      3-Mar-20
    ## 626      3-Mar-20
    ## 627     27-Feb-20
    ## 628     27-Feb-20
    ## 629     26-Feb-20
    ## 630     24-Feb-20
    ## 631     21-Feb-20
    ## 632     20-Feb-20
    ## 633     11-Feb-20
    ## 634     11-Feb-20
    ## 635      6-Feb-20
    ## 636      6-Feb-20
    ## 637      5-Feb-20
    ## 638      5-Feb-20
    ## 639      5-Feb-20
    ## 640      5-Feb-20
    ## 641      5-Feb-20
    ## 642      4-Feb-20
    ## 643      4-Feb-20
    ## 644      4-Feb-20
    ## 645      4-Feb-20
    ## 646   31 Jan 2020
    ## 647   31 Jan 2020
    ## 648   30 Jan 2020
    ## 649   28 Jan 2020
    ## 650   28 Jan 2020
    ## 651   22 Jan 2020
    ## 652   22 Jan 2020
    ## 653   22 Jan 2020
    ## 654   22 Jan 2020
    ## 655   22 Jan 2020
    ## 656   22 Jan 2020
    ## 657   21 Jan 2020
    ## 658   21 Jan 2020
    ## 659   21 Jan 2020
    ## 660   21 Jan 2020
    ## 661   17 Jan 2020
    ## 662   15 Jan 2020
    ## 663   14 Jan 2020
    ## 664   14 Jan 2020
    ## 665   10 Jan 2020
    ## 666   10 Jan 2020
    ## 667   10 Jan 2020
    ## 668   07 Jan 2020
    ## 669   07 Jan 2020
    ## 670   04 Jan 2020
    ## 671   01 Jan 2020
    ## 672   19 Dec 2019
    ## 673   12 Dec 2019
    ## 674   11 Dec 2019
    ## 675   10 Dec 2019
    ## 676   10 Dec 2019
    ## 677   09 Dec 2019
    ## 678   08 Dec 2019
    ## 679   06 Dec 2019
    ## 680   01 Dec 2019
    ## 681     29-Nov-19
    ## 682     28-Nov-19
    ## 683     28-Nov-19
    ## 684     27-Nov-19
    ## 685     27-Nov-19
    ## 686     26-Nov-19
    ## 687     25-Nov-19
    ## 688     25-Nov-19
    ## 689     20-Nov-19
    ## 690     20-Nov-19
    ## 691     19-Nov-19
    ## 692     18-Nov-19
    ## 693     18-Nov-19
    ## 694     16-Nov-19
    ## 695     14-Nov-19
    ## 696     14-Nov-19
    ## 697     13-Nov-19
    ## 698     12-Nov-19
    ## 699     11-Nov-19
    ## 700     10-Nov-19
    ## 701     10-Nov-19
    ## 702     10-Nov-19
    ## 703      8-Nov-19
    ## 704      6-Nov-19
    ## 705      5-Nov-19
    ## 706      4-Nov-19
    ## 707      4-Nov-19
    ## 708      2-Nov-19
    ## 709      1-Nov-19
    ## 710     28-Oct-19
    ## 711     26-Oct-19
    ## 712     26-Oct-19
    ## 713     25-Oct-19
    ## 714     24-Oct-19
    ## 715     24-Oct-19
    ## 716     24-Oct-19
    ## 717     23-Oct-19
    ## 718     22-Oct-19
    ## 719     22-Oct-19
    ## 720     22-Oct-19
    ## 721     21-Oct-19
    ## 722     19-Oct-19
    ## 723     19-Oct-19
    ## 724     19-Oct-19
    ## 725     19-Oct-19
    ## 726     17-Oct-19
    ## 727     15-Oct-19
    ## 728     15-Oct-19
    ## 729     14-Oct-19
    ## 730      7-Oct-19
    ## 731      5-Oct-19
    ## 732      3-Oct-19
    ## 733      3-Oct-19
    ## 734      3-Oct-19
    ## 735      3-Oct-19
    ## 736      3-Oct-19
    ## 737      3-Oct-19
    ## 738      2-Oct-19
    ## 739   28 Sep 2019
    ## 740   27 Sep 2019
    ## 741   27 Sep 2019
    ## 742   27 Sep 2019
    ## 743   27 Sep 2019
    ## 744   27 Sep 2019
    ## 745   27 Sep 2019
    ## 746   27 Sep 2019
    ## 747   27 Sep 2019
    ## 748   27 Sep 2019
    ## 749   27 Sep 2019
    ## 750   27 Sep 2019
    ## 751   27 Sep 2019
    ## 752   27 Sep 2019
    ## 753   27 Sep 2019
    ## 754   27 Sep 2019
    ## 755   25 Sep 2019
    ## 756   21 Sep 2019
    ## 757   20 Sep 2019
    ## 758   19 Sep 2019
    ## 759   18 Sep 2019
    ## 760   15 Sep 2019
    ## 761   15 Sep 2019
    ## 762   13 Sep 2019
    ## 763   13 Sep 2019
    ## 764   12 Sep 2019
    ## 765   12 Sep 2019
    ## 766   12 Sep 2019
    ## 767   12 Sep 2019
    ## 768   12 Sep 2019
    ## 769   12 Sep 2019
    ## 770   11 Sep 2019
    ## 771   10 Sep 2019
    ## 772   10 Sep 2019
    ## 773   09 Sep 2019
    ## 774   09 Sep 2019
    ## 775   09 Sep 2019
    ## 776   09 Sep 2019
    ## 777   09 Sep 2019
    ## 778   09 Sep 2019
    ## 779   06 Sep 2019
    ## 780   05 Sep 2019
    ## 781   05 Sep 2019
    ## 782   04 Sep 2019
    ## 783   04 Sep 2019
    ## 784   04 Sep 2019
    ## 785   04 Sep 2019
    ## 786   04 Sep 2019
    ## 787   02 Sep 2019
    ## 788   01 Sep 2019
    ## 789   01 Sep 2019
    ## 790   01 Sep 2019
    ## 791   30 Aug 2019
    ## 792   29 Aug 2019
    ## 793   28 Aug 2019
    ## 794   27 Aug 2019
    ## 795   26 Aug 2019
    ## 796   24 Aug 2019
    ## 797   23 Aug 2019
    ## 798   23 Aug 2019
    ## 799   23 Aug 2019
    ## 800   23 Aug 2019
    ## 801   23 Aug 2019
    ## 802   23 Aug 2019
    ## 803   23 Aug 2019
    ## 804   23 Aug 2019
    ## 805   23 Aug 2019
    ## 806   23 Aug 2019
    ## 807   22 Aug 2019
    ## 808   22 Aug 2019
    ## 809   22 Aug 2019
    ## 810   22 Aug 2019
    ## 811   22 Aug 2019
    ## 812   22 Aug 2019
    ## 813   22 Aug 2019
    ## 814   09 Aug 2019
    ## 815   08 Aug 2019
    ## 816   08 Aug 2019
    ## 817   05 Aug 2019
    ## 818   05 Aug 2019
    ## 819   04 Aug 2019
    ## 820   04 Aug 2019
    ## 821   04 Aug 2019
    ## 822   02 Aug 2019
    ## 823   01 Aug 2019
    ## 824   01 Aug 2019
    ## 825   01 Aug 2019
    ## 826   01 Aug 2019
    ## 827     30-Jul-19
    ## 828     30-Jul-19
    ## 829     28-Jul-19
    ## 830     26-Jul-19
    ## 831     25-Jul-19
    ## 832     25-Jul-19
    ## 833     25-Jul-19
    ## 834     24-Jul-19
    ## 835     23-Jul-19
    ## 836     22-Jul-19
    ## 837     22-Jul-19
    ## 838     22-Jul-19
    ## 839     22-Jul-19
    ## 840     16-Jul-19
    ## 841     16-Jul-19
    ## 842     16-Jul-19
    ## 843     14-Jul-19
    ## 844     13-Jul-19
    ## 845     13-Jul-19
    ## 846     13-Jul-19
    ## 847     10-Jul-19
    ## 848      9-Jul-19
    ## 849      8-Jul-19
    ## 850      8-Jul-19
    ## 851      8-Jul-19
    ## 852      8-Jul-19
    ## 853      8-Jul-19
    ## 854      8-Jul-19
    ## 855      4-Jul-19
    ## 856     27-Jun-19
    ## 857     26-Jun-19
    ## 858     26-Jun-19
    ## 859     26-Jun-19
    ## 860     20-Jun-19
    ## 861     20-Jun-19
    ## 862     20-Jun-19
    ## 863     20-Jun-19
    ## 864     20-Jun-19
    ## 865     29-May-19
    ## 866     29-May-19
    ## 867     29-May-19
    ## 868     29-May-19
    ## 869     22-May-19
    ## 870     21-May-19
    ## 871      3-May-19
    ## 872     29-Mar-19
    ## 873     29-Mar-19
    ## 874     29-Mar-19
    ## 875      1-Mar-19
    ## 876      1-Mar-19
    ## 877     28-Feb-19
    ## 878     26-Feb-19
    ## 879     26-Feb-19
    ## 880     14-Feb-19
    ## 881     13-Feb-19
    ## 882     13-Feb-19
    ## 883      5-Feb-19
    ## 884      5-Feb-19
    ## 885      4-Feb-19
    ## 886   30 Jan 2019
    ## 887   17 Jan 2019
    ## 888   16 Jan 2019
    ## 889   14 Jan 2019
    ## 890   14 Jan 2019
    ## 891   14 Jan 2019
    ## 892   03 Jan 2019
    ## 893   03 Jan 2019
    ## 894   27 Dec 2018
    ## 895   26 Dec 2018
    ## 896   26 Dec 2018
    ## 897   19 Dec 2018
    ## 898   19 Dec 2018
    ## 899   19 Dec 2018
    ## 900   14 Dec 2018
    ## 901   13 Dec 2018
    ## 902   13 Dec 2018
    ## 903   07 Dec 2018
    ## 904   07 Dec 2018
    ## 905   07 Dec 2018
    ## 906   07 Dec 2018
    ## 907   07 Dec 2018
    ## 908     30-Nov-18
    ## 909     29-Nov-18
    ## 910     26-Nov-18
    ## 911     26-Nov-18
    ## 912     25-Nov-18
    ## 913     24-Nov-18
    ## 914     24-Nov-18
    ## 915     23-Nov-18
    ## 916     23-Nov-18
    ## 917     23-Nov-18
    ## 918     23-Nov-18
    ## 919     19-Nov-18
    ## 920     16-Nov-18
    ## 921     13-Nov-18
    ## 922     13-Nov-18
    ## 923     12-Nov-18
    ## 924     12-Nov-18
    ## 925     12-Nov-18
    ## 926     12-Nov-18
    ## 927     10-Nov-18
    ## 928     10-Nov-18
    ## 929     10-Nov-18
    ## 930     10-Nov-18
    ## 931     10-Nov-18
    ## 932     10-Nov-18
    ## 933     10-Nov-18
    ## 934     10-Nov-18
    ## 935     10-Nov-18
    ## 936      9-Nov-18
    ## 937      9-Nov-18
    ## 938      8-Nov-18
    ## 939      8-Nov-18
    ## 940      8-Nov-18
    ## 941      8-Nov-18
    ## 942      7-Nov-18
    ## 943      7-Nov-18
    ## 944      7-Nov-18
    ## 945      7-Nov-18
    ## 946      7-Nov-18
    ## 947      5-Nov-18
    ## 948     30-Oct-18
    ## 949     30-Oct-18
    ## 950     30-Oct-18
    ## 951     30-Oct-18
    ## 952     22-Oct-18
    ## 953     22-Oct-18
    ## 954     22-Oct-18
    ## 955     19-Oct-18
    ## 956     17-Oct-18
    ## 957     17-Oct-18
    ## 958     15-Oct-18
    ## 959      7-Oct-18
    ## 960      7-Oct-18
    ## 961      4-Oct-18
    ## 962      4-Oct-18
    ## 963      4-Oct-18
    ## 964      4-Oct-18
    ## 965      4-Oct-18
    ## 966      4-Oct-18
    ## 967      2-Oct-18
    ## 968   29 Sep 2018
    ## 969   29 Sep 2018
    ## 970   29 Sep 2018
    ## 971   29 Sep 2018
    ## 972   29 Sep 2018
    ## 973   29 Sep 2018
    ## 974   29 Sep 2018
    ## 975   29 Sep 2018
    ## 976   29 Sep 2018
    ## 977   29 Sep 2018
    ## 978   29 Sep 2018
    ## 979   29 Sep 2018
    ## 980   29 Sep 2018
    ## 981   29 Sep 2018
    ## 982   29 Sep 2018
    ## 983   29 Sep 2018
    ## 984   29 Sep 2018
    ## 985   29 Sep 2018
    ## 986   29 Sep 2018
    ## 987   29 Sep 2018
    ## 988   29 Sep 2018
    ## 989   29 Sep 2018
    ## 990   29 Sep 2018
    ## 991   29 Sep 2018
    ## 992   29 Sep 2018
    ## 993   29 Sep 2018
    ## 994   29 Sep 2018
    ## 995   29 Sep 2018
    ## 996   29 Sep 2018
    ## 997   29 Sep 2018
    ## 998   29 Sep 2018
    ## 999   29 Sep 2018
    ## 1000  29 Sep 2018
    ## 1001  29 Sep 2018
    ## 1002  29 Sep 2018
    ## 1003  29 Sep 2018
    ## 1004  29 Sep 2018
    ## 1005  29 Sep 2018
    ## 1006  29 Sep 2018
    ## 1007  29 Sep 2018
    ## 1008  29 Sep 2018
    ## 1009  29 Sep 2018
    ## 1010  29 Sep 2018
    ## 1011  29 Sep 2018
    ## 1012  29 Sep 2018
    ## 1013  29 Sep 2018
    ## 1014  29 Sep 2018
    ## 1015  29 Sep 2018
    ## 1016  29 Sep 2018
    ## 1017  16 Sep 2018
    ## 1018  15 Sep 2018
    ## 1019  15 Sep 2018
    ## 1020  15 Sep 2018
    ## 1021  08 Sep 2018
    ## 1022  08 Sep 2018
    ## 1023  08 Sep 2018
    ## 1024  08 Sep 2018
    ## 1025  08 Sep 2018
    ## 1026  08 Sep 2018
    ## 1027  08 Sep 2018
    ## 1028  08 Sep 2018
    ## 1029  08 Sep 2018
    ## 1030  08 Sep 2018
    ## 1031  29 Aug 2018
    ## 1032  29 Aug 2018
    ## 1033  29 Aug 2018
    ## 1034  29 Aug 2018
    ## 1035  29 Aug 2018
    ## 1036  29 Aug 2018
    ## 1037  29 Aug 2018
    ## 1038  22 Aug 2018
    ## 1039  14 Aug 2018
    ## 1040  14 Aug 2018
    ## 1041  10 Aug 2018
    ## 1042  08 Aug 2018
    ## 1043  08 Aug 2018
    ## 1044  08 Aug 2018
    ## 1045  08 Aug 2018
    ## 1046  08 Aug 2018
    ## 1047    23-Jul-18
    ## 1048    23-Jul-18
    ## 1049    23-Jul-18
    ## 1050    23-Jul-18
    ## 1051    23-Jul-18
    ## 1052    23-Jul-18
    ## 1053    23-Jul-18
    ## 1054    23-Jul-18
    ## 1055     8-Jul-18
    ## 1056     8-Jul-18
    ## 1057     8-Jul-18
    ## 1058     3-Jul-18
    ## 1059     2-Jul-18
    ## 1060     2-Jul-18
    ## 1061     2-Jul-18
    ## 1062     2-Jul-18
    ## 1063    25-Jun-18
    ## 1064    18-Jun-18
    ## 1065    15-Jun-18
    ## 1066    14-Jun-18
    ## 1067    14-Jun-18
    ## 1068     1-Jun-18
    ## 1069     1-Jun-18
    ## 1070     1-Jun-18
    ## 1071    31-May-18
    ## 1072    31-May-18
    ## 1073    31-May-18
    ## 1074    31-May-18
    ## 1075    31-May-18
    ## 1076    31-May-18
    ## 1077    28-May-18
    ## 1078    23-May-18
    ## 1079    23-May-18
    ## 1080    18-May-18
    ## 1081    18-May-18
    ## 1082    14-May-18
    ## 1083    14-May-18
    ## 1084    14-May-18
    ## 1085    14-May-18
    ## 1086    14-May-18
    ## 1087    14-May-18
    ## 1088    14-May-18
    ## 1089    10-May-18
    ## 1090    10-May-18
    ## 1091     7-May-18
    ## 1092     7-May-18
    ## 1093     5-May-18
    ## 1094     3-May-18
    ## 1095     3-May-18
    ## 1096     1-May-18
    ## 1097     1-May-18
    ## 1098  30 Apr 2018
    ## 1099  30 Apr 2018
    ## 1100  30 Apr 2018
    ## 1101  30 Apr 2018
    ## 1102  30 Apr 2018
    ## 1103  30 Apr 2018
    ## 1104  30 Apr 2018
    ## 1105  27 Apr 2018
    ## 1106  27 Apr 2018
    ## 1107  27 Apr 2018
    ## 1108  26 Apr 2018
    ## 1109  26 Apr 2018
    ## 1110  26 Apr 2018
    ## 1111  26 Apr 2018
    ## 1112  26 Apr 2018
    ## 1113  25 Apr 2018
    ## 1114  25 Apr 2018
    ## 1115  25 Apr 2018
    ## 1116  25 Apr 2018
    ## 1117  25 Apr 2018
    ## 1118  25 Apr 2018
    ## 1119  25 Apr 2018
    ## 1120  24 Apr 2018
    ## 1121  24 Apr 2018
    ## 1122  24 Apr 2018
    ## 1123  24 Apr 2018
    ## 1124  19 Apr 2018
    ## 1125  17 Apr 2018
    ## 1126  17 Apr 2018
    ## 1127  12 Apr 2018
    ## 1128  03 Apr 2018
    ## 1129  03 Apr 2018
    ## 1130  03 Apr 2018
    ## 1131    28-Mar-18
    ## 1132    26-Mar-18
    ## 1133    26-Mar-18
    ## 1134    26-Mar-18
    ## 1135    26-Mar-18
    ## 1136    26-Mar-18
    ## 1137    19-Mar-18
    ## 1138    15-Mar-18
    ## 1139    14-Mar-18
    ## 1140    13-Mar-18
    ## 1141     7-Mar-18
    ## 1142     6-Mar-18
    ## 1143     6-Mar-18
    ## 1144     5-Mar-18
    ## 1145     2-Mar-18
    ## 1146     2-Mar-18
    ## 1147    28-Feb-18
    ## 1148    27-Feb-18
    ## 1149    20-Feb-18
    ## 1150    18-Feb-18
    ## 1151    16-Feb-18
    ## 1152    13-Feb-18
    ## 1153    13-Feb-18
    ## 1154     8-Feb-18
    ## 1155     8-Feb-18
    ## 1156     8-Feb-18
    ## 1157     8-Feb-18
    ## 1158     5-Feb-18
    ## 1159     5-Feb-18
    ## 1160  31 Jan 2018
    ## 1161  31 Jan 2018
    ## 1162  31 Jan 2018
    ## 1163  31 Jan 2018
    ## 1164  29 Jan 2018
    ## 1165  29 Jan 2018
    ## 1166  26 Jan 2018
    ## 1167  26 Jan 2018
    ## 1168  25 Jan 2018
    ## 1169  25 Jan 2018
    ## 1170  25 Jan 2018
    ## 1171  25 Jan 2018
    ## 1172  24 Jan 2018
    ## 1173  24 Jan 2018
    ## 1174  23 Jan 2018
    ## 1175  18 Jan 2018
    ## 1176  18 Jan 2018
    ## 1177  18 Jan 2018
    ## 1178  18 Jan 2018
    ## 1179  18 Jan 2018
    ## 1180  17 Jan 2018
    ## 1181  16 Jan 2018
    ## 1182  16 Jan 2018
    ## 1183  13 Jan 2018
    ## 1184  11 Jan 2018
    ## 1185  11 Jan 2018
    ## 1186  10 Jan 2018
    ## 1187  10 Jan 2018
    ## 1188  08 Jan 2018
    ## 1189  08 Jan 2018
    ## 1190  08 Jan 2018
    ## 1191  07 Jan 2018
    ## 1192  26 Dec 2017
    ## 1193  14 Dec 2017
    ## 1194  13 Dec 2017
    ## 1195  13 Dec 2017
    ## 1196  13 Dec 2017
    ## 1197  12 Dec 2017
    ## 1198  12 Dec 2017
    ## 1199  06 Dec 2017
    ## 1200  04 Dec 2017
    ## 1201  01 Dec 2017
    ## 1202    30-Nov-17
    ## 1203    29-Nov-17
    ## 1204    29-Nov-17
    ## 1205    28-Nov-17
    ## 1206    28-Nov-17
    ## 1207    28-Nov-17
    ## 1208    28-Nov-17
    ## 1209    28-Nov-17
    ## 1210    25-Nov-17
    ## 1211    24-Nov-17
    ## 1212     8-Nov-17
    ## 1213     2-Nov-17
    ## 1214    31-Oct-17
    ## 1215    31-Oct-17
    ## 1216    20-Oct-17
    ## 1217    18-Oct-17
    ## 1218    12-Oct-17
    ## 1219     9-Oct-17
    ## 1220     9-Oct-17
    ## 1221     9-Oct-17
    ## 1222     9-Oct-17
    ## 1223     9-Oct-17
    ## 1224  18 Sep 2017
    ## 1225  12 Sep 2017
    ## 1226  09 Sep 2017
    ## 1227  07 Sep 2017
    ## 1228  05 Sep 2017
    ## 1229  05 Sep 2017
    ## 1230  05 Sep 2017
    ## 1231  05 Sep 2017
    ## 1232  29 Aug 2017
    ## 1233  29 Aug 2017
    ## 1234  18 Aug 2017
    ## 1235  18 Aug 2017
    ## 1236  07 Aug 2017
    ## 1237    12-Jul-17
    ## 1238    11-Jul-17
    ## 1239    11-Jul-17
    ## 1240    11-Jul-17
    ## 1241    11-Jul-17
    ## 1242     4-Jul-17
    ## 1243     2-Jul-17
    ## 1244    16-Jun-17
    ## 1245    26-May-17
    ## 1246    25-May-17
    ## 1247     4-May-17
    ## 1248  26 Apr 2017
    ## 1249  24 Apr 2017
    ## 1250  22 Apr 2017
    ## 1251  19 Apr 2017
    ## 1252  19 Apr 2017
    ## 1253  14 Apr 2017
    ## 1254  02 Apr 2017
    ## 1255  01 Apr 2017
    ## 1256    30-Mar-17
    ## 1257    21-Mar-17
    ## 1258    13-Mar-17
    ## 1259    13-Mar-17
    ## 1260    13-Mar-17
    ## 1261    13-Mar-17
    ## 1262    16-Feb-17
    ## 1263    15-Feb-17
    ## 1264    14-Feb-17
    ## 1265    13-Feb-17
    ## 1266     8-Feb-17
    ## 1267  30 Jan 2017
    ## 1268  27 Jan 2017
    ## 1269  26 Jan 2017
    ## 1270  26 Jan 2017
    ## 1271  25 Jan 2017
    ## 1272  24 Jan 2017
    ## 1273  24 Jan 2017
    ## 1274  24 Jan 2017
    ## 1275  24 Jan 2017
    ## 1276  24 Jan 2017
    ## 1277  24 Jan 2017
    ## 1278  24 Jan 2017
    ## 1279  24 Jan 2017
    ## 1280  24 Jan 2017
    ## 1281  24 Jan 2017
    ## 1282  24 Jan 2017
    ## 1283  24 Jan 2017
    ## 1284  24 Jan 2017
    ## 1285  24 Jan 2017
    ## 1286  24 Jan 2017
    ## 1287  24 Jan 2017
    ## 1288  24 Jan 2017

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

df1
```

    ##      Var1 Var2
    ## 1      67    4
    ## 2     166    4
    ## 3     184    4
    ## 4     211    4
    ## 5     212    4
    ## 6     326    4
    ## 7     372    4
    ## 8     498    4
    ## 9     568    4
    ## 10    852    4
    ## 11    898    4
    ## 12    987    4
    ## 13   1046    4
    ## 14   1225    4
    ## 15   1266    4
    ## 16   1287    4
    ## 17   1288    4
    ## 19    166   67
    ## 20    184   67
    ## 21    211   67
    ## 22    212   67
    ## 23    326   67
    ## 24    372   67
    ## 25    498   67
    ## 26    568   67
    ## 27    852   67
    ## 28    898   67
    ## 29    987   67
    ## 30   1046   67
    ## 31   1225   67
    ## 32   1266   67
    ## 33   1287   67
    ## 34   1288   67
    ## 37    184  166
    ## 38    211  166
    ## 39    212  166
    ## 40    326  166
    ## 41    372  166
    ## 42    498  166
    ## 43    568  166
    ## 44    852  166
    ## 45    898  166
    ## 46    987  166
    ## 47   1046  166
    ## 48   1225  166
    ## 49   1266  166
    ## 50   1287  166
    ## 51   1288  166
    ## 55    211  184
    ## 56    212  184
    ## 57    326  184
    ## 58    372  184
    ## 59    498  184
    ## 60    568  184
    ## 61    852  184
    ## 62    898  184
    ## 63    987  184
    ## 64   1046  184
    ## 65   1225  184
    ## 66   1266  184
    ## 67   1287  184
    ## 68   1288  184
    ## 73    212  211
    ## 74    326  211
    ## 75    372  211
    ## 76    498  211
    ## 77    568  211
    ## 78    852  211
    ## 79    898  211
    ## 80    987  211
    ## 81   1046  211
    ## 82   1225  211
    ## 83   1266  211
    ## 84   1287  211
    ## 85   1288  211
    ## 91    326  212
    ## 92    372  212
    ## 93    498  212
    ## 94    568  212
    ## 95    852  212
    ## 96    898  212
    ## 97    987  212
    ## 98   1046  212
    ## 99   1225  212
    ## 100  1266  212
    ## 101  1287  212
    ## 102  1288  212
    ## 109   372  326
    ## 110   498  326
    ## 111   568  326
    ## 112   852  326
    ## 113   898  326
    ## 114   987  326
    ## 115  1046  326
    ## 116  1225  326
    ## 117  1266  326
    ## 118  1287  326
    ## 119  1288  326
    ## 127   498  372
    ## 128   568  372
    ## 129   852  372
    ## 130   898  372
    ## 131   987  372
    ## 132  1046  372
    ## 133  1225  372
    ## 134  1266  372
    ## 135  1287  372
    ## 136  1288  372
    ## 145   568  498
    ## 146   852  498
    ## 147   898  498
    ## 148   987  498
    ## 149  1046  498
    ## 150  1225  498
    ## 151  1266  498
    ## 152  1287  498
    ## 153  1288  498
    ## 163   852  568
    ## 164   898  568
    ## 165   987  568
    ## 166  1046  568
    ## 167  1225  568
    ## 168  1266  568
    ## 169  1287  568
    ## 170  1288  568
    ## 181   898  852
    ## 182   987  852
    ## 183  1046  852
    ## 184  1225  852
    ## 185  1266  852
    ## 186  1287  852
    ## 187  1288  852
    ## 199   987  898
    ## 200  1046  898
    ## 201  1225  898
    ## 202  1266  898
    ## 203  1287  898
    ## 204  1288  898
    ## 217  1046  987
    ## 218  1225  987
    ## 219  1266  987
    ## 220  1287  987
    ## 221  1288  987
    ## 235  1225 1046
    ## 236  1266 1046
    ## 237  1287 1046
    ## 238  1288 1046
    ## 253  1266 1225
    ## 254  1287 1225
    ## 255  1288 1225
    ## 271  1287 1266
    ## 272  1288 1266
    ## 289  1288 1287
    ## 307    14    6
    ## 308   119    6
    ## 309   141    6
    ## 310   309    6
    ## 311   412    6
    ## 312   620    6
    ## 313   709    6
    ## 314   797    6
    ## 315   827    6
    ## 316   937    6
    ## 317   949    6
    ## 318   971    6
    ## 319  1063    6
    ## 320  1068    6
    ## 321  1069    6
    ## 322  1146    6
    ## 323  1188    6
    ## 324  1238    6
    ## 326   119   14
    ## 327   141   14
    ## 328   309   14
    ## 329   412   14
    ## 330   620   14
    ## 331   709   14
    ## 332   797   14
    ## 333   827   14
    ## 334   937   14
    ## 335   949   14
    ## 336   971   14
    ## 337  1063   14
    ## 338  1068   14
    ## 339  1069   14
    ## 340  1146   14
    ## 341  1188   14
    ## 342  1238   14
    ## 345   141  119
    ## 346   309  119
    ## 347   412  119
    ## 348   620  119
    ## 349   709  119
    ## 350   797  119
    ## 351   827  119
    ## 352   937  119
    ## 353   949  119
    ## 354   971  119
    ## 355  1063  119
    ## 356  1068  119
    ## 357  1069  119
    ## 358  1146  119
    ## 359  1188  119
    ## 360  1238  119
    ## 364   309  141
    ## 365   412  141
    ## 366   620  141
    ## 367   709  141
    ## 368   797  141
    ## 369   827  141
    ## 370   937  141
    ## 371   949  141
    ## 372   971  141
    ## 373  1063  141
    ## 374  1068  141
    ## 375  1069  141
    ## 376  1146  141
    ## 377  1188  141
    ## 378  1238  141
    ## 383   412  309
    ## 384   620  309
    ## 385   709  309
    ## 386   797  309
    ## 387   827  309
    ## 388   937  309
    ## 389   949  309
    ## 390   971  309
    ## 391  1063  309
    ## 392  1068  309
    ## 393  1069  309
    ## 394  1146  309
    ## 395  1188  309
    ## 396  1238  309
    ## 402   620  412
    ## 403   709  412
    ## 404   797  412
    ## 405   827  412
    ## 406   937  412
    ## 407   949  412
    ## 408   971  412
    ## 409  1063  412
    ## 410  1068  412
    ## 411  1069  412
    ## 412  1146  412
    ## 413  1188  412
    ## 414  1238  412
    ## 421   709  620
    ## 422   797  620
    ## 423   827  620
    ## 424   937  620
    ## 425   949  620
    ## 426   971  620
    ## 427  1063  620
    ## 428  1068  620
    ## 429  1069  620
    ## 430  1146  620
    ## 431  1188  620
    ## 432  1238  620
    ## 440   797  709
    ## 441   827  709
    ## 442   937  709
    ## 443   949  709
    ## 444   971  709
    ## 445  1063  709
    ## 446  1068  709
    ## 447  1069  709
    ## 448  1146  709
    ## 449  1188  709
    ## 450  1238  709
    ## 459   827  797
    ## 460   937  797
    ## 461   949  797
    ## 462   971  797
    ## 463  1063  797
    ## 464  1068  797
    ## 465  1069  797
    ## 466  1146  797
    ## 467  1188  797
    ## 468  1238  797
    ## 478   937  827
    ## 479   949  827
    ## 480   971  827
    ## 481  1063  827
    ## 482  1068  827
    ## 483  1069  827
    ## 484  1146  827
    ## 485  1188  827
    ## 486  1238  827
    ## 497   949  937
    ## 498   971  937
    ## 499  1063  937
    ## 500  1068  937
    ## 501  1069  937
    ## 502  1146  937
    ## 503  1188  937
    ## 504  1238  937
    ## 516   971  949
    ## 517  1063  949
    ## 518  1068  949
    ## 519  1069  949
    ## 520  1146  949
    ## 521  1188  949
    ## 522  1238  949
    ## 535  1063  971
    ## 536  1068  971
    ## 537  1069  971
    ## 538  1146  971
    ## 539  1188  971
    ## 540  1238  971
    ## 554  1068 1063
    ## 555  1069 1063
    ## 556  1146 1063
    ## 557  1188 1063
    ## 558  1238 1063
    ## 573  1069 1068
    ## 574  1146 1068
    ## 575  1188 1068
    ## 576  1238 1068
    ## 592  1146 1069
    ## 593  1188 1069
    ## 594  1238 1069
    ## 611  1188 1146
    ## 612  1238 1146
    ## 630  1238 1188
    ## 649   111    9
    ## 650   120    9
    ## 651   193    9
    ## 653   120  111
    ## 654   193  111
    ## 657   193  120
    ## 661   400   12
    ## 662   784   12
    ## 663  1171   12
    ## 665   784  400
    ## 666  1171  400
    ## 669  1171  784
    ## 673  1142   17
    ## 675   725   18
    ## 677   251   25
    ## 678   269   25
    ## 679   825   25
    ## 681   269  251
    ## 682   825  251
    ## 685   825  269
    ## 689    48   27
    ## 690   102   27
    ## 692   102   48
    ## 695    29   28
    ## 696    34   28
    ## 697    41   28
    ## 698    52   28
    ## 699    79   28
    ## 700   107   28
    ## 701   109   28
    ## 702   114   28
    ## 703   127   28
    ## 704   133   28
    ## 705   146   28
    ## 706   162   28
    ## 707   163   28
    ## 708   174   28
    ## 709   177   28
    ## 710   236   28
    ## 711   244   28
    ## 712   254   28
    ## 713   262   28
    ## 714   271   28
    ## 715   281   28
    ## 716   381   28
    ## 718    34   29
    ## 719    41   29
    ## 720    52   29
    ## 721    79   29
    ## 722   107   29
    ## 723   109   29
    ## 724   114   29
    ## 725   127   29
    ## 726   133   29
    ## 727   146   29
    ## 728   162   29
    ## 729   163   29
    ## 730   174   29
    ## 731   177   29
    ## 732   236   29
    ## 733   244   29
    ## 734   254   29
    ## 735   262   29
    ## 736   271   29
    ## 737   281   29
    ## 738   381   29
    ## 741    41   34
    ## 742    52   34
    ## 743    79   34
    ## 744   107   34
    ## 745   109   34
    ## 746   114   34
    ## 747   127   34
    ## 748   133   34
    ## 749   146   34
    ## 750   162   34
    ## 751   163   34
    ## 752   174   34
    ## 753   177   34
    ## 754   236   34
    ## 755   244   34
    ## 756   254   34
    ## 757   262   34
    ## 758   271   34
    ## 759   281   34
    ## 760   381   34
    ## 764    52   41
    ## 765    79   41
    ## 766   107   41
    ## 767   109   41
    ## 768   114   41
    ## 769   127   41
    ## 770   133   41
    ## 771   146   41
    ## 772   162   41
    ## 773   163   41
    ## 774   174   41
    ## 775   177   41
    ## 776   236   41
    ## 777   244   41
    ## 778   254   41
    ## 779   262   41
    ## 780   271   41
    ## 781   281   41
    ## 782   381   41
    ## 787    79   52
    ## 788   107   52
    ## 789   109   52
    ## 790   114   52
    ## 791   127   52
    ## 792   133   52
    ## 793   146   52
    ## 794   162   52
    ## 795   163   52
    ## 796   174   52
    ## 797   177   52
    ## 798   236   52
    ## 799   244   52
    ## 800   254   52
    ## 801   262   52
    ## 802   271   52
    ## 803   281   52
    ## 804   381   52
    ## 810   107   79
    ## 811   109   79
    ## 812   114   79
    ## 813   127   79
    ## 814   133   79
    ## 815   146   79
    ## 816   162   79
    ## 817   163   79
    ## 818   174   79
    ## 819   177   79
    ## 820   236   79
    ## 821   244   79
    ## 822   254   79
    ## 823   262   79
    ## 824   271   79
    ## 825   281   79
    ## 826   381   79
    ## 833   109  107
    ## 834   114  107
    ## 835   127  107
    ## 836   133  107
    ## 837   146  107
    ## 838   162  107
    ## 839   163  107
    ## 840   174  107
    ## 841   177  107
    ## 842   236  107
    ## 843   244  107
    ## 844   254  107
    ## 845   262  107
    ## 846   271  107
    ## 847   281  107
    ## 848   381  107
    ## 856   114  109
    ## 857   127  109
    ## 858   133  109
    ## 859   146  109
    ## 860   162  109
    ## 861   163  109
    ## 862   174  109
    ## 863   177  109
    ## 864   236  109
    ## 865   244  109
    ## 866   254  109
    ## 867   262  109
    ## 868   271  109
    ## 869   281  109
    ## 870   381  109
    ## 879   127  114
    ## 880   133  114
    ## 881   146  114
    ## 882   162  114
    ## 883   163  114
    ## 884   174  114
    ## 885   177  114
    ## 886   236  114
    ## 887   244  114
    ## 888   254  114
    ## 889   262  114
    ## 890   271  114
    ## 891   281  114
    ## 892   381  114
    ## 902   133  127
    ## 903   146  127
    ## 904   162  127
    ## 905   163  127
    ## 906   174  127
    ## 907   177  127
    ## 908   236  127
    ## 909   244  127
    ## 910   254  127
    ## 911   262  127
    ## 912   271  127
    ## 913   281  127
    ## 914   381  127
    ## 925   146  133
    ## 926   162  133
    ## 927   163  133
    ## 928   174  133
    ## 929   177  133
    ## 930   236  133
    ## 931   244  133
    ## 932   254  133
    ## 933   262  133
    ## 934   271  133
    ## 935   281  133
    ## 936   381  133
    ## 948   162  146
    ## 949   163  146
    ## 950   174  146
    ## 951   177  146
    ## 952   236  146
    ## 953   244  146
    ## 954   254  146
    ## 955   262  146
    ## 956   271  146
    ## 957   281  146
    ## 958   381  146
    ## 971   163  162
    ## 972   174  162
    ## 973   177  162
    ## 974   236  162
    ## 975   244  162
    ## 976   254  162
    ## 977   262  162
    ## 978   271  162
    ## 979   281  162
    ## 980   381  162
    ## 994   174  163
    ## 995   177  163
    ## 996   236  163
    ## 997   244  163
    ## 998   254  163
    ## 999   262  163
    ## 1000  271  163
    ## 1001  281  163
    ## 1002  381  163
    ## 1017  177  174
    ## 1018  236  174
    ## 1019  244  174
    ## 1020  254  174
    ## 1021  262  174
    ## 1022  271  174
    ## 1023  281  174
    ## 1024  381  174
    ## 1040  236  177
    ## 1041  244  177
    ## 1042  254  177
    ## 1043  262  177
    ## 1044  271  177
    ## 1045  281  177
    ## 1046  381  177
    ## 1063  244  236
    ## 1064  254  236
    ## 1065  262  236
    ## 1066  271  236
    ## 1067  281  236
    ## 1068  381  236
    ## 1086  254  244
    ## 1087  262  244
    ## 1088  271  244
    ## 1089  281  244
    ## 1090  381  244
    ## 1109  262  254
    ## 1110  271  254
    ## 1111  281  254
    ## 1112  381  254
    ## 1132  271  262
    ## 1133  281  262
    ## 1134  381  262
    ## 1155  281  271
    ## 1156  381  271
    ## 1178  381  281
    ## 1201  273   36
    ## 1203  943   38
    ## 1205  196   40
    ## 1207  226   42
    ## 1208  230   42
    ## 1209  240   42
    ## 1210  245   42
    ## 1212  230  226
    ## 1213  240  226
    ## 1214  245  226
    ## 1217  240  230
    ## 1218  245  230
    ## 1222  245  240
    ## 1227  180   43
    ## 1228  272   43
    ## 1230  272  180
    ## 1233 1004   51
    ## 1235   89   53
    ## 1236   90   53
    ## 1237   92   53
    ## 1239   90   89
    ## 1240   92   89
    ## 1243   92   90
    ## 1247  345   57
    ## 1248  470   57
    ## 1249  567   57
    ## 1250  702   57
    ## 1251  712   57
    ## 1252  831   57
    ## 1253  932   57
    ## 1254  941   57
    ## 1255 1054   57
    ## 1256 1065   57
    ## 1257 1104   57
    ## 1258 1122   57
    ## 1260  470  345
    ## 1261  567  345
    ## 1262  702  345
    ## 1263  712  345
    ## 1264  831  345
    ## 1265  932  345
    ## 1266  941  345
    ## 1267 1054  345
    ## 1268 1065  345
    ## 1269 1104  345
    ## 1270 1122  345
    ## 1273  567  470
    ## 1274  702  470
    ## 1275  712  470
    ## 1276  831  470
    ## 1277  932  470
    ## 1278  941  470
    ## 1279 1054  470
    ## 1280 1065  470
    ## 1281 1104  470
    ## 1282 1122  470
    ## 1286  702  567
    ## 1287  712  567
    ## 1288  831  567
    ## 1289  932  567
    ## 1290  941  567
    ## 1291 1054  567
    ## 1292 1065  567
    ## 1293 1104  567
    ## 1294 1122  567
    ## 1299  712  702
    ## 1300  831  702
    ## 1301  932  702
    ## 1302  941  702
    ## 1303 1054  702
    ## 1304 1065  702
    ## 1305 1104  702
    ## 1306 1122  702
    ## 1312  831  712
    ## 1313  932  712
    ## 1314  941  712
    ## 1315 1054  712
    ## 1316 1065  712
    ## 1317 1104  712
    ## 1318 1122  712
    ## 1325  932  831
    ## 1326  941  831
    ## 1327 1054  831
    ## 1328 1065  831
    ## 1329 1104  831
    ## 1330 1122  831
    ## 1338  941  932
    ## 1339 1054  932
    ## 1340 1065  932
    ## 1341 1104  932
    ## 1342 1122  932
    ## 1351 1054  941
    ## 1352 1065  941
    ## 1353 1104  941
    ## 1354 1122  941
    ## 1364 1065 1054
    ## 1365 1104 1054
    ## 1366 1122 1054
    ## 1377 1104 1065
    ## 1378 1122 1065
    ## 1390 1122 1104
    ## 1403  570   61
    ## 1404  603   61
    ## 1405  948   61
    ## 1406 1204   61
    ## 1408  603  570
    ## 1409  948  570
    ## 1410 1204  570
    ## 1413  948  603
    ## 1414 1204  603
    ## 1418 1204  948
    ## 1423  781   62
    ## 1425  112   63
    ## 1426  135   63
    ## 1428  135  112
    ## 1431  134   64
    ## 1432  161   64
    ## 1433  214   64
    ## 1435  161  134
    ## 1436  214  134
    ## 1439  214  161
    ## 1443  337   65
    ## 1446  202   69
    ## 1447  330   69
    ## 1448  373   69
    ## 1449  486   69
    ## 1450  542   69
    ## 1451  604   69
    ## 1452  695   69
    ## 1453  780   69
    ## 1454  856   69
    ## 1455  914   69
    ## 1456  924   69
    ## 1457  961   69
    ## 1458 1042   69
    ## 1459 1083   69
    ## 1460 1103   69
    ## 1461 1133   69
    ## 1462 1140   69
    ## 1464  202   71
    ## 1465  330   71
    ## 1466  373   71
    ## 1467  486   71
    ## 1468  542   71
    ## 1469  604   71
    ## 1470  695   71
    ## 1471  780   71
    ## 1472  856   71
    ## 1473  914   71
    ## 1474  924   71
    ## 1475  961   71
    ## 1476 1042   71
    ## 1477 1083   71
    ## 1478 1103   71
    ## 1479 1133   71
    ## 1480 1140   71
    ## 1483  330  202
    ## 1484  373  202
    ## 1485  486  202
    ## 1486  542  202
    ## 1487  604  202
    ## 1488  695  202
    ## 1489  780  202
    ## 1490  856  202
    ## 1491  914  202
    ## 1492  924  202
    ## 1493  961  202
    ## 1494 1042  202
    ## 1495 1083  202
    ## 1496 1103  202
    ## 1497 1133  202
    ## 1498 1140  202
    ## 1502  373  330
    ## 1503  486  330
    ## 1504  542  330
    ## 1505  604  330
    ## 1506  695  330
    ## 1507  780  330
    ## 1508  856  330
    ## 1509  914  330
    ## 1510  924  330
    ## 1511  961  330
    ## 1512 1042  330
    ## 1513 1083  330
    ## 1514 1103  330
    ## 1515 1133  330
    ## 1516 1140  330
    ## 1521  486  373
    ## 1522  542  373
    ## 1523  604  373
    ## 1524  695  373
    ## 1525  780  373
    ## 1526  856  373
    ## 1527  914  373
    ## 1528  924  373
    ## 1529  961  373
    ## 1530 1042  373
    ## 1531 1083  373
    ## 1532 1103  373
    ## 1533 1133  373
    ## 1534 1140  373
    ## 1540  542  486
    ## 1541  604  486
    ## 1542  695  486
    ## 1543  780  486
    ## 1544  856  486
    ## 1545  914  486
    ## 1546  924  486
    ## 1547  961  486
    ## 1548 1042  486
    ## 1549 1083  486
    ## 1550 1103  486
    ## 1551 1133  486
    ## 1552 1140  486
    ## 1559  604  542
    ## 1560  695  542
    ## 1561  780  542
    ## 1562  856  542
    ## 1563  914  542
    ## 1564  924  542
    ## 1565  961  542
    ## 1566 1042  542
    ## 1567 1083  542
    ## 1568 1103  542
    ## 1569 1133  542
    ## 1570 1140  542
    ## 1578  695  604
    ## 1579  780  604
    ## 1580  856  604
    ## 1581  914  604
    ## 1582  924  604
    ## 1583  961  604
    ## 1584 1042  604
    ## 1585 1083  604
    ## 1586 1103  604
    ## 1587 1133  604
    ## 1588 1140  604
    ## 1597  780  695
    ## 1598  856  695
    ## 1599  914  695
    ## 1600  924  695
    ## 1601  961  695
    ## 1602 1042  695
    ## 1603 1083  695
    ## 1604 1103  695
    ## 1605 1133  695
    ## 1606 1140  695
    ## 1616  856  780
    ## 1617  914  780
    ## 1618  924  780
    ## 1619  961  780
    ## 1620 1042  780
    ## 1621 1083  780
    ## 1622 1103  780
    ## 1623 1133  780
    ## 1624 1140  780
    ## 1635  914  856
    ## 1636  924  856
    ## 1637  961  856
    ## 1638 1042  856
    ## 1639 1083  856
    ## 1640 1103  856
    ## 1641 1133  856
    ## 1642 1140  856
    ## 1654  924  914
    ## 1655  961  914
    ## 1656 1042  914
    ## 1657 1083  914
    ## 1658 1103  914
    ## 1659 1133  914
    ## 1660 1140  914
    ## 1673  961  924
    ## 1674 1042  924
    ## 1675 1083  924
    ## 1676 1103  924
    ## 1677 1133  924
    ## 1678 1140  924
    ## 1692 1042  961
    ## 1693 1083  961
    ## 1694 1103  961
    ## 1695 1133  961
    ## 1696 1140  961
    ## 1711 1083 1042
    ## 1712 1103 1042
    ## 1713 1133 1042
    ## 1714 1140 1042
    ## 1730 1103 1083
    ## 1731 1133 1083
    ## 1732 1140 1083
    ## 1749 1133 1103
    ## 1750 1140 1103
    ## 1768 1140 1133
    ## 1787  293   72
    ## 1788  504   72
    ## 1789  903   72
    ## 1790 1056   72
    ## 1792  504  293
    ## 1793  903  293
    ## 1794 1056  293
    ## 1797  903  504
    ## 1798 1056  504
    ## 1802 1056  903
    ## 1807  308   73
    ## 1808  501   73
    ## 1809  944   73
    ## 1811  501  308
    ## 1812  944  308
    ## 1815  944  501
    ## 1819  521   75
    ## 1820  662   75
    ## 1821  879   75
    ## 1822  884   75
    ## 1823 1090   75
    ## 1824 1217   75
    ## 1825 1253   75
    ## 1826 1259   75
    ## 1828  662  521
    ## 1829  879  521
    ## 1830  884  521
    ## 1831 1090  521
    ## 1832 1217  521
    ## 1833 1253  521
    ## 1834 1259  521
    ## 1837  879  662
    ## 1838  884  662
    ## 1839 1090  662
    ## 1840 1217  662
    ## 1841 1253  662
    ## 1842 1259  662
    ## 1846  884  879
    ## 1847 1090  879
    ## 1848 1217  879
    ## 1849 1253  879
    ## 1850 1259  879
    ## 1855 1090  884
    ## 1856 1217  884
    ## 1857 1253  884
    ## 1858 1259  884
    ## 1864 1217 1090
    ## 1865 1253 1090
    ## 1866 1259 1090
    ## 1873 1253 1217
    ## 1874 1259 1217
    ## 1882 1259 1253
    ## 1891  115   77
    ## 1892  125   77
    ## 1893  218   77
    ## 1894  235   77
    ## 1895  242   77
    ## 1897  125  115
    ## 1898  218  115
    ## 1899  235  115
    ## 1900  242  115
    ## 1903  218  125
    ## 1904  235  125
    ## 1905  242  125
    ## 1909  235  218
    ## 1910  242  218
    ## 1915  242  235
    ## 1921  473   80
    ## 1922  986   80
    ## 1924  986  473
    ## 1927  149   82
    ## 1928  190   82
    ## 1930  190  149
    ## 1933  187   84
    ## 1934  198   84
    ## 1935  261   84
    ## 1936  769   84
    ## 1938  198  187
    ## 1939  261  187
    ## 1940  769  187
    ## 1943  261  198
    ## 1944  769  198
    ## 1948  769  261
    ## 1953  454   85
    ## 1954  475   85
    ## 1955  518   85
    ## 1956  527   85
    ## 1957  608   85
    ## 1958  749   85
    ## 1959  861   85
    ## 1960 1019   85
    ## 1961 1027   85
    ## 1962 1189   85
    ## 1963 1215   85
    ## 1965  475  454
    ## 1966  518  454
    ## 1967  527  454
    ## 1968  608  454
    ## 1969  749  454
    ## 1970  861  454
    ## 1971 1019  454
    ## 1972 1027  454
    ## 1973 1189  454
    ## 1974 1215  454
    ## 1977  518  475
    ## 1978  527  475
    ## 1979  608  475
    ## 1980  749  475
    ## 1981  861  475
    ## 1982 1019  475
    ## 1983 1027  475
    ## 1984 1189  475
    ## 1985 1215  475
    ## 1989  527  518
    ## 1990  608  518
    ## 1991  749  518
    ## 1992  861  518
    ## 1993 1019  518
    ## 1994 1027  518
    ## 1995 1189  518
    ## 1996 1215  518
    ## 2001  608  527
    ## 2002  749  527
    ## 2003  861  527
    ## 2004 1019  527
    ## 2005 1027  527
    ## 2006 1189  527
    ## 2007 1215  527
    ## 2013  749  608
    ## 2014  861  608
    ## 2015 1019  608
    ## 2016 1027  608
    ## 2017 1189  608
    ## 2018 1215  608
    ## 2025  861  749
    ## 2026 1019  749
    ## 2027 1027  749
    ## 2028 1189  749
    ## 2029 1215  749
    ## 2037 1019  861
    ## 2038 1027  861
    ## 2039 1189  861
    ## 2040 1215  861
    ## 2049 1027 1019
    ## 2050 1189 1019
    ## 2051 1215 1019
    ## 2061 1189 1027
    ## 2062 1215 1027
    ## 2073 1215 1189
    ## 2085  145   88
    ## 2086  730   88
    ## 2088  730  145
    ## 2091  248   91
    ## 2093  100   93
    ## 2094  113   93
    ## 2095  239   93
    ## 2096  280   93
    ## 2098  113  100
    ## 2099  239  100
    ## 2100  280  100
    ## 2103  239  113
    ## 2104  280  113
    ## 2108  280  239
    ## 2113  268  101
    ## 2114  859  101
    ## 2115  891  101
    ## 2116  940  101
    ## 2117  989  101
    ## 2118 1130  101
    ## 2119 1245  101
    ## 2121  859  268
    ## 2122  891  268
    ## 2123  940  268
    ## 2124  989  268
    ## 2125 1130  268
    ## 2126 1245  268
    ## 2129  891  859
    ## 2130  940  859
    ## 2131  989  859
    ## 2132 1130  859
    ## 2133 1245  859
    ## 2137  940  891
    ## 2138  989  891
    ## 2139 1130  891
    ## 2140 1245  891
    ## 2145  989  940
    ## 2146 1130  940
    ## 2147 1245  940
    ## 2153 1130  989
    ## 2154 1245  989
    ## 2161 1245 1130
    ## 2169  291  104
    ## 2170  552  104
    ## 2171  957  104
    ## 2172  966  104
    ## 2174  552  291
    ## 2175  957  291
    ## 2176  966  291
    ## 2179  957  552
    ## 2180  966  552
    ## 2184  966  957
    ## 2189  576  116
    ## 2191  411  118
    ## 2192 1149  118
    ## 2194 1149  411
    ## 2197  223  121
    ## 2198  232  121
    ## 2199  241  121
    ## 2200  270  121
    ## 2201  353  121
    ## 2202  382  121
    ## 2203  468  121
    ## 2204  511  121
    ## 2205  605  121
    ## 2206 1077  121
    ## 2207 1111  121
    ## 2208 1119  121
    ## 2209 1136  121
    ## 2210 1179  121
    ## 2211 1243  121
    ## 2213  232  223
    ## 2214  241  223
    ## 2215  270  223
    ## 2216  353  223
    ## 2217  382  223
    ## 2218  468  223
    ## 2219  511  223
    ## 2220  605  223
    ## 2221 1077  223
    ## 2222 1111  223
    ## 2223 1119  223
    ## 2224 1136  223
    ## 2225 1179  223
    ## 2226 1243  223
    ## 2229  241  232
    ## 2230  270  232
    ## 2231  353  232
    ## 2232  382  232
    ## 2233  468  232
    ## 2234  511  232
    ## 2235  605  232
    ## 2236 1077  232
    ## 2237 1111  232
    ## 2238 1119  232
    ## 2239 1136  232
    ## 2240 1179  232
    ## 2241 1243  232
    ## 2245  270  241
    ## 2246  353  241
    ## 2247  382  241
    ## 2248  468  241
    ## 2249  511  241
    ## 2250  605  241
    ## 2251 1077  241
    ## 2252 1111  241
    ## 2253 1119  241
    ## 2254 1136  241
    ## 2255 1179  241
    ## 2256 1243  241
    ## 2261  353  270
    ## 2262  382  270
    ## 2263  468  270
    ## 2264  511  270
    ## 2265  605  270
    ## 2266 1077  270
    ## 2267 1111  270
    ## 2268 1119  270
    ## 2269 1136  270
    ## 2270 1179  270
    ## 2271 1243  270
    ## 2277  382  353
    ## 2278  468  353
    ## 2279  511  353
    ## 2280  605  353
    ## 2281 1077  353
    ## 2282 1111  353
    ## 2283 1119  353
    ## 2284 1136  353
    ## 2285 1179  353
    ## 2286 1243  353
    ## 2293  468  382
    ## 2294  511  382
    ## 2295  605  382
    ## 2296 1077  382
    ## 2297 1111  382
    ## 2298 1119  382
    ## 2299 1136  382
    ## 2300 1179  382
    ## 2301 1243  382
    ## 2309  511  468
    ## 2310  605  468
    ## 2311 1077  468
    ## 2312 1111  468
    ## 2313 1119  468
    ## 2314 1136  468
    ## 2315 1179  468
    ## 2316 1243  468
    ## 2325  605  511
    ## 2326 1077  511
    ## 2327 1111  511
    ## 2328 1119  511
    ## 2329 1136  511
    ## 2330 1179  511
    ## 2331 1243  511
    ## 2341 1077  605
    ## 2342 1111  605
    ## 2343 1119  605
    ## 2344 1136  605
    ## 2345 1179  605
    ## 2346 1243  605
    ## 2357 1111 1077
    ## 2358 1119 1077
    ## 2359 1136 1077
    ## 2360 1179 1077
    ## 2361 1243 1077
    ## 2373 1119 1111
    ## 2374 1136 1111
    ## 2375 1179 1111
    ## 2376 1243 1111
    ## 2389 1136 1119
    ## 2390 1179 1119
    ## 2391 1243 1119
    ## 2405 1179 1136
    ## 2406 1243 1136
    ## 2421 1243 1179
    ## 2437  665  129
    ## 2438  678  129
    ## 2439  843  129
    ## 2441  678  665
    ## 2442  843  665
    ## 2445  843  678
    ## 2449  466  132
    ## 2450  593  132
    ## 2451 1252  132
    ## 2453  593  466
    ## 2454 1252  466
    ## 2457 1252  593
    ## 2461  183  136
    ## 2462  224  136
    ## 2463  233  136
    ## 2464  388  136
    ## 2466  224  183
    ## 2467  233  183
    ## 2468  388  183
    ## 2471  233  224
    ## 2472  388  224
    ## 2476  388  233
    ## 2481  556  142
    ## 2482 1075  142
    ## 2483 1093  142
    ## 2485 1075  556
    ## 2486 1093  556
    ## 2489 1093 1075
    ## 2493  147  143
    ## 2494  170  143
    ## 2495  257  143
    ## 2497  170  147
    ## 2498  257  147
    ## 2501  257  170
    ## 2505  336  152
    ## 2507  487  155
    ## 2509  264  167
    ## 2511  195  175
    ## 2512  201  175
    ## 2513  361  175
    ## 2514  513  175
    ## 2515  528  175
    ## 2516  641  175
    ## 2517  773  175
    ## 2518  809  175
    ## 2519  951  175
    ## 2520 1029  175
    ## 2521 1286  175
    ## 2523  201  195
    ## 2524  361  195
    ## 2525  513  195
    ## 2526  528  195
    ## 2527  641  195
    ## 2528  773  195
    ## 2529  809  195
    ## 2530  951  195
    ## 2531 1029  195
    ## 2532 1286  195
    ## 2535  361  201
    ## 2536  513  201
    ## 2537  528  201
    ## 2538  641  201
    ## 2539  773  201
    ## 2540  809  201
    ## 2541  951  201
    ## 2542 1029  201
    ## 2543 1286  201
    ## 2547  513  361
    ## 2548  528  361
    ## 2549  641  361
    ## 2550  773  361
    ## 2551  809  361
    ## 2552  951  361
    ## 2553 1029  361
    ## 2554 1286  361
    ## 2559  528  513
    ## 2560  641  513
    ## 2561  773  513
    ## 2562  809  513
    ## 2563  951  513
    ## 2564 1029  513
    ## 2565 1286  513
    ## 2571  641  528
    ## 2572  773  528
    ## 2573  809  528
    ## 2574  951  528
    ## 2575 1029  528
    ## 2576 1286  528
    ## 2583  773  641
    ## 2584  809  641
    ## 2585  951  641
    ## 2586 1029  641
    ## 2587 1286  641
    ## 2595  809  773
    ## 2596  951  773
    ## 2597 1029  773
    ## 2598 1286  773
    ## 2607  951  809
    ## 2608 1029  809
    ## 2609 1286  809
    ## 2619 1029  951
    ## 2620 1286  951
    ## 2631 1286 1029
    ## 2643  287  181
    ## 2644  321  181
    ## 2645  323  181
    ## 2646  324  181
    ## 2647  327  181
    ## 2648  366  181
    ## 2649  375  181
    ## 2650  410  181
    ## 2651  431  181
    ## 2652  432  181
    ## 2653  433  181
    ## 2654  493  181
    ## 2655  507  181
    ## 2656  509  181
    ## 2658  321  287
    ## 2659  323  287
    ## 2660  324  287
    ## 2661  327  287
    ## 2662  366  287
    ## 2663  375  287
    ## 2664  410  287
    ## 2665  431  287
    ## 2666  432  287
    ## 2667  433  287
    ## 2668  493  287
    ## 2669  507  287
    ## 2670  509  287
    ## 2673  323  321
    ## 2674  324  321
    ## 2675  327  321
    ## 2676  366  321
    ## 2677  375  321
    ## 2678  410  321
    ## 2679  431  321
    ## 2680  432  321
    ## 2681  433  321
    ## 2682  493  321
    ## 2683  507  321
    ## 2684  509  321
    ## 2688  324  323
    ## 2689  327  323
    ## 2690  366  323
    ## 2691  375  323
    ## 2692  410  323
    ## 2693  431  323
    ## 2694  432  323
    ## 2695  433  323
    ## 2696  493  323
    ## 2697  507  323
    ## 2698  509  323
    ## 2703  327  324
    ## 2704  366  324
    ## 2705  375  324
    ## 2706  410  324
    ## 2707  431  324
    ## 2708  432  324
    ## 2709  433  324
    ## 2710  493  324
    ## 2711  507  324
    ## 2712  509  324
    ## 2718  366  327
    ## 2719  375  327
    ## 2720  410  327
    ## 2721  431  327
    ## 2722  432  327
    ## 2723  433  327
    ## 2724  493  327
    ## 2725  507  327
    ## 2726  509  327
    ## 2733  375  366
    ## 2734  410  366
    ## 2735  431  366
    ## 2736  432  366
    ## 2737  433  366
    ## 2738  493  366
    ## 2739  507  366
    ## 2740  509  366
    ## 2748  410  375
    ## 2749  431  375
    ## 2750  432  375
    ## 2751  433  375
    ## 2752  493  375
    ## 2753  507  375
    ## 2754  509  375
    ## 2763  431  410
    ## 2764  432  410
    ## 2765  433  410
    ## 2766  493  410
    ## 2767  507  410
    ## 2768  509  410
    ## 2778  432  431
    ## 2779  433  431
    ## 2780  493  431
    ## 2781  507  431
    ## 2782  509  431
    ## 2793  433  432
    ## 2794  493  432
    ## 2795  507  432
    ## 2796  509  432
    ## 2808  493  433
    ## 2809  507  433
    ## 2810  509  433
    ## 2823  507  493
    ## 2824  509  493
    ## 2838  509  507
    ## 2853  731  185
    ## 2854 1121  185
    ## 2855 1170  185
    ## 2857 1121  731
    ## 2858 1170  731
    ## 2861 1170 1121
    ## 2865 1010  205
    ## 2867  491  209
    ## 2869  820  210
    ## 2871  252  225
    ## 2872  256  225
    ## 2874  256  252
    ## 2877  858  228
    ## 2879  613  253
    ## 2880  873  253
    ## 2882  873  613
    ## 2885  260  258
    ## 2886  290  258
    ## 2887  310  258
    ## 2888  341  258
    ## 2889  359  258
    ## 2890  364  258
    ## 2891  492  258
    ## 2892  494  258
    ## 2893  578  258
    ## 2894  583  258
    ## 2895  632  258
    ## 2896  643  258
    ## 2897  646  258
    ## 2898  647  258
    ## 2899  654  258
    ## 2900  661  258
    ## 2901  668  258
    ## 2902  680  258
    ## 2903  681  258
    ## 2904  686  258
    ## 2905  692  258
    ## 2906  698  258
    ## 2907  717  258
    ## 2908  737  258
    ## 2909  742  258
    ## 2910  745  258
    ## 2911  755  258
    ## 2912  757  258
    ## 2913  770  258
    ## 2914  775  258
    ## 2915  789  258
    ## 2916  793  258
    ## 2917  794  258
    ## 2918  799  258
    ## 2919  800  258
    ## 2920  803  258
    ## 2921  804  258
    ## 2922  814  258
    ## 2923  822  258
    ## 2924  828  258
    ## 2925  832  258
    ## 2926  833  258
    ## 2927  844  258
    ## 2928  849  258
    ## 2929  862  258
    ## 2930  869  258
    ## 2931  886  258
    ## 2932  890  258
    ## 2933  894  258
    ## 2934  920  258
    ## 2935  946  258
    ## 2936  947  258
    ## 2937 1002  258
    ## 2938 1017  258
    ## 2939 1070  258
    ## 2940 1098  258
    ## 2941 1099  258
    ## 2942 1100  258
    ## 2943 1101  258
    ## 2944 1113  258
    ## 2945 1137  258
    ## 2946 1178  258
    ## 2947 1182  258
    ## 2949  290  260
    ## 2950  310  260
    ## 2951  341  260
    ## 2952  359  260
    ## 2953  364  260
    ## 2954  492  260
    ## 2955  494  260
    ## 2956  578  260
    ## 2957  583  260
    ## 2958  632  260
    ## 2959  643  260
    ## 2960  646  260
    ## 2961  647  260
    ## 2962  654  260
    ## 2963  661  260
    ## 2964  668  260
    ## 2965  680  260
    ## 2966  681  260
    ## 2967  686  260
    ## 2968  692  260
    ## 2969  698  260
    ## 2970  717  260
    ## 2971  737  260
    ## 2972  742  260
    ## 2973  745  260
    ## 2974  755  260
    ## 2975  757  260
    ## 2976  770  260
    ## 2977  775  260
    ## 2978  789  260
    ## 2979  793  260
    ## 2980  794  260
    ## 2981  799  260
    ## 2982  800  260
    ## 2983  803  260
    ## 2984  804  260
    ## 2985  814  260
    ## 2986  822  260
    ## 2987  828  260
    ## 2988  832  260
    ## 2989  833  260
    ## 2990  844  260
    ## 2991  849  260
    ## 2992  862  260
    ## 2993  869  260
    ## 2994  886  260
    ## 2995  890  260
    ## 2996  894  260
    ## 2997  920  260
    ## 2998  946  260
    ## 2999  947  260
    ## 3000 1002  260
    ## 3001 1017  260
    ## 3002 1070  260
    ## 3003 1098  260
    ## 3004 1099  260
    ## 3005 1100  260
    ## 3006 1101  260
    ## 3007 1113  260
    ## 3008 1137  260
    ## 3009 1178  260
    ## 3010 1182  260
    ## 3013  310  290
    ## 3014  341  290
    ## 3015  359  290
    ## 3016  364  290
    ## 3017  492  290
    ## 3018  494  290
    ## 3019  578  290
    ## 3020  583  290
    ## 3021  632  290
    ## 3022  643  290
    ## 3023  646  290
    ## 3024  647  290
    ## 3025  654  290
    ## 3026  661  290
    ## 3027  668  290
    ## 3028  680  290
    ## 3029  681  290
    ## 3030  686  290
    ## 3031  692  290
    ## 3032  698  290
    ## 3033  717  290
    ## 3034  737  290
    ## 3035  742  290
    ## 3036  745  290
    ## 3037  755  290
    ## 3038  757  290
    ## 3039  770  290
    ## 3040  775  290
    ## 3041  789  290
    ## 3042  793  290
    ## 3043  794  290
    ## 3044  799  290
    ## 3045  800  290
    ## 3046  803  290
    ## 3047  804  290
    ## 3048  814  290
    ## 3049  822  290
    ## 3050  828  290
    ## 3051  832  290
    ## 3052  833  290
    ## 3053  844  290
    ## 3054  849  290
    ## 3055  862  290
    ## 3056  869  290
    ## 3057  886  290
    ## 3058  890  290
    ## 3059  894  290
    ## 3060  920  290
    ## 3061  946  290
    ## 3062  947  290
    ## 3063 1002  290
    ## 3064 1017  290
    ## 3065 1070  290
    ## 3066 1098  290
    ## 3067 1099  290
    ## 3068 1100  290
    ## 3069 1101  290
    ## 3070 1113  290
    ## 3071 1137  290
    ## 3072 1178  290
    ## 3073 1182  290
    ## 3077  341  310
    ## 3078  359  310
    ## 3079  364  310
    ## 3080  492  310
    ## 3081  494  310
    ## 3082  578  310
    ## 3083  583  310
    ## 3084  632  310
    ## 3085  643  310
    ## 3086  646  310
    ## 3087  647  310
    ## 3088  654  310
    ## 3089  661  310
    ## 3090  668  310
    ## 3091  680  310
    ## 3092  681  310
    ## 3093  686  310
    ## 3094  692  310
    ## 3095  698  310
    ## 3096  717  310
    ## 3097  737  310
    ## 3098  742  310
    ## 3099  745  310
    ## 3100  755  310
    ## 3101  757  310
    ## 3102  770  310
    ## 3103  775  310
    ## 3104  789  310
    ## 3105  793  310
    ## 3106  794  310
    ## 3107  799  310
    ## 3108  800  310
    ## 3109  803  310
    ## 3110  804  310
    ## 3111  814  310
    ## 3112  822  310
    ## 3113  828  310
    ## 3114  832  310
    ## 3115  833  310
    ## 3116  844  310
    ## 3117  849  310
    ## 3118  862  310
    ## 3119  869  310
    ## 3120  886  310
    ## 3121  890  310
    ## 3122  894  310
    ## 3123  920  310
    ## 3124  946  310
    ## 3125  947  310
    ## 3126 1002  310
    ## 3127 1017  310
    ## 3128 1070  310
    ## 3129 1098  310
    ## 3130 1099  310
    ## 3131 1100  310
    ## 3132 1101  310
    ## 3133 1113  310
    ## 3134 1137  310
    ## 3135 1178  310
    ## 3136 1182  310
    ## 3141  359  341
    ## 3142  364  341
    ## 3143  492  341
    ## 3144  494  341
    ## 3145  578  341
    ## 3146  583  341
    ## 3147  632  341
    ## 3148  643  341
    ## 3149  646  341
    ## 3150  647  341
    ## 3151  654  341
    ## 3152  661  341
    ## 3153  668  341
    ## 3154  680  341
    ## 3155  681  341
    ## 3156  686  341
    ## 3157  692  341
    ## 3158  698  341
    ## 3159  717  341
    ## 3160  737  341
    ## 3161  742  341
    ## 3162  745  341
    ## 3163  755  341
    ## 3164  757  341
    ## 3165  770  341
    ## 3166  775  341
    ## 3167  789  341
    ## 3168  793  341
    ## 3169  794  341
    ## 3170  799  341
    ## 3171  800  341
    ## 3172  803  341
    ## 3173  804  341
    ## 3174  814  341
    ## 3175  822  341
    ## 3176  828  341
    ## 3177  832  341
    ## 3178  833  341
    ## 3179  844  341
    ## 3180  849  341
    ## 3181  862  341
    ## 3182  869  341
    ## 3183  886  341
    ## 3184  890  341
    ## 3185  894  341
    ## 3186  920  341
    ## 3187  946  341
    ## 3188  947  341
    ## 3189 1002  341
    ## 3190 1017  341
    ## 3191 1070  341
    ## 3192 1098  341
    ## 3193 1099  341
    ## 3194 1100  341
    ## 3195 1101  341
    ## 3196 1113  341
    ## 3197 1137  341
    ## 3198 1178  341
    ## 3199 1182  341
    ## 3205  364  359
    ## 3206  492  359
    ## 3207  494  359
    ## 3208  578  359
    ## 3209  583  359
    ## 3210  632  359
    ## 3211  643  359
    ## 3212  646  359
    ## 3213  647  359
    ## 3214  654  359
    ## 3215  661  359
    ## 3216  668  359
    ## 3217  680  359
    ## 3218  681  359
    ## 3219  686  359
    ## 3220  692  359
    ## 3221  698  359
    ## 3222  717  359
    ## 3223  737  359
    ## 3224  742  359
    ## 3225  745  359
    ## 3226  755  359
    ## 3227  757  359
    ## 3228  770  359
    ## 3229  775  359
    ## 3230  789  359
    ## 3231  793  359
    ## 3232  794  359
    ## 3233  799  359
    ## 3234  800  359
    ## 3235  803  359
    ## 3236  804  359
    ## 3237  814  359
    ## 3238  822  359
    ## 3239  828  359
    ## 3240  832  359
    ## 3241  833  359
    ## 3242  844  359
    ## 3243  849  359
    ## 3244  862  359
    ## 3245  869  359
    ## 3246  886  359
    ## 3247  890  359
    ## 3248  894  359
    ## 3249  920  359
    ## 3250  946  359
    ## 3251  947  359
    ## 3252 1002  359
    ## 3253 1017  359
    ## 3254 1070  359
    ## 3255 1098  359
    ## 3256 1099  359
    ## 3257 1100  359
    ## 3258 1101  359
    ## 3259 1113  359
    ## 3260 1137  359
    ## 3261 1178  359
    ## 3262 1182  359
    ## 3269  492  364
    ## 3270  494  364
    ## 3271  578  364
    ## 3272  583  364
    ## 3273  632  364
    ## 3274  643  364
    ## 3275  646  364
    ## 3276  647  364
    ## 3277  654  364
    ## 3278  661  364
    ## 3279  668  364
    ## 3280  680  364
    ## 3281  681  364
    ## 3282  686  364
    ## 3283  692  364
    ## 3284  698  364
    ## 3285  717  364
    ## 3286  737  364
    ## 3287  742  364
    ## 3288  745  364
    ## 3289  755  364
    ## 3290  757  364
    ## 3291  770  364
    ## 3292  775  364
    ## 3293  789  364
    ## 3294  793  364
    ## 3295  794  364
    ## 3296  799  364
    ## 3297  800  364
    ## 3298  803  364
    ## 3299  804  364
    ## 3300  814  364
    ## 3301  822  364
    ## 3302  828  364
    ## 3303  832  364
    ## 3304  833  364
    ## 3305  844  364
    ## 3306  849  364
    ## 3307  862  364
    ## 3308  869  364
    ## 3309  886  364
    ## 3310  890  364
    ## 3311  894  364
    ## 3312  920  364
    ## 3313  946  364
    ## 3314  947  364
    ## 3315 1002  364
    ## 3316 1017  364
    ## 3317 1070  364
    ## 3318 1098  364
    ## 3319 1099  364
    ## 3320 1100  364
    ## 3321 1101  364
    ## 3322 1113  364
    ## 3323 1137  364
    ## 3324 1178  364
    ## 3325 1182  364
    ## 3333  494  492
    ## 3334  578  492
    ## 3335  583  492
    ## 3336  632  492
    ## 3337  643  492
    ## 3338  646  492
    ## 3339  647  492
    ## 3340  654  492
    ## 3341  661  492
    ## 3342  668  492
    ## 3343  680  492
    ## 3344  681  492
    ## 3345  686  492
    ## 3346  692  492
    ## 3347  698  492
    ## 3348  717  492
    ## 3349  737  492
    ## 3350  742  492
    ## 3351  745  492
    ## 3352  755  492
    ## 3353  757  492
    ## 3354  770  492
    ## 3355  775  492
    ## 3356  789  492
    ## 3357  793  492
    ## 3358  794  492
    ## 3359  799  492
    ## 3360  800  492
    ## 3361  803  492
    ## 3362  804  492
    ## 3363  814  492
    ## 3364  822  492
    ## 3365  828  492
    ## 3366  832  492
    ## 3367  833  492
    ## 3368  844  492
    ## 3369  849  492
    ## 3370  862  492
    ## 3371  869  492
    ## 3372  886  492
    ## 3373  890  492
    ## 3374  894  492
    ## 3375  920  492
    ## 3376  946  492
    ## 3377  947  492
    ## 3378 1002  492
    ## 3379 1017  492
    ## 3380 1070  492
    ## 3381 1098  492
    ## 3382 1099  492
    ## 3383 1100  492
    ## 3384 1101  492
    ## 3385 1113  492
    ## 3386 1137  492
    ## 3387 1178  492
    ## 3388 1182  492
    ## 3397  578  494
    ## 3398  583  494
    ## 3399  632  494
    ## 3400  643  494
    ## 3401  646  494
    ## 3402  647  494
    ## 3403  654  494
    ## 3404  661  494
    ## 3405  668  494
    ## 3406  680  494
    ## 3407  681  494
    ## 3408  686  494
    ## 3409  692  494
    ## 3410  698  494
    ## 3411  717  494
    ## 3412  737  494
    ## 3413  742  494
    ## 3414  745  494
    ## 3415  755  494
    ## 3416  757  494
    ## 3417  770  494
    ## 3418  775  494
    ## 3419  789  494
    ## 3420  793  494
    ## 3421  794  494
    ## 3422  799  494
    ## 3423  800  494
    ## 3424  803  494
    ## 3425  804  494
    ## 3426  814  494
    ## 3427  822  494
    ## 3428  828  494
    ## 3429  832  494
    ## 3430  833  494
    ## 3431  844  494
    ## 3432  849  494
    ## 3433  862  494
    ## 3434  869  494
    ## 3435  886  494
    ## 3436  890  494
    ## 3437  894  494
    ## 3438  920  494
    ## 3439  946  494
    ## 3440  947  494
    ## 3441 1002  494
    ## 3442 1017  494
    ## 3443 1070  494
    ## 3444 1098  494
    ## 3445 1099  494
    ## 3446 1100  494
    ## 3447 1101  494
    ## 3448 1113  494
    ## 3449 1137  494
    ## 3450 1178  494
    ## 3451 1182  494
    ## 3461  583  578
    ## 3462  632  578
    ## 3463  643  578
    ## 3464  646  578
    ## 3465  647  578
    ## 3466  654  578
    ## 3467  661  578
    ## 3468  668  578
    ## 3469  680  578
    ## 3470  681  578
    ## 3471  686  578
    ## 3472  692  578
    ## 3473  698  578
    ## 3474  717  578
    ## 3475  737  578
    ## 3476  742  578
    ## 3477  745  578
    ## 3478  755  578
    ## 3479  757  578
    ## 3480  770  578
    ## 3481  775  578
    ## 3482  789  578
    ## 3483  793  578
    ## 3484  794  578
    ## 3485  799  578
    ## 3486  800  578
    ## 3487  803  578
    ## 3488  804  578
    ## 3489  814  578
    ## 3490  822  578
    ## 3491  828  578
    ## 3492  832  578
    ## 3493  833  578
    ## 3494  844  578
    ## 3495  849  578
    ## 3496  862  578
    ## 3497  869  578
    ## 3498  886  578
    ## 3499  890  578
    ## 3500  894  578
    ## 3501  920  578
    ## 3502  946  578
    ## 3503  947  578
    ## 3504 1002  578
    ## 3505 1017  578
    ## 3506 1070  578
    ## 3507 1098  578
    ## 3508 1099  578
    ## 3509 1100  578
    ## 3510 1101  578
    ## 3511 1113  578
    ## 3512 1137  578
    ## 3513 1178  578
    ## 3514 1182  578
    ## 3525  632  583
    ## 3526  643  583
    ## 3527  646  583
    ## 3528  647  583
    ## 3529  654  583
    ## 3530  661  583
    ## 3531  668  583
    ## 3532  680  583
    ## 3533  681  583
    ## 3534  686  583
    ## 3535  692  583
    ## 3536  698  583
    ## 3537  717  583
    ## 3538  737  583
    ## 3539  742  583
    ## 3540  745  583
    ## 3541  755  583
    ## 3542  757  583
    ## 3543  770  583
    ## 3544  775  583
    ## 3545  789  583
    ## 3546  793  583
    ## 3547  794  583
    ## 3548  799  583
    ## 3549  800  583
    ## 3550  803  583
    ## 3551  804  583
    ## 3552  814  583
    ## 3553  822  583
    ## 3554  828  583
    ## 3555  832  583
    ## 3556  833  583
    ## 3557  844  583
    ## 3558  849  583
    ## 3559  862  583
    ## 3560  869  583
    ## 3561  886  583
    ## 3562  890  583
    ## 3563  894  583
    ## 3564  920  583
    ## 3565  946  583
    ## 3566  947  583
    ## 3567 1002  583
    ## 3568 1017  583
    ## 3569 1070  583
    ## 3570 1098  583
    ## 3571 1099  583
    ## 3572 1100  583
    ## 3573 1101  583
    ## 3574 1113  583
    ## 3575 1137  583
    ## 3576 1178  583
    ## 3577 1182  583
    ## 3589  643  632
    ## 3590  646  632
    ## 3591  647  632
    ## 3592  654  632
    ## 3593  661  632
    ## 3594  668  632
    ## 3595  680  632
    ## 3596  681  632
    ## 3597  686  632
    ## 3598  692  632
    ## 3599  698  632
    ## 3600  717  632
    ## 3601  737  632
    ## 3602  742  632
    ## 3603  745  632
    ## 3604  755  632
    ## 3605  757  632
    ## 3606  770  632
    ## 3607  775  632
    ## 3608  789  632
    ## 3609  793  632
    ## 3610  794  632
    ## 3611  799  632
    ## 3612  800  632
    ## 3613  803  632
    ## 3614  804  632
    ## 3615  814  632
    ## 3616  822  632
    ## 3617  828  632
    ## 3618  832  632
    ## 3619  833  632
    ## 3620  844  632
    ## 3621  849  632
    ## 3622  862  632
    ## 3623  869  632
    ## 3624  886  632
    ## 3625  890  632
    ## 3626  894  632
    ## 3627  920  632
    ## 3628  946  632
    ## 3629  947  632
    ## 3630 1002  632
    ## 3631 1017  632
    ## 3632 1070  632
    ## 3633 1098  632
    ## 3634 1099  632
    ## 3635 1100  632
    ## 3636 1101  632
    ## 3637 1113  632
    ## 3638 1137  632
    ## 3639 1178  632
    ## 3640 1182  632
    ## 3653  646  643
    ## 3654  647  643
    ## 3655  654  643
    ## 3656  661  643
    ## 3657  668  643
    ## 3658  680  643
    ## 3659  681  643
    ## 3660  686  643
    ## 3661  692  643
    ## 3662  698  643
    ## 3663  717  643
    ## 3664  737  643
    ## 3665  742  643
    ## 3666  745  643
    ## 3667  755  643
    ## 3668  757  643
    ## 3669  770  643
    ## 3670  775  643
    ## 3671  789  643
    ## 3672  793  643
    ## 3673  794  643
    ## 3674  799  643
    ## 3675  800  643
    ## 3676  803  643
    ## 3677  804  643
    ## 3678  814  643
    ## 3679  822  643
    ## 3680  828  643
    ## 3681  832  643
    ## 3682  833  643
    ## 3683  844  643
    ## 3684  849  643
    ## 3685  862  643
    ## 3686  869  643
    ## 3687  886  643
    ## 3688  890  643
    ## 3689  894  643
    ## 3690  920  643
    ## 3691  946  643
    ## 3692  947  643
    ## 3693 1002  643
    ## 3694 1017  643
    ## 3695 1070  643
    ## 3696 1098  643
    ## 3697 1099  643
    ## 3698 1100  643
    ## 3699 1101  643
    ## 3700 1113  643
    ## 3701 1137  643
    ## 3702 1178  643
    ## 3703 1182  643
    ## 3717  647  646
    ## 3718  654  646
    ## 3719  661  646
    ## 3720  668  646
    ## 3721  680  646
    ## 3722  681  646
    ## 3723  686  646
    ## 3724  692  646
    ## 3725  698  646
    ## 3726  717  646
    ## 3727  737  646
    ## 3728  742  646
    ## 3729  745  646
    ## 3730  755  646
    ## 3731  757  646
    ## 3732  770  646
    ## 3733  775  646
    ## 3734  789  646
    ## 3735  793  646
    ## 3736  794  646
    ## 3737  799  646
    ## 3738  800  646
    ## 3739  803  646
    ## 3740  804  646
    ## 3741  814  646
    ## 3742  822  646
    ## 3743  828  646
    ## 3744  832  646
    ## 3745  833  646
    ## 3746  844  646
    ## 3747  849  646
    ## 3748  862  646
    ## 3749  869  646
    ## 3750  886  646
    ## 3751  890  646
    ## 3752  894  646
    ## 3753  920  646
    ## 3754  946  646
    ## 3755  947  646
    ## 3756 1002  646
    ## 3757 1017  646
    ## 3758 1070  646
    ## 3759 1098  646
    ## 3760 1099  646
    ## 3761 1100  646
    ## 3762 1101  646
    ## 3763 1113  646
    ## 3764 1137  646
    ## 3765 1178  646
    ## 3766 1182  646
    ## 3781  654  647
    ## 3782  661  647
    ## 3783  668  647
    ## 3784  680  647
    ## 3785  681  647
    ## 3786  686  647
    ## 3787  692  647
    ## 3788  698  647
    ## 3789  717  647
    ## 3790  737  647
    ## 3791  742  647
    ## 3792  745  647
    ## 3793  755  647
    ## 3794  757  647
    ## 3795  770  647
    ## 3796  775  647
    ## 3797  789  647
    ## 3798  793  647
    ## 3799  794  647
    ## 3800  799  647
    ## 3801  800  647
    ## 3802  803  647
    ## 3803  804  647
    ## 3804  814  647
    ## 3805  822  647
    ## 3806  828  647
    ## 3807  832  647
    ## 3808  833  647
    ## 3809  844  647
    ## 3810  849  647
    ## 3811  862  647
    ## 3812  869  647
    ## 3813  886  647
    ## 3814  890  647
    ## 3815  894  647
    ## 3816  920  647
    ## 3817  946  647
    ## 3818  947  647
    ## 3819 1002  647
    ## 3820 1017  647
    ## 3821 1070  647
    ## 3822 1098  647
    ## 3823 1099  647
    ## 3824 1100  647
    ## 3825 1101  647
    ## 3826 1113  647
    ## 3827 1137  647
    ## 3828 1178  647
    ## 3829 1182  647
    ## 3845  661  654
    ## 3846  668  654
    ## 3847  680  654
    ## 3848  681  654
    ## 3849  686  654
    ## 3850  692  654
    ## 3851  698  654
    ## 3852  717  654
    ## 3853  737  654
    ## 3854  742  654
    ## 3855  745  654
    ## 3856  755  654
    ## 3857  757  654
    ## 3858  770  654
    ## 3859  775  654
    ## 3860  789  654
    ## 3861  793  654
    ## 3862  794  654
    ## 3863  799  654
    ## 3864  800  654
    ## 3865  803  654
    ## 3866  804  654
    ## 3867  814  654
    ## 3868  822  654
    ## 3869  828  654
    ## 3870  832  654
    ## 3871  833  654
    ## 3872  844  654
    ## 3873  849  654
    ## 3874  862  654
    ## 3875  869  654
    ## 3876  886  654
    ## 3877  890  654
    ## 3878  894  654
    ## 3879  920  654
    ## 3880  946  654
    ## 3881  947  654
    ## 3882 1002  654
    ## 3883 1017  654
    ## 3884 1070  654
    ## 3885 1098  654
    ## 3886 1099  654
    ## 3887 1100  654
    ## 3888 1101  654
    ## 3889 1113  654
    ## 3890 1137  654
    ## 3891 1178  654
    ## 3892 1182  654
    ## 3909  668  661
    ## 3910  680  661
    ## 3911  681  661
    ## 3912  686  661
    ## 3913  692  661
    ## 3914  698  661
    ## 3915  717  661
    ## 3916  737  661
    ## 3917  742  661
    ## 3918  745  661
    ## 3919  755  661
    ## 3920  757  661
    ## 3921  770  661
    ## 3922  775  661
    ## 3923  789  661
    ## 3924  793  661
    ## 3925  794  661
    ## 3926  799  661
    ## 3927  800  661
    ## 3928  803  661
    ## 3929  804  661
    ## 3930  814  661
    ## 3931  822  661
    ## 3932  828  661
    ## 3933  832  661
    ## 3934  833  661
    ## 3935  844  661
    ## 3936  849  661
    ## 3937  862  661
    ## 3938  869  661
    ## 3939  886  661
    ## 3940  890  661
    ## 3941  894  661
    ## 3942  920  661
    ## 3943  946  661
    ## 3944  947  661
    ## 3945 1002  661
    ## 3946 1017  661
    ## 3947 1070  661
    ## 3948 1098  661
    ## 3949 1099  661
    ## 3950 1100  661
    ## 3951 1101  661
    ## 3952 1113  661
    ## 3953 1137  661
    ## 3954 1178  661
    ## 3955 1182  661
    ## 3973  680  668
    ## 3974  681  668
    ## 3975  686  668
    ## 3976  692  668
    ## 3977  698  668
    ## 3978  717  668
    ## 3979  737  668
    ## 3980  742  668
    ## 3981  745  668
    ## 3982  755  668
    ## 3983  757  668
    ## 3984  770  668
    ## 3985  775  668
    ## 3986  789  668
    ## 3987  793  668
    ## 3988  794  668
    ## 3989  799  668
    ## 3990  800  668
    ## 3991  803  668
    ## 3992  804  668
    ## 3993  814  668
    ## 3994  822  668
    ## 3995  828  668
    ## 3996  832  668
    ## 3997  833  668
    ## 3998  844  668
    ## 3999  849  668
    ## 4000  862  668
    ## 4001  869  668
    ## 4002  886  668
    ## 4003  890  668
    ## 4004  894  668
    ## 4005  920  668
    ## 4006  946  668
    ## 4007  947  668
    ## 4008 1002  668
    ## 4009 1017  668
    ## 4010 1070  668
    ## 4011 1098  668
    ## 4012 1099  668
    ## 4013 1100  668
    ## 4014 1101  668
    ## 4015 1113  668
    ## 4016 1137  668
    ## 4017 1178  668
    ## 4018 1182  668
    ## 4037  681  680
    ## 4038  686  680
    ## 4039  692  680
    ## 4040  698  680
    ## 4041  717  680
    ## 4042  737  680
    ## 4043  742  680
    ## 4044  745  680
    ## 4045  755  680
    ## 4046  757  680
    ## 4047  770  680
    ## 4048  775  680
    ## 4049  789  680
    ## 4050  793  680
    ## 4051  794  680
    ## 4052  799  680
    ## 4053  800  680
    ## 4054  803  680
    ## 4055  804  680
    ## 4056  814  680
    ## 4057  822  680
    ## 4058  828  680
    ## 4059  832  680
    ## 4060  833  680
    ## 4061  844  680
    ## 4062  849  680
    ## 4063  862  680
    ## 4064  869  680
    ## 4065  886  680
    ## 4066  890  680
    ## 4067  894  680
    ## 4068  920  680
    ## 4069  946  680
    ## 4070  947  680
    ## 4071 1002  680
    ## 4072 1017  680
    ## 4073 1070  680
    ## 4074 1098  680
    ## 4075 1099  680
    ## 4076 1100  680
    ## 4077 1101  680
    ## 4078 1113  680
    ## 4079 1137  680
    ## 4080 1178  680
    ## 4081 1182  680
    ## 4101  686  681
    ## 4102  692  681
    ## 4103  698  681
    ## 4104  717  681
    ## 4105  737  681
    ## 4106  742  681
    ## 4107  745  681
    ## 4108  755  681
    ## 4109  757  681
    ## 4110  770  681
    ## 4111  775  681
    ## 4112  789  681
    ## 4113  793  681
    ## 4114  794  681
    ## 4115  799  681
    ## 4116  800  681
    ## 4117  803  681
    ## 4118  804  681
    ## 4119  814  681
    ## 4120  822  681
    ## 4121  828  681
    ## 4122  832  681
    ## 4123  833  681
    ## 4124  844  681
    ## 4125  849  681
    ## 4126  862  681
    ## 4127  869  681
    ## 4128  886  681
    ## 4129  890  681
    ## 4130  894  681
    ## 4131  920  681
    ## 4132  946  681
    ## 4133  947  681
    ## 4134 1002  681
    ## 4135 1017  681
    ## 4136 1070  681
    ## 4137 1098  681
    ## 4138 1099  681
    ## 4139 1100  681
    ## 4140 1101  681
    ## 4141 1113  681
    ## 4142 1137  681
    ## 4143 1178  681
    ## 4144 1182  681
    ## 4165  692  686
    ## 4166  698  686
    ## 4167  717  686
    ## 4168  737  686
    ## 4169  742  686
    ## 4170  745  686
    ## 4171  755  686
    ## 4172  757  686
    ## 4173  770  686
    ## 4174  775  686
    ## 4175  789  686
    ## 4176  793  686
    ## 4177  794  686
    ## 4178  799  686
    ## 4179  800  686
    ## 4180  803  686
    ## 4181  804  686
    ## 4182  814  686
    ## 4183  822  686
    ## 4184  828  686
    ## 4185  832  686
    ## 4186  833  686
    ## 4187  844  686
    ## 4188  849  686
    ## 4189  862  686
    ## 4190  869  686
    ## 4191  886  686
    ## 4192  890  686
    ## 4193  894  686
    ## 4194  920  686
    ## 4195  946  686
    ## 4196  947  686
    ## 4197 1002  686
    ## 4198 1017  686
    ## 4199 1070  686
    ## 4200 1098  686
    ## 4201 1099  686
    ## 4202 1100  686
    ## 4203 1101  686
    ## 4204 1113  686
    ## 4205 1137  686
    ## 4206 1178  686
    ## 4207 1182  686
    ## 4229  698  692
    ## 4230  717  692
    ## 4231  737  692
    ## 4232  742  692
    ## 4233  745  692
    ## 4234  755  692
    ## 4235  757  692
    ## 4236  770  692
    ## 4237  775  692
    ## 4238  789  692
    ## 4239  793  692
    ## 4240  794  692
    ## 4241  799  692
    ## 4242  800  692
    ## 4243  803  692
    ## 4244  804  692
    ## 4245  814  692
    ## 4246  822  692
    ## 4247  828  692
    ## 4248  832  692
    ## 4249  833  692
    ## 4250  844  692
    ## 4251  849  692
    ## 4252  862  692
    ## 4253  869  692
    ## 4254  886  692
    ## 4255  890  692
    ## 4256  894  692
    ## 4257  920  692
    ## 4258  946  692
    ## 4259  947  692
    ## 4260 1002  692
    ## 4261 1017  692
    ## 4262 1070  692
    ## 4263 1098  692
    ## 4264 1099  692
    ## 4265 1100  692
    ## 4266 1101  692
    ## 4267 1113  692
    ## 4268 1137  692
    ## 4269 1178  692
    ## 4270 1182  692
    ## 4293  717  698
    ## 4294  737  698
    ## 4295  742  698
    ## 4296  745  698
    ## 4297  755  698
    ## 4298  757  698
    ## 4299  770  698
    ## 4300  775  698
    ## 4301  789  698
    ## 4302  793  698
    ## 4303  794  698
    ## 4304  799  698
    ## 4305  800  698
    ## 4306  803  698
    ## 4307  804  698
    ## 4308  814  698
    ## 4309  822  698
    ## 4310  828  698
    ## 4311  832  698
    ## 4312  833  698
    ## 4313  844  698
    ## 4314  849  698
    ## 4315  862  698
    ## 4316  869  698
    ## 4317  886  698
    ## 4318  890  698
    ## 4319  894  698
    ## 4320  920  698
    ## 4321  946  698
    ## 4322  947  698
    ## 4323 1002  698
    ## 4324 1017  698
    ## 4325 1070  698
    ## 4326 1098  698
    ## 4327 1099  698
    ## 4328 1100  698
    ## 4329 1101  698
    ## 4330 1113  698
    ## 4331 1137  698
    ## 4332 1178  698
    ## 4333 1182  698
    ## 4357  737  717
    ## 4358  742  717
    ## 4359  745  717
    ## 4360  755  717
    ## 4361  757  717
    ## 4362  770  717
    ## 4363  775  717
    ## 4364  789  717
    ## 4365  793  717
    ## 4366  794  717
    ## 4367  799  717
    ## 4368  800  717
    ## 4369  803  717
    ## 4370  804  717
    ## 4371  814  717
    ## 4372  822  717
    ## 4373  828  717
    ## 4374  832  717
    ## 4375  833  717
    ## 4376  844  717
    ## 4377  849  717
    ## 4378  862  717
    ## 4379  869  717
    ## 4380  886  717
    ## 4381  890  717
    ## 4382  894  717
    ## 4383  920  717
    ## 4384  946  717
    ## 4385  947  717
    ## 4386 1002  717
    ## 4387 1017  717
    ## 4388 1070  717
    ## 4389 1098  717
    ## 4390 1099  717
    ## 4391 1100  717
    ## 4392 1101  717
    ## 4393 1113  717
    ## 4394 1137  717
    ## 4395 1178  717
    ## 4396 1182  717
    ## 4421  742  737
    ## 4422  745  737
    ## 4423  755  737
    ## 4424  757  737
    ## 4425  770  737
    ## 4426  775  737
    ## 4427  789  737
    ## 4428  793  737
    ## 4429  794  737
    ## 4430  799  737
    ## 4431  800  737
    ## 4432  803  737
    ## 4433  804  737
    ## 4434  814  737
    ## 4435  822  737
    ## 4436  828  737
    ## 4437  832  737
    ## 4438  833  737
    ## 4439  844  737
    ## 4440  849  737
    ## 4441  862  737
    ## 4442  869  737
    ## 4443  886  737
    ## 4444  890  737
    ## 4445  894  737
    ## 4446  920  737
    ## 4447  946  737
    ## 4448  947  737
    ## 4449 1002  737
    ## 4450 1017  737
    ## 4451 1070  737
    ## 4452 1098  737
    ## 4453 1099  737
    ## 4454 1100  737
    ## 4455 1101  737
    ## 4456 1113  737
    ## 4457 1137  737
    ## 4458 1178  737
    ## 4459 1182  737
    ## 4485  745  742
    ## 4486  755  742
    ## 4487  757  742
    ## 4488  770  742
    ## 4489  775  742
    ## 4490  789  742
    ## 4491  793  742
    ## 4492  794  742
    ## 4493  799  742
    ## 4494  800  742
    ## 4495  803  742
    ## 4496  804  742
    ## 4497  814  742
    ## 4498  822  742
    ## 4499  828  742
    ## 4500  832  742
    ## 4501  833  742
    ## 4502  844  742
    ## 4503  849  742
    ## 4504  862  742
    ## 4505  869  742
    ## 4506  886  742
    ## 4507  890  742
    ## 4508  894  742
    ## 4509  920  742
    ## 4510  946  742
    ## 4511  947  742
    ## 4512 1002  742
    ## 4513 1017  742
    ## 4514 1070  742
    ## 4515 1098  742
    ## 4516 1099  742
    ## 4517 1100  742
    ## 4518 1101  742
    ## 4519 1113  742
    ## 4520 1137  742
    ## 4521 1178  742
    ## 4522 1182  742
    ## 4549  755  745
    ## 4550  757  745
    ## 4551  770  745
    ## 4552  775  745
    ## 4553  789  745
    ## 4554  793  745
    ## 4555  794  745
    ## 4556  799  745
    ## 4557  800  745
    ## 4558  803  745
    ## 4559  804  745
    ## 4560  814  745
    ## 4561  822  745
    ## 4562  828  745
    ## 4563  832  745
    ## 4564  833  745
    ## 4565  844  745
    ## 4566  849  745
    ## 4567  862  745
    ## 4568  869  745
    ## 4569  886  745
    ## 4570  890  745
    ## 4571  894  745
    ## 4572  920  745
    ## 4573  946  745
    ## 4574  947  745
    ## 4575 1002  745
    ## 4576 1017  745
    ## 4577 1070  745
    ## 4578 1098  745
    ## 4579 1099  745
    ## 4580 1100  745
    ## 4581 1101  745
    ## 4582 1113  745
    ## 4583 1137  745
    ## 4584 1178  745
    ## 4585 1182  745
    ## 4613  757  755
    ## 4614  770  755
    ## 4615  775  755
    ## 4616  789  755
    ## 4617  793  755
    ## 4618  794  755
    ## 4619  799  755
    ## 4620  800  755
    ## 4621  803  755
    ## 4622  804  755
    ## 4623  814  755
    ## 4624  822  755
    ## 4625  828  755
    ## 4626  832  755
    ## 4627  833  755
    ## 4628  844  755
    ## 4629  849  755
    ## 4630  862  755
    ## 4631  869  755
    ## 4632  886  755
    ## 4633  890  755
    ## 4634  894  755
    ## 4635  920  755
    ## 4636  946  755
    ## 4637  947  755
    ## 4638 1002  755
    ## 4639 1017  755
    ## 4640 1070  755
    ## 4641 1098  755
    ## 4642 1099  755
    ## 4643 1100  755
    ## 4644 1101  755
    ## 4645 1113  755
    ## 4646 1137  755
    ## 4647 1178  755
    ## 4648 1182  755
    ## 4677  770  757
    ## 4678  775  757
    ## 4679  789  757
    ## 4680  793  757
    ## 4681  794  757
    ## 4682  799  757
    ## 4683  800  757
    ## 4684  803  757
    ## 4685  804  757
    ## 4686  814  757
    ## 4687  822  757
    ## 4688  828  757
    ## 4689  832  757
    ## 4690  833  757
    ## 4691  844  757
    ## 4692  849  757
    ## 4693  862  757
    ## 4694  869  757
    ## 4695  886  757
    ## 4696  890  757
    ## 4697  894  757
    ## 4698  920  757
    ## 4699  946  757
    ## 4700  947  757
    ## 4701 1002  757
    ## 4702 1017  757
    ## 4703 1070  757
    ## 4704 1098  757
    ## 4705 1099  757
    ## 4706 1100  757
    ## 4707 1101  757
    ## 4708 1113  757
    ## 4709 1137  757
    ## 4710 1178  757
    ## 4711 1182  757
    ## 4741  775  770
    ## 4742  789  770
    ## 4743  793  770
    ## 4744  794  770
    ## 4745  799  770
    ## 4746  800  770
    ## 4747  803  770
    ## 4748  804  770
    ## 4749  814  770
    ## 4750  822  770
    ## 4751  828  770
    ## 4752  832  770
    ## 4753  833  770
    ## 4754  844  770
    ## 4755  849  770
    ## 4756  862  770
    ## 4757  869  770
    ## 4758  886  770
    ## 4759  890  770
    ## 4760  894  770
    ## 4761  920  770
    ## 4762  946  770
    ## 4763  947  770
    ## 4764 1002  770
    ## 4765 1017  770
    ## 4766 1070  770
    ## 4767 1098  770
    ## 4768 1099  770
    ## 4769 1100  770
    ## 4770 1101  770
    ## 4771 1113  770
    ## 4772 1137  770
    ## 4773 1178  770
    ## 4774 1182  770
    ## 4805  789  775
    ## 4806  793  775
    ## 4807  794  775
    ## 4808  799  775
    ## 4809  800  775
    ## 4810  803  775
    ## 4811  804  775
    ## 4812  814  775
    ## 4813  822  775
    ## 4814  828  775
    ## 4815  832  775
    ## 4816  833  775
    ## 4817  844  775
    ## 4818  849  775
    ## 4819  862  775
    ## 4820  869  775
    ## 4821  886  775
    ## 4822  890  775
    ## 4823  894  775
    ## 4824  920  775
    ## 4825  946  775
    ## 4826  947  775
    ## 4827 1002  775
    ## 4828 1017  775
    ## 4829 1070  775
    ## 4830 1098  775
    ## 4831 1099  775
    ## 4832 1100  775
    ## 4833 1101  775
    ## 4834 1113  775
    ## 4835 1137  775
    ## 4836 1178  775
    ## 4837 1182  775
    ## 4869  793  789
    ## 4870  794  789
    ## 4871  799  789
    ## 4872  800  789
    ## 4873  803  789
    ## 4874  804  789
    ## 4875  814  789
    ## 4876  822  789
    ## 4877  828  789
    ## 4878  832  789
    ## 4879  833  789
    ## 4880  844  789
    ## 4881  849  789
    ## 4882  862  789
    ## 4883  869  789
    ## 4884  886  789
    ## 4885  890  789
    ## 4886  894  789
    ## 4887  920  789
    ## 4888  946  789
    ## 4889  947  789
    ## 4890 1002  789
    ## 4891 1017  789
    ## 4892 1070  789
    ## 4893 1098  789
    ## 4894 1099  789
    ## 4895 1100  789
    ## 4896 1101  789
    ## 4897 1113  789
    ## 4898 1137  789
    ## 4899 1178  789
    ## 4900 1182  789
    ## 4933  794  793
    ## 4934  799  793
    ## 4935  800  793
    ## 4936  803  793
    ## 4937  804  793
    ## 4938  814  793
    ## 4939  822  793
    ## 4940  828  793
    ## 4941  832  793
    ## 4942  833  793
    ## 4943  844  793
    ## 4944  849  793
    ## 4945  862  793
    ## 4946  869  793
    ## 4947  886  793
    ## 4948  890  793
    ## 4949  894  793
    ## 4950  920  793
    ## 4951  946  793
    ## 4952  947  793
    ## 4953 1002  793
    ## 4954 1017  793
    ## 4955 1070  793
    ## 4956 1098  793
    ## 4957 1099  793
    ## 4958 1100  793
    ## 4959 1101  793
    ## 4960 1113  793
    ## 4961 1137  793
    ## 4962 1178  793
    ## 4963 1182  793
    ## 4997  799  794
    ## 4998  800  794
    ## 4999  803  794
    ## 5000  804  794
    ## 5001  814  794
    ## 5002  822  794
    ## 5003  828  794
    ## 5004  832  794
    ## 5005  833  794
    ## 5006  844  794
    ## 5007  849  794
    ## 5008  862  794
    ## 5009  869  794
    ## 5010  886  794
    ## 5011  890  794
    ## 5012  894  794
    ## 5013  920  794
    ## 5014  946  794
    ## 5015  947  794
    ## 5016 1002  794
    ## 5017 1017  794
    ## 5018 1070  794
    ## 5019 1098  794
    ## 5020 1099  794
    ## 5021 1100  794
    ## 5022 1101  794
    ## 5023 1113  794
    ## 5024 1137  794
    ## 5025 1178  794
    ## 5026 1182  794
    ## 5061  800  799
    ## 5062  803  799
    ## 5063  804  799
    ## 5064  814  799
    ## 5065  822  799
    ## 5066  828  799
    ## 5067  832  799
    ## 5068  833  799
    ## 5069  844  799
    ## 5070  849  799
    ## 5071  862  799
    ## 5072  869  799
    ## 5073  886  799
    ## 5074  890  799
    ## 5075  894  799
    ## 5076  920  799
    ## 5077  946  799
    ## 5078  947  799
    ## 5079 1002  799
    ## 5080 1017  799
    ## 5081 1070  799
    ## 5082 1098  799
    ## 5083 1099  799
    ## 5084 1100  799
    ## 5085 1101  799
    ## 5086 1113  799
    ## 5087 1137  799
    ## 5088 1178  799
    ## 5089 1182  799
    ## 5125  803  800
    ## 5126  804  800
    ## 5127  814  800
    ## 5128  822  800
    ## 5129  828  800
    ## 5130  832  800
    ## 5131  833  800
    ## 5132  844  800
    ## 5133  849  800
    ## 5134  862  800
    ## 5135  869  800
    ## 5136  886  800
    ## 5137  890  800
    ## 5138  894  800
    ## 5139  920  800
    ## 5140  946  800
    ## 5141  947  800
    ## 5142 1002  800
    ## 5143 1017  800
    ## 5144 1070  800
    ## 5145 1098  800
    ## 5146 1099  800
    ## 5147 1100  800
    ## 5148 1101  800
    ## 5149 1113  800
    ## 5150 1137  800
    ## 5151 1178  800
    ## 5152 1182  800
    ## 5189  804  803
    ## 5190  814  803
    ## 5191  822  803
    ## 5192  828  803
    ## 5193  832  803
    ## 5194  833  803
    ## 5195  844  803
    ## 5196  849  803
    ## 5197  862  803
    ## 5198  869  803
    ## 5199  886  803
    ## 5200  890  803
    ## 5201  894  803
    ## 5202  920  803
    ## 5203  946  803
    ## 5204  947  803
    ## 5205 1002  803
    ## 5206 1017  803
    ## 5207 1070  803
    ## 5208 1098  803
    ## 5209 1099  803
    ## 5210 1100  803
    ## 5211 1101  803
    ## 5212 1113  803
    ## 5213 1137  803
    ## 5214 1178  803
    ## 5215 1182  803
    ## 5253  814  804
    ## 5254  822  804
    ## 5255  828  804
    ## 5256  832  804
    ## 5257  833  804
    ## 5258  844  804
    ## 5259  849  804
    ## 5260  862  804
    ## 5261  869  804
    ## 5262  886  804
    ## 5263  890  804
    ## 5264  894  804
    ## 5265  920  804
    ## 5266  946  804
    ## 5267  947  804
    ## 5268 1002  804
    ## 5269 1017  804
    ## 5270 1070  804
    ## 5271 1098  804
    ## 5272 1099  804
    ## 5273 1100  804
    ## 5274 1101  804
    ## 5275 1113  804
    ## 5276 1137  804
    ## 5277 1178  804
    ## 5278 1182  804
    ## 5317  822  814
    ## 5318  828  814
    ## 5319  832  814
    ## 5320  833  814
    ## 5321  844  814
    ## 5322  849  814
    ## 5323  862  814
    ## 5324  869  814
    ## 5325  886  814
    ## 5326  890  814
    ## 5327  894  814
    ## 5328  920  814
    ## 5329  946  814
    ## 5330  947  814
    ## 5331 1002  814
    ## 5332 1017  814
    ## 5333 1070  814
    ## 5334 1098  814
    ## 5335 1099  814
    ## 5336 1100  814
    ## 5337 1101  814
    ## 5338 1113  814
    ## 5339 1137  814
    ## 5340 1178  814
    ## 5341 1182  814
    ## 5381  828  822
    ## 5382  832  822
    ## 5383  833  822
    ## 5384  844  822
    ## 5385  849  822
    ## 5386  862  822
    ## 5387  869  822
    ## 5388  886  822
    ## 5389  890  822
    ## 5390  894  822
    ## 5391  920  822
    ## 5392  946  822
    ## 5393  947  822
    ## 5394 1002  822
    ## 5395 1017  822
    ## 5396 1070  822
    ## 5397 1098  822
    ## 5398 1099  822
    ## 5399 1100  822
    ## 5400 1101  822
    ## 5401 1113  822
    ## 5402 1137  822
    ## 5403 1178  822
    ## 5404 1182  822
    ## 5445  832  828
    ## 5446  833  828
    ## 5447  844  828
    ## 5448  849  828
    ## 5449  862  828
    ## 5450  869  828
    ## 5451  886  828
    ## 5452  890  828
    ## 5453  894  828
    ## 5454  920  828
    ## 5455  946  828
    ## 5456  947  828
    ## 5457 1002  828
    ## 5458 1017  828
    ## 5459 1070  828
    ## 5460 1098  828
    ## 5461 1099  828
    ## 5462 1100  828
    ## 5463 1101  828
    ## 5464 1113  828
    ## 5465 1137  828
    ## 5466 1178  828
    ## 5467 1182  828
    ## 5509  833  832
    ## 5510  844  832
    ## 5511  849  832
    ## 5512  862  832
    ## 5513  869  832
    ## 5514  886  832
    ## 5515  890  832
    ## 5516  894  832
    ## 5517  920  832
    ## 5518  946  832
    ## 5519  947  832
    ## 5520 1002  832
    ## 5521 1017  832
    ## 5522 1070  832
    ## 5523 1098  832
    ## 5524 1099  832
    ## 5525 1100  832
    ## 5526 1101  832
    ## 5527 1113  832
    ## 5528 1137  832
    ## 5529 1178  832
    ## 5530 1182  832
    ## 5573  844  833
    ## 5574  849  833
    ## 5575  862  833
    ## 5576  869  833
    ## 5577  886  833
    ## 5578  890  833
    ## 5579  894  833
    ## 5580  920  833
    ## 5581  946  833
    ## 5582  947  833
    ## 5583 1002  833
    ## 5584 1017  833
    ## 5585 1070  833
    ## 5586 1098  833
    ## 5587 1099  833
    ## 5588 1100  833
    ## 5589 1101  833
    ## 5590 1113  833
    ## 5591 1137  833
    ## 5592 1178  833
    ## 5593 1182  833
    ## 5637  849  844
    ## 5638  862  844
    ## 5639  869  844
    ## 5640  886  844
    ## 5641  890  844
    ## 5642  894  844
    ## 5643  920  844
    ## 5644  946  844
    ## 5645  947  844
    ## 5646 1002  844
    ## 5647 1017  844
    ## 5648 1070  844
    ## 5649 1098  844
    ## 5650 1099  844
    ## 5651 1100  844
    ## 5652 1101  844
    ## 5653 1113  844
    ## 5654 1137  844
    ## 5655 1178  844
    ## 5656 1182  844
    ## 5701  862  849
    ## 5702  869  849
    ## 5703  886  849
    ## 5704  890  849
    ## 5705  894  849
    ## 5706  920  849
    ## 5707  946  849
    ## 5708  947  849
    ## 5709 1002  849
    ## 5710 1017  849
    ## 5711 1070  849
    ## 5712 1098  849
    ## 5713 1099  849
    ## 5714 1100  849
    ## 5715 1101  849
    ## 5716 1113  849
    ## 5717 1137  849
    ## 5718 1178  849
    ## 5719 1182  849
    ## 5765  869  862
    ## 5766  886  862
    ## 5767  890  862
    ## 5768  894  862
    ## 5769  920  862
    ## 5770  946  862
    ## 5771  947  862
    ## 5772 1002  862
    ## 5773 1017  862
    ## 5774 1070  862
    ## 5775 1098  862
    ## 5776 1099  862
    ## 5777 1100  862
    ## 5778 1101  862
    ## 5779 1113  862
    ## 5780 1137  862
    ## 5781 1178  862
    ## 5782 1182  862
    ## 5829  886  869
    ## 5830  890  869
    ## 5831  894  869
    ## 5832  920  869
    ## 5833  946  869
    ## 5834  947  869
    ## 5835 1002  869
    ## 5836 1017  869
    ## 5837 1070  869
    ## 5838 1098  869
    ## 5839 1099  869
    ## 5840 1100  869
    ## 5841 1101  869
    ## 5842 1113  869
    ## 5843 1137  869
    ## 5844 1178  869
    ## 5845 1182  869
    ## 5893  890  886
    ## 5894  894  886
    ## 5895  920  886
    ## 5896  946  886
    ## 5897  947  886
    ## 5898 1002  886
    ## 5899 1017  886
    ## 5900 1070  886
    ## 5901 1098  886
    ## 5902 1099  886
    ## 5903 1100  886
    ## 5904 1101  886
    ## 5905 1113  886
    ## 5906 1137  886
    ## 5907 1178  886
    ## 5908 1182  886
    ## 5957  894  890
    ## 5958  920  890
    ## 5959  946  890
    ## 5960  947  890
    ## 5961 1002  890
    ## 5962 1017  890
    ## 5963 1070  890
    ## 5964 1098  890
    ## 5965 1099  890
    ## 5966 1100  890
    ## 5967 1101  890
    ## 5968 1113  890
    ## 5969 1137  890
    ## 5970 1178  890
    ## 5971 1182  890
    ## 6021  920  894
    ## 6022  946  894
    ## 6023  947  894
    ## 6024 1002  894
    ## 6025 1017  894
    ## 6026 1070  894
    ## 6027 1098  894
    ## 6028 1099  894
    ## 6029 1100  894
    ## 6030 1101  894
    ## 6031 1113  894
    ## 6032 1137  894
    ## 6033 1178  894
    ## 6034 1182  894
    ## 6085  946  920
    ## 6086  947  920
    ## 6087 1002  920
    ## 6088 1017  920
    ## 6089 1070  920
    ## 6090 1098  920
    ## 6091 1099  920
    ## 6092 1100  920
    ## 6093 1101  920
    ## 6094 1113  920
    ## 6095 1137  920
    ## 6096 1178  920
    ## 6097 1182  920
    ## 6149  947  946
    ## 6150 1002  946
    ## 6151 1017  946
    ## 6152 1070  946
    ## 6153 1098  946
    ## 6154 1099  946
    ## 6155 1100  946
    ## 6156 1101  946
    ## 6157 1113  946
    ## 6158 1137  946
    ## 6159 1178  946
    ## 6160 1182  946
    ## 6213 1002  947
    ## 6214 1017  947
    ## 6215 1070  947
    ## 6216 1098  947
    ## 6217 1099  947
    ## 6218 1100  947
    ## 6219 1101  947
    ## 6220 1113  947
    ## 6221 1137  947
    ## 6222 1178  947
    ## 6223 1182  947
    ## 6277 1017 1002
    ## 6278 1070 1002
    ## 6279 1098 1002
    ## 6280 1099 1002
    ## 6281 1100 1002
    ## 6282 1101 1002
    ## 6283 1113 1002
    ## 6284 1137 1002
    ## 6285 1178 1002
    ## 6286 1182 1002
    ## 6341 1070 1017
    ## 6342 1098 1017
    ## 6343 1099 1017
    ## 6344 1100 1017
    ## 6345 1101 1017
    ## 6346 1113 1017
    ## 6347 1137 1017
    ## 6348 1178 1017
    ## 6349 1182 1017
    ## 6405 1098 1070
    ## 6406 1099 1070
    ## 6407 1100 1070
    ## 6408 1101 1070
    ## 6409 1113 1070
    ## 6410 1137 1070
    ## 6411 1178 1070
    ## 6412 1182 1070
    ## 6469 1099 1098
    ## 6470 1100 1098
    ## 6471 1101 1098
    ## 6472 1113 1098
    ## 6473 1137 1098
    ## 6474 1178 1098
    ## 6475 1182 1098
    ## 6533 1100 1099
    ## 6534 1101 1099
    ## 6535 1113 1099
    ## 6536 1137 1099
    ## 6537 1178 1099
    ## 6538 1182 1099
    ## 6597 1101 1100
    ## 6598 1113 1100
    ## 6599 1137 1100
    ## 6600 1178 1100
    ## 6601 1182 1100
    ## 6661 1113 1101
    ## 6662 1137 1101
    ## 6663 1178 1101
    ## 6664 1182 1101
    ## 6725 1137 1113
    ## 6726 1178 1113
    ## 6727 1182 1113
    ## 6789 1178 1137
    ## 6790 1182 1137
    ## 6853 1182 1178
    ## 6917  614  286
    ## 6919  385  288
    ## 6920  496  288
    ## 6921 1058  288
    ## 6922 1187  288
    ## 6923 1195  288
    ## 6924 1264  288
    ## 6926  496  385
    ## 6927 1058  385
    ## 6928 1187  385
    ## 6929 1195  385
    ## 6930 1264  385
    ## 6933 1058  496
    ## 6934 1187  496
    ## 6935 1195  496
    ## 6936 1264  496
    ## 6940 1187 1058
    ## 6941 1195 1058
    ## 6942 1264 1058
    ## 6947 1195 1187
    ## 6948 1264 1187
    ## 6954 1264 1195
    ## 6961  391  289
    ## 6962  553  289
    ## 6963  577  289
    ## 6964  701  289
    ## 6965  956  289
    ## 6966 1212  289
    ## 6968  553  391
    ## 6969  577  391
    ## 6970  701  391
    ## 6971  956  391
    ## 6972 1212  391
    ## 6975  577  553
    ## 6976  701  553
    ## 6977  956  553
    ## 6978 1212  553
    ## 6982  701  577
    ## 6983  956  577
    ## 6984 1212  577
    ## 6989  956  701
    ## 6990 1212  701
    ## 6996 1212  956
    ## 7003  587  292
    ## 7005  663  295
    ## 7007  376  302
    ## 7009  962  303
    ## 7010 1190  303
    ## 7012 1190  962
    ## 7015  343  313
    ## 7016 1045  313
    ## 7018 1045  343
    ## 7021  690  315
    ## 7022  788  315
    ## 7023 1197  315
    ## 7025  788  690
    ## 7026 1197  690
    ## 7029 1197  788
    ## 7033 1166  316
    ## 7035  758  319
    ## 7036  933  319
    ## 7038  933  758
    ## 7041  346  320
    ## 7043  355  325
    ## 7044  462  325
    ## 7045 1011  325
    ## 7047  462  355
    ## 7048 1011  355
    ## 7051 1011  462
    ## 7055  396  328
    ## 7056  409  328
    ## 7057  718  328
    ## 7058  881  328
    ## 7059 1148  328
    ## 7061  409  396
    ## 7062  718  396
    ## 7063  881  396
    ## 7064 1148  396
    ## 7067  718  409
    ## 7068  881  409
    ## 7069 1148  409
    ## 7073  881  718
    ## 7074 1148  718
    ## 7079 1148  881
    ## 7085  497  332
    ## 7086  771  332
    ## 7087  783  332
    ## 7088  930  332
    ## 7089 1086  332
    ## 7091  771  497
    ## 7092  783  497
    ## 7093  930  497
    ## 7094 1086  497
    ## 7097  783  771
    ## 7098  930  771
    ## 7099 1086  771
    ## 7103  930  783
    ## 7104 1086  783
    ## 7109 1086  930
    ## 7115  517  334
    ## 7117  819  335
    ## 7119  633  351
    ## 7120  838  351
    ## 7121 1062  351
    ## 7122 1250  351
    ## 7124  838  633
    ## 7125 1062  633
    ## 7126 1250  633
    ## 7129 1062  838
    ## 7130 1250  838
    ## 7134 1250 1062
    ## 7139  384  357
    ## 7140  490  357
    ## 7141  533  357
    ## 7142  727  357
    ## 7143  790  357
    ## 7144  818  357
    ## 7145  945  357
    ## 7147  490  384
    ## 7148  533  384
    ## 7149  727  384
    ## 7150  790  384
    ## 7151  818  384
    ## 7152  945  384
    ## 7155  533  490
    ## 7156  727  490
    ## 7157  790  490
    ## 7158  818  490
    ## 7159  945  490
    ## 7163  727  533
    ## 7164  790  533
    ## 7165  818  533
    ## 7166  945  533
    ## 7171  790  727
    ## 7172  818  727
    ## 7173  945  727
    ## 7179  818  790
    ## 7180  945  790
    ## 7187  945  818
    ## 7195  922  371
    ## 7197  508  378
    ## 7198  561  378
    ## 7199  719  378
    ## 7200  926  378
    ## 7201 1120  378
    ## 7203  561  508
    ## 7204  719  508
    ## 7205  926  508
    ## 7206 1120  508
    ## 7209  719  561
    ## 7210  926  561
    ## 7211 1120  561
    ## 7215  926  719
    ## 7216 1120  719
    ## 7221 1120  926
    ## 7227  988  379
    ## 7228 1125  379
    ## 7230 1125  988
    ## 7233 1003  383
    ## 7235  634  395
    ## 7237  418  402
    ## 7238  424  402
    ## 7239  435  402
    ## 7240  457  402
    ## 7242  424  418
    ## 7243  435  418
    ## 7244  457  418
    ## 7247  435  424
    ## 7248  457  424
    ## 7252  457  435
    ## 7257  738  408
    ## 7258  874  408
    ## 7259 1172  408
    ## 7260 1260  408
    ## 7262  874  738
    ## 7263 1172  738
    ## 7264 1260  738
    ## 7267 1172  874
    ## 7268 1260  874
    ## 7272 1260 1172
    ## 7277  997  417
    ## 7279  609  436
    ## 7280 1107  436
    ## 7281 1209  436
    ## 7283 1107  609
    ## 7284 1209  609
    ## 7287 1209 1107
    ## 7291  616  445
    ## 7293  839  448
    ## 7294  896  448
    ## 7296  896  839
    ## 7299 1105  456
    ## 7301 1242  465
    ## 7303  621  479
    ## 7304  928  479
    ## 7305 1228  479
    ## 7307  928  621
    ## 7308 1228  621
    ## 7311 1228  928
    ## 7315  711  489
    ## 7316  733  489
    ## 7317  765  489
    ## 7318  913  489
    ## 7319  964  489
    ## 7320 1160  489
    ## 7322  733  711
    ## 7323  765  711
    ## 7324  913  711
    ## 7325  964  711
    ## 7326 1160  711
    ## 7329  765  733
    ## 7330  913  733
    ## 7331  964  733
    ## 7332 1160  733
    ## 7336  913  765
    ## 7337  964  765
    ## 7338 1160  765
    ## 7343  964  913
    ## 7344 1160  913
    ## 7350 1160  964
    ## 7357  670  495
    ## 7359  625  500
    ## 7360  710  500
    ## 7361  883  500
    ## 7362  965  500
    ## 7363 1126  500
    ## 7364 1249  500
    ## 7365 1279  500
    ## 7367  710  625
    ## 7368  883  625
    ## 7369  965  625
    ## 7370 1126  625
    ## 7371 1249  625
    ## 7372 1279  625
    ## 7375  883  710
    ## 7376  965  710
    ## 7377 1126  710
    ## 7378 1249  710
    ## 7379 1279  710
    ## 7383  965  883
    ## 7384 1126  883
    ## 7385 1249  883
    ## 7386 1279  883
    ## 7391 1126  965
    ## 7392 1249  965
    ## 7393 1279  965
    ## 7399 1249 1126
    ## 7400 1279 1126
    ## 7407 1279 1249
    ## 7415  536  502
    ## 7416  754  502
    ## 7417  927  502
    ## 7418 1081  502
    ## 7420  754  536
    ## 7421  927  536
    ## 7422 1081  536
    ## 7425  927  754
    ## 7426 1081  754
    ## 7430 1081  927
    ## 7435  599  514
    ## 7436  870  514
    ## 7438  870  599
    ## 7441  638  515
    ## 7442  778  515
    ## 7443  802  515
    ## 7444 1193  515
    ## 7446  778  638
    ## 7447  802  638
    ## 7448 1193  638
    ## 7451  802  778
    ## 7452 1193  778
    ## 7456 1193  802
    ## 7461  580  516
    ## 7462  689  516
    ## 7464  689  580
    ## 7467  810  522
    ## 7469  707  544
    ## 7470  868  544
    ## 7472  868  707
    ## 7475  569  547
    ## 7477 1208  550
    ## 7479  579  551
    ## 7481 1154  565
    ## 7483 1020  573
    ## 7485  863  595
    ## 7487  882  619
    ## 7488 1071  619
    ## 7490 1071  882
    ## 7493  772  630
    ## 7494 1026  630
    ## 7495 1057  630
    ## 7496 1108  630
    ## 7497 1282  630
    ## 7499 1026  772
    ## 7500 1057  772
    ## 7501 1108  772
    ## 7502 1282  772
    ## 7505 1057 1026
    ## 7506 1108 1026
    ## 7507 1282 1026
    ## 7511 1108 1057
    ## 7512 1282 1057
    ## 7517 1282 1108
    ## 7523  982  637
    ## 7524  983  637
    ## 7525 1015  637
    ## 7527  983  982
    ## 7528 1015  982
    ## 7531 1015  983
    ## 7535  895  644
    ## 7537 1110  652
    ## 7539 1158  655
    ## 7541  659  658
    ## 7542 1144  658
    ## 7544 1144  659
    ## 7547 1177  666
    ## 7549  950  688
    ## 7551  746  703
    ## 7552 1041  703
    ## 7553 1102  703
    ## 7555 1041  746
    ## 7556 1102  746
    ## 7559 1102 1041
    ## 7563 1200  706
    ## 7564 1230  706
    ## 7565 1273  706
    ## 7567 1230 1200
    ## 7568 1273 1200
    ## 7571 1273 1230
    ## 7575 1031  714
    ## 7577 1018  736
    ## 7579  798  782
    ## 7581  801  791
    ## 7583 1106  813
    ## 7585 1089  816
    ## 7586 1216  816
    ## 7587 1227  816
    ## 7588 1233  816
    ## 7589 1268  816
    ## 7590 1272  816
    ## 7592 1216 1089
    ## 7593 1227 1089
    ## 7594 1233 1089
    ## 7595 1268 1089
    ## 7596 1272 1089
    ## 7599 1227 1216
    ## 7600 1233 1216
    ## 7601 1268 1216
    ## 7602 1272 1216
    ## 7606 1233 1227
    ## 7607 1268 1227
    ## 7608 1272 1227
    ## 7613 1268 1233
    ## 7614 1272 1233
    ## 7620 1272 1268
    ## 7627 1021  821
    ## 7629  969  823
    ## 7631  958  824
    ## 7632 1076  824
    ## 7633 1220  824
    ## 7634 1275  824
    ## 7635 1280  824
    ## 7636 1281  824
    ## 7638 1076  958
    ## 7639 1220  958
    ## 7640 1275  958
    ## 7641 1280  958
    ## 7642 1281  958
    ## 7645 1220 1076
    ## 7646 1275 1076
    ## 7647 1280 1076
    ## 7648 1281 1076
    ## 7652 1275 1220
    ## 7653 1280 1220
    ## 7654 1281 1220
    ## 7659 1280 1275
    ## 7660 1281 1275
    ## 7666 1281 1280
    ## 7673 1169  835
    ## 7675 1088  860
    ## 7676 1203  860
    ## 7678 1203 1088
    ## 7681 1256  867
    ## 7683  877  875
    ## 7685 1067  887
    ## 7687  967  902
    ## 7689 1224  907
    ## 7691 1053  912
    ## 7693 1073  955
    ## 7694 1112  955
    ## 7695 1156  955
    ## 7697 1112 1073
    ## 7698 1156 1073
    ## 7701 1156 1112
    ## 7705 1039  976
    ## 7706 1123  976
    ## 7708 1123 1039
    ## 7711 1030  981
    ## 7712 1115  981
    ## 7714 1115 1030
    ## 7717 1163 1040
    ## 7719 1186 1150
    ## 7721 1261 1240

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
