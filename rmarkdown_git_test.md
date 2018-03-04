---
title: "got rmarkdown test"
author: "Bryan Shalloway"
date: "March 4, 2018"
output: 
  html_document:
    keep_md: true
    code_folding: show
    toc: yes
    toc_depth: 5
    toc_float:
      collapsed: no


---



## R Markdown

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


```r
p <- pressure %>% 
  ggplot(aes(x = temperature, y = pressure, colour = pressure))+
  geom_point()

plotly::ggplotly(p)
```

<!--html_preserve--><div id="88c6fc07723" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="88c6fc07723">{"x":{"data":[{"x":[0,20,40,60,80,100,120,140,160,180,200,220,240,260,280,300,320,340,360],"y":[0.0002,0.0012,0.006,0.03,0.09,0.27,0.75,1.85,4.2,8.8,17.3,32.1,57,96,157,247,376,558,806],"text":["temperature:   0<br />pressure:   0.0002<br />pressure:   0.0002","temperature:  20<br />pressure:   0.0012<br />pressure:   0.0012","temperature:  40<br />pressure:   0.0060<br />pressure:   0.0060","temperature:  60<br />pressure:   0.0300<br />pressure:   0.0300","temperature:  80<br />pressure:   0.0900<br />pressure:   0.0900","temperature: 100<br />pressure:   0.2700<br />pressure:   0.2700","temperature: 120<br />pressure:   0.7500<br />pressure:   0.7500","temperature: 140<br />pressure:   1.8500<br />pressure:   1.8500","temperature: 160<br />pressure:   4.2000<br />pressure:   4.2000","temperature: 180<br />pressure:   8.8000<br />pressure:   8.8000","temperature: 200<br />pressure:  17.3000<br />pressure:  17.3000","temperature: 220<br />pressure:  32.1000<br />pressure:  32.1000","temperature: 240<br />pressure:  57.0000<br />pressure:  57.0000","temperature: 260<br />pressure:  96.0000<br />pressure:  96.0000","temperature: 280<br />pressure: 157.0000<br />pressure: 157.0000","temperature: 300<br />pressure: 247.0000<br />pressure: 247.0000","temperature: 320<br />pressure: 376.0000<br />pressure: 376.0000","temperature: 340<br />pressure: 558.0000<br />pressure: 558.0000","temperature: 360<br />pressure: 806.0000<br />pressure: 806.0000"],"type":"scatter","mode":"markers","marker":{"autocolorscale":false,"color":["rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,44,68,1)","rgba(20,44,69,1)","rgba(20,46,70,1)","rgba(21,48,73,1)","rgba(23,51,78,1)","rgba(26,57,86,1)","rgba(31,66,99,1)","rgba(38,81,118,1)","rgba(49,102,146,1)","rgba(64,133,187,1)","rgba(86,177,247,1)"],"opacity":1,"size":5.66929133858268,"symbol":"circle","line":{"width":1.88976377952756,"color":["rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,43,67,1)","rgba(19,44,68,1)","rgba(20,44,69,1)","rgba(20,46,70,1)","rgba(21,48,73,1)","rgba(23,51,78,1)","rgba(26,57,86,1)","rgba(31,66,99,1)","rgba(38,81,118,1)","rgba(49,102,146,1)","rgba(64,133,187,1)","rgba(86,177,247,1)"]}},"hoveron":"points","showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[0],"y":[0],"name":"99_28bc36e52c5bef969e8161dc323ca577","type":"scatter","mode":"markers","opacity":0,"hoverinfo":"none","showlegend":false,"marker":{"color":[0,1],"colorscale":[[0,"#132B43"],[0.0526315789473684,"#16314B"],[0.105263157894737,"#193754"],[0.157894736842105,"#1D3E5C"],[0.210526315789474,"#204465"],[0.263157894736842,"#234B6E"],[0.315789473684211,"#275277"],[0.368421052631579,"#2A5980"],[0.421052631578947,"#2E608A"],[0.473684210526316,"#316793"],[0.526315789473684,"#356E9D"],[0.578947368421053,"#3875A6"],[0.631578947368421,"#3C7CB0"],[0.684210526315789,"#3F83BA"],[0.736842105263158,"#438BC4"],[0.789473684210526,"#4792CE"],[0.842105263157895,"#4B9AD8"],[0.894736842105263,"#4EA2E2"],[0.947368421052632,"#52A9ED"],[1,"#56B1F7"]],"colorbar":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"thickness":23.04,"title":"pressure","titlefont":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"tickmode":"array","ticktext":["200","400","600","800"],"tickvals":[0.248138771250315,0.49627779063965,0.744416810028985,0.99255582941832],"tickfont":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895},"ticklen":2,"len":0.5}},"xaxis":"x","yaxis":"y","frame":null}],"layout":{"margin":{"t":26.2283105022831,"r":7.30593607305936,"b":40.1826484018265,"l":43.1050228310502},"plot_bgcolor":"rgba(235,235,235,1)","paper_bgcolor":"rgba(255,255,255,1)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xaxis":{"domain":[0,1],"type":"linear","autorange":false,"range":[-18,378],"tickmode":"array","ticktext":["0","100","200","300"],"tickvals":[0,100,200,300],"categoryorder":"array","categoryarray":["0","100","200","300"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":null,"gridwidth":0,"zeroline":false,"anchor":"y","title":"temperature","titlefont":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"hoverformat":".2f"},"yaxis":{"domain":[0,1],"type":"linear","autorange":false,"range":[-40.29979,846.29999],"tickmode":"array","ticktext":["0","200","400","600","800"],"tickvals":[0,200,400,600,800],"categoryorder":"array","categoryarray":["0","200","400","600","800"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":null,"gridwidth":0,"zeroline":false,"anchor":"x","title":"pressure","titlefont":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"hoverformat":".2f"},"shapes":[{"type":"rect","fillcolor":null,"line":{"color":null,"width":0,"linetype":[]},"yref":"paper","xref":"paper","x0":0,"x1":1,"y0":0,"y1":1}],"showlegend":false,"legend":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"font":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895}},"hovermode":"closest","barmode":"relative"},"config":{"doubleClick":"reset","modeBarButtonsToAdd":[{"name":"Collaborate","icon":{"width":1000,"ascent":500,"descent":-50,"path":"M487 375c7-10 9-23 5-36l-79-259c-3-12-11-23-22-31-11-8-22-12-35-12l-263 0c-15 0-29 5-43 15-13 10-23 23-28 37-5 13-5 25-1 37 0 0 0 3 1 7 1 5 1 8 1 11 0 2 0 4-1 6 0 3-1 5-1 6 1 2 2 4 3 6 1 2 2 4 4 6 2 3 4 5 5 7 5 7 9 16 13 26 4 10 7 19 9 26 0 2 0 5 0 9-1 4-1 6 0 8 0 2 2 5 4 8 3 3 5 5 5 7 4 6 8 15 12 26 4 11 7 19 7 26 1 1 0 4 0 9-1 4-1 7 0 8 1 2 3 5 6 8 4 4 6 6 6 7 4 5 8 13 13 24 4 11 7 20 7 28 1 1 0 4 0 7-1 3-1 6-1 7 0 2 1 4 3 6 1 1 3 4 5 6 2 3 3 5 5 6 1 2 3 5 4 9 2 3 3 7 5 10 1 3 2 6 4 10 2 4 4 7 6 9 2 3 4 5 7 7 3 2 7 3 11 3 3 0 8 0 13-1l0-1c7 2 12 2 14 2l218 0c14 0 25-5 32-16 8-10 10-23 6-37l-79-259c-7-22-13-37-20-43-7-7-19-10-37-10l-248 0c-5 0-9-2-11-5-2-3-2-7 0-12 4-13 18-20 41-20l264 0c5 0 10 2 16 5 5 3 8 6 10 11l85 282c2 5 2 10 2 17 7-3 13-7 17-13z m-304 0c-1-3-1-5 0-7 1-1 3-2 6-2l174 0c2 0 4 1 7 2 2 2 4 4 5 7l6 18c0 3 0 5-1 7-1 1-3 2-6 2l-173 0c-3 0-5-1-8-2-2-2-4-4-4-7z m-24-73c-1-3-1-5 0-7 2-2 3-2 6-2l174 0c2 0 5 0 7 2 3 2 4 4 5 7l6 18c1 2 0 5-1 6-1 2-3 3-5 3l-174 0c-3 0-5-1-7-3-3-1-4-4-5-6z"},"click":"function(gd) { \n        // is this being viewed in RStudio?\n        if (location.search == '?viewer_pane=1') {\n          alert('To learn about plotly for collaboration, visit:\\n https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html');\n        } else {\n          window.open('https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html', '_blank');\n        }\n      }"}],"cloud":false},"source":"A","attrs":{"88c5ff82e7d":{"x":{},"y":{},"colour":{},"type":"scatter"}},"cur_data":"88c5ff82e7d","visdat":{"88c5ff82e7d":["function (y) ","x"]},"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1}},"base_url":"https://plot.ly"},"evals":["config.modeBarButtonsToAdd.0.click"],"jsHooks":{"render":[{"code":"function(el, x) { var ctConfig = crosstalk.var('plotlyCrosstalkOpts').set({\"on\":\"plotly_click\",\"persistent\":false,\"dynamic\":false,\"selectize\":false,\"opacityDim\":0.2,\"selected\":{\"opacity\":1}}); }","data":null}]}}</script><!--/html_preserve-->

