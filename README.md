## Experimenting with `nonlinearTseries`

[`nonlinearTseries`](https://github.com/constantino-garcia/nonlinearTseries)
provides functions for nonlinear time series analysis. This package permits the
computation of the most-used nonlinear statistics/algorithms including
generalized correlation dimension, information dimension, largest Lyapunov
exponent, sample entropy and Recurrence Quantification Analysis (RQA),
among others. Basic routines for surrogate data testing are also included.
The package is largely inspired by the book [Nonlinear time series analysis](https://www.amazon.com/Nonlinear-Time-Analysis-Holger-Kantz/dp/0521529026)
by Holger Kantz and Thomas Schreiber.


## Getting started
For a quick introduction to `nonlinearTseries`, see its
[vignette](https://cran.r-project.org/web/packages/nonlinearTseries/vignettes/nonlinearTseries_quickstart.html) or the [package documentation](https://cran.r-project.org/web/packages/nonlinearTseries/nonlinearTseries.pdf).

## Dependencies

Install the following dependencies

```
R
mirror_repo <- 'https://www.stats.bris.ac.uk/R/'
install.packages("tseries", repos=mirror_repo, dependencies = TRUE)
install.packages("TSA", repos=mirror_repo, dependencies = TRUE)
install.packages("RcppArmadillo", repos=mirror_repo, dependencies = TRUE)

```


## Developing Debugging and Testing with nonlinearTseries

```
cd ~/mxochicale/github/nonlinearTseries
R
library(roxygen2); library("devtools")
install('nonlinearTseries')
library('nonlinearTseries')
buildTakens(1:20,embedding.dim=5,time.lag=3)
```


## Loading nonlinearTseries from a given path

```
library(devtools)
load_all('~/mxochicale/github/nonlinearTseries')
buildTakens(1:20,embedding.dim=5,time.lag=3)
```

## You can also install the library from a given path as follows
```
library(devtools)
install('~/mxochicale/github/nonlinearTseries')
library('nonlinearTseries')
buildTakens(1:20,embedding.dim=5,time.lag=3)
```

# TESTING ZONE
In [TESTING ZONE](https://github.com/mxochicale/nonlinearTseries/tree/master/tests/_testings),
you will find all the experiments regarding the use of this library.

# TODO
This is the [TODO List](https://github.com/mxochicale/nonlinearTseries/blob/master/TODO.md)

# SUGGESTIONS
* When modifying the code, avoid to delete blank lines as these are a bit strange
to follow in the continues modification of the library. __28DEC2017__
