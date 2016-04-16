

# leaflet: Create Interactive Web Maps with the JavaScript 'Leaflet' Library

Javascriptライブラリleafletを用いたインタラクティブな地図の可視化

[![](http://www.r-pkg.org/badges/version/leaflet)](http://cran.rstudio.com/web/packages/leaflet/index.html)

* CRAN: http://cran.r-project.org/web/packages/leaflet/index.html
* GitHub: https://github.com/rstudio/leaflet/
* URL: http://rstudio.github.io/leaflet/


```r
> library(leaflet)
```

```

Attaching package: 'leaflet'
```

```
The following object is masked from 'package:dendextend':

    %>%
```

バージョン: 1.0.1.9003

-----


|.                                                                      |
|:----------------------------------------------------------------------|
|JS                      Objects imported from other packages           |
|addAwesomeMarkers       Add Awesome Markers                            |
|addControl              Graphics elements and layers                   |
|addLayersControl        Add UI controls to switch layers on and off    |
|addLegend               Add a color legend to a map                    |
|addMagnifyingGlass      Add a Magnifying glass on a map                |
|addMeasure              Add a measure control to the map.              |
|addMiniMap              Add a minimap to the Map <URL:                 |
|https://github.com/Norkart/Leaflet-MiniMap>                            |
|addProviderTiles        Add a tile layer from a known map provider     |
|addRasterImage          Add a raster image as a layer                  |
|addScaleBar             Add or remove a scale bar                      |
|addSimpleGraticule      Add a simple Graticule on the map see <URL:    |
|https://github.com/ablakey/Leaflet.SimpleGraticule>                    |
|addTerminator           Add a daylight layer on top of the map         |
|awesomeIconList         Make awesome-icon set                          |
|awesomeIcons            Create a list of awesome icon data see <URL:   |
|https://github.com/lvoogdt/Leaflet.awesome-markers>                    |
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
|makeAwesomeIcon         Make Awesome Icon                              |
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
| `addAwesomeMarkers` | Add Awesome Markers |
| `addControl` | Graphics elements and layers |
| `addLayersControl` | Add UI controls to switch layers on and off |
| `addLegend` | Add a color legend to a map |
| `addMagnifyingGlass` | Add a Magnifying glass on a map |
| `addMeasure` | Add a measure control to the map. |
| `addMiniMap` | Add a minimap to the Map <URL: https://github.com/Norkart/Leaflet-MiniMap> |
| `addProviderTiles` | Add a tile layer from a known map provider |
| `addRasterImage` | Add a raster image as a layer |
| `addScaleBar` | Add or remove a scale bar |
| `addSimpleGraticule` | Add a simple Graticule on the map see <URL: https://github.com/ablakey/Leaflet.SimpleGraticule> |
| `addTerminator` | Add a daylight layer on top of the map |
| `awesomeIconList` | Make awesome-icon set |
| `awesomeIcons` | Create a list of awesome icon data see <URL: https://github.com/lvoogdt/Leaflet.awesome-markers> |
| `colorNumeric` | Color mapping |
| `createLeafletMap` | Legacy functions |
| `dispatch` | Extension points for plugins |
| `iconList` | Make icon set |
| `icons` | Create a list of icon data |
| `leaflet` | Create a Leaflet map widget |
| `leafletOutput` | Wrapper functions for using 'leaflet' in 'shiny' |
| `leafletProxy` | Send commands to a Leaflet instance in a Shiny app |
| `makeAwesomeIcon` | Make Awesome Icon |
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

## leaflet

leaflet地図ウィジェットの作成

### Arguments

* data
* width
* height


```r
> leaflet() %>% addTiles()
```


## tileOptions / WMSTileOptions / popupOptions / labelOptions / markerOptions / markerClusterOptions / pathOptions


```r
> tileOptions(minZoom = 0, maxZoom = 18, maxNativeZoom = NULL,
+   tileSize = 256, subdomains = "abc", errorTileUrl = "", tms = FALSE,
+   continuousWorld = FALSE, noWrap = FALSE, zoomOffset = 0,
+   zoomReverse = FALSE, opacity = 1, zIndex = NULL,
+   unloadInvisibleTiles = NULL, updateWhenIdle = NULL,
+   detectRetina = FALSE, reuseTiles = FALSE)
> 
> WMSTileOptions(styles = "", format = "image/jpeg", transparent = FALSE,
+   version = "1.1.1", crs = NULL, ...)
> 
> popupOptions(maxWidth = 300, minWidth = 50, maxHeight = NULL,
+   autoPan = TRUE, keepInView = FALSE, closeButton = TRUE,
+   zoomAnimation = TRUE, closeOnClick = NULL, className = "")
> 
> labelOptions(clickable = FALSE, noHide = FALSE, className = "",
+   direction = "right", offset = c(12, -15), opacity = 1,
+   zoomAnimation = TRUE)
> 
> markerOptions(clickable = TRUE, draggable = FALSE, keyboard = TRUE,
+   title = "", alt = "", zIndexOffset = 0, opacity = 1,
+   riseOnHover = FALSE, riseOffset = 250)
> 
> markerClusterOptions(showCoverageOnHover = TRUE, zoomToBoundsOnClick = TRUE,
+   spiderfyOnMaxZoom = TRUE, removeOutsideVisibleBounds = TRUE, ...)
> 
> pathOptions(lineCap = NULL, lineJoin = NULL, clickable = TRUE,
+   pointerEvents = NULL, className = "")
```

