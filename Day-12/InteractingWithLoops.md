
```r
BlastOffPaste <- function(x) {
    ans <- paste("5,", "4,", "3,", "2,", "1,", "Blastoff!", seq = "")
    return(cat(ans))
}
```


# Very close, can't finish

```r
blastOffFor <- function(x) {
    count <- 0
    ans <- c()
    for (k in x:1) {
        count <- k
        ans <- c(ans, count)
    }
    return(paste(ans, "Blastoff!", collapse = ""))
}
```








