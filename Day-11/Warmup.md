# Warm Up: Running sum, running product
============

```r
mySum <- function(v) {
    soFar <- 0
    k <- 1
    repeat {
        soFar <- soFar + v[k]
        k <- k + 1
        if (k == length(v) + 1) 
            break
    }
    return(soFar)
}
mySum(c(2, 3, 4))
```

```
## [1] 9
```


Sums using while


```r
mySumWhile <- function(v) {
    soFar <- 0
    k <- 1
    while (k < length(v) + 1) {
        soFar <- soFar + v[k]
        k <- k + 1
    }
    return(soFar)
}
```


Sums using for


```r
mySumFor <- function(v) {
    soFar <- 0
    for (k in 1:length(v)) {
        soFar <- soFar + v[k]
    }
    return(soFar)
}
mySumFor(c(5))
```

```
## [1] 5
```


Running Sums


```r
myRunningSum <- function(v) {
    soFar <- 0
    ans <- c()
    for (k in 1:length(v)) {
        soFar <- soFar + v[k]
        ans <- c(ans, soFar)
    }
    return(ans)
}
myRunningSum(1:5)
```

```
## [1]  1  3  6 10 15
```



```r
RunningSumBack <- function(v) {
    soFar <- 0
    ans <- c()
    for (k in v) {
        soFar <- soFar + k
        ans <- c(soFar, ans)
    }
    return(ans)
}
```



```r
myUnique <- function(v) {
    already <- c()
    for (k in v) {
        if (k %in% already) {
            already <- c(already, "***")
        } else {
            already <- c(already, k)
        }
    }
    return(already)
}
```
