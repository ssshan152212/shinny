---
title: "Vehicle MPG Prediction Application"
author: "Vaibhav Kumar Singh"
date: "7/30/2020"
output: html_document
---

## **Overview**

This presentation and the application was build for the course Developing Data Products as part of the Coursera Data Science Specializaion.

The Shiny app developed for this assignment is available at: https://kevinhuang.shinyapps.io/MPGPrediction/

The source codes of ui.R and server.R are available on the GitHub repo: https://github.com/kevhuang710/Coursera-Shiny-Application-and-Reproducible-Pitch

## **Idea**

The idea of this application is to let users be able to predict their vehicles' MPG by entering specs such as transmission type, weight, horse power, and number of cylinders.

## **Dataset**

For this application, we used the mtcars dataset from datasets library The summary of the dataset is below:

```R
summary(mtcars)
```


          mpg             cyl             disp             hp       
     Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0  
     1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5  
     Median :19.20   Median :6.000   Median :196.3   Median :123.0  
     Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7  
     3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0  
     Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0  
          drat             wt             qsec             vs        
     Min.   :2.760   Min.   :1.513   Min.   :14.50   Min.   :0.0000  
     1st Qu.:3.080   1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000  
     Median :3.695   Median :3.325   Median :17.71   Median :0.0000  
     Mean   :3.597   Mean   :3.217   Mean   :17.85   Mean   :0.4375  
     3rd Qu.:3.920   3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000  
     Max.   :4.930   Max.   :5.424   Max.   :22.90   Max.   :1.0000  
           am              gear            carb      
     Min.   :0.0000   Min.   :3.000   Min.   :1.000  
     1st Qu.:0.0000   1st Qu.:3.000   1st Qu.:2.000  
     Median :0.0000   Median :4.000   Median :2.000  
     Mean   :0.4062   Mean   :3.688   Mean   :2.812  
     3rd Qu.:1.0000   3rd Qu.:4.000   3rd Qu.:4.000  
     Max.   :1.0000   Max.   :5.000   Max.   :8.000  

## **Model**

We used lm to fit a multivariable regression; mpg as outcome, am, cyl, hp, and wt as predictors. The coefficients is shown below,

```R
lm(mpg ~ am + cyl + hp + wt, data = mtcars)
```


    
    Call:
    lm(formula = mpg ~ am + cyl + hp + wt, data = mtcars)
    
    Coefficients:
    (Intercept)           am          cyl           hp           wt  
       36.14654      1.47805     -0.74516     -0.02495     -2.60648  
    



```R

```
