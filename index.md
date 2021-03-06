---
title       : Mileage Predictor Proposal
subtitle    : 
author      : ldmacdonald
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## What am I selling?

# An application that will predict whether or not a user has enough gas in their car for a current trip.

---  

## Why?
1. Planning: The user needs to know how much gas they'll need for a trip.
2. Savings: The user can save money by filling up when they have a good price since they will know how much gas they will need.

--- 
## How is the app making this prediction?
Currently, we are making  a few assumptions.  Most cars built in America are designed with a 300 mile range.  We take the percentage of the gas remaining in the tank and do some basic calculations.  The current calculation is shown below.


```r
    dist <- 10 # This is set by the mileage control
    gas <- 1/4 *(300) # This is set by the gas Remaining control
    gasUsed <- dist/12.5 # this will be set by the car type input.

    if(dist <= gas) {
      out <- paste('Yes, you have enough gas.  You will use ',gasUsed,' gallons of gas.')
    } else { out <- 'No, you do not have enough gas.'}
    out
```

```
## [1] "Yes, you have enough gas.  You will use  0.8  gallons of gas."
```
  

--- 
## Next Steps
* Pull in more accurate car data.  
  * We can make more accurate predictions about the car's range
  * Allows a level of customization per user
* Integrate gas station prices
  * Allows app to suggest locations that offer the best price for gas in the range
* Integrate address/ direction functionality
  * Suggest pathing with the best prices for gas based upon the destination.




