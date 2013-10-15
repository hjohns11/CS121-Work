
```r
firstInt <- function(x) {
    as.character(x)
    a = as.numeric(substr(x, 0, 1))
    
    return(a)
}
firstInt(109294)
```

```
## [1] 1
```
