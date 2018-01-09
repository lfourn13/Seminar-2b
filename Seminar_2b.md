---
title: "Seminar 2b"
author: "Louis-Alexandre Fournier"
date: "January 8, 2018"
output: 
  html_document: 
    keep_md: yes
---



#STAT 540 Seminar 2B

#Part 1
library(tidyverse)

###Do cars with big engines use more fuel than cars with small engines? 
mpg

ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy))



