

# ndjson: Wicked-Fast Streaming 'JSON' ('ndjson') Reader

行区切りのJSONデータに対応

[![](http://www.r-pkg.org/badges/version/ndjson)](http://cran.rstudio.com/web/packages/ndjson/index.html)

- CRAN: http://cran.r-project.org/web/packages/ndjson/index.html
- GitHub: http://gitlab.com/hrbrmstr/ndjson


```r
> library(ndjson)
```

バージョン: 0.2.0

-----



| 関数名 | 概略 |
|--------|------|
| `ndjson` | Wicked-fast Streaming JSON ('ndjson) Reader |
| `stream_in` | Stream in & flatten an ndjson file into a 'tbl_dt' |
| `validate` | Validate ndjson file |

------

## stream_in


```r
> stream_in(system.file("extdata", "test.json", package="ndjson"))
```

```
Error: Argument 'con' must be a connection.
```


