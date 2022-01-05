# Chaithra-N-P-IP-Lab
# Develop the program to perform linear transformation on a image

import cv2

image = cv2.imread('rickky.jpg')

height, width = image.shape[:2]

center = (width/2, height/2)

rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=45, scale=1)

rotated_image = cv2.warpAffine(src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow('Original image', image)
cv2.imshow('Rotated image', rotated_image)
cv2.waitKey(0)
cv2.imwrite('rickky.jpg', rotated_image)

# OUTPUT:
# Original image:
![image](https://user-images.githubusercontent.com/95745568/148197479-7c09a78e-d762-4cdc-ab16-df64de02c0a1.png)
# Rotated image:
![image](https://user-images.githubusercontent.com/95745568/148197817-acdecb4b-b17c-411a-86fa-a7d885544d27.png)
