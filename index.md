---
title       : Learning Shiny
subtitle    : Learning Shiny from Coursera
author      : Krishna Prasad
job         : Software Engineer
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction of Shiny

1. Shiny is a platform for creating interactive Rprograms embedded into a webpage.
2. Suppose that you create a prediction algorithm, with shiny you can very easily create web input
form that calls R and thus your prediction algorithm and displays the results.

3. Shiny is made by the fine folk sat RStudio.
4. Shiny doesn't really require it, but as with all web programming, a little knowledge of html, css and js is very helpful
5. Shiny uses css [bootstrap](getbootstrap.com/css/) style, which seems to look nice and renders well on mobile platform.

--- .class #id 

## Getting started with Shiny
* Make sure you have the latest release of R installed
    You can check the installed version by following command

```r
paste0(version$major, '.', version$minor)
```

```
## [1] "3.3.0"
```
* How to install the shiny library in R

```r
install.packages("shiny")
# load as
library(shiny)
```

--- .class #id 

## Create A Shiny project
* A shiny project is a directory containing at least two parts
    - One named ui.R (for user interface) controls how it works.
    - One named server.R that controls what is does
* Example of ui.R and server.R


```r
#ui.R
library(shiny)
shinyUI(pageWithSidebar(
  headerPanel("Data science FTW!"),
  sidebarPanel(h3('Sidebar text')),
  mainPanel(h3('Main Panel text'))
))
```


--- .class #id 

## server.R


## How to run it
* In R, change to the directories with these files and type `runApp()`
* or put the path to the directory where ui.R and server.R contains as an arguments in the method `runApp()`
* It should open an browser window with the app running

--- .class #id 

##  Check list and Thank you page

Your presentation must satisfy the following

1. It must be done in Slidify or Rstudio Presenter: Yes
2. It must be 5 pages: Yes
3. It must be hosted on github or Rpubs : Yes, hosted on github pages with url is: http://krishnaiitd.github.io/learningSlidify
4. It must contained some embedded R code that gets run when slidifying the document: Yes, it contains slide number 3, with the code `paste0(version$major, '.', version$minor)`

### Thank you very much for going through slides
