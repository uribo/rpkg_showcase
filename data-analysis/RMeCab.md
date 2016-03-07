

# RMeCab: interfacee to MeCab

[![](http://www.r-pkg.org/badges/version/RMeCab)](http://cran.rstudio.com/web/packages/RMeCab/index.html)

* CRAN: http://cran.r-project.org/web/packages/RMeCab/index.html
* GitHub: https://github.com/cpsievert/RMeCab/


```r
> library(RMeCab)
```

バージョン: 0.99991

-----



| 関数名 | 概略 |
|--------|------|
| `Ngram` | Ngram |
| `NgramDF` | NgramDF |
| `NgramDF2` | NgramDF2 |
| `RMeCabC` | RMeCabC |
| `RMeCabDF` | RMeCabDF |
| `RMeCabDoc` | RMeCabDoc |
| `RMeCabFreq` | RMeCabFreq |
| `RMeCabMx` | RMeCabMx |
| `RMeCabText` | RMeCabText |
| `coOccurrence` | co-occurrence Matrix (Matrices) options |
| `collScores` | collScores |
| `collocate` | collocate |
| `docDF` | docDF |
| `docMatrix` | docMatrix |
| `docMatrix2` | docMatrix2 |
| `docMatrixDF` | docMatrixDF |
| `docNgram` | docNgram |
| `docNgram2` | docNgram2 |
| `docNgramDF` | docNgramDF |
| `entropy` | Weighting Matrix (Matrices) options   |
| `print.docMatrix` | print.docMatrix |
| `rmSign` | rmSign |

-----

## collocate

ファイルから共起語の頻度表を作成

### Arguments

* filename
* node
* span
* dic
* mecabrc
* etc


```r
> collocate(filename, node, span , dic = "", mecabrc = "", etc = "")
```

## collScores

共起語のスコアを計算

### Arguments

* kakka
* node
* span


```r
> collScores(kekka, node, span = 0)
```

## docMatrix

ターム・文書行列の作成

## docMatrixDF

データフレームからターム・文書行列を作成

### Arguments

* charVec
* pos
* minFreq
* weight
* co
* dic
* mecabrc
* etc


```r
> docMatrixDF(charVec = c("MeCab","CaBoCha"), pos = "Default", minFreq = 1, weight = "no", co = 0 , dic = "", mecabrc = "", etc = "")
```


## Ngram

### Arguments

* filename
* type
* N
* pos
* dic
* mecabrc
* etc


```r
> Ngram(filename, type = 0, N = 2, pos = "Default",  dic = "", mecabrc = "", etc = "" )
```

## RMeCabC

文字列の形態素解析

### Arguments

* str
* mypref
* dic
* mecabrc
* etc


```r
> RMeCabC(str = "すもももももももものうち")
```

```
[[1]]
    名詞 
"すもも" 

[[2]]
助詞 
"も" 

[[3]]
  名詞 
"もも" 

[[4]]
助詞 
"も" 

[[5]]
  名詞 
"もも" 

[[6]]
助詞 
"の" 

[[7]]
  名詞 
"うち" 
```

## RMeCabDF

データフレームの指定列の解析

### Arguments

* dataf
* coln
* mypref
* dic
* mecabrc
* etc



```r
> RMeCabDF(dataf, coln, mypref, dic = "", mecabrc = "", etc = "")
```


## RMeCabDoc

文章ファイルからの形態素解析

### Arguments

* filename
* mypref
* kigo
* dic
* mecabrc
* etc


```r
> RMeCabDoc(filename, mypref= 1, kigo = 0, dic = "", mecabrc = "", etc = "")
```


## RMeCabFreq


```r
> library(dplyr)
> df_dic <- read_delim("~/Downloads/pn_ja.dic",
+                      delim = ":",
+                      col_names = c("Term", "kana", "Info1", "value"),
+                      col_types = cols(Term  = "c",
+                                       kana  = "c",
+                                       Info1   = "c",
+                                       value = "d"),
+                      locale = locale(encoding = "cp932")) %>% 
+   aggregate(value ~ Term + Info1, ., mean)
> 
> RMeCabFreq(filename = paste0(tmp_path, "/", log_js[i], ".txt"),
+              dic      = "~/git/clone/mecab-ipadic-neologd/build/mecab-ipadic-2.7.0-20070801-neologd-20160104") %>% 
+     dplyr::inner_join(df_dic)
> 
> # tw_2015[[1]] %>% head()
> #       Term Info1 Info2 Freq      value
> # 1   かなり  副詞  一般    1 -0.2666110
> # 2     つい  副詞  一般    1 -0.5456660
> # 3 ともかく  副詞  一般    1 -0.6976480
```



