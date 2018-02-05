# Conference Day 1

## Keynote - To the Tidyverse and Beyond -- Dianne Cook

* Visaul inference protocol cf. traditional statistical inference
    - Porschach protocol: compare what the results look at in scrambled data
    - Lineup protocol: put true data side-by-side with null plots to see if one can pick it out.
* How to generate NULL samples?
    - Permutation: scrambles the order of data
    - simulation
* Before any analysis, think about:
    - what questions?
    - How variables can be mapped (i.e. `aes` in `ggplot2`)
    - NULL generating mechanism
    - Alternative design of the plot
* P-value
    - check out the `nullabor` package
* Inference & interactive graphics

## Shiny async programming

* Async programming solves the problem that Shiny can only run in one single R Sesssion
* `promises` package to resue
* wrap `future()` around slow functions and use `%...>%` to pass to functions that looks at the results (e.g. `View()`)

## Shiny test

* `shinytest` package gets a snapshot of the current state of the apps and compare with future changes.
* the snapshot contains a JSON file and screenshot of the app

## Shiny make shiny faster 

* The workflow 
    1. Benchmarking - see how it performances at the moment, is it reasonalbe and expected to take a long time.
    2. Analysis - Identify the slowest part. `profvis` give a Ganht chart like view of the time each function takes
    3. Recomendation - list all possible solutions, some may not worth it since it may take 3 months to optimise only to sace performance by a few minutes
    4. Optimisation

## Shiny for 10,000 users

* Shiny is totally capable of handling an app that has 10,000 users concurrently. It may require running on several R sessions and servers though.
* Shiny is performance is linearly scalable with the number of users. Therefore it's only a matter of resources not a technical problem for scaling up to a large app.

## Tidy lesser known stars in tidyverse

* `na_if("")` to replace empty strings to `NA`
* `skimr::skim()` better summary of dataframe (with histogram!)
* `stringr::str_split() %>% unnest()` to split string to nested df and then unnest.
* `reprex::reprex()` reproducible example
* `ggthemer` package to set the theme of ggplot and default colours at the very begining.

## Tidy interactive web graphics for exploratory data analysis

* plotly highlighting
    - `highlight(ggplotly(p), dynamic = TRUE, selectize = TRUE)`
* plotly + crosstalk to allow plotly embedded in other language framworks?

## Multingual Rmarkdown

* `knit_engine$set()` see what languages are suppported
* In SQL code chunk, you can set `output.var = "output"` in order to access this output in subsequent R code chunks
* Rmarkdown great for collaborating with people using other languages (e.g. python)

## Rmarkdown branding & automating your work

* You can supply a word doc in the YAML as the template for rendering word report.
* Branding images with Magick
* Use R package as template storage (store in the /inst folder), pull the template when using in the report

## Programming -- Tidy evaluation

* Tidy eval == principled NSE
* three big ideas

## Programming -- data rectangling

* [slider]/(std.io/rectangling)
* why list?
    - string processing
    - JSON, XML returned from web APIs
    - Models, plots and collections thereof
* `library(repurrrsive)` for nested df

## Best practice working with DB

* Demo of `dbplyr` functions
* `dbplot` calculate stats in the DB before plotting

## Case study -- developing & deploying large scale Shiny app

* Talk by FRISS a Netherland Company
* 4 components to build a large professional Shiny app
    - Modules
    - R6 Class
    - HTML widgets
    - HTML template
* FRISS has a Shiny web app that has pre-rendered report, check the slide
* FRISSAnalytics [github](https://github.com/FrissAnalytics/RSTUDIO-conf-2018.git) hosts the codes for the FRISS Shiny app




 