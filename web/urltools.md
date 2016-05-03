

# urltools: Vectorised Tools for URL Handling and Parsing

[![](http://www.r-pkg.org/badges/version/urltools)](http://cran.rstudio.com/web/packages/urltools/index.html)

* CRAN: http://cran.r-project.org/web/packages/urltools/index.html
* GitHub: https://github.com/Ironholds/urltools


```r
> library(urltools)
```

バージョン: 1.4.0

-----



| 関数名 | 概略 |
|--------|------|
| `domain` | Get or set a URL's domain |
| `fragment` | Get or set a URL's fragment |
| `param_get` | get the values of a URL's parameters |
| `param_remove` | Remove key-value pairs from query strings |
| `param_set` | Set the value associated with a parameter in a URL's query. |
| `parameters` | Get or set a URL's parameters |
| `path` | Get or set a URL's path |
| `port` | Get or set a URL's port |
| `scheme` | Get or set a URL's scheme |
| `suffix_dataset` | Dataset of public suffixes |
| `suffix_extract` | extract the suffix from domain names |
| `url_compose` | Recompose Parsed URLs |
| `url_decode` | Encode or decode a URI |
| `url_parse` | split URLs into their component parts |
| `urltools` | Tools for handling URLs |

-----

## domain

ドメイン名取得


```r
> domain("http://cran.r-project.org/submit.html")
```

```
[1] "cran.r-project.org"
```

## fragment


```r
> example_url <- "http://en.wikipedia.org/wiki/Aaron_Halfaker?debug=true#test"
> fragment(example_url)
```

```
[1] "test"
```

## param_get

### Arguments

* urls
* parameter_names


```r
> url <- "https://google.com:80/foo.php?this_parameter=selfreferencing&hiphop=awesome"
> (parameter_values <- param_get(url, c("this_parameter","hiphop")))
```

```
   this_parameter  hiphop
1 selfreferencing awesome
```

## parameters

パラメータとその値を取得


```r
> parameters("http://en.wikipedia.org/wiki/Aaron_Halfaker?debug=true")
```

```
[1] "debug=true"
```

## path

## port

ポート番号取得


```r
> port("http://cran.r-project.org:80/submit.html")
```

```
[1] "80"
```

## scheme

URLスキーム


```r
> example_url <- "http://cran.r-project.org/submit.html"
> scheme(example_url)
```

```
[1] "http"
```

## suffix_dataset


```r
> data("suffix_dataset")
> suffix_dataset %>% str()
```

```
 chr [1:7432] "ac" "com.ac" "edu.ac" "gov.ac" "net.ac" ...
```

## suffix_extract


```r
> domain_name <- url_parse("http://en.wikipedia.org")$domain
> suffix_extract(domain_name)
```

```
              host subdomain    domain suffix
1 en.wikipedia.org        en wikipedia    org
```

## url_decode / url_encode

URLのエンコードとデコード


```r
> url_decode("https://ja.wikipedia.org/wiki/東京ドーム") %>% {
+   print(.)
+   url_encode(.)
+ }
```

```
[1] "https://ja.wikipedia.org/wiki/東京ドーム"
```

```
[1] "https://ja.wikipedia.org/wiki%2f%e6%9d%b1%e4%ba%ac%e3%83%89%e3%83%bc%e3%83%a0"
```


## url_parse

URLを分割する


```r
> url_parse("https://en.wikipedia.org/wiki/Article")
```

```
  scheme           domain port         path parameter fragment
1  https en.wikipedia.org <NA> wiki/Article      <NA>     <NA>
```

