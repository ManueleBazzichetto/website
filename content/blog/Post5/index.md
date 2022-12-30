---
title: Mapping confidence intervals for species occurrence probability in SDMs
tags: stats, R, ecology
date: 2022-11-25

math: true
---

[WORK IN PROGRESS!!]

Typical outputs of species distribution models (SDM) are maps of the predicted probability of occurrence of species across the study area. These probabilities of occurrence are estimated from the fitted SDM, and, therefore, inevitably bring uncertainty with them (they are estimated from the data). However, maps representing this uncertainty are seldom reported along with maps of estimated probabilities in papers about SDMs. One possible explanation is that there are not ready-to-use (R) functions to compute (and map) such uncertainty.  

But, first: how to measure such uncertainty? Well, we can use [**confidence intervals**](https://mbazzichetto.netlify.app/blog/post2/). Confidence intervals combine information on precision (width of the confidence interval) and accuracy (assumed coverage). Looking at confidence intervals, we have an intuitive representation about how precisely parameters (in this post, occurrence probability) are estimated, plus we have a full range of plausible values for the true, unknown parameter.

While working on a paper using SDM, I decided to take on this challenge, and write down an R function for mapping the width of confidence intervals associated with the probability of occurrence of _Fagus sylavatica_ (this was the study species). The function does some pretty easy task:

1. raster layers associated with the predictors are coerced to a data.frame object with coordinates for the center of each grid cell.

2. a grid is overlayed to the study area. This will come handy for computing confidence intervals across wide study areas, as, basically, these get split in small pieces and confidence intervals are computed across chunks.

3. predictions and confidence intervals are computed within each cell of the grid mentioned in step 2.

4. width of the confidence intervals is reported to a raster layer with same resolution of the input raster layers of the predictors.

All we need to make it work is: 1) a fitted model object (at the moment, the function only accepts binomial glm); 2) a raster stack/brick or whatever list of raster layers that can be coerced to a data frame. Extra-work is needed in case polynomials terms are in the model. Polynomials are considered in the working example provided on [GitHub]().

```r
1+1
```

WARNING: be aware that the function must be used for mapping confidence intervals across the study area. Avoid extrapolating predictions outside the range of values of predictors used to train the models. The correlation among predictors may be different, as well as the relationship between them and the occurrence of the species.

Don't hesitate to contact me if you find mistakes or want to help me making this more efficient/general!
