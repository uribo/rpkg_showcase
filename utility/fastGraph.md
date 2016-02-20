

# fastGraph: Fast Drawing and Shading of Graphs of Statistical Distributions

確率分布の図を描画するのを補助する関数

[![](http://www.r-pkg.org/badges/version/fastGraph)](http://cran.rstudio.com/web/packages/fastGraph/index.html)

* CRAN: http://cran.r-project.org/web/packages/fastGraph/index.html


```r
> library(fastGraph)
```

バージョン: 1.0

-----



| 関数名 | 概略 |
|--------|------|
| `fastGraph-package` | Fast Drawing and Shading of Graphs of Statistical Distributions |
| `getMinMax` | Finds a Reasonable Domain for Plotting a Graph |
| `plotDist` | Plotting of Statistical Distributions |
| `plotLine` | X-Y Plotting with Simple Linear Regression Line and Equation |
| `shadeDist` | Displays Area Under Curve of Probability Density Function |
| `shadePhat` | Displays Area Under Curve of Probability Density Function of Sample Proportion |

-----

## plotDist

### Arguments

* dist
* param


```r
> plotDist(distA = "dnorm", 
+          parmA1 = 0, 
+          parmA2 = 1, 
+          distB = "dt", 
+          parmB1 = 3, 
+          parmB2 = 0, 
+          distC = "dt", 
+          parmC1 = 3, 
+          parmC2 = 1.4) 
```

## plotLine


```r
> x <- c( 2, 6, 5, -3, 11, 3 )
> y <- c( 16, 12, 19, -13, 27, 5 )
> plotLine(x, y )
```

## shadeDist

### Arguments

* xshade
* ddist
* parm1, param2
* lower.tail
* xlab
* xmin
* xmax
* xtic
* digits.prob
* digits.xtic
* is.discrete
* additional.x.range
* main
* col
* lwd
* ...


```r
> shadeDist(1.96)
```

## shadePhat


```r
> shadePhat(0.3, 20, 0.4)
```


