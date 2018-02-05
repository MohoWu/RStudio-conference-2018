# Day 2

## Keynote -- Machine learning tensorflow -- JJ Allaire

* Tensorflow started 2 years ago
* Tensorflow a GENERAL numerical computing library
* Tensors -- multidimensional arrays
    - 0D a number
    - 1D an atomic vector
    - 2D Matrix
    - 3D 3D matrix
    - 4D 4D array
* Flow -- building the graphs?
* What are layers?
    - A data transformation parameterised by weights and biases
    - information distillation pipeline
* Statistics vs ML
    - Statistical inference explains the causes of a phenomenon
    - ML focused on predicting the future but not neccessarily understand why it works, mainly due to its black box nature and the large number (in millions) of coefficients in the ML model
* Problems
    - Not easily interpreted, black box nature
    - Brittle (adversarial examples)
    - Tends to work best only with large amount of training data
    - Computationally expensive to train
* _Keras_ is probably the best interface for Tensorflow
* Some work on interpreting the ML model `lime` package
* Takeaways
    - TF is a general purpose numerical computing package
    - Deep learning is likely to see increase usage in various other fields
    - Great sets of APIs
* My takeaway: 
    - ML is really the best method for image recognisation at the moment. 
    - More quantative modelling best use traditional statistical models.
    - some business may have regulative restriction on using ML models since the model is required to be interpretable.
    - Check out the non-ML aspects of TF packages like GAM modelling in chapter 8 of Deep Learning in R
    - talk slides [here](rstd.io/ml-with-tensorflow-and-r/)

## Teaching tidyverse to beginners

* understand the goals the students want to achieve and teach them how to do it ASAP
* Forget data types, if statement, loops at the begining. Teach useful stuff first!

## Making package in 20 mins

* slide at rstd.io/rpkgs2018
* rOpenSci onboarding (book for R package)
* `usethis` package
* components
    - DESCRIPTION
    - R/
    - tests/
    - NAMESPACE
    - man/
    - vignettes
    - etc...
* `usethis::create_package("~/myPackage")`
* `usethis::use_package("dplyr")`
* `usethis::use_readme()`
* `usethis::use_test()`
* `covr::report()` see which function in the package is not covered by the test

## What makes a great R package

* CRAN with 12,000 packages now
* CRAN task views
    - 35 taks views
    - all curated by experts
    - about 2,960 package are great and unique packages
* CRAN == Best statistical knowledge library

## Case study breaking down barrier

## Differentiate business by data science

* Stitch fix has algorithm for every part of business decision. Algorithm tour

## Production -- parameterised RMarkdown report

* RStudio connect can host and render parameterised Rmarkdown report with history view.

## Production -- drilling down and up Shiny app

* Add and remove UI
    - `appendTab` and `removeTab`
    - `showModal` and `removeModal`
    - `insertUI` and `removeUI`
* Demo app and slide code at https://github.com/bborgesr/rstudio-conf-2018

## R admin

* R admin - A bridge between R users and IT
* R Notebook | Automate simple workflows | Pull data from the web and write to a database
* Shiny app | Easily publish, host, and manage at scale | Web page on Apache web server
* R Markdown Report | Create dynamic, self-serve reports | Email on demand or scheduled
* Plumber API | Easily host multiple endpoints and output types | REST call
* slides on (github)[https://github.com/nwstephens/r-admin-2018] 


    
    
    




    


