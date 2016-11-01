

# XML2R: EasieR XML data collection

[![](http://www.r-pkg.org/badges/version/XML2R)](http://cran.rstudio.com/web/packages/XML2R/index.html)

- CRAN: http://cran.r-project.org/web/packages/XML2R/index.html
- GitHub: https://github.com/cpsievert/XML2R
- URL: http://cpsievert.github.io/XML2R/


```r
> library(XML2R)
```

バージョン: 0.0.6

-----



| 関数名 | 概略 |
|--------|------|
| `XML2Obs` | Parse XML files into a list of "observations" |
| `XML2R` | Parse XML files into (a list of) matrices or data frame(s) |
| `add_key` | Add a key to connect parents to descendants  |
| `collapse_obs` | Collapse a list of observations into a list of tables. |
| `docsToNodes` | Parse XML Documents into XML Nodes |
| `listsToObs` | Flatten nested list into a list of observations |
| `nodesToList` | Coerce XML Nodes into a list with both attributes and values |
| `re_name` | Rename rows of a list |
| `urlsToDocs` | Parse XML Files into XML Documents |

-----

## XML2Obs


```r
> obs <- XML2Obs("http://gd2.mlb.com/components/game/mlb/year_2013/month_06/day_14/gid_2013_06_14_seamlb_oakmlb_1/inning/inning_all.xml")
```

```
http://gd2.mlb.com/components/game/mlb/year_2013/month_06/day_14/gid_2013_06_14_seamlb_oakmlb_1/inning/inning_all.xml 
```

```r
> table(names(obs))
```

```

                               game                        game//inning 
                                  1                                   9 
       game//inning//bottom//action         game//inning//bottom//atbat 
                                  5                                  35 
 game//inning//bottom//atbat//pitch     game//inning//bottom//atbat//po 
                                131                                   2 
game//inning//bottom//atbat//runner           game//inning//top//action 
                                 24                                   3 
           game//inning//top//atbat     game//inning//top//atbat//pitch 
                                 39                                 167 
       game//inning//top//atbat//po    game//inning//top//atbat//runner 
                                  6                                  36 
```

## XML2R


```r
> res <- XML2R("http://gd2.mlb.com/components/game/mlb/year_2013/month_06/day_14/gid_2013_06_14_seamlb_oakmlb_1/inning/inning_all.xml")
```

```
http://gd2.mlb.com/components/game/mlb/year_2013/month_06/day_14/gid_2013_06_14_seamlb_oakmlb_1/inning/inning_all.xml 
```

```r
> res %>% class()
```

```
[1] "array"
```

```r
> res %>% names()
```

```
 [1] "game"                               
 [2] "game//inning"                       
 [3] "game//inning//bottom//action"       
 [4] "game//inning//bottom//atbat"        
 [5] "game//inning//bottom//atbat//pitch" 
 [6] "game//inning//bottom//atbat//po"    
 [7] "game//inning//bottom//atbat//runner"
 [8] "game//inning//top//action"          
 [9] "game//inning//top//atbat"           
[10] "game//inning//top//atbat//pitch"    
[11] "game//inning//top//atbat//po"       
[12] "game//inning//top//atbat//runner"   
```


