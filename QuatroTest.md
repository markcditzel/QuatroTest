# TestingQuatro


## Quarto

Quarto enables you to weave together content and executable code into a
finished document. To learn more about Quarto see <https://quarto.org>.

## Running Code

When you click the **Render** button a document will be generated that
includes both content and the output of embedded code. You can embed
code like this:

``` r
1 + 1
```

    [1] 2

You can add options to executable code like this

    [1] 4

The `echo: false` option disables the printing of code (only output is
displayed).

``` r
library(tidyverse)
```

    ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
    ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
    ✔ purrr     1.0.2     
    ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ✖ dplyr::filter() masks stats::filter()
    ✖ dplyr::lag()    masks stats::lag()
    ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
smaller <- diamonds %>% 
  filter(carat <= 2.5)
```

``` r
smaller
```

    # A tibble: 53,814 × 10
       carat cut       color clarity depth table price     x     y     z
       <dbl> <ord>     <ord> <ord>   <dbl> <dbl> <int> <dbl> <dbl> <dbl>
     1  0.23 Ideal     E     SI2      61.5    55   326  3.95  3.98  2.43
     2  0.21 Premium   E     SI1      59.8    61   326  3.89  3.84  2.31
     3  0.23 Good      E     VS1      56.9    65   327  4.05  4.07  2.31
     4  0.29 Premium   I     VS2      62.4    58   334  4.2   4.23  2.63
     5  0.31 Good      J     SI2      63.3    58   335  4.34  4.35  2.75
     6  0.24 Very Good J     VVS2     62.8    57   336  3.94  3.96  2.48
     7  0.24 Very Good I     VVS1     62.3    57   336  3.95  3.98  2.47
     8  0.26 Very Good H     SI1      61.9    55   337  4.07  4.11  2.53
     9  0.22 Fair      E     VS2      65.1    61   337  3.87  3.78  2.49
    10  0.23 Very Good H     VS1      59.4    61   338  4     4.05  2.39
    # ℹ 53,804 more rows

smaller
