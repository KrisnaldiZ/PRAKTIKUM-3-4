# PRAKTIKUM 3

### Pada line 1 dan 2 ini untuk mengimpor pustaka OpenCV
1. import cv2

2. import matplotlib.pyplot as plt

### Lalu line 3 dan 4 dibawah ini untuk membaca gambar dengan cv2.imread

3. img = cv2.imread("gambar.png") # Ganti dengan path gambar Anda

4. gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

### Line 5,6,7,8,9,10 dibawah untuk membuat histogram dari gambar grayscale

5. fix, axs = plt.subplots(1, 2, figsize = (10,5))

6. ax = axs.ravel()

7. ax[0].hist(gray.ravel(), bins=256)

8. ax[0].set_title("Histogram")

9. ax[1].imshow(thresh, cmap = 'gray')

10. ax[1].set_title("Gambar Threshold")

# Praktikum 4

### Line 1,2,3,4,5 untuk mengimpor pustaka yang diperlukan: OpenCV (cv2) untuk pemrosesan gambar

1. import cv2

2. import matplotlib.pyplot as plt

3. import numpy as np

4. from skimage import data

5. from skimage.feature import graycomatrix, graycoprops

### Line 6,7,8,9,10,11,12,13 untuk membaca gambar astronaut dari dataset skimage dan mengubahnya menjadi gambar grayscale menggunakan OpenCV.

6. img = skimage.data.astronaut()

7. img_gray = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)

8. fig, axs = plt.subplots(1, 2, figsize = (10, 10))

9. ax = axs.ravel()

10. ax[0].imshow(img)

11. ax[0].set_title("RGB")

12. ax[1].imshow(img_gray, cmap="gray")

13. ax[1].set_title("GRAY")
