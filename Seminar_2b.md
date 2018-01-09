---
title: "Seminar 2b"
author: "Louis-Alexandre Fournier"
date: "January 8, 2018"
output: 
  html_document: 
    keep_md: yes
---



#STAT 540 Seminar 2B

#Part 1 - First time ggplot-ing


```r
library(tidyverse)
```

```
## ── Attaching packages ─────────────────────────────────────────────── tidyverse 1.2.1 ──
```

```
## ✔ ggplot2 2.2.1     ✔ purrr   0.2.4
## ✔ tibble  1.4.1     ✔ dplyr   0.7.4
## ✔ tidyr   0.7.2     ✔ stringr 1.2.0
## ✔ readr   1.1.1     ✔ forcats 0.2.0
```

```
## ── Conflicts ────────────────────────────────────────────────── tidyverse_conflicts() ──
## ✖ dplyr::filter() masks stats::filter()
## ✖ dplyr::lag()    masks stats::lag()
```

###Do cars with big engines use more fuel than cars with small engines? 
####mpg dataset

```r
mpg
```

```
## # A tibble: 234 x 11
##    manufac… model   displ  year   cyl trans  drv     cty   hwy fl    class
##    <chr>    <chr>   <dbl> <int> <int> <chr>  <chr> <int> <int> <chr> <chr>
##  1 audi     a4       1.80  1999     4 auto(… f        18    29 p     comp…
##  2 audi     a4       1.80  1999     4 manua… f        21    29 p     comp…
##  3 audi     a4       2.00  2008     4 manua… f        20    31 p     comp…
##  4 audi     a4       2.00  2008     4 auto(… f        21    30 p     comp…
##  5 audi     a4       2.80  1999     6 auto(… f        16    26 p     comp…
##  6 audi     a4       2.80  1999     6 manua… f        18    26 p     comp…
##  7 audi     a4       3.10  2008     6 auto(… f        18    27 p     comp…
##  8 audi     a4 qua…  1.80  1999     4 manua… 4        18    26 p     comp…
##  9 audi     a4 qua…  1.80  1999     4 auto(… 4        16    25 p     comp…
## 10 audi     a4 qua…  2.00  2008     4 manua… 4        20    28 p     comp…
## # ... with 224 more rows
```
####Highway miles per gallon in function of engine displacement (L)

```r
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy))
```

![](Seminar_2b_files/figure-html/ggplot of mpg-1.png)<!-- -->

####City miles per gallon in function of engine displacement (L)

```r
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = cty))
```

![](Seminar_2b_files/figure-html/barebones graphing template-1.png)<!-- -->



