# Utilities

## Human Logistics
[https://doodle.com/create][Doodle]
[http://whenisgood.net/][WhenIsGood]

## Cheat Sheets
[https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet][Markdown Cheatsheet]
[https://www.tug.org/twg/mactex/tutorials/ltxprimer-1.0.pdf][Latex Extended Guide]
[https://reu.dimacs.rutgers.edu/Symbols.pdf][Latex Symbols & Equations]

## Evaluation Rubrics
[http://www-scf.usc.edu/~csci401/finalproject/FinalProjectPresentationGradingRubric.pdf][CSCI401 Capstone Presentation]

## ggplot2
[http://ggplot2.tidyverse.org/reference/ggtheme.html][ggthemes]
[https://web.archive.org/web/20160320034441/cran.r-project.org/web/packages/GGally/vignettes/ggpairs.html][ggpairs]
[https://github.com/ropensci/plotly][ggplotly]
[https://github.com/rstudio/cheatsheets/blob/master/data-visualization-2.1.pdf][PDF Cheat Sheet to ggplot2, by tidyverse]
## Bokeh
[http://holoviews.org/gallery/index.html][holoviews]
[http://www.ancienteco.com/2012/05/quickly-visualize-your-whole-dataset.html][Visualize tableplot of data]


# R tip
Warnings as errors: `options(warn=2)`   
`options(error=browser)` or default as `options(error=NULL)`  
trycatch example:
```
readUrl <- function(url) {
    out <- tryCatch(
        {
            # Just to highlight: if you want to use more than one 
            # R expression in the "try" part then you'll have to 
            # use curly brackets.
            # 'tryCatch()' will return the last evaluated expression 
            # in case the "try" part was completed successfully

            message("This is the 'try' part")

            readLines(con=url, warn=FALSE) 
            # The return value of `readLines()` is the actual value 
            # that will be returned in case there is no condition 
            # (e.g. warning or error). 
            # You don't need to state the return value via `return()` as code 
            # in the "try" part is not wrapped insided a function (unlike that
            # for the condition handlers for warnings and error below)
        },
        error=function(cond) {
            message(paste("URL does not seem to exist:", url))
            message("Here's the original error message:")
            message(cond)
            # Choose a return value in case of error
            return(NA)
        },
        warning=function(cond) {
            message(paste("URL caused a warning:", url))
            message("Here's the original warning message:")
            message(cond)
            # Choose a return value in case of warning
            return(NULL)
        },
        finally={
        # NOTE:
        # Here goes everything that should be executed at the end,
        # regardless of success or error.
        # If you want more than one expression to be executed, then you 
        # need to wrap them in curly brackets ({...}); otherwise you could
        # just have written 'finally=<expression>' 
            message(paste("Processed URL:", url))
            message("Some other message at the end")
        }
    )    
    return(out)
}
```

# Electronics
[https://www.youtube.com/watch?v=pTVek7v0_R8][NOT gate]

# iTerm/SublimeText
`bash /Users/briancohn/scripts/iterm_open_with.sh \5 \1 \2 `
[https://gist.github.com/trinitronx/f59a8308d42d71fdba41][Command click to subl to specific line]


hit and run visualization:
https://healthyalgorithms.com/2011/01/28/mcmc-in-python-pymc-step-methods-and-their-pitfalls/


