

# multiplyr: Data Manipulation with Parallelism and Shared Memory Matrices

[![](http://www.r-pkg.org/badges/version/multiplyr)](http://cran.rstudio.com/web/packages/multiplyr/index.html)

* CRAN: http://cran.r-project.org/web/packages/multiplyr/index.html
* Vignettes:
    * [Multiplyr basics](https://cran.rstudio.com/web/packages/multiplyr/vignettes/basics.pdf)


```r
> library(multiplyr)
```

```

Attaching package: 'multiplyr'
```

```
The following objects are masked from 'package:dplyr':

    arrange, arrange_, distinct, distinct_, filter, filter_,
    group_by, group_by_, mutate, mutate_, regroup, rename,
    rename_, rowwise, select, select_, slice, summarise,
    summarise_, transmute, transmute_, ungroup
```

```
The following object is masked from 'package:stats':

    filter
```

バージョン: 0.1.0

-----



| 関数名 | 概略 |
|--------|------|
| `Multiplyr-class` | Parallel processing data frame |
| `Multiplyr-methods` | Data access methods for Multiplyr arrange Sort data define Define new columns |
| `distinct` | Select unique rows or unique combinations of variables |
| `distribute` | Calculations for how to distribute x items over N nodes |
| `filter` | Filter data group_by Group data |
| `group_sizes` | Return size of groups |
| `multiplyr` | Data Manipulation with Parellelism and Shared Memory Matrices |
| `mutate` | Change values of existing variables (and create new ones) |
| `nsa` |No strings attached mode |
| `partition_even` | Partition data evenly amongst cluster nodes |
| `partition_group` |  Partition data so that each group is wholly on a node |
| `reduce` | Summarise data (with local reduction) |
| `regroup` | Return to grouped data |
| `rename` | Rename variables |
| `select` | Retain only specified variables |
| `shutdown` | Shutdown running cluster |
| `slice` | Select rows by position |
| `summarise` | Summarise data |
| `transmute` | Change variables and drop all others |
| `undefine` | Delete variables |
| `ungroup` | Return data to non-grouped |
| `within_group` | Execute code within a group |
| `within_node` | Execute code within a node |

