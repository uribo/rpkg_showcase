

# zoo: S3 Infrastructure for Regular and Irregular Time Series (Z's Ordered Observations)

[![](http://www.r-pkg.org/badges/version/zoo)](http://cran.rstudio.com/web/packages/zoo/index.html)

* CRAN: http://cran.r-project.org/web/packages/zoo/index.html
* URL: http://zoo.R-Forge.R-project.org/


```r
> library(zoo)
```

バージョン: 1.7.12

-----



| 関数名 | 概略 |
|--------|------|
| `MATCH` | Value Matching |
| `ORDER` | Ordering Permutation |
| `aggregate.zoo` | Compute Summary Statistics of zoo Objects |
| `as.zoo` | Coercion from and to zoo |
| `coredata` | Extracting/Replacing the Core Data of Objects |
| `frequency<-` | Replacing the Index of Objects |
| `ggplot2.zoo` | Convenience Functions for Plotting zoo Objects with ggplot2 |
| `index` | Extracting/Replacing the Index of Objects |
| `is.regular` | Check Regularity of a Series |
| `lag.zoo` | Lags and Differences of zoo Objects |
| `make.par.list` | Make a List from a Parameter Specification |
| `merge.zoo` | Merge Two or More zoo Objects |
| `na.StructTS` | Fill NA or specified positions. |
| `na.aggregate` | Replace NA by Aggregation |
| `na.approx` | Replace NA by Interpolation |
| `na.fill` | Fill NA or specified positions. |
| `na.locf` | Last Observation Carried Forward |
| `na.trim` | Trim Leading/Trailing Missing Observations |
| `plot.zoo` | Plotting zoo Objects |
| `read.zoo` | Reading and Writing zoo Series |
| `rollapply` | Apply Rolling Functions |
| `rollmean` | Rolling Means/Maximums/Medians/Sums |
| `window.zoo` | Extract/Replacing the Time Windows of Objects |
| `xblocks` | Plot contiguous blocks along x axis. |
| `xyplot.zoo` | Plot zoo Series with Lattice |
| `yearmon` | An Index Class for Monthly Data |
| `yearqtr` | An Index Class for Quarterly Data |
| `zoo` | Z's Ordered Observations |
| `zooreg` | Regular zoo Series |

-----

## MATCH


```r
> MATCH(x = c(1:5), table = c(2:3))
```

```
[1] NA  1  2 NA NA
```

## ORDER


```r
> set.seed(123)
> rnorm(5)
```

```
[1] -0.56047565 -0.23017749  1.55870831  0.07050839  0.12928774
```

```r
> set.seed(123)
> ORDER(rnorm(5))
```

```
[1] 1 2 4 5 3
```

## na.StructTS


```r
> z <- zooreg(rep(10 * seq(8), each = 4) + rep(c(3, 1, 2, 4), times = 8), 
+             start = as.yearqtr(2000), freq = 4)
> z[25] <- NA
> na.StructTS(z)
```

```
 2000 Q1  2000 Q2  2000 Q3  2000 Q4  2001 Q1  2001 Q2  2001 Q3  2001 Q4 
13.00000 11.00000 12.00000 14.00000 23.00000 21.00000 22.00000 24.00000 
 2002 Q1  2002 Q2  2002 Q3  2002 Q4  2003 Q1  2003 Q2  2003 Q3  2003 Q4 
33.00000 31.00000 32.00000 34.00000 43.00000 41.00000 42.00000 44.00000 
 2004 Q1  2004 Q2  2004 Q3  2004 Q4  2005 Q1  2005 Q2  2005 Q3  2005 Q4 
53.00000 51.00000 52.00000 54.00000 63.00000 61.00000 62.00000 64.00000 
 2006 Q1  2006 Q2  2006 Q3  2006 Q4  2007 Q1  2007 Q2  2007 Q3  2007 Q4 
72.99682 71.00000 72.00000 74.00000 83.00000 81.00000 82.00000 84.00000 
```


## na.aggregate

欠損値の置換


```r
> (z <- zoo(c(1, NA, 3:9),
+          c(as.Date("2010-01-01") + 0:2,
+            as.Date("2010-02-01") + 0:2,
+            as.Date("2011-01-01") + 0:2)))
```

```
2010-01-01 2010-01-02 2010-01-03 2010-02-01 2010-02-02 2010-02-03 
         1         NA          3          4          5          6 
2011-01-01 2011-01-02 2011-01-03 
         7          8          9 
```

```r
> na.aggregate(z)
```

```
2010-01-01 2010-01-02 2010-01-03 2010-02-01 2010-02-02 2010-02-03 
     1.000      5.375      3.000      4.000      5.000      6.000 
2011-01-01 2011-01-02 2011-01-03 
     7.000      8.000      9.000 
```

```r
> na.aggregate(z, as.yearmon)
```

```
2010-01-01 2010-01-02 2010-01-03 2010-02-01 2010-02-02 2010-02-03 
         1          2          3          4          5          6 
2011-01-01 2011-01-02 2011-01-03 
         7          8          9 
```

```r
> na.aggregate(z, months)
```

```
2010-01-01 2010-01-02 2010-01-03 2010-02-01 2010-02-02 2010-02-03 
       1.0        5.6        3.0        4.0        5.0        6.0 
2011-01-01 2011-01-02 2011-01-03 
       7.0        8.0        9.0 
```




## read.zoo

### Arguments

* file
* format
* tz
* FUN
* regular
* index.column
* drop
* x
* index.name
* row.names
* FUN2
* split


```r
> Lines <- "2013-12-24  2
+ 2013-12-25 3
+ 2013-12-26 8"
> read.zoo(text = Lines, tz = "Asia/Tokyo", FUN = as.Date)
```

```
2013-12-24 2013-12-25 2013-12-26 
         2          3          8 
```

 
## yearmon


```r
> as.yearmon(2000 + seq(0, 23)/12)
```

```
 [1] "Jan 2000" "Feb 2000" "Mar 2000" "Apr 2000" "May 2000" "Jun 2000"
 [7] "Jul 2000" "Aug 2000" "Sep 2000" "Oct 2000" "Nov 2000" "Dec 2000"
[13] "Jan 2001" "Feb 2001" "Mar 2001" "Apr 2001" "May 2001" "Jun 2001"
[19] "Jul 2001" "Aug 2001" "Sep 2001" "Oct 2001" "Nov 2001" "Dec 2001"
```

```r
> as.yearmon("mar07", "%b%y")
```

```
[1] "Mar 2007"
```

```r
> as.yearmon("2007-12")
```

```
[1] "Dec 2007"
```

## zoo


```r
> zoo(1:10, seq(2000, 2002.25, by = 0.25), frequency = 4)
```

```
2000(1) 2000(2) 2000(3) 2000(4) 2001(1) 2001(2) 2001(3) 2001(4) 2002(1) 
      1       2       3       4       5       6       7       8       9 
2002(2) 
     10 
```

