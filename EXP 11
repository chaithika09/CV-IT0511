import cv2
import numpy as np
from google.colab.patches import cv2_imshow
from google.colab import files

uploaded = files.upload()

img = cv2.imread(next(iter(uploaded)))

rows, cols = img.shape[:2]

M = np.float32([
    [1, 0, 100],
    [0, 1, 50]
])

affine_img = cv2.warpAffine(img, M, (cols, rows))

print("Original Image:")
cv2_imshow(img)

print("Affine Transformed Image:")
cv2_imshow(affine_img)

cv2.imwrite("Affine_Transformed.jpg", affine_img)
