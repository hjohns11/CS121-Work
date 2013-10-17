words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))

```r

NumOfOneLet <- function(x) {
    oneLet <- length(grep("^.$", x))
    return(oneLet)
}
NumOfOneLet(words)
```

```
## Error: object 'words' not found
```

```r

NumOfTwoLet <- function(x) {
    twoLet <- length(grep("^..$", x))
    return(twoLet)
}
NumOfTwoLet(words)
```

```
## Error: object 'words' not found
```

```r

NumOfThreeLet <- function(x) {
    ThreeLet <- length(grep("^...$", x))
    return(ThreeLet)
}
NumOfThreeLet(words)
```

```
## Error: object 'words' not found
```



```r
v <- c("a", "bros", "hey", "ba", "r", "o", "o")
longestWords <- function(x) {
    results <- c()
    b <- which.max(nchar(x))
    results <- c(results, x[b])
    x <- x[-b]
    
    c <- which.max(nchar(x))
    results <- c(results, x[c])
    x <- x[-c]
    
    
    d <- which.max(nchar(x))
    results <- c(results, x[d])
    x <- x[-d]
    
    
    e <- which.max(nchar(x))
    results <- c(results, x[e])
    x <- x[-e]
    return(results)
}
```





```r
startWithA <- function(x) {
    a <- grep("^a.*", x)
    return(length(a))
}
startWithA(c("apple", "ass", "nad", "bad"))
```

```
## [1] 2
```

```r

startWithB <- function(x) {
    b <- grep("^b.*", x)
    return(length(b))
}
startWithB(c("apple", "ass", "nad", "bad"))
```

```
## [1] 1
```

```r

startWithC <- function(x) {
    c <- grep("^c.*", x)
    return(length(c))
}
startWithC(c("apple", "ass", "nad", "bad"))
```

```
## [1] 0
```



```r
v <- c("uoqu", "uquo", "aqao", "uoqoaq", "abcd", "abqgohn", "aqua", "aqaa", 
    "aaaoaoaoaoaoaoaoquofofofofofof", "ahahahahaqhahahaha")
qButNoU <- function(x) {
    a = grep("q[^u]", x)
    return(v[c(a)])
}
qButNoU(v)
```

```
## [1] "aqao"               "uoqoaq"             "abqgohn"           
## [4] "aqaa"               "ahahahahaqhahahaha"
```



```r
v <- (c("a", "bb", "cccc", "dddd", "eeeee"))
crossword <- function(x) {
    ans <- grep(x, v)
    return(v[ans])
}
crossword("cc")
```

```
## [1] "cccc"
```



```r
words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))

crosswordPattern <- function(word, length) {
    subLength <- rep(".", length)
    subLength[word] <- names(word)
    grepSub <- paste("^", paste(subLength, collapse = ""), "$", sep = "")
    ans <- grep(grepSub, words)
    return(words[ans])
}
crosswordPattern(c(a = 1, b = 2), 7)
```

```
##  [1] "abalone" "abandon" "abasers" "abashed" "abashes" "abasing" "abaters"
##  [8] "abating" "abators" "abattis" "abaxial" "abaxile" "abbotcy" "abdomen"
## [15] "abduced" "abduces" "abducts" "abettal" "abetted" "abetter" "abettor"
## [22] "abeyant" "abfarad" "abhenry" "abiders" "abiding" "abigail" "ability"
## [29] "abioses" "abiosis" "abiotic" "abjured" "abjurer" "abjures" "ablated"
## [36] "ablates" "ablauts" "ablings" "abluent" "abluted" "aboding" "abolish"
## [43] "abollae" "abomasa" "abomasi" "aborted" "aborter" "abought" "aboulia"
## [50] "aboulic" "abounds" "abraded" "abrader" "abrades" "abreact" "abreast"
## [57] "abridge" "abroach" "abscess" "abscise" "abscond" "absence" "absents"
## [64] "absinth" "absolve" "absorbs" "abstain" "absurds" "abubble" "abulias"
## [71] "abusers" "abusing" "abusive" "abuttal" "abutted" "abutter" "abvolts"
## [78] "abwatts" "abysmal" "abyssal" "abysses"
```




```r
scrabble <- function(x) {
    newString = strsplit(x, split = "")[[1]]
    search = newString[1]
    otherWords = words[grep(search, words)]
    search2 = newString[2]
    otherWords = otherWords[grep(search2, otherWords)]
    search3 = newString[3]
    otherWords = otherWords[grep(search3, otherWords)]
    search4 = newString[4]
    otherWords = otherWords[grep(search4, otherWords)]
    search5 = newString[5]
    otherWords = otherWords[grep(search5, otherWords)]
    
    results = c()
    topWord = otherWords[which.max(nchar(otherWords))]
    results = c(results, topWord)
    otherWords = otherWords[-topWord]
    
    sceondWord = otherWords[which.max(nchar(otherWords))]
    results = c(results, secondWord)
    otherWords = otherWords[-secondWord]
}
scrabble("abczz")
```

```
## Error: invalid argument to unary operator
```



```r
scrabble <- function(word) {
    splitword <- strsplit(word, split = "")[[1]]
    search <- c()
    for (k in 1:length(splitword)) {
        search <- splitword[k]
        words <- words[grep(search, words)]
    }
    results <- c()
    topword <- c()
    for (topword in words) {
        ind <- which.max(nchar(words))
        topword <- words[ind]
        words <- words[-ind]
        results <- c(results, topword)
        if (length(results) >= 10) 
            break
    }
    return(results)
}
scrabble("apple")
```

```
##  [1] "electrocardiographs" "chemotherapeutical"  "electrocardiograph" 
##  [4] "hypernationalistic"  "indispensabilities"  "perpendicularities" 
##  [7] "postfertilizations"  "rehospitalizations"  "superintellectuals" 
## [10] "countercomplaints"
```

