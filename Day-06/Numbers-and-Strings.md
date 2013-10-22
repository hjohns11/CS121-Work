
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
    ans <- lang[num + 1]
    return(ans)
}
numToText(2, EnglishNumbers)
```

```
## [1] "two"
```



```r
EnglishNumbers <- c("zero", "one", "two", "three", "four")
TextToNum <- function(word, lang) {
    ans = which(lang == word)
    return(ans - 1)
}
TextToNum("three", EnglishNumbers)
```

```
## [1] 3
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
    a = grep(pattern, words)
    return(a)
}
lettersMatch(c("apple", "berry", "carrie", "rr"), "rr")
```

```
## [1] 2 3 4
```


