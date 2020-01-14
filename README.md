# colorsys-go

[![Build Status](https://travis-ci.com/cckuailong/colorsys-go.svg?branch=master)](https://travis-ci.com/cckuailong/colorsys-go)

## What is colorsys-go

colorsys-go is a go package(or lib) for everyone to 
transform one color system to another. The transformation 
is among RGB, YIQ, HLS and HSV.

The repertory [MosaicImage](https://github.com/cckuailong/MosaicImage) 
has use the package correctly.

## Install

```
go get github.com/cckuailong/colorsys-go
```
## Import

```
import "github.com/cckuailong/colorsys-go"
```

## How to use it

### Parameter Range
All inputs and outputs are three floats in the range [0.0...1.0] 
(with the exception of I and Q, which covers a slightly larger range
also with the exception of R, G and B, which range from 0 to 255
also with the exception of H, which range from 0 to 360).

```
range of each parameter
R, G, B :    0 ~ 255
I, Q :      -1 ~ 1.X
H :          0 ~ 360
Y, S, V, L : 0 ~ 1
```

### Examples

1. RGB to YIQ
```
y, i, q := colorsys.Rgb2Yiq(r, g, b)
```
2. YIQ to RGB
```
r, g, b := colorsys.Yiq2Rgb(y, i, q)
```
3. RGB to HLS
```
h, l, s := colorsys.Rgb2Hls(r, g, b)
```
4. HLS to RGB
```
r, g, b := colorsys.Hls2Rgb(h, l, s)
```
5. RGB to HSV
```
h, s, v := colorsys.Rgb2Hsv(r, g, b)
```
6. HSV to RGB
```
r, g, b := colorsys.Hsv2Rgb(h, s, v)
```
7. Yiq to Hls
```
h, l, s := colorsys.Yiq2Hls(y, i, q)
```
8. YIQ to HSV
```
h, s, v := colorsys.Yiq2Hsv(y, i, q)
```
9. HLS to YIQ
```
y, i, q := colorsys.Hls2Yiq(h, l, s)
```
10. HLS to HSV
```
h, s, v := colorsys.Hls2Hsv(h, l, s)
```
11. HSV to YIQ
```
y, i, q := colorsys.Hsv2Yiq(h, s, v)
```
12. HSV to HLS
```
h, l, s := colorsys.Hsv2Hls(h, s, v)
```

## Contact

Any questions, welcome to email me at 346813862Hjj@gmail.com

My Blog is lovebear.top