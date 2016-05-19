

# rvg: R Graphics Devices for Vector Graphics Output

* CRAN: http://cran.r-project.org/web/packages/pipeR/index.html
* GitHub: https://github.com/davidgohel/rvg


```r
> library(rvg)
```

```

Attaching package: 'rvg'
```

```
The following object is masked from 'package:magrittr':

    set_attr
```

バージョン: 0.0.9

-----



| 関数名 | 概略 |
|--------|------|
| `dml_docx` | DrawingML graphic device for Microsoft Word |
| `dml_pptx` | DrawingML graphic device for Microsoft PowerPoint |
| `drawDetails.interactivePointsGrob` | interactivePointsGrob drawing |
| `drawDetails.interactivePolygonGrob` | interactivePolygonGrob drawing |
| `drawDetails.interactivePolylineGrob` | interactivePolylineGrob drawing |
| `drawDetails.interactiveRectGrob` | interactiveRectGrob drawing |
| `drawDetails.interactiveSegmentsGrob` | interactiveSegmentsGrob drawing |
| `drawDetails.interactiveTextGrob` | interactiveTextGrob drawing |
| `dsvg` | SVG Graphics Driver |
| `dsvg_view` | Run plotting code and view svg in RStudio Viewer or web broswer. |
| `interactivePointsGrob` | Generate interactive grob points |
| `interactivePolygonGrob` | Generate interactive grob polygons |
| `interactivePolylineGrob` | Generate an Interactive Grob Path |
| `interactiveRectGrob` | Generate interactive grob rectangles |
| `interactiveSegmentsGrob` | Generate interactive grob segments |
| `interactiveTextGrob` | Generate interactive grob text |
| `rvg_tracer_off` | trace off id colection |
| `rvg_tracer_on` | trace on id colection |
| `send_click` | send click |
| `send_tooltip` | send tooltip |
| `set_data_id` | add id |
| `write_docx` | Microsoft Word Graphics Device |
| `write_pptx` | Microsoft PowerPoint Graphics Device |

-----

## dsvg_view


```r
> dsvg_view(hist(rnorm(100)))
```


## write_docx


```r
> write_docx(file = "my_plot_1.docx", code = plot(rnorm(10)) )
```


## write_pptx



