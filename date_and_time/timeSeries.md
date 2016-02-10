

# timeSeries: Rmetrics - Financial Time Series Objects

[![](http://www.r-pkg.org/badges/version/timeSeries)](http://cran.rstudio.com/web/packages/timeSeries/index.html)

* CRAN: http://cran.r-project.org/web/packages/timeSeries/index.html
* URL: http://www.rmetrics.org


```r
> library(timeSeries)
> data("LPP2005REC")
> data("MSFT")
> data("USDCHF")
```

バージョン: 3022.101.2

-----



| 関数名 | 概略 |
|--------|------|
| `TimeSeriesClass` | timeSeries Class |
| `TimeSeriesData` | Time Series Data Sets |
| `TimeSeriesSubsettings` | Subsettig Time Series |
| `aggregate-methods` | timeSeries Class, Functions and Methods |
| `align-methods` | timeSeries Class, Functions and Methods |
| `as` | timeSeries Class, Coercion and Transformation |
| `attach` | Attach a timSeries to the search path |
| `attributes` | Get and Set Optional Attributes of a 'timeSeries' |
| `cbind` | Bind two timeSeries objects |
| `colCum` | Cumulated Column Statistics |
| `colStats` | Column Statistics |
| `comment,timeSeries-method` | comment for timeSeries objects |
| `cumulated` | Cumulated Time Series from Returns |
| `daily` | Special Daily Time Series |
| `description` | Creates Date and User Information |
| `diff` | diff |
| `dim,timeSeries-method` | Time Series Columns and Rows |
| `drawdowns` | Calculations of Drawdowns |
| `durations` | Durations from a Time Series |
| `endOfPeriod` | End-of-Period Series, Stats, and Benchmarks |
| `fapply` | Apply Functions Over Time Series Periods |
| `filter,timeSeries-method` | Linear Filtering on a Time Series |
| `getDataPart,timeSeries-method` | DataPart,timeSeries-method |
| `getFinCenter` | Get and Set Financial Center of a 'timeSeries' |
| `getUnits` | Get and Set Unit Names of a 'timeSeries' |
| `index2wealth` | Conversion of an index to wealth |
| `is.timeSeries` | timeSeries Class, Coercion and Transformation |
| `isDaily,timeSeries-method` | Checks if a time series is regular |
| `isUnivariate` | Checks if a Time Series is Univariate |
| `lag` | Lag a Time Series |
| `math` | Mathematical Time Series Operations |
| `mean,timeSeries-method` | Methods for 'timeSeries' object |
| `merge` | Merges two 'timeSeries' objects |
| `model.frame` | Model Frames for Time Series Objects |
| `monthly` | Special Monthly Series |
| `na` | Handling Missing Time Series Values |
| `na.contiguous,timeSeries-method` | Find Longest Contiguous Stretch of non-NAs |
| `orderColnames` | Reorder Column Names of a Time Series |
| `orderStatistics` | order Statistics |
| `plot` | Plot a Time Series |
| `rank,timeSeries-method` | Sample Ranks of a Time Series |
| `readSeries` | Reads a 'timeSeries' from a File |
| `returns` | Financial Returns |
| `rev,timeSeries-method` | Reversion of a 'timeSeries' |
| `rollMean` | Rolling Statistics |
| `rowCum` | Cumulated Column Statistics |
| `runlengths` | Runlengths of a Time Series |
| `sd-methods` | Time Series Correlations |
| `series` | Get and Set Data of a 'timeSeries' |
| `seriesPositions` | Deprecated functions in timeSeries package |
| `show,timeSeries-method` | Print a Time Series |
| `smoothLowess` | Smoothes Time Series Objects |
| `sort,timeSeries-method` | Sorting a 'timeSeries' by Time Stamps |
| `splits` | splits |
| `spreads` | Spreads and Mid Quotes |
| `start,timeSeries-method` | Start and End of a 'timeSeries' |
| `str` | timeSeries Object Structure |
| `t,timeSeries-method` | timeSeries Transpose |
| `time` | Get and Set Time stamps of a 'timeSeries' |
| `timeSeries-package` | Utilities and Tools Package |
| `turns` | Turning Points of a Time Series |
| `window` | window |

-----

## TimeSeriesData

時系列データセット


```r
> data("LPP2005REC")
> data("MSFT")
> data("USDCHF")
```


## readSeries



## window

時系列データの抽出


```r
> timeSeries::window(LPP2005REC[, 7:9], "2006-01-01", "2006-01-31")
```

```
GMT
                  LPP25        LPP40        LPP60
2006-01-02  0.000165480  0.000297932  0.000444413
2006-01-03  0.000019500 -0.000076900  0.000009450
2006-01-04  0.001847585  0.002227044  0.002945121
2006-01-05 -0.000602521 -0.000805771 -0.001093968
2006-01-06  0.000553944  0.000844125  0.001291886
2006-01-09  0.001844267  0.003025315  0.004325551
2006-01-10 -0.001280919 -0.001540235 -0.001981789
2006-01-11  0.000960843  0.002094522  0.003631846
2006-01-12  0.002548068  0.003119294  0.003796029
2006-01-13 -0.001161811 -0.001200778 -0.001223253
2006-01-16  0.000193729  0.000162094  0.000196195
2006-01-17 -0.001337495 -0.002720934 -0.004437794
2006-01-18 -0.002019320 -0.004157731 -0.006873332
2006-01-19  0.001650710  0.003430897  0.005727921
2006-01-20 -0.002759185 -0.003613313 -0.004887407
2006-01-23 -0.002815600 -0.005072953 -0.007675798
2006-01-24  0.000253631  0.001224870  0.002318423
2006-01-25 -0.000604919  0.000462553  0.001621599
2006-01-26  0.001842887  0.003443139  0.005584311
2006-01-27  0.003394103  0.005791901  0.008762193
2006-01-30  0.001319517  0.002116907  0.003086897
2006-01-31  0.000222982  0.000133349  0.000055900
```



