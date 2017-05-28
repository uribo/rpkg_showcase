

# franc: Detect the Language of Text

[![](http://www.r-pkg.org/badges/version/franc)](http://cran.rstudio.com/web/packages/franc/index.html)

- CRAN: http://cran.r-project.org/web/packages/franc/index.html
- GitHub: https://github.com/mangothecat/franc


```r
> library(franc)
```

バージョン: 1.1.1

-----



| 関数名 | 概略 |
|--------|------|
| `franc` | Detect the language of a string |
| `franc_all` | List of probably languages for a text |
| `speakers` | Number of speakers for 370 languages |

------

## franc


```r
> franc("吾輩は猫である。")
```

```
[1] "und"
```

```r
> franc("吾輩は猫である。", min_length = 2)
```

```
[1] "jpn"
```

```r
> franc("吾輩は猫である。名前はまだない。")
```

```
[1] "jpn"
```

## franc_all


```r
> franc_all("吾輩は猫である。名前はまだない。")
```

```
  language score
1      jpn     1
```

## speakers


```r
> speakers %>% class()
```

```
[1] "data.frame"
```

```r
> speakers %>% tibble::glimpse()
```

```
Observations: 370
Variables: 5
$ language <chr> "cmn", "spa", "eng", "rus", "arb", "ben", "hin", "por...
$ speakers <int> 885000000, 332000000, 322000000, 288000000, 280000000...
$ name     <chr> "Mandarin Chinese", "Spanish", "English", "Russian", ...
$ iso6391  <chr> NA, "es", "en", "ru", NA, "bn", "hi", "pt", "id", "ja...
$ iso6392  <chr> NA, "spa", "eng", "rus", NA, "ben", "hin", "por", "in...
```

