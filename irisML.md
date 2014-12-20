Shiny App: Machine Learning of Iris dataset(irisApp)
========================================================
author: Pritimayee Patra 
date: December 20 2014
autosize: true

Description of shiny App(irisApp)
========================================================

This web application is based on application of machine learning on famous  **Fisher's Iris data set**.Its interface provides users five functionality 


- Prediction of species based on user's input
- exploration whole iris data set
- Data analysis(summary of data and scatterplot of feaures of data)
- Displays Prediction model used , a property table of model prediction for out of sample data showing how much percentage of each species are misclassified in out of sample data and a plot displaying important variable for the model
- Documentation to help user for using app

Fisher's Iris data set
====================================
This data set became a typical test case for many classification techniques in machine learning.This data set has 5 features i.e 4 predictor variables (Petal.Length, Petal.Width, Sepal.Length, Sepal.Width) and one response variable(Species).

```r
table(iris$Species)
```

```

    setosa versicolor  virginica 
        50         50         50 
```
so the dataset contains 50 rows from each of 3 species of iris.we've sub divided data in ratio of 70:30 for cross validation purpose. 70% data used for training and remaining 30% for validation  

Prediction Model
========================================================
**Randomforest** is the fitted prediction model for this app.The random forest doesn't overfit and also gives a very good accuracy.Follwing confusion matrix for the prediction model also confirms high accuracy. 


```r
iris.rf$confusion
```

```
           setosa versicolor virginica class.error
setosa         35          0         0     0.00000
versicolor      0         33         2     0.05714
virginica       0          1        34     0.02857
```
Only Versicolor and virginica has class.error 5.7% and 2.9% respectively.
 
Programming tools and Links
========================================================
The app is developed in **RStudio**  with **shiny** library. **randomForest** library is also used for building prediction model.  

  It's deployed on Rstudio shiny server(https://pritipatra.shinyapps.io/irisApp/)  
  
  It's code is available on github repo(https://github.com/rstudio/shinyapps)  
After getting the repo,  
1. set path to app directory   
2. load library(shiny)   
3. call runApp() from R console to run the application.      






