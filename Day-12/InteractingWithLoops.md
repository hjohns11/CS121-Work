# 1 Section Left


```r
BlastOffPaste <- function(x) {
    ans <- paste("5,", "4,", "3,", "2,", "1,", "Blastoff!", collapse = "/n")
    return(cat(ans))
}
BlastOffPaste(5)
```

```
## 5, 4, 3, 2, 1, Blastoff!
```




```r
blastOffFor <- function(x) {
    count <- 0
    ans <- c()
    for (k in x:1) {
        count <- k
        ans <- paste(ans, count)
    }
    newans <- paste(ans, "BlastOff!", collapse = "")
    return(newans)
}

blastOffFor(5)
```

```
## [1] " 5 4 3 2 1 BlastOff!"
```



```r
blastWhile <- function(x) {
    ans <- c()
    while (x <= 1) {
        ans <- c(ans, x)
        x <- x + 1
    }
    return(ans)
}
blastWhile(5)
```

```
## NULL
```



```r
blastOffRep <- function(x) {
    time <- 5
    repeat {
        x <- cat(time, " ")
        time <- time - 1
        if (time < 1) 
            break
    }
    
    return(cat(paste(x, "Blastoff!", sep = "")))
}
blastOffRep(5)
```

```
## 5  4  3  2  1  Blastoff!
```



```r
testLatency <- function(N) {
    result <- rep(NA, N)
    readline("Ready?")
    
    for (k in 1:20) {
        
        start <- Sys.time()
        readline("Press return:")
        end <- Sys.time()
        total <- as.numeric(end - start)
        cat(rep("\n", 1))
        result[k] <- total
        Sys.sleep(runif(1, 1, 5))
    }
    return(result)
}
```



```r
Elaboration <- function(n) {
    result <- rep(NA, N)
    readline("ready")
    
    for (k in 1:n) {
        cat(rep("\n", 20))
        Sys.Sleep(pauses[k])
        start <- Sys.time()
        scramble <- strsplit("random", split = character(0))
        inpuut <- scramble[[1]][sample(nchar("random"):1)]
        inpuut <- paste(inpuut, collapse = "")
        val <- readline(paste("Type in:", inpuut, " "))
        while (inpuut != val) {
            val <- readline(paste("Try again: "))
        }
        end <- Sys.time()
        total <- as.numeric(end - start)
        cat(rep("\n", 1))
        result[k] <- total
        Sys.sleep(runif(1, 1, 5))
    }
    return(result)
}
```
