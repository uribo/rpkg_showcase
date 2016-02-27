

# gridSVG: Export 'grid' Graphics as SVG

[![](http://www.r-pkg.org/badges/version/gridSVG)](http://cran.rstudio.com/web/packages/gridSVG/index.html)

* CRAN: http://cran.r-project.org/web/packages/gridSVG/index.html
* Vignettes:
    * [animation](https://cran.r-project.org/web/packages/gridSVG/vignettes/animation.pdf)
    * [extensibility](https://cran.r-project.org/web/packages/gridSVG/vignettes/extensibility.pdf)
    * [gridSVG](https://cran.r-project.org/web/packages/gridSVG/vignettes/gridSVG.pdf)


```r
> library(gridSVG)
```

```

Attaching package: 'gridSVG'
```

```
The following object is masked from 'package:grDevices':

    dev.off
```

バージョン: 1.5.0

-----



| 関数名 | 概略 |
|--------|------|
| `animUnit` | Generate a set of animation values. |
| `animate` | Convert animation specifications to SVG elements. |
| `clipPath` | Create the definition of a non-rectangular clipping path. |
| `fe` | Creating a generic filter effect |
| `feBlend` | Blend two objects together. |
| `feColorMatrix` | Apply a matrix transformation on colour values. |
| `feComponentTransfer` | Perform Colour Component-wise Remapping. |
| `feComposite` | Combine images using Porter-Duff operations. |
| `feConvolveMatrix` | Apply a matrix convolution filter effect. |
| `feDiffuseLighting` | Light an image using the alpha channel as a bump map. |
| `feDisplacementMap` | Displace pixel values from a filter input.  |
| `feDistantLight` | Create a Distant Light Source  |
| `feFlood` | Create and fill a rectangular region. |
| `feGaussianBlur` | Apply a Gaussian blur to an image. |
| `feImage` | Draw a referred image. |
| `feMerge` | Composite image layers together. |
| `feMorphology` | "Fatten" or "thin" artwork. |
| `feOffset` | Offset an input image relative to its current position. |
| `fePointLight` | Create a Point Light Source |
| `feSpecularLighting` | Light an image using the alpha channel as a bump map. |
| `feSpotLight` | Create a Spot Light Source |
| `feTile` | Fill a rectangle with a tiled pattern of an input image. |
| `feTurbulence` | Create an image using the Perlin turbulence function. |
| `filterEffect` | Creating Filter Effects |
| `filterInputs` | Identifies input for a filter effect primitive. |
| `garnish` | Convert animation specifications to SVG elements. |
| `getSVGFonts` | Manage SVG fonts  |
| `getSVGMappings` | Retrieving Viewport, Grob, and Reference Names as SVG IDs, CSS Selectors and XPath Expressions |
| `grid.animate` | Animate a grid grob |
| `grid.clipPath` | Apply a clipping path to a grid grob. |
| `grid.comment` | Create a grid grob representing a comment |
| `grid.element` | Create a grid grob representing an SVG element |
| `grid.export` | Generate SVG output from a grid graphic |
| `grid.filter` | Associate a filter effect with a grid grob. |
| `grid.garnish` | Associate arbitrary SVG attributes with a grid grob |
| `grid.gradientFill` | Associate a gradient fill with a grid grob  |
| `grid.hyperlink` | Associate a hyperlink with a grid grob  |
| `grid.mask` | Apply an opacity mask to a grid grob. |
| `grid.patternFill` | Associate a pattern fill with a grid grob |
| `grid.script` | Create a grid grob containing an SVG script |
| `gridSVG.newpage` | Move to a New Page on a gridSVG Device  |
| `gridSVGCoords` | Importing an external coordinate system |
| `gridSVGMappings` | Mapping Viewport, Grob and Reference Names to SVG IDs |
| `gridsvg` | gridSVG Graphics Device |
| `grobToDev` | Convert a grob to device calls |
| `linearGradient` | Create Linear and Radial Gradients |
| `listSVGDefinitions` | List All Reference Definitions |
| `mask` | Create the definition of an opacity mask. |
| `pattern` | Create a definition of a fill pattern.  |
| `popContext` | Leaving A Modified Viewport Context |
| `primToDev` | Convert a grob to device calls |
| `pushClipPath` | Apply a clipping context to the current viewport. |
| `pushMask` | Apply a masking context to the current viewport. |
| `readCoordsJS` | Importing JavaScript coordinate information. |
| `readMappingsJS` | Importing JavaScript mapping information. |
| `registerFilter` | Create the definition a filter effect.  |
| `registerGradientFill` | Create a definition of a gradient fill. |
| `setSVGoptions` | Get and Set Global Options |
| `viewportConvertX` | Functions for using an imported coordinate system |
| `viewportCreate` | Recreate a viewport from imported coordinate information. |

-----
