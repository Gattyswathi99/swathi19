# swathi19
1) developa program linear transformation on a image

import cv2
image = cv2.imread('1.jpg')
height, width = image.shape[:2]
center = (width/2, height/2)
rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=45, scale=1)
rotated_image = cv2.warpAffine(src=image, M=rotate_matrix, dsize=(width, height))
cv2.imshow('Original image', image)
cv2.imshow('Rotated image', rotated_image)
cv2.waitKey(0)
cv2.imwrite('rotated_image.jpg', rotated_image)
![image](https://user-images.githubusercontent.com/97158063/148200809-dce46198-83a4-400c-a77c-ec319ebe86ee.png)
