

# leaflet: Create Interactive Web Maps with the JavaScript 'Leaflet' Library

Javascriptライブラリleafletを用いたインタラクティブな地図の可視化

[![](http://www.r-pkg.org/badges/version/leaflet)](http://cran.rstudio.com/web/packages/leaflet/index.html)

* GitHub: https://github.com/rstudio/leaflet/
* CRAN: http://cran.r-project.org/web/packages/leaflet/index.html
* URL: http://rstudio.github.io/leaflet/


```r
> library(leaflet)
```

バージョン: 1.0.0

-----


|.                                                                      |
|:----------------------------------------------------------------------|
|JS                      Objects imported from other packages           |
|addControl              Graphics elements and layers                   |
|addLayersControl        Add UI controls to switch layers on and off    |
|addLegend               Add a color legend to a map                    |
|addProviderTiles        Add a tile layer from a known map provider     |
|addRasterImage          Add a raster image as a layer                  |
|colorNumeric            Color mapping                                  |
|createLeafletMap        Legacy functions                               |
|dispatch                Extension points for plugins                   |
|iconList                Make icon set                                  |
|icons                   Create a list of icon data                     |
|leaflet                 Create a Leaflet map widget                    |
|leafletOutput           Wrapper functions for using 'leaflet' in       |
|'shiny'                                                                |
|leafletProxy            Send commands to a Leaflet instance in a Shiny |
|app                                                                    |
|makeIcon                Define icon sets                               |
|mapOptions              Set options on a leaflet map object            |
|previewColors           Color previewing utility                       |
|removeControl           Remove elements from a map                     |
|setView                 Methods to manipulate the map widget           |
|showGroup               Show or hide layer groups                      |
|tileOptions             Extra options for map elements and layers      |


| 関数名 | 概略 |
|--------|------|
| `JS` | Objects imported from other packages |
| `addControl` | Graphics elements and layers |
| `addLayersControl` | Add UI controls to switch layers on and off |
| `addLegend` | Add a color legend to a map |
| `addProviderTiles` | Add a tile layer from a known map provider |
| `addRasterImage` | Add a raster image as a layer |
| `colorNumeric` | Color mapping |
| `createLeafletMap` | Legacy functions |
| `dispatch` | Extension points for plugins |
| `iconList` | Make icon set |
| `icons` | Create a list of icon data |
| `leaflet` | Create a Leaflet map widget |
| `leafletOutput` | Wrapper functions for using 'leaflet' in 'shiny' |
| `leafletProxy` | Send commands to a Leaflet instance in a Shiny app |
| `makeIcon` | Define icon sets |
| `mapOptions` | Set options on a leaflet map object |
| `previewColors` | Color previewing utility |
| `removeControl` | Remove elements from a map |
| `setView` | Methods to manipulate the map widget |
| `showGroup` | Show or hide layer groups |
| `tileOptions` | Extra options for map elements and layers |

-----

## colorNumeric


```r
> colorNumeric("Blues", domain = NULL) %>% previewColors(sort(rexp(16)))
> 
> pal <- colorBin("Greens", domain = 0:100)
> pal(runif(10, 60, 100))
```
