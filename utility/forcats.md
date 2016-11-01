

# forcats: Tools for Working with Categorical Variables (Factors)

要因型データの操作

[![](http://www.r-pkg.org/badges/version/forcats)](http://cran.rstudio.com/web/packages/forcats/index.html)

- CRAN: http://cran.r-project.org/web/packages/forcats/index.html
- GitHub: https://github.com/hadley/forcats


```r
> library(forcats)
```

バージョン: 0.1.1

-----



| 関数名 | 概略 |
|--------|------|
| `fct_anon` | Anonymise factor levels |
| `fct_c` | Concatenate factors, unioning levels. |
| `fct_collapse` | Collapse factors into groups. |
| `fct_count` | Count entries in a factor |
| `fct_drop` | Drop unnused levels |
| `fct_expand` | Add additional levels to a factor |
| `fct_explicit_na` | Make missing values explicit |
| `fct_inorder` | Reorders levels in order of first appearance or frequency. |
| `fct_lump` | Lump together least/most common levels into "other". |
| `fct_recode` | Change the levels of a factor |
| `fct_relevel` | Change the order of levels in a factor |
| `fct_reorder` | Reorder the levels of a function according to another variable |
| `fct_rev` | Reverse the levels of a factor |
| `fct_shift` | Shift the order of levels of a factor |
| `fct_shuffle` | Randomly permute the levels of a factor |
| `fct_unify` | Unify the levels in a list of factors |
| `fct_unique` | Unique values of a factor |
| `gss_cat` | A sample of categorical variables from the General Social survey |
| `lvls` | Low-level functions for manipulating levels |
| `lvls_union` | Find all levels in a list of factors |

-----

## fct_anon

水準の数値化


```r
> f <- factor(c("a", "b", "c", "c"))
> f %>% fct_anon()
```

```
[1] 1 2 3 3
Levels: 1 2 3
```

```r
> f %>% fct_anon("X")
```

```
[1] X3 X2 X1 X1
Levels: X1 X2 X3
```

## fct_c

水準の結合。重複はユニークにする


```r
> fs <- list(factor("a"), factor("b"), factor(c("a", "b")))
> fct_c(fs)
```

```
[1] a b a b
Levels: a b
```

## fct_count

水準の数を数えてデータフレームで返す


```r
> f <- factor(sample(letters)[rpois(1000, 10)])
> table(f)
```

```
f
  a   c   e   f   g   h   k   l   m   n   o   p   q   s   t   u   v   w 
 22   1 100   1  53 141   5  52   4  42  91  31  16  92  69   1   7   1 
  x   y   z 
 18 121 132 
```

```r
> fct_count(f) %>% dplyr::arrange(desc(n)) %>% head()
```

```
# A tibble: 6 × 2
       f     n
  <fctr> <int>
1      h   141
2      z   132
3      y   121
4      e   100
5      s    92
6      o    91
```

## fct_drop


```r
> f <- factor(c("a", "b"), levels = c("a", "b", "c"))
> f
```

```
[1] a b
Levels: a b c
```

```r
> fct_drop(f)
```

```
[1] a b
Levels: a b
```

## fct_expand

水準を追加する


```r
> f <- factor(sample(letters[1:3], 20, replace = TRUE))
> f %>% table()
```

```
.
 a  b  c 
 3 10  7 
```

```r
> fct_expand(f, "d", "e", "f") %>% table()
```

```
.
 a  b  c  d  e  f 
 3 10  7  0  0  0 
```

```r
> # fct_expand(f, letters[1:6]) %>% table()
```

## fct_explicit_na

NAの水準を明確化する

### Arguments

- f
- na_level


```r
> f1 <- factor(c("a", "a", NA, NA, "a", "b", NA, "c", "a", "c", "b"))
> table(f1)
```

```
f1
a b c 
4 2 2 
```

```r
> f2 <- fct_explicit_na(f1)
> table(f2)
```

```
f2
        a         b         c (Missing) 
        4         2         2         3 
```

## fct_infreq / fct_inorder


```r
> f <- factor(c("b", "b", "a", "c", "c", "c"))
> fct_inorder(f) %>% levels() # 出現した順
```

```
[1] "b" "a" "c"
```

```r
> fct_infreq(f) # 頻度の高い順
```

```
[1] b b a c c c
Levels: c b a
```

## fct_lump

特定の水準以外を統一する（頻度の高い２つの水準以外を other として扱う）

### Arguments

- f
- n, prop
- other_level
- ties.method


```r
> x <- factor(rep(LETTERS[1:9], times = c(40, 10, 5, 27, 1, 1, 1, 1, 1)))
> x %>% table()
```

```
.
 A  B  C  D  E  F  G  H  I 
40 10  5 27  1  1  1  1  1 
```

```r
> x %>% fct_lump() %>% table()
```

```
.
    A     D Other 
   40    27    20 
```

## fct_recode

水準名の変更


```r
> x <- factor(c("apple", "bear", "banana", "dear"))
> levels(x)
```

```
[1] "apple"  "banana" "bear"   "dear"  
```

```r
> fct_recode(x, fruit = "apple", fruit = "banana") %>% levels()
```

```
[1] "fruit" "bear"  "dear" 
```

```r
> fct_recode(x, fruit = "apple", fruit = "bananana")
```

```
Warning: Unknown levels in `f`: bananana
```

```
[1] fruit  bear   banana dear  
Levels: fruit banana bear dear
```

```r
> fct_recode(x, NULL = "apple", fruit = "banana")
```

```
[1] <NA>  bear  fruit dear 
Levels: fruit bear dear
```


## fct_relevel

水準のならびを変更する

### Arguments

- f
- ...


```r
> f <- factor(c("a", "b", "c"))
> # 標準のならび
> fct_relevel(f)
```

```
[1] a b c
Levels: a b c
```

```r
> # cを第一水準に
> fct_relevel(f, "c")
```

```
[1] a b c
Levels: c a b
```

```r
> # b, a, (c) のならびに変更
> fct_relevel(f, "b", "a")
```

```
[1] a b c
Levels: b a c
```

## fct_reorder / fct_reorder2


```r
> levels(iris$Species)
```

```
[1] "setosa"     "versicolor" "virginica" 
```

```r
> iris %$% fct_reorder(Species, Sepal.Width) %>% levels()
```

```
[1] "versicolor" "virginica"  "setosa"    
```

```r
> iris %$% fct_reorder2(Species, Sepal.Width, Petal.Width) %>% levels()
```

```
[1] "virginica"  "versicolor" "setosa"    
```

## fct_rev

水準のならびを反転させる


```r
> f <- factor(c("a", "b", "c"))
> fct_rev(f)
```

```
[1] a b c
Levels: c b a
```

## fct_shift


```r
> x <- factor(
+   c("Mon", "Tue", "Wed"),
+   levels = c("Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"),
+   ordered = TRUE
+ )
> x
```

```
[1] Mon Tue Wed
Levels: Sun < Mon < Tue < Wed < Thu < Fri < Sat
```

```r
> fct_shift(x)
```

```
[1] Mon Tue Wed
Levels: Mon < Tue < Wed < Thu < Fri < Sat < Sun
```

```r
> fct_shift(x, 2)
```

```
[1] Mon Tue Wed
Levels: Tue < Wed < Thu < Fri < Sat < Sun < Mon
```

```r
> fct_shift(x, -1)
```

```
[1] Mon Tue Wed
Levels: Sat < Sun < Mon < Tue < Wed < Thu < Fri
```

## fct_shuffle

ランダムに順序を変更する


```r
> fct_shuffle(iris$Species) %>% levels()
```

```
[1] "virginica"  "versicolor" "setosa"    
```

```r
> fct_shuffle(iris$Species) %>% levels()
```

```
[1] "virginica"  "setosa"     "versicolor"
```

```r
> fct_shuffle(iris$Species) %>% levels()
```

```
[1] "setosa"     "versicolor" "virginica" 
```

## fct_unify


```r
> fs <- list(factor("a"), factor("b"), factor(c("a", "b")))
> fct_unify(fs)
```

```
[[1]]
[1] a
Levels: a b

[[2]]
[1] b
Levels: a b

[[3]]
[1] a b
Levels: a b
```

## fct_unique


```r
> f <- factor(letters[rpois(100, 10)])
> unique(f)
```

```
 [1] l k j m g h c e n i f r d o s p q
Levels: c d e f g h i j k l m n o p q r s
```

```r
> fct_unique(f)
```

```
 [1] c d e f g h i j k l m n o p q r s
Levels: c d e f g h i j k l m n o p q r s
```

## lvls_union


```r
> fs <- list(factor("a"), factor("b"), factor(c("a", "b")))
> lvls_union(fs)
```

```
[1] "a" "b"
```

