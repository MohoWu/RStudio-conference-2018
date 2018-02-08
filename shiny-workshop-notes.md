# Day 1

## Intro -- Dean

* Always name single app file as app.R
* Check out RStudio Connect
    - Publish Shiny apps, Rmarkdown docs, etc
    - Scheduled report
    - Self-managed content
    - support
    - 45 days free trial (not free afterwards)

## Reactivity -- Dean

* Reactive value `reactiveValues` creates a _R environment like_ object.
Unlike input value it's not read-only.
* `reactive` is LAZY. It wouldn't evalulate its content until it's absolutely necessary.
`observe` is EAGER. It will update whenever the reactive content changes (e.g. input, reactive values)
* reactive values `reactiveValues` best updated in the observer, if updated in `reactive` --> best to create a new reactive conductor.

## Understand UI -- Joe

* _objective_: use tags to customise ui.R
* `shinythemes::themeSelector()` in ui.R --> live preview of the themes
* put UI creation into functions and then into packages to have consistency in Shiny app UI across the organisation. Achieve this by using `HTML::tags`.
* Some cool examples about web design:
    - [US Web desgin standard](https://18f.gsa.gov/2015/09/28/web-design-standards/)
    - [Shiny scorecard app](https://github.com/jcheng5/scorecard-app)
    - [HTML template](https://shiny.rstudio.com/articles/templates.html)

## Advanced Reactivity -- Joe

* Effecive reactive programming video from 2016 RStudio Shiny conference
* `invalidateLater(1000)` use _time_ as a reactive input
* __`throttle()`__ & __`debounce()`__ control the execution interval of reactive expression. This is useful to avoid unnecessary rendering of faster input changes.


# Day 2

## Modules -- Joe (new to me)

* modules are like functions that are self-contained and can be combined to make a large app
* [Dynamic interface UI video from last year's conference](https://www.rstudio.com/resources/videos/dynamic-shiny-interfaces/)
* reactives
    - no parens -- meaning capture all future values, a rare case where no parens for reactive stuff. Consider this as reactive functions.
    - with parens -- meaning capture the current value. This usually means that the reactivity is not preserved when used in the context of module functions.
    
## Bookmarking -- Dean

* Share links to Shiny apps where the state of the session is preserved.
* Put `enableBookmarking(store = "url")` in the _global.r_ for 2-files Shiny app. Another option for `store` is `"server"`

## Troubleshooting -- Dean

* Quick and simple: put `print` in the server and see the output in the console. Only works locally. For app on the server, check out `shinyjs::logjs()`. This can be accessed in the JavaScript console. For Chrome on Windows, hit F12.
* Always use `browser()`. RStudio debugger may not work all the time.

## Dashboard -- Joe

* Dashboard for constantly changing data source. Dashboard generally doesn't have a lot interactivity as it updates on its own.
* Solution for reading constantly changing data:
    - `reactiveFileReader` reads file when the timestamp changes
    - `reactivePoll` reads data from other sources.
    
## Q&A

* reactive values can be put at the top level of the app outside the `server()` function.
* `readReactiveFile` is a prime example to be put outside `server()`.
* `memoise` package for handling slow calculation that takes a long time to avoid timeout limit on Shiny server 
* [advanced-shiny](https://github.com/daattali/advanced-shiny)

    
    




