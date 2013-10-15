words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))

```r
findScrabble <- function(letters) {
    
    for (k in 1:length(letters)) {
        words <- words[grep(letters[k], words)]
        if (length(words) < 10) 
            break  # When the vector of words contains less than 10 vectors, break out of loop
    }
    return(length(words))
}
findScrabble(c("n", "r", "b"))
```

```
## Error: object 'words' not found
```



```r
currentFib <- function(n) {
    current <- 1
    beforeIt <- 0
    for (k in 1:n) {
        tmp <- current + beforeIt
        beforeIt <- current
        current <- tmp
    }
    return(current)
}
fib(1)
```

```
## Error: could not find function "fib"
```

```r
fib(2)
```

```
## Error: could not find function "fib"
```

```r
fib(4)
```

```
## Error: could not find function "fib"
```

```r
fib(6)
```

```
## Error: could not find function "fib"
```

```r
fib(7)
```

```
## Error: could not find function "fib"
```


```r
listOfFib <- function(n) {
    if (n < 0 | floor(n) != n) {
        warning("Wrong input")
        return(NA)
    }
    sofar <- c(0, 1)
    for (k in 3:n) {
        sofar[k] <- sofar[k - 1] + sofar[k - 2]
    }
    return(sofar)
}
listOfFib(10)
```

```
##  [1]  0  1  1  2  3  5  8 13 21 34
```

```r
listOfFib(-4)
```

```
## Warning: Wrong input
```

```
## [1] NA
```

