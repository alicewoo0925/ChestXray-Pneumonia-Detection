# Pneumonia Detection using Chest X-ray Image

## Introduction
Pneumonia is an acute respiratory inflammation of one or both lungs due to several causes, such as bacteria and viruses, resulting in the difficulty of breath and subsequent complications. we designed three different multi-classclassifiers using chest X-ray images. The  X-ray images were classified into **normal**, **bacterial pneumonia** and **viral pneumonia**. We focused on representative supervised non-CNN models, **Gaussian Naïve Bayes**, **Random Forest** and **support vector machine (SVM)**. The image features were extracted by using **the first-order statistic and gray-level co-occurrence matrix (GLCM)** and pretrained convolutional neural network (CNN), especially **ResNet50**. All models were trained and tested based on the extracted feature sets.

## Data
The dataset used in this project was gathered from the study described in:
Kermany, Daniel S et al. “[Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep Learning](https://doi.org/10.1016/j.cell.2018.02.010).” Cell (Cambridge) 172.5 (2018): 1122–1131.e9.

The dataset citation is as follows:
Kermany, Daniel; Zhang, Kang; Goldbaum, Michael (2018), “Large Dataset of Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images”, Mendeley Data, V3, doi: 10.17632/rscbjbr9sj.3 
http://dx.doi.org/10.17632/rscbjbr9sj.3

In this project, a collection of 1,951 chest X-ray images acquired from children was used. The breakdown of this dataset is as follows:

| Dataset | Class     | Count |
|---------|-----------|------:|
| Train   | Viral     |   342 |
|         | Bacterial |   649 |
|         | Normal    |   336 |
|         | Total     | 1,327 |
| Test    | Viral     |   148 |
|         | Bacterial |   242 |
|         | Normal    |   234 |
|         | Total     |   624 |

## Result
![image](https://github.com/alicewoo0925/pneumonia/assets/48823257/2a28af18-5297-4c44-b416-e8a7bbec38a0)
As a result, we accomplished satisfactory prediction performances with our models. Image features extracted using the pre-trained ResNet50 model demonstrated superior predictive performance across all models. By utilising relatively small dataset and traditional machine learning models, we were able to achieve exceptional processing speeds. On average, the entire processes including training and prediction were completed within 1 minute.

However, none of models reaches the accuracy of 90%, which may lead to the limitation of applying to the medical field. In future work, Stratified K-fold cross validation can be used to improve the performance by balancing dataset although it will create a new test set with different combinations. Segmentation mask also can be applied to the images in order to extract the features only from lungs, while reducing interference with bones, other tissues and artifacts. As CNN has been reported high performance with high accuracy, sensitivity and specificity, ResNet50 or VGG16 can be tried for the classification.


## Meet our Team
The success of this project is attributed to the remarkable commitment and steadfast efforts of our team members:

- **[Alice Yoonjung Woo](https://www.linkedin.com/in/alice-yoonjung-woo/)**
- **Yaming Xu**
- **Kexin Liu**

Special thanks to anyone who provided feedback, reported issues, or helped in any way to make this project better.
