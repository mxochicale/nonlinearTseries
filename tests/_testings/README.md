

# Recurrence Plot recurrencePlot() and rqa()
__5JANUARY2018__


* The recurrencePlotFromMatrix() function in RQA.R
use neighbourList2SparseMatrix to convert values to a matrix and sparse its values


* Before to use recurrencePlot(), it is important that in buildTakens(), you do the following:
uncomment:
```
attr(takens,"embedding.dim") = embedding.dim
attr(takens,"time.lag") = time.lag
attr(takens,"id") = id
takens
```
and commenting
```
  # list(takens,embedding.dim,time.lag,id)
```


Example:
```
lorenz.ts = lorenz(time=seq(0,10,by=0.01), do.plot=FALSE)$x
recurrencePlot(takens = NULL, time.series = lorenz.ts, embedding.dim=2, time.lag=1,radius=2)
```




# buildTakens() with data.table
__28DEC2017__

commenting
```
# attr(takens,"embedding.dim") = embedding.dim
# attr(takens,"time.lag") = time.lag
# attr(takens,"id") = id
# takens
```
to work with "list(takens,embedding.dim,time.lag,id)"


# timelag() function
__7NOV2017__

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

For returning results, instead of "attr(lag,"fx") = fd" the function was
modified to use "list(lag, fx)"