

# assertthat: Easy pre and post assertions.

[![](http://www.r-pkg.org/badges/version/assertthat)](http://cran.rstudio.com/web/packages/assertthat/index.html)

* CRAN: http://cran.r-project.org/web/packages/assertthat/index.html
* GitHub: https://github.com/hadley/assertthat


```r
> library(assertthat)
```

バージョン: 0.1

-----



| 関数名 | 概略 |
|--------|------|
| `are_equal` | Are two objects equal? |
| `assert_that` | Assert that certain conditions are true. |
| `assertions-file` | Useful test related to files |
| `has_args` | Check a function has specified arguments |
| `has_attr` | Has attribute or name? |
| `is.count` | Assert input is a scalar. |
| `is.date` | Missing is functions. |
| `noNA` | Does object contain any missing values? |
| `not_empty` | Check an object doesn't have any empty dimensions |
| `on_failure` | Custom failure messages for assertions. |
| `validate_that` | Validate that certain conditions are true. |

------

## are_equal

オブジェクトが等しいかを確認


```r
> x <- pi %>% round(2)
> are_equal(3.14, x)
```

```
[1] TRUE
```

## assert-is / is.error / is.time / is.date


```r
> a <- Sys.time()
> is.time(a)
```

```
[1] TRUE
```

```r
> b <- Sys.Date()
> is.date(b)
```

```
[1] TRUE
```

```r
> c <- try(stop("!!"))
> is.error(c)
```

```
[1] TRUE
```


## assert_that / see_if


```r
> x <- 2
> are_equal(x, 1.9) %>% see_if()
```

```
Error: is.call(call) is not TRUE
```

## has_args

関数が対象の引数をもつかを判定

### Arguments

* f
* args
* exact


```r
> has_args(mean, "x")
```

```
[1] TRUE
```

```r
> has_args(mean, "x", exact = TRUE)
```

```
[1] FALSE
```

```r
> see_if(mean %has_args% "x")
```

```
[1] TRUE
```

## noNA

オブジェクトが欠損値を含まないか


```r
> see_if(noNA("a"))
```

```
[1] TRUE
```

```r
> see_if(noNA(c(TRUE, NA)))
```

```
[1] FALSE
attr(,"msg")
[1] "c(TRUE, NA) contains 1 missing values"
```

## not_empty


```r
> not_empty(mtcars[0, ])
```

```
[1] FALSE
```

```r
> c(NULL, 3, "", 1) %>% not_empty()
```

```
[1] TRUE
```



## scalar / is.scalar / is.string / is.number / is.flag / is.count


```r
> see_if(is.scalar("a"))
```

```
[1] TRUE
```

## validate_that


```r
> validate_that(is.numeric(x))
```

```
[1] TRUE
```

```r
> validate_that(is.character(x))
```

```
[1] "x is not a character vector"
```

```r
> validate_that(length(x) == 3)
```

```
[1] "length(x) not equal to 3"
```
