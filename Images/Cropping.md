
# Left Paw

```r
install_url("http://dtkaplan.github.io/ScientificComputing/Resources/COMP121_0.1.tar.gz")
```

```
## Error: could not find function "install_url"
```

```r
require(devtools)
```

```
## Loading required package: devtools
```

```r
require(COMP121)
```

```
## Loading required package: COMP121 Loading required package: jpeg Loading
## required package: png Loading required package: RCurl Loading required
## package: bitops Loading required package: markdown
```

```r


canvas(x = c(1, 220), y = c(1, 220), asp = 1)
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 

```r
part <- puppy[160:200, 1:70, ]
```

```
## Error: object 'puppy' not found
```

```r
rasterImage(part, 1, 1, 216, 198)
```

```
## Error: object 'part' not found
```

