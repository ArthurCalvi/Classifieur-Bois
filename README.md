# Wood Classifier - Version 0.1a of the 10/09/2020

## Intro :
This repository contains the work of my 3 months Internship at *ENSAPM* (Ecole Nationale Supérieure d'Architecture Paris Malaquais), as a data scientist I had to develop a binary classifier to filter out false positives of wood defect in order to improve a wood defect detection algorithm. No dataset existed for this task, so I had also to create my own dataset. Wood defect detection algorithm are used in industry to process woodbeam, woodboard, etc. False positives which are clearwood detected as defects could lead to material losses for the wood producer or negative errors of wood classification.

The purpose of this repository is to easily continue my work, in particular widening the dataset or creating a dataset of just one specie. This tasks can be easily done with the Jupyter Notebooks I provide in this repository. Likewise, a more complex neural network could be trained with a larger database.

## Content :
- Jupyter NoteBook 1 - [Images preprocessing and prediction](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Images_preprocessing_and_prediction.ipynb) : This code helps you to prepare your images for the neural net, it is basicaly rescaling and reshaping. It prepares images of the IMAGES_raw folder and saved them into the /IMAGES_preprocessed folder on your google drive.
- Jupyter NoteBook 2 - [Creation of your dataset](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Creation_of_your_dataset.ipynb) : This code helps you to create a new dataset by automatically classifying images with the wood classifier.
- Jupyter NoteBook 3 - [Filter](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Filter.ipynb) : This code filter out the false positives of the /IMAGES_preprocessed folder and save the images of defect into the /IMAGES_filtered folder.
- GitHub Page - [Wood Classifier Tutorial](https://arthurcalvi.github.io/Classifieur-Bois/) : This page contains one tutorial to clone this github repository to your own google drive and afterwhile easily use the jupyter notebooks.
- Dataset - [Binary Dataset](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Binary_dataset_256.rar) : This is a 500 images dataset containing images of clearwood and 5 different defects which are : live and dead knot, pitch pocket, stain and split. The dimensions of the images are 256x256 px. The dataset contains more than 200 different species of wood.
- Keras Neural net trained model - [Wood classifier KERAS](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/MODEL_CNN1_bs32_ep100_augTrue_t1593511641.h5) : This keras convolutional neural network have been trained on the binary dataset. The architecture, the weights and the hyperparameters have been saved. Its accuracy is about 94%.
- Python functions - [Custom functions](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/custom_functions_v1.py) : This python code contains several functions used during the data generation to perform : random cropping and hue changes.
- MIT License.
- Folder 1 - raw images : Once this folder cloned into your google drive, you will deposit your (non prepared) images in this folder on your google drive.
- Folder 2 - preprocessed images : The images prepared by the Jupyter NoteBook 1 will be saved in this folder on your google drive.
- Folder 3 - new dataset : The images classified by the Jupyter NoteBook 2 will be saved in this folder on your google drive. 
- Folder 4 - filtred images : The images filtred by the Jupyter NoteBook 3 will be saved in this folder on your google drive. 

## GitHub Clone
To easily use the Jupyter NoteBooks : you have to open them in Google Colaboratory. Google Colaboratory is a cloud platform where you can execute python codes, you don't have to install any package and you will benefit from a great computational power. Following the instructions on the GitHub Page, you will clone this repository on your google drive to comfortably execute the Jupyter Notebooks (Don't forget to create the folder "Project_google_colab" at the root of /My Drive before cloning the repository). In your google drive clone will be stored all the codes and models needed to use the wood classifier. In addition, four folders will be availabe on your google drive ( My Drive/Project_google_colab/Classifieur-bois) :
- /IMAGES_raw : you will upload the images you want estimate here.
- /IMAGES_preprocessed : the Jupyter Notebook 1 will store prepared images here.
- /New_Dataset : the Jupyter Notebook 2 will store classified images here. 
- /IMAGES_filtered : the Jupyter Notebook 3 will store filtred images here.

## Contact
- Arthur Calvi at arthur.calvi@ens-paris-saclay.fr
