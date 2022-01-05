# Chaithra-N-P-IP-Lab
# Develop the program to perform linear transformation on a image

import cv2

image = cv2.imread('rk.jpg')

height, width = image.shape[:2]

center = (width/2, height/2)

rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=45, scale=1)

rotated_image = cv2.warpAffine(src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow('Original image', image)
cv2.imshow('Rotated image', rotated_image)
cv2.waitKey(0)
cv2.imwrite('rk.jpg', rotated_image)

# OUTPUT:
![image](https://user-images.githubusercontent.com/95745568/148203720-fbd0fa2d-de7a-4bd2-a7d6-9688d20897a5.png)

![image](https://user-images.githubusercontent.com/95745568/148203773-82f8b8ac-6d14-4f2a-8843-365e760fe846.png)
