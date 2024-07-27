# Project Overview
Satellite Image Classification using Deep Learning.
This project focuses on land use and land cover classification using the EuroSAT dataset, leveraging deep learning techniques and convolutional neural networks (CNNs). The model achieved an accuracy of 85.23%, utilizing a stage-wise implementation of the popular ResNet50 architecture.

## Dataset
The EuroSAT dataset consists of 27,000 RGB images captured by the Sentinel-2 satellite. These images are labeled into 10 different land use and land cover classes:

![download](https://github.com/user-attachments/assets/155747c3-bf4c-4845-9eb8-5e9551e2d8cf)
![image](https://github.com/user-attachments/assets/19e2c511-5463-4c85-84ec-57d434bbe637)


1. Residential
2. Industrial
3. Annual Crop
4. Permanent Crop
5. River
6. Sea and Lake
7. Herbaceous Vegetation
8. Highways
9. Pasture
10. Forest

    
Each image in the dataset has a spatial resolution of 10 meters per pixel on a 64px*64px image, providing detailed and accurate data for land classification tasks. This dataset is widely used for remote sensing and earth observation research, making it an excellent choice for applying deep learning techniques in land use and land cover classification.


## Model Architecture
The model employs the ResNet50 architecture, known for its robustness in image classification tasks. The stage-wise implementation of ResNet50 used in this project is as follows:


CONV2D -> BATCHNORM -> RELU -> MAXPOOL -> CONVBLOCK -> IDBLOCK*2 -> CONVBLOCK -> IDBLOCK*3 -> CONVBLOCK -> IDBLOCK*5 -> CONVBLOCK -> IDBLOCK*2 -> AVGPOOL -> FLATTEN -> DENSE

## Training Parameters

 -> **Epochs:** 20
 
 -> **Batch Size:** 32
 
 -> **Classes:** 10


## Technologies Used
#### TensorFlow and Keras: For building and training the deep learning model.
#### Rasterio: For handling and visualizing the satellite images.
#### Matplotlib and Seaborn: For plotting and visualizing data and results.
#### scikit-learn: For evaluating the model's performance using metrics such as the confusion matrix.


## References

[1] Eurosat: A novel dataset and deep learning benchmark for land use and land cover classification. Patrick Helber, Benjamin Bischke, Andreas Dengel, Damian Borth. IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing, 2019.

[2] Introducing EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification. Patrick Helber, Benjamin Bischke, Andreas Dengel. 2018 IEEE International Geoscience and Remote Sensing Symposium, 2018.
