# In Class: Oct 22

## Derivatives
### Returns function of derivative, have to plug in number after to find output of deriv.

```r
myD <- function(f, h = 1e-06) {
    fPrime <- function(x) {
        ((f(x + h) - f(x))/h)
    }
    return(fPrime)
}

# prime <- myD(sin) prime(3)

myD2 <- function(f, h = 1e-07) {
    fPrime <- function(x) {
        ((f(x + h) - f(x))/h)
    }  # OR myd(f,h=h)
    dPrime <- function(x) {
        ((fPrime(x + h) - fPrime(x))/h)
    }  # OR myD(fPrime, h=h)
    return(dPrime)
}
```


#3 Returns number(x) when inputted into the derivative

```r
otherD <- function(f, x) {
    h <- 1e-07
    res <- (f(x + h) - f(x))/h
    return(res)
}
```



