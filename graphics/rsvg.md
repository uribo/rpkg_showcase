

# rsvg: Render SVG Images into PDF, PNG, PostScript, or Bitmap Arrays

[![](http://www.r-pkg.org/badges/version/rsvg)](http://cran.rstudio.com/web/packages/rsvg/index.html)

* CRAN: http://cran.r-project.org/web/packages/rsvg/index.html
* GitHub: https://github.com/jeroenooms/rsvg


```r
> library(rsvg)
```

バージョン: 0.4

-----



| 関数名 | 概略 |
|--------|------|
| `rsvg` | Render SVG into Bitmap |

-----

## rsvg


```r
> # 図を作る
> tmp <- tempfile()
> svglite::svglite(tmp, width = 10, height = 7)
> ggplot2::qplot(mpg, wt, data = mtcars, colour = factor(cyl))
> dev.off()
> 
> bitmap <- rsvg(tmp, height = 1440)
> dim(bitmap) # h*w*c
> 
> # ファイルへの保存
> rsvg_pdf(svg = tmp, file = "out.pdf")
> rsvg_png(tmp, "out.png")
> rsvg_svg(tmp, "out.svg")
> rsvg_ps(tmp, "out.ps")
```

