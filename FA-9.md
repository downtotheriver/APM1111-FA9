Untitled
================

``` r
# 2 Way ANOVA of Political Interest
library(tidyverse)
```

    ## Warning: package 'tidyverse' was built under R version 4.3.3

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.4.4     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
library(readr)
library(car)
```

    ## Loading required package: carData
    ## 
    ## Attaching package: 'car'
    ## 
    ## The following object is masked from 'package:dplyr':
    ## 
    ##     recode
    ## 
    ## The following object is masked from 'package:purrr':
    ## 
    ##     some

``` r
library(Hmisc)
```

    ## 
    ## Attaching package: 'Hmisc'
    ## 
    ## The following objects are masked from 'package:dplyr':
    ## 
    ##     src, summarize
    ## 
    ## The following objects are masked from 'package:base':
    ## 
    ##     format.pval, units

``` r
library(dplyr)
politicalInterest <- read_csv("Political Interest.csv")
```

    ## Rows: 58 Columns: 3
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## dbl (3): gender, education_level, political_interest
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
politicalInterest
```

    ## # A tibble: 58 × 3
    ##    gender education_level political_interest
    ##     <dbl>           <dbl>              <dbl>
    ##  1      1               1               38  
    ##  2      1               1               39  
    ##  3      1               1               35  
    ##  4      1               1               38  
    ##  5      1               1               41  
    ##  6      1               1               40  
    ##  7      1               1               36  
    ##  8      1               1               37  
    ##  9      1               1               33  
    ## 10      1               2               41.5
    ## # ℹ 48 more rows

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
