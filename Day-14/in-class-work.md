## Day 14

# Reverse a vector recursively


```r
revRec <- function(v) {
    browser()
    if (length(v) == 1) 
        return(v) else {
        c(revRec(v[-1]), v[1])
    }
    
}
revRec(c(5, 4, 3, 2, 1))
```

```
## Called from: revRec(c(5, 4, 3, 2, 1))
## Called from: revRec(v[-1])
## Called from: revRec(v[-1])
## Called from: revRec(v[-1])
## Called from: revRec(v[-1])
```

```
## [1] 1 2 3 4 5
```



