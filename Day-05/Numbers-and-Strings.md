
```r
outliers <- function(x) {
    a <- quantile(x)[2]
    b <- quantile(x)[4]
    as.logical(x < a | x > b)
    
}
outliers(1:10)
```

```
##  [1]  TRUE  TRUE  TRUE FALSE FALSE FALSE FALSE  TRUE  TRUE  TRUE
```



```r
EnglishNumbers <- c("zero", "one", "two", "three", "four")
numToText <- function(num, lang) {
    return(lang[num + 1])
}
numToText(2, EnglishNumbers)
```

```
## [1] "two"
```




```r
digitToWord <- function(integer, language) {
    if (v == 0) {
        return("dog")
    }
}
```

digitToWord(0)





```r
lettersMatch <- function(words, pattern) {
    a = grepl("^.pattern", words)
    return(a)
}
lettersMatch(c("aa", "aaa", "bb"), aa)
```

```
## [1] FALSE FALSE FALSE
```



