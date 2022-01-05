# swathi19


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


![image](https://user-images.githubusercontent.com/97158063/148204262-ced16a73-e622-4d3d-938b-8906a6639b1c.png)











