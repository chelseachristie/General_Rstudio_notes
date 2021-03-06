general\_rRstudio\_notes
================
Chelsea Christie
October 1, 2016

Chelsea's notes from Stat545 about how to use R Studio
------------------------------------------------------

### Basic R notes

see: <http://stat545.com/block002_hello-r-workspace-wd-project.html>

For more tips on R markdown: <http://stat545.com/block007_first-use-rmarkdown.html> or <http://r4ds.had.co.nz/r-markdown.html>

Start by loading my favorite packages

``` r
library(tidyverse)
```

    ## Loading tidyverse: ggplot2
    ## Loading tidyverse: tibble
    ## Loading tidyverse: tidyr
    ## Loading tidyverse: readr
    ## Loading tidyverse: purrr
    ## Loading tidyverse: dplyr

    ## Conflicts with tidy packages ----------------------------------------------

    ## filter(): dplyr, stats
    ## lag():    dplyr, stats

``` r
library(psych)
```

    ## 
    ## Attaching package: 'psych'

    ## The following objects are masked from 'package:ggplot2':
    ## 
    ##     %+%, alpha

``` r
library(foreign)
library(forcats)
library(ggplot2)
```

``` r
# <- ## makes an assignment (kind of like giving something a name/short hand)
objects() ## tells me what objects are in my workspace 
```

    ## character(0)

``` r
# ls() ## also tells me what objects are in my workspace
# rm() ## will remove an object
# rm(list = ls()) ## will remove all objects in workspace (can also do with broom in the environment)

# (name <- whatever I'm naming/assigning ) putting an assignment in brackets will cause it print at the same time

# q() = quit Rstudio 

# getwd() = shows which working directory I"m "working in" and importantly where all the stuff I'm doing will get saved to

# Rstudio projects keep all the files associated with a project organized together – input data, R scripts, analytical results, figures

# It's always a good idea to test run things using fake data. To make a fake dataset:

(A <- data.frame(
        c1 = c('A', 'A', 'A', 'A', 'A', 'B', 'B'),
        c2 = c('a', 'a', 'a', 'b', 'b', 'c', 'd'),
        c3 = c(1, 3, 1, 1, 2, 2, 1)))
```

    ##   c1 c2 c3
    ## 1  A  a  1
    ## 2  A  a  3
    ## 3  A  a  1
    ## 4  A  b  1
    ## 5  A  b  2
    ## 6  B  c  2
    ## 7  B  d  1

``` r
# to make tables pretty, use:

# knitr::kable()

# For example: 

(knitr::kable(A))
```

| c1  | c2  |   c3|
|:----|:----|----:|
| A   | a   |    1|
| A   | a   |    3|
| A   | a   |    1|
| A   | b   |    1|
| A   | b   |    2|
| B   | c   |    2|
| B   | d   |    1|

Some more general Rstudio information:

to find keyboard shortcuts press ctrl + shift + K

%&gt;%: the “pipe” operator is used to connect multiple verb actions together into a pipeline. Once you travel down the pipeline with %&gt;%, the first argument is taken to be the output of the previous element in the pipeline.
