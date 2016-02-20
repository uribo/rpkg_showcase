

# svglite: An 'SVG' Graphics Device

[![](http://www.r-pkg.org/badges/version/svglite)](http://cran.rstudio.com/web/packages/svglite/index.html)

* CRAN: http://cran.r-project.org/web/packages/svglite/index.html
* GitHub: https://github.com/hadley/svglite


```r
> library(svglite)
```

バージョン: 1.1.0

-----



| 関数名 | 概略 |
|--------|------|
| `editSVG` | Run plotting code and open svg in OS/system default svg viewer or editor. |
| `htmlSVG` | Run plotting code and view svg in RStudio Viewer or web broswer. |
| `svglite` | An SVG Graphics Driver |
| `svgstring` | Access current SVG as a string. |
| `xmlSVG` | Run plotting code and return svg |

-----

## editSVG

RプロットをSVG形式（テキスト）に変換して、編集する


```r
> editSVG(plot(1:10))
```

```
Saving 7" x 7" image
```

## htmlSVG

Viewerパネルでプロットを出力


```r
> htmlSVG(hist(rnorm(100)))
```


## svglite

### Arguments

* file
* height, width
* bg
* pointsize
* standalone


```r
> svglite("Rplots.svg")
> plot(1:11, (-5:5)^2, type = 'b', main = "Simple Example")
> dev.off()
```

## svgstring

文字列をSVGに


```r
> s <- svgstring(); s()
> 
> plot.new(); s();
> text(0.5, 0.5, "Hi!"); s()
> dev.off()
```

## xmlSVG


```r
> xmlSVG(plot(1, axes = FALSE)) %>% {
+   print(.)
+   xml2::xml_find_all(., ".//text")
+ }
```

```
{xml_document}
<svg>
[1] <defs>\n  <style type="text/css"><![CDATA[\n    line, polyline, path ...
[2] <rect width="100%" height="100%" style="stroke: none; fill: #FFFFFF;"/>
[3] <defs>\n  <clipPath id="cp1">\n    <rect x="59.04" y="59.04" width=" ...
[4] <circle cx="266.40" cy="244.80" r="2.70pt" style="stroke-width: 0.75 ...
[5] <defs>\n  <clipPath id="cp2">\n    <rect x="0.00" y="0.00" width="50 ...
[6] <g clip-path="url(#cp2)">\n  <text x="246.83" y="485.28" style="font ...
[7] <g clip-path="url(#cp2)">\n  <text transform="translate(12.96,249.25 ...
```

```
{xml_nodeset (2)}
[1] <text x="246.83" y="485.28" style="font-size: 12.00pt; font-family:  ...
[2] <text transform="translate(12.96,249.25) rotate(-90)" style="font-si ...
```

