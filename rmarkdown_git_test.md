---
title: "got rmarkdown test"
author: "Bryan Shalloway"
date: "March 4, 2018"
output: 
  html_document:
    keep_md: true
    toc: yes
    toc_depth: 3


---

One nice thing about the `keep_md` option is that it does not require separate folders for caching.

# R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:


```r
summary(cars)
```

```
##      speed           dist       
##  Min.   : 4.0   Min.   :  2.00  
##  1st Qu.:12.0   1st Qu.: 26.00  
##  Median :15.0   Median : 36.00  
##  Mean   :15.4   Mean   : 42.98  
##  3rd Qu.:19.0   3rd Qu.: 56.00  
##  Max.   :25.0   Max.   :120.00
```

## Including Plots

You can also embed plots, for example:

![](rmarkdown_git_test_files/figure-html/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.


```r
pressure %>% 
  ggplot(aes(x = temperature, y = pressure, colour = pressure))+
  geom_point()
```

![](rmarkdown_git_test_files/figure-html/ggglot-1.png)<!-- -->


Note that this plotly does not show-up in the simple .md documents on github as it's rendering javascript here

```r
p <- pressure %>% 
  ggplot(aes(x = temperature, y = pressure, colour = pressure))+
  geom_point()

plotly::ggplotly(p)
```

