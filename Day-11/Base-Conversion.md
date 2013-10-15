
```r
toBase <- function(int, base) {
    sofar <- c()
    
    while (int != 0) {
        r <- (int%%base)
        sofar <- c(sofar, r)
        int <- (int - r)/b
    }
    return(sofar)
}
toBase(43)
```

```
## Error: 'base' is missing
```

