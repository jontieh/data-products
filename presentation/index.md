---
title       : ESTIMATING HOUSE PRICES
subtitle    : Course Project for Developing Data Products
author      : Jonathan Tieh
job         : April 17, 2016
framework   : io2012
highlighter : highlight.js
hitheme     : default
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : standalone # {standalone, draft}
knit        : slidify::knit2slides
---
<style>

sup {
    vertical-align: super;
    font-size: smaller;
} 

pre {
  font-size: 16px;
  line-height: 18px;
  font-family: "Courier New",monospace;
}

</style>

## MOTIVATION

<br/>

### PROBLEM

* Selling a house is <span style="color:#cc0000">ONE OF THE MOST STRESSFUL EVENTS</span> in life.

* It was found to be even more stressful than bankruptcy, divorce or loss of someone you love<sup>1</sup>. 

* With the housing market finally recovering, many people are looking to sell their homes.

* One way to avoid stress is to <span style="color:#cc0000">OFFER YOUR HOUSE AT A COMPETITIVE PRICE</span>.

</br>

### YET, HOW TO DETERMINE THE OPTIMAL PRICE FOR YOUR HOUSE?

<br/>

<br/>

<hr style="width: 50%; float: left;"/>
<br/>
<span style="font-size:smaller">
<sup>1</sup> Source: [independent.co.uk](http://www.independent.co.uk/property/buying-or-selling-a-house-is-most-stressful-part-of-modern-life-9584752.html)</span>

--- #custbg

## SOLUTION: HOUSE PRICE ESTIMATOR

<style>
#custbg {
  background-color:white;
  background-image:url(./figure/hpe2.png); 
  background-repeat: no-repeat;
  background-position: bottom right;
  background-size: auto;
}
</style>

<br/>

* <span style="color:#cc0000">HOUSE PRICE ESTIMATOR (HPE)</span> is an online platform which will help you estimate the value of your house on the market based on the following criteria:
  + Construction Year,
  + Number of Bedrooms,
  + House Size,
  + Lot Size,
  + Location, and
  + Month when you plan to sell.
  

---

## HOW DOES IT WORK?

<br/>

* HPE builds its prediction model based on the <span style="color:#cc0000">nutshell::sanfrancisco.home.sales</span> dataset:

```r
library(nutshell)
data(sanfrancisco.home.sales)
str(sanfrancisco.home.sales)
```

```
## 'data.frame':	3281 obs. of  15 variables:
##  $ line        : int  65083 4893 4959 27880 78680 17110 11363 56564 4964 30465 ...
##  $ county      : Factor w/ 1 level "San Francisco County": 1 1 1 1 1 1 1 1 1 1 ...
##  $ street      : Factor w/ 3227 levels "1 Burnett Avenue",..: 1 2 3 4 5 6 7 8 9 10 ...
##  $ city        : Factor w/ 1 level "San Francisco": 1 1 1 1 1 1 1 1 1 1 ...
##  $ zip         : int  94131 94134 94107 94109 94109 94107 94124 94103 94117 94110 ...
##  $ date        : Date, format: "2008-06-11" "2009-06-12" ...
##  $ price       : int  1470000 385000 1043000 560000 419000 552000 228000 2200000 1475000 565000 ...
##  $ bedrooms    : int  3 0 2 2 NA NA 0 3 0 2 ...
##  $ squarefeet  : int  2424 1304 1400 1149 NA NA 1060 2873 1225 660 ...
##  $ lotsize     : int  NA 2143 NA NA NA NA 2247 3140 NA 2365 ...
##  $ year        : int  1983 1945 1997 1988 1988 NA NA 1919 1918 1918 ...
##  $ latitude    : num  37.8 37.7 37.8 37.8 37.8 ...
##  $ longitude   : num  -122 -122 -122 -122 -122 ...
##  $ month       : Factor w/ 18 levels "2008-02-01","2008-03-01",..: 5 17 17 12 2 14 16 7 17 11 ...
##  $ neighborhood: Factor w/ 34 levels "Bayview","Bernal Heights",..: 31 32 30 34 34 30 1 16 13 2 ...
```

---

## READY FOR YOUR FIRST ESTIMATION?

<br/>

* Try the [HOUSE PRICE ESTIMATOR](https://jontieh.shinyapps.io/house-price-estimator/) now.

* If you are a techie person and want to learn more about how this app works, you can check out the code from its [GitHub repository](https://github.com/jontieh/data-products).

<br/>
<br/>
<br/>

### <div style="width:100%; text-align:center">THANK YOU, </div>
### <div style="width:100%; text-align:center">AND I WISH YOU A STRESS-FREE SELLING EXPERIENCE!</div>
