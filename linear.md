```python
import cv2

```


```python
image = cv2.imread('1.jpg')

```


```python
height, width = image.shape[:2]

```


```python
center = (width/2, height/2)

```


```python
rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=45, scale=1)

```


```python
rotated_image = cv2.warpAffine(src=image, M=rotate_matrix, dsize=(width, height))

```


```python
cv2.imshow('Original image', image)
cv2.imshow('Rotated image', rotated_image)

```


```python
cv2.waitKey(0)

```


```python
cv2.imwrite('rotated_image.jpg', rotated_image)

```
