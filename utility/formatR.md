

# formatR: Format R Code Automatically

Rコードの自動的整形

[![](http://www.r-pkg.org/badges/version/formatR)](http://cran.rstudio.com/web/packages/formatR/index.html)

- CRAN: http://cran.r-project.org/web/packages/formatR/index.html
- GitHub: https://github.com/yihui/formatR
- URL: http://yihui.name/formatR


```r
> library(formatR)
```

バージョン: 1.4

-----



| 関数名 | 概略 |
|--------|------|
| `tidy_app` | A Shiny app to format R code |
| `tidy_dir` | Format the R scripts under a directory  |
| `tidy_eval` | Evaluate R code and mask the output by a prefix |
| `tidy_source` | Reformat R code while preserving blank lines and comments |
| `usage` | Show the usage of a function |

-----

## tidy_app

## 


```r
> tidy_eval(text = c("a<-1+1;a", "matrix(rnorm(10),5)"))
```

```
a <- 1 + 1
a
## [1] 2

matrix(rnorm(10), 5)
##            [,1]       [,2]
## [1,]  0.7797394 -0.3443671
## [2,]  0.9413417  2.7080593
## [3,] -1.4073092 -2.4704076
## [4,]  0.6452825 -0.7786994
## [5,] -0.5611467  0.7118624
```


## tidy_source


```r
> messy = system.file("format", "messy.R", package = "formatR")
> readLines(messy)
```

```
 [1] "    # a single line of comments is preserved"                                                                            
 [2] "1+1"                                                                                                                     
 [3] ""                                                                                                                        
 [4] "if(TRUE){"                                                                                                               
 [5] "x=1  # inline comments"                                                                                                  
 [6] "}else{"                                                                                                                  
 [7] "x=2;print('Oh no... ask the right bracket to go away!')}"                                                                
 [8] "1*3 # one space before this comment will become two!"                                                                    
 [9] "2+2+2    # 'short comments'"                                                                                             
[10] ""                                                                                                                        
[11] "# only 'single quotes' are allowed in comments"                                                                          
[12] "df=data.frame(y=rnorm(100),x1=rnorm(100),x2=rnorm(100))"                                                                 
[13] "lm(y~x1+x2, data=df)"                                                                                                    
[14] "1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1+1  ## comments after a long line"                                            
[15] ""                                                                                                                        
[16] "## here is a long long long long long long long long long long long long long long long long long long long long comment"
```

```r
> tidy_source(messy)
```

```
# a single line of comments is preserved
1 + 1

if (TRUE) {
    x = 1  # inline comments
} else {
    x = 2
    print("Oh no... ask the right bracket to go away!")
}
1 * 3  # one space before this comment will become two!
2 + 2 + 2  # 'short comments'

# only 'single quotes' are allowed in comments
df = data.frame(y = rnorm(100), x1 = rnorm(100), x2 = rnorm(100))
lm(y ~ x1 + x2, data = df)
1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 
    1 + 1 + 1 + 1  ## comments after a long line

## here is a long long long long long long long long long long long long long
## long long long long long long long comment
```

## usage


```r
> usage(var)
```

```
var(x, y = NULL, na.rm = FALSE, use)
```

```r
> usage(plot)
```

```
plot(x, y, ...)
```

```r
> usage("plot.lm")
```

```
## S3 method for class 'lm'
plot(x, which = c(1L:3L, 5L), caption = list("Residuals vs Fitted", "Normal Q-Q", 
    "Scale-Location", "Cook's distance", "Residuals vs Leverage", expression("Cook's dist vs Leverage  " * 
        h[ii]/(1 - h[ii]))), panel = if (add.smooth) panel.smooth else points, 
    sub.caption = NULL, main = "", ask = prod(par("mfcol")) < length(which) && 
        dev.interactive(), ..., id.n = 3, labels.id = names(residuals(x)), cex.id = 0.75, 
    qqline = TRUE, cook.levels = c(0.5, 1), add.smooth = getOption("add.smooth"), 
    label.pos = c(4, 2), cex.caption = 1, cex.oma.main = 1.25)
```

