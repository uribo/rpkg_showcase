

# sentimentr: Calculate Text Polarity Sentiment

[![](http://www.r-pkg.org/badges/version/sentimentr)](http://cran.rstudio.com/web/packages/sentimentr/index.html)

- CRAN: http://cran.r-project.org/web/packages/sentimentr/index.html
- GitHub: http://github.com/trinker/sentimentr


```r
> library(sentimentr)
> data("cannon_reviews")
```

バージョン: 0.2.2

-----



| 関数名 | 概略 |
|--------|------|
| `as_key` | Create/Manipulate Hash Keys |
| `cannon_reviews` | Cannon G3 Camera Product Reviews From Amazon |
| `emoticons` | Emoticons Data Set |
| `get_sentences` | Get Sentences |
| `grades` | Grades Data Set |
| `highlight` | Polarity Text Highlighting |
| `kotzias_reviews` | Kotzias Reviews |
| `plot.sentiment` | Plots a sentiment object |
| `plot.sentiment_by` | Plots a sentiment_by object |
| `polarity_table` | Polarity Lookup Key |
| `presidential_debates_2012` | 2012 U.S. Presidential Debates |
| `ratings` | Ratings Data Set |
| `replace_emoticon` | Replace Emoticons With Words |
| `replace_grade` | Replace Grades With Words |
| `replace_rating` | Replace Ratings With Words |
| `sam_i_am` | Sam I Am Text |
| `sentiment` | Polarity Score (Sentiment Analysis) |
| `sentiment_by` | Polarity Score (Sentiment Analysis) By Groups |
| `sentimentr` | Calculate Text Polarity Sentiment |
| `sentiword` | Polarity Lookup Key 2 |
| `uncombine` | Ungroup a 'sentiment_by' Object to the Sentence Level |
| `valence_shifters_table` | Valence Shifters |

-----

## cannon_reviews

Cannon G3に関するAmazonでの評価


```r
> cannon_reviews %>% str()
```

```
'data.frame':	597 obs. of  3 variables:
 $ number       : chr  "1" "1" "1" "1" ...
 $ opinion.score: num  3 2 0 0 2 ...
 $ review       : chr  "canon powershot g3 i recently purchased the canon powershot g3 and am extremely satisfied with the purchase." "use the camera is very easy to use, in fact on a recent trip this past week i was asked to take a picture of a vacationing elde"| __truncated__ "after i took their picture with their camera, they offered to take a picture of us." "i just told them, press halfway, wait for the box to turn green and press the rest of the way." ...
```


## sentiment

感情スコアリング


```r
> sentiment(c(
+     'do you like it?  But I hate really bad dogs',
+     'I am the best friend.',
+     'Do you really like it?  I\'m not a fan'
+ ))
```

```
   element_id sentence_id word_count  sentiment
1:          1           1          4  0.5000000
2:          1           2          6 -2.6781088
3:          2           1          5  0.4472136
4:          3           1          5  0.8049845
5:          3           2          4  0.0000000
```

## sentiment_by


```r
> mytext <- c(
+     'do you like it?  But I hate really bad dogs',
+     'I am the best friend.',
+     'Do you really like it?  I\'m not a fan'
+ )
> sentiment_by(mytext)
```

```
   element_id word_count       sd ave_sentiment
1:          1         10 2.247262    -1.0890544
2:          2          5       NA     0.4472136
3:          3          9 0.569210     0.4024922
```

```r
> # subset(cannon_reviews, number %in% sample(unique(number), 3)) %>% with(sentiment_by(review, number)) %>% highlight()
```


