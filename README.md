## What is `nonlinearTseries`
[`nonlinearTseries`](https://github.com/constantino-garcia/nonlinearTseries)
provides functions for nonlinear time series analysis. This package permits the
computation of the most-used nonlinear statistics/algorithms including
generalized correlation dimension, information dimension, largest Lyapunov
exponent, sample entropy and Recurrence Quantification Analysis (RQA),
among others. Basic routines for surrogate data testing are also included.
The package is largely inspired by the book [Nonlinear time series analysis](https://www.amazon.com/Nonlinear-Time-Analysis-Holger-Kantz/dp/0521529026)
by Holger Kantz and Thomas Schreiber.

*NB* Many thanks to [constantino-garcia](https://github.com/constantino-garcia/)
for making the [`nonlinearTseries`](https://github.com/constantino-garcia/nonlinearTseries)
package available in GitHub.

## Installation
You can install the he latest released version from
[CRAN](https://cran.r-project.org/web/packages/nonlinearTseries/index.html) with:

```
install.packages("nonlinearTseries")
```

## Getting started
For a quick introduction to `nonlinearTseries`, see its
[vignette](https://cran.r-project.org/web/packages/nonlinearTseries/vignettes/nonlinearTseries_quickstart.html).



## Developing Debugging and Testing with nonlinearTseries

```
cd ~/mxochicale/github/nonlinearTseries
R
library(roxygen2); library("devtools")
install('nonlinearTseries')
library('nonlinearTseries')
```

```
buildTakens(1:20,embedding.dim=5,time.lag=3)
```


## Loading nonlinearTseries from a given path

```
library(devtools)
load_all('~/mxochicale/github/nonlinearTseries')
buildTakens(1:20,embedding.dim=5,time.lag=3)
```

or
```
library(devtools)
install('~/mxochicale/github/nonlinearTseries')
library('nonlinearTseries')
buildTakens(1:20,embedding.dim=5,time.lag=3)
```


## TESTING timelag() function
timelag() funciton is at ~/nonlinearTseries/R/basicNonLinearFunctions.R

The aim for such testing is to extract the values for the autocorrelation function
and the average mutual information in order to compare them with other similar
methods.

There is little description about the properties of the lag.max value.
"@param lag.max Maximum lag at which to calculate the acf/AMI."
It was not too obviosu but it can be said that lag.max is the maximum
value where acf/AMI can be decay




The default method to determine the minumum time delay embedding is base on
on when acf/AMI function decays to 1/e of its value at zero \emph{first.e.decay}
where no explanation for e is given.



## TODO

- [ ] use ggplot2 as an alternative for plotting results
- [ ] use data.table for Multivariate Uniform Delay Embedding
