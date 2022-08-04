
<!-- README.md is generated from README.Rmd. Please edit that file -->

# fExtremes

[![AppVeyor Build
Status](https://ci.appveyor.com/api/projects/status/github/paulnorthrop/fExtremes?branch=main&svg=true)](https://ci.appveyor.com/project/paulnorthrop/fExtremes)
[![R-CMD-check](https://github.com/paulnorthrop/fExtremes/workflows/R-CMD-check/badge.svg)](https://github.com/paulnorthrop/fExtremes/actions)
[![CRAN_Status_Badge](https://www.r-pkg.org/badges/version/fExtremes)](https://cran.r-project.org/package=fExtremes)
[![Downloads
(monthly)](https://cranlogs.r-pkg.org/badges/fExtremes?color=brightgreen)](https://cran.r-project.org/package=fExtremes)
[![Downloads
(total)](https://cranlogs.r-pkg.org/badges/grand-total/fExtremes?color=brightgreen)](https://cran.r-project.org/package=fExtremes)

## Rmetrics - Modelling Extreme Events in Finance

The **fExtremes** package provides functions for analysing and modelling
extreme events in financial time Series. The topics include: (i) data
pre-processing, (ii) explorative data analysis, (iii) peak over
threshold modelling, (iv) block maxima modelling, (v) estimation of VaR
and CVaR, and (vi) the computation of the extreme index. It is part of
the [Rmetrics software project](https://www.rmetrics.org/).

### An example

The following code simulates data from a GEV distribution, fits a GEV
distribution to these data and creates model diagnostic plots.

``` r
library(fExtremes)
# Simulate GEV Data, use default length n=1000
x <- gevSim(model = list(xi = 0.25, mu = 0 , beta = 1), n = 1000)

# Fit GEV data using maximum likelihood estimation
fit <- gevFit(x, type = "mle") 
fit
#> 
#> Title:
#>  GEV Parameter Estimation 
#> 
#> Call:
#>  gevFit(x = x, type = "mle")
#> 
#> Estimation Type:
#>   gev mle 
#> 
#> Estimated Parameters:
#>          xi          mu        beta 
#>  0.26031160 -0.01315679  0.99479288 
#> 
#> Description
#>   Thu Aug  4 14:14:34 2022
```

### Installation

To get the current released version from CRAN:

``` r
install.packages("fExtremes")
```
