

# colormap: Color Palettes using Colormaps Node Module

[![](http://www.r-pkg.org/badges/version/colormap)](http://cran.rstudio.com/web/packages/colormap/index.html)

- CRAN: http://cran.r-project.org/web/packages/colormap/index.html
- GitHub: https://github.com/bhaskarvk/colormap


```r
> library(colormap)
```

バージョン: 0.1.3

-----



| 関数名 | 概略 |
|--------|------|
|colormap | A package to generate colors from a list of 44 pre-defined palettes |
|colormap_pal | Create a Palette generating function |
|colormaps | List of pre-defined colormaps |
|scale_color_colormap | Colormap color scales |

-----

## colormap


```r
> colormap()
```

```
 [1] "#000083ff" "#000687ff" "#000e8cff" "#001390ff" "#001b95ff"
 [6] "#00239aff" "#00299dff" "#0030a2ff" "#0036a6ff" "#003caaff"
[11] "#0048afff" "#0152b3ff" "#015eb9ff" "#0167bdff" "#0174c2ff"
[16] "#0280c8ff" "#0289ccff" "#0296d1ff" "#039fd5ff" "#03abdbff"
[21] "#03b8e0ff" "#03c1e4ff" "#04cde9ff" "#04d7edff" "#04e3f3ff"
[26] "#05f0f8ff" "#05f9fcff" "#09fffbff" "#15ffefff" "#25ffdfff"
[31] "#35ffceff" "#41ffc2ff" "#50ffb2ff" "#5cffa6ff" "#6cff96ff"
[36] "#7cff86ff" "#88ff79ff" "#98ff69ff" "#a8ff59ff" "#b4ff4dff"
[41] "#c3ff3dff" "#cfff31ff" "#dfff20ff" "#efff10ff" "#fbff04ff"
[46] "#fff700ff" "#ffeb00ff" "#fedb00ff" "#feca00ff" "#febe00ff"
[51] "#fdae00ff" "#fda200ff" "#fd9200ff" "#fd8200ff" "#fc7500ff"
[56] "#fc6500ff" "#fc5900ff" "#fb4900ff" "#fb3900ff" "#fb2d00ff"
[61] "#fb1c00ff" "#fa1000ff" "#fa0000ff" "#ee0000ff" "#e20000ff"
[66] "#d30000ff" "#c70000ff" "#b70000ff" "#a70000ff" "#9c0000ff"
[71] "#8c0000ff" "#800000ff"
```

```r
> colormap(colormap = c('#000000','#FF0000'), 
+          nshades = 20)
```

```
 [1] "#000000ff" "#0d0000ff" "#1a0000ff" "#280000ff" "#350000ff"
 [6] "#430000ff" "#500000ff" "#5e0000ff" "#6b0000ff" "#790000ff"
[11] "#860000ff" "#940000ff" "#a10000ff" "#af0000ff" "#bc0000ff"
[16] "#ca0000ff" "#d70000ff" "#e50000ff" "#f20000ff" "#ff0000ff"
```

## colormap_pal


```r
> scales::show_col(colormap_pal()(10))
```

## colormaps


```r
> colormaps %>% names()
```

```
 [1] "jet"              "hsv"              "hot"             
 [4] "cool"             "spring"           "summer"          
 [7] "autumn"           "winter"           "bone"            
[10] "copper"           "greys"            "YIGnBu"          
[13] "greens"           "YIOrRd"           "bluered"         
[16] "RdBu"             "picnic"           "rainbow"         
[19] "portland"         "blackbody"        "earth"           
[22] "electric"         "viridis"          "inferno"         
[25] "magma"            "plasma"           "warm"            
[28] "cool"             "rainbow_soft"     "bathymetry"      
[31] "cdom"             "chlorophyll"      "density"         
[34] "freesurface_blue" "freesurface_red"  "oxygen"          
[37] "par"              "phase"            "salinity"        
[40] "temperature"      "turbidity"        "velocity_blue"   
[43] "velocity_green"   "cubehelix"       
```

## scale_color_colormap


```r
> scale_color_colormap
```

