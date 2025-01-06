# Noise-Reduction-and-Image-Optimization-for-Captcha-Number-Recognition

## Overview 📊

This project focuses on the preprocessing of captcha images to remove intentional noise and enhance the clarity of the numbers for improved recognition. The dataset is sourced from the [Captcha Dataset on Kaggle](https://www.kaggle.com/datasets/huthayfahodeb/captcha-dataset/data), which contains captcha images with added noise to make automated recognition challenging. The new dataset can be found [here](https://www.kaggle.com/datasets/theiturhs/captcha-image-preprocessing-for-number-recognition/data).

The goal of this preprocessing pipeline is to optimize the images by reducing the complexity, making it easier to train models for captcha number recognition.

## Preprocessing Techniques 🔧

Several image processing techniques have been applied to the captcha dataset to enhance the visibility of the numbers and reduce the noise that interferes with the recognition process. The key preprocessing steps are as follows:

### 1. **Grayscale Conversion** 🌑
   - **Objective**: Convert the captcha images to grayscale to simplify the data and focus only on pixel intensities, which reduces the complexity of color information.
   - **Benefit**: By removing color information, the model can focus purely on the intensity variations within the image, making it easier to extract numbers.

### 2. **Median Filtering** 🧹
   - **Objective**: Apply a median filter to the grayscale image to reduce random noise and preserve the structure of the characters.
   - **Benefit**: Median filtering helps in removing small pixel-based noise while maintaining the edges of the numbers, which is crucial for recognition accuracy.

### 3. **Mean Filtering** 🌀
   - **Objective**: Apply a mean filter (or box filter) to smooth the image by averaging the pixel values in a local neighborhood.
   - **Benefit**: This helps in reducing noise by smoothing out pixel variations, which is particularly useful when the captcha images have added random noise patterns.

### 4. **Threshold Calculation** 🔲
   - **Objective**: Calculate a threshold value based on the pixel intensity distribution of the filtered image.
   - **Method**: A histogram of pixel values is created, and the median of the histogram is used to identify a significant range of pixel values. This helps in distinguishing the foreground (numbers) from the background noise.
   - **Benefit**: This thresholding process ensures that only the important pixel information (the numbers) is retained while eliminating unnecessary noise.


     ![image](https://github.com/user-attachments/assets/d7046256-e4ab-4042-831b-960fb3f7c229)




### 5. **Binary Image Creation** ⬛
   - **Objective**: Convert the filtered grayscale image into a binary image using the calculated threshold.
   - **Benefit**: The binary image makes the recognition process easier by turning the image into a simple black-and-white format, where the numbers are clearly distinguishable from the background.

## Result 📈

By applying the above preprocessing techniques, the captcha images are optimized, making them much easier for machine learning models to train on. The result is a cleaner, less complex dataset that is well-suited for number recognition tasks.

Refer the pictorial flowchart which represents the actual implementation:

![image](https://github.com/user-attachments/assets/98283d83-7248-4978-9e56-4aaf3a08c358)


## Conclusion ✅

The preprocessing pipeline significantly reduces the noise in captcha images and simplifies the data, enabling more accurate and efficient model training for captcha number recognition. This pipeline can be easily adapted and extended to other image processing tasks involving noisy datasets.

### Connect with me
For any inquiries or feedback, feel free to reach out:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shrutikshrivastava/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shrutishrivastava22ss@gmail.com)
[![Carrd](https://img.shields.io/badge/carrd-000000?style=for-the-badge&logo=carrd&logoColor=white)](https://theiturhs.carrd.co/)
[![Kaggle](https://img.shields.io/badge/kaggle-0077B5?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/theiturhs)
[![GitHub](https://img.shields.io/badge/github-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/theiturhs)
