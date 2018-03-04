github document test
================
Bryan Shalloway
March 4, 2018

-   [R Markdown](#r-markdown)
    -   [Including Plots](#including-plots)
-   [Other](#other)
    -   [ggplotly](#ggplotly)

Note that the header options in the .rmd support outputs to both html and md documents -- allowing you to specify which chunks not to render (e.g. not rendering chunks with plotly code that would need to be in html to work properly.)

``` r
rmarkdown::render("github_doc_test.Rmd", output_format = "all")

##below are a couple of options I was looking at
# always_allow_html: yes
# html_preview: false

##This will force it to continue rendering even when faced with errors
# knitr::opts_chunk$set(error = TRUE)
```

R Markdown
==========

``` r
library(dplyr)
library(ggplot2)

params$output_type
```

    ## [1] FALSE

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

Including Plots
---------------

You can also embed plots, for example:

![](github_doc_test_files/figure-markdown_github/pressure-1.png)

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.

Other
=====

Test of other

``` r
plot(mtcars)
```

![](github_doc_test_files/figure-markdown_github/unnamed-chunk-3-1.png)

New change made.

ggplotly
--------

Note that this plotly does not show-up in the simple .md documents on github as it's rendering javascript here

``` r
p <- pressure %>% 
  ggplot(aes(x = temperature, y = pressure, colour = pressure))+
  geom_point()

plotly::ggplotly(p)
```
