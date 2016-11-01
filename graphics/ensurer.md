

# ensurer: Ensure Values at Runtime

[![](http://www.r-pkg.org/badges/version/ensurer)](http://cran.rstudio.com/web/packages/ensurer/index.html)

- CRAN: http://cran.r-project.org/web/packages/ensurer/index.html
- Vignettes: 
    - [The ensurer package](https://cran.r-project.org/web/packages/ensurer/vignettes/ensurer.html)
- GitHub: https://github.com/smbache/ensurer


```r
> library(ensurer)
```

バージョン: 1.1

-----



| 関数名 | 概略 |
|--------|------|
| `check_that` | Ensure Certain Conditions for a Value at Runtime. |
| `ensurer` | ensurer - Ensure Values at Runtime |
| `print.ensurer` | Print method for ensurer contracts |

-----

## check_that / check


```r
> if (check_that(my_sequence, is.numeric))
+   message("Success!")
```

```
Error in check_(.): object 'my_sequence' not found
```


## ensurer / ensure_that / ensures_that / ensures


```r
> ensure_that(1:10, is.integer)
```

```
 [1]  1  2  3  4  5  6  7  8  9 10
```

```r
> letters %>%
+   ensure_that(length(.) == 26) %>%
+   ensure_that(all(. == tolower(.)))
```

```
 [1] "a" "b" "c" "d" "e" "f" "g" "h" "i" "j" "k" "l" "m" "n" "o" "p" "q"
[18] "r" "s" "t" "u" "v" "w" "x" "y" "z"
```

