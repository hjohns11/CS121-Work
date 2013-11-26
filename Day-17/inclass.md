# Generate a plane of colors

```r

planeBind <- function(red, green, blue) {
    array(c(red, green, blue), dim <- c(dim(red)[1], dim(red)[2], 3))
}


npixels <- 50
howMuchBlue <- 0.5

x <- seq(0, 1, length = npixels)

# initialize state
red <- matrix(0, nrow = npixels, ncol = npixels)
for (k in 1:npixels) {
    # update
    red[, k] <- cbind(x)
}

green <- matrix(0, nrow = npixels, ncol = npixels)
for (k in 1:npixels) {
    green[k, ] <- rbind(x)
}

blue <- matrix(howMuchBlue, nrow = npixels, ncol = npixels)

ShowImage <- function(image) {
    size <- dim(image)
    canvas(x = c(1, size[2]), y = c(1, size[1]), asp = 1)
    rasterImage(image, 1, 1, size[2], size[1])
}

# vvvvvvvvvvvvvvvvvvvvvvvvvvvv
showImage <- function(img) {
    z <- dim(img)
    canvas(x = c(1, z[2]), y = c(1, z[1]), asp = 1)
    rasterImage(img, 1, 1, z[2], z[1])
}
# ^^^^^^^^^^^^^^^^^^^^^^^^^^^^


ShowImage(planeBind(red, green, blue))
```

```
## Error: could not find function "canvas"
```
