
<!-- README.md is generated from README.Rmd. Please edit the README.Rmd file -->

``` r
url <- "https://www.baseball-reference.com/awards/hof_2023.shtml"
pg <- read_html(url)
tb <- html_table(pg, fill = TRUE)
HallOfFame23 <- tb[[1]]

colnames(HallOfFame23)<-HallOfFame23[1,]
HallOfFame23<-HallOfFame23[-1,]
HallOfFame23
```

    ## # A tibble: 28 × 39
    ##    Rk    Name      YoB   Votes `%vote` HOFm  HOFs  Yrs   WAR   WAR7  JAWS  Jpos 
    ##    <chr> <chr>     <chr> <chr> <chr>   <chr> <chr> <chr> <chr> <chr> <chr> <chr>
    ##  1 1     Scott Ro… 6th   297   76.3%   99    40    17    70.1  43.6  56.9  56.3 
    ##  2 2     Todd Hel… 5th   281   72.2%   175   59    17    61.8  46.6  54.2  53.4 
    ##  3 3     Billy Wa… 8th   265   68.1%   107   24    16    27.7  19.8  23.7  32.5 
    ##  4 4     Andruw J… 6th   226   58.1%   109   34    17    62.7  46.4  54.6  58.2 
    ##  5 5     Gary She… 9th   214   55.0%   158   61    22    60.5  38.0  49.3  56.7 
    ##  6 6     Carlos B… 1st   181   46.5%   126   52    20    70.1  44.4  57.3  58.2 
    ##  7 7     X-Jeff K… 10th  181   46.5%   123   51    17    55.4  35.8  45.6  57.1 
    ##  8 8     Alex Rod… 2nd   139   35.7%   390   77    22    117.6 64.3  90.9  55.5 
    ##  9 9     Manny Ra… 7th   129   33.2%   226   69    19    69.3  39.9  54.6  53.4 
    ## 10 10    Omar Viz… 6th   76    19.5%   120   42    24    45.6  26.8  36.2  55.5 
    ## # ℹ 18 more rows
    ## # ℹ 27 more variables: G <chr>, AB <chr>, R <chr>, H <chr>, HR <chr>,
    ## #   RBI <chr>, SB <chr>, BB <chr>, BA <chr>, OBP <chr>, SLG <chr>, OPS <chr>,
    ## #   `OPS+` <chr>, W <chr>, L <chr>, ERA <chr>, `ERA+` <chr>, WHIP <chr>,
    ## #   G <chr>, GS <chr>, SV <chr>, IP <chr>, H <chr>, HR <chr>, BB <chr>,
    ## #   SO <chr>, `Pos Summary` <chr>
