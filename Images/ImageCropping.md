# NOT FINSISHED





```r
puppy <- readPNG(getURLContent("http://dtkaplan.github.io/ScientificComputing/Resources/Images/mindo.png"))
canvas(x = c(1, 220), y = c(1, 220), asp = 1)
partPaw <- puppy[160:198, 1:70, ]
rasterImage(partPaw, 1, 1, 3 * 70, 3 * 38)
```

<img src="figure/unnamed-chunk-2.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="40%" />



```r
puppy <- readPNG(getURLContent("http://dtkaplan.github.io/ScientificComputing/Resources/Images/mindo.png"))
canvas(x = c(1, 220), y = c(1, 220), asp = 1)
partFace <- puppy[30:120, 90:180, ]
rasterImage(partFace, 1, 1, 2 * 90, 2 * 90)
```

<img src="figure/unnamed-chunk-3.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" width="40%" />



```r
puppy <- readPNG(getURLContent("http://dtkaplan.github.io/ScientificComputing/Resources/Images/mindo.png"))
canvas(x = c(1, 220), y = c(1, 220), asp = 1)
partTag <- puppy[120:140, 100:120, ]
rasterImage(partTag, 1, 1, 4 * 20, 4 * 20)
```

<img src="figure/unnamed-chunk-4.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="40%" />



```r
puppy <- readPNG(getURLContent("http://dtkaplan.github.io/ScientificComputing/Resources/Images/mindo.png"))
red <- puppy[, , 1]
framed <- cbind(red[, (1:30)], red, red[, (187:216)])
canvas(x = c(1, 60 + 216), y = c(1, 198), asp = 1)
rasterImage(framed, 1, 1, 60 + 216, 198)
```

<img src="figure/unnamed-chunk-5.png" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" width="40%" />


```r
ShowImage <- function(image) {
    size <- dim(image)
    canvas(x = c(1, size[2]), y = c(1, size[1]), asp = 1)
    rasterImage(image, 1, 1, size[2], size[1])
}
```

## Can't finish, need image as input

```r
mirrorImage <- function(image, frameWidth) {
    puppy <- readPNG(getURLContent("http://dtkaplan.github.io/ScientificComputing/Resources/Images/mindo.png"))
    red <- puppy[, , 1]
    C <- dim(puppy)
    lengthC <- C[2]
    lengthR <- C[1]
    
    framed <- cbind(red[, rev(1:frameWidth + 1)], red, red[, (lengthC - (1:frameWidth))])
    all <- rbind(framed[rev(1:frameWidth + 1), ], framed, framed[rev(lengthC - 
        frameWidth:lengthC), ])
    ShowImage(puppy)
    
}
# canvas( x=c(1, lengthC+30), y=c(1, lengthR+30), asp=1)
# rasterImage(framed,1 , 1, 5*frameWidth , 5 * frameWi
dim(mirrorImage(puppy, 30))
```

<img src="figure/unnamed-chunk-7.png" title="plot of chunk unnamed-chunk-7" alt="plot of chunk unnamed-chunk-7" width="40%" />

```
## NULL
```




```r
brightness <- function(image, frameWidth, bright) {
    puppy <- readPNG(getURLContent("http://dtkaplan.github.io/ScientificComputing/Resources/Images/mindo.png"))
    red <- puppy[, , 1]
    C <- dim(puppy[, 1, ])
    lengthC <- C[1]
    R <- dim(puppy[1, , ])
    lengthR <- R[1]
    
    framed <- cbind(bright * red[, rev(1:frameWidth + 1)], red, bright * red[, 
        rev(lengthC - frameWidth:lengthC)])
    all <- rbind(bright * framed[rev(1:frameWidth + 1), ], framed, bright * 
        framed[rev(lengthC - frameWidth:lengthC), ])
    
    canvas(x = c(1, lengthC + 30), y = c(1, lengthR + 30), asp = 1)
    rasterImage(framed, 1, 1, 5 * frameWidth, 5 * frameWidth)
}
brightness(puppy, 30, 0.4)
```

<img src="figure/unnamed-chunk-8.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="40%" />


#??

```r
Frame <- function(frameWidth) {
    puppy <- readPNG(getURLContent("http://dtkaplan.github.io/ScientificComputing/Resources/Images/mindo.png"))
    red <- puppy[, , 1]
    framed <- cbind(red[, 1:(frameWidth + 1)], red, red[, ((216 - frameWidth):216)])
    all <- rbind(framed[1:(frameWidth + 1), ], framed, framed[(198 - frameWidth):198], 
        )
    canvas(x = c(1, 60 + 216), y = c(1, 198), asp = 1)
    rasterImage(all, 1, 1, 60 + 216, 198)
}
Frame(20)
```

```
## Error: argument is missing, with no default
```


