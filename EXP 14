import cv2
import numpy as np
from google.colab import files
from google.colab.patches import cv2_imshow

uploaded = files.upload()

img = cv2.imread(next(iter(uploaded)))

rows, cols = img.shape[:2]

src_points = np.float32([
    [0, 0],
    [cols - 1, 0],
    [0, rows - 1],
    [cols - 1, rows - 1]
])

dst_points = np.float32([
    [0, 0],
    [cols - 1, 0],
    [0, int(0.7 * rows)],
    [cols - 1, int(0.7 * rows)]
])

M, _ = cv2.findHomography(src_points, dst_points)

homography_img = cv2.warpPerspective(
    img, M, (cols, rows)
)

cv2_imshow(img)

cv2_imshow(homography_img)

cv2.imwrite(
    "transformation_using_Homography_Image.jpg",
    homography_img
)
