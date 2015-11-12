

# LeafArea: Rapid Digital Image Analysis of Leaf Area

[![](http://www.r-pkg.org/badges/version/LeafArea)](http://cran.rstudio.com/web/packages/LeafArea/index.html)

* CRAN: http://cran.r-project.org/web/packages/LeafArea/index.html
* GitHub: https://github.com/mattocci27/LeafArea


```r
> library(LeafArea)
> data("leafdata")
```

バージョン: 0.1.1

-----



| 関数名 | 概略 |
|--------|------|
| `LeafArea-package` | LeafArea: Rapid digital image analysis of leaf area |
| `eximg` | Utility function |
| `find.ij` | Checking a path to ImageJ |
| `leafdata` | LeafArea default data |
| `readtext.ij` | File management |
| `resmerge.ij` | File management |
| `run.ij` | Automated leaf area analysis |

-----

## find.ij

Image.Jのインストール状況を確認する


```r
> find.ij()
```

## leafdata


```r
> data("leafdata")
> str(leafdata, max.level = 2)
```

```
List of 7
 $ A1-01.jpeg.txt  :'data.frame':	2 obs. of  1 variable:
  ..$ Area: num [1:2] 117 124
 $ A1-02.jpeg.txt  :'data.frame':	1 obs. of  1 variable:
  ..$ Area: num 109
 $ A123-01.jpeg.txt:'data.frame':	1 obs. of  1 variable:
  ..$ Area: num 185
 $ A123-02.jpeg.txt:'data.frame':	2 obs. of  1 variable:
  ..$ Area: num [1:2] 123 111
 $ A2.jpeg.txt     :'data.frame':	4 obs. of  1 variable:
  ..$ Area: num [1:4] 43.3 47.6 41.4 44.9
 $ A300-1.jpeg.txt :'data.frame':	1 obs. of  1 variable:
  ..$ Area: num 158
 $ A300-2.jpeg.txt :'data.frame':	2 obs. of  1 variable:
  ..$ Area: num [1:2] 125 102
```

## run.ij


```r
> ex.dir <- eximg()
> run.ij(set.directory = ex.dir, save.image = TRUE)
```


