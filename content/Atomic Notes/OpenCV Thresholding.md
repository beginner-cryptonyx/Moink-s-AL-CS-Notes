---
related:
  - "[[03. Efforts/Ongoing/Programming]]"
---

source : https://docs.opencv.org/4.x/d7/d4d/tutorial_py_thresholding.html

# Thresholding
1. For each pixel, a same **threshold value** is applied.
2. If pixel value is smaller than or equal to the threshold, it is **set to 0**, else set to a **maximum value**
3. uses function `cv.threshold`

# Thresholding Types
## Basic:

### Syntax:
`cv.threshold(source image, threshhold value, maximum value, thresholding types)`

arguments:
1. **Source Image**: Should be a *Greyscale Image*
2. **Threshold Value**: used to classify the image
3. **Maximum Value**: which is assigned to pixels which exceed the threshold
4. ***[[#Basic Thresholding Types|Threshold type]]***

Returns 2 values
1. Threshold used
2. threshold image

### Basic Thresholding Types:
1. [cv.THRESH_BINARY](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa9e58d2860d4afa658ef70a9b1115576a147222a96556ebc1d948b372bcd7ac59)
2. [cv.THRESH_BINARY_INV](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa9e58d2860d4afa658ef70a9b1115576a19120b1a11d8067576cc24f4d2f03754)
3. [cv.THRESH_TRUNC](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa9e58d2860d4afa658ef70a9b1115576ac7e89a5e95490116e7d2082b3096b2b8)
4. [cv.THRESH_TOZERO](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa9e58d2860d4afa658ef70a9b1115576a0e50a338a4b711a8c48f06a6b105dd98)
5. [cv.THRESH_TOZERO_INV](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa9e58d2860d4afa658ef70a9b1115576a47518a30aae90d799035bdcf0bb39a50)
```python
ret,thresh1 = cv.threshold(img,127,255,cv.THRESH_BINARY)
ret,thresh2 = cv.threshold(img,127,255,cv.THRESH_BINARY_INV)
ret,thresh3 = cv.threshold(img,127,255,cv.THRESH_TRUNC)
ret,thresh4 = cv.threshold(img,127,255,cv.THRESH_TOZERO)
ret,thresh5 = cv.threshold(img,127,255,cv.THRESH_TOZERO_INV)
```

![[Pasted image 20241116114342.webp|70%|center]]
## Adaptive:

- used when there could be different lighting conditions
- An **Algorithm determines the threshold** for a pixel **based on a small region around it**
- Giving different thresholds for different regions

### Syntax:
`cv.adaptiveThreshold(Source Image, maxValyue,  adaptive method, threshold type, block size, C)`

1. **Source Image**: Should be a *Greyscale Image*
2. **Max Value**: Threshold value
3. **[[#Adaptive Thresholding Types|Adaptive Method]]**: Adaptive thresholding algorithm to use
4. **[[#Basic Thresholding Types|Thresholding Type]]**: either [THRESH_BINARY](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa9e58d2860d4afa658ef70a9b1115576a147222a96556ebc1d948b372bcd7ac59) or [THRESH_BINARY_INV](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa9e58d2860d4afa658ef70a9b1115576a19120b1a11d8067576cc24f4d2f03754)
5. **Block size**: *Size of a pixel neighborhood* that is *used to calculate a threshold value* for the pixel
6. **C**: Constant subtracted from the mean or weighted mean

### Adaptive Thresholding Types:
1. [cv.ADAPTIVE_THRESH_MEAN_C](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa42a3e6ef26247da787bf34030ed772cad0c5199ae8637a6b195062fea4789fa9): The threshold value is the mean of the neighborhood area minus the constant **C**.
2. [cv.ADAPTIVE_THRESH_GAUSSIAN_C](https://docs.opencv.org/4.x/d7/d1b/group__imgproc__misc.html#ggaa42a3e6ef26247da787bf34030ed772caf262a01e7a3f112bbab4e8d8e28182dd): The threshold value is a gaussian-weighted sum of the neighborhood values minus the constant **C**.

```python
ret,th1 = cv.threshold(img,127,255,cv.THRESH_BINARY)
th2 = cv.adaptiveThreshold(img,255,cv.ADAPTIVE_THRESH_MEAN_C,cv.THRESH_BINARY,11,2)
th3 = cv.adaptiveThreshold(img,255,cv.ADAPTIVE_THRESH_GAUSSIAN_C,cv.THRESH_BINARY,11,2)
```

![[Pasted image 20241116121013.webp|70%|center]]

# Otsu's Binarization
- Global Thresholding used arbitrary value as a threshold
- Otsu determines it automatically (optimal global threshold determined)

### Syntax: [[#Syntax|Same as basic syntax]]
- `cv.threshold(source, Threshold value, maximum value, THRESH_BINARY+cv.THRESH_OTSU`

```python
# global thresholding
ret1,th1 = cv.threshold(img,127,255,cv.THRESH_BINARY)
 
# Otsu's thresholding
ret2,th2 = cv.threshold(img,0,255,cv.THRESH_BINARY+cv.THRESH_OTSU)
 
# Otsu's thresholding after Gaussian filtering
blur = cv.GaussianBlur(img,(5,5),0)
ret3,th3 = cv.threshold(blur,0,255,cv.THRESH_BINARY+cv.THRESH_OTSU)
```

![[Pasted image 20241116124821.webp|70%|center]]
