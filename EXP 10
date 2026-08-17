import cv2
import numpy as np
from google.colab.patches import cv2_imshow
img = cv2.imread("/content/yu-chin-tsai-piTEABtlR1Q-unsplash.jpg")
rows, cols = img.shape[:2]
M = np.float32([[1, 0, 100],
                [0, 1, 50]])
translated = cv2.warpAffine(img, M, (cols, rows))
print("Original Image")
cv2_imshow(img)
print("Translated Image")
cv2_imshow(translated)
