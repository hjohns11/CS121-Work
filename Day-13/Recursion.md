
```r
addEm <- function(v) {
    sum <- 0  #accumulator
    for (k in 1:length(v)) {
        sum <- sum + v[k]
    }
    return(sum)
}
addEm(1:5)
```

```
## [1] 15
```



```r
newAddEm <- function(v) {
    if (length(v) == 0) 
        return(0)
    return(v[1] + newAddEm(v[-1]))
}
```


## ??

```r
fibLoop <- function(n) {
    
}
```



```r
fibRecurse <- function(n) {
    # handle the cases that are really simple
    if (n == 1) {
        return(1)
    } else {
        if (n == 0) 
            return(0)
    }
    thisF <- fibRecurse(n - 1) + fibRecurse(n - 2)
    # Return the answer assembled from the simple bits
    return(thisF)
}
fibRecurse(4)
```

```
## [1] 3
```


#??

```r
addNSeq <- function(n) {
    sum <- c()
    while (n > 0) {
        return(n)
    }
    sum <- c(sum, n)
    return(addNSeq(n - 1) + addNSeq(n - 2))
    
}
```



```r
addNLoop <- function(n) {
    sum <- c()
    for (k in n:0) {
        sum <- c(sum, k)
        k <- k - 1
    }
    
    return(sum(sum))
}
```


# ??

```r
addRecur <- function(x) {
    
}
```


#??

```r
addRecurLoop <- function(x) {
    sum <- c()
    l <- length(x)
    while (x > x[l]) {
        sum <- c(sum, x)
        x <- x - 1
    }
    return(sum)
}
addRecurLoop(c(5))
```

```
## NULL
```


# NOT FINISHED
