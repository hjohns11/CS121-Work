## Drawing Circles and Squares


```r
plot(1:2, ylab = "y-axis", type = "n", xlim = c(0, 100), ylim = c(0, 100))

polygon(c(25, 35, 35, 25), c(25, 25, 35, 35), angle = 90, col = "red")

polygon(c(15, 35, 35, 15), c(45, 45, 70, 70), angle = 90, col = "green", border = "blue")

polygon(c(65, 80, 85, 72.5, 60), c(50, 50, 70, 80, 70), angle = 75, col = "yellow")

polygon(15, 20, angle = seq(0, 2 * pi, length = 1000), col = "blue")
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 

