
```r
countOdds <- function(x) {
    k <- 0
    for (n in x) {
        if (n%%2 == 1) 
            k <- k + 1
    }
    return(k)
}

countOdds(c(3, 5))
```

```
## [1] 2
```




```r
countEvens <- function(x) {
    k <- 0
    for (n in x) {
        if (n%%2 == 0) 
            k <- k + 1
    }
    return(k)
}

countEvens(c(1, 2, 3, 4, 5))
```

```
## [1] 2
```




```r
hypotenuseLength <- function(x, y) {
    h = sqrt(x^2 + y^2)
    return(h)
}

hypotenuseLength(3, 4)
```

```
## [1] 5
```




```r
lawOfCosines <- function(x, y, z) {
    a = x^2 + y^2
    b = 2 * x * y * cos(z)
    h = sqrt(a - b)
    return(h)
}

lawOfCosines(13, 84, pi/2)
```

```
## [1] 85
```



```r
thetaFromLengths <- function(x, y, z) {
    numerator = z^2 - x^2 - y^2
    denominator = -2 * x * y
    theta = acos(numerator/denominator)
    return(theta)
}
thetaFromLengths(3, 4, 5)
```

```
## [1] 1.571
```




```r
canvas <- function(x) {
    a = plot(x, type = "n", xlim = c(0, x[1]), ylim = c(0, x[2]))
    return(a)
}
canvas(c(7, 5))
```

![plot of chunk unnamed-chunk-6](figure/unnamed-chunk-6.png) 

```
## NULL
```
