# Wood Classifier - Version 0.1 of the 10/08/2020

## Intro :
This repository contains the work of my 3 months Internship at *ENSAPM* (Ecole Nationale Supérieure d'Architecture Paris Malaquais), as a data scientist I had to developp a binary classifier to filter out false positives of wood defect in order to improve a wood defect detection algorithm. No dataset existed for this task so I had also to create my own dataset. Wood defect detection algorithm are used in industry to process woodbeam, woodboard, etc. False positives which are clearwood detected as defects could lead to material losses for the wood producer or negative errors of wood classification. 

The purpose of this repository is to easily continue my work, in particular widening the dataset or creating a dataset of just one specie. This tasks can be easily done with the Jupyter Notebooks I provide in this repository. Likewise, a more complex neural network could be trained with a larger database. 
 
## Content :
- Jupyter NoteBook 1 - [Neural net Preprocessing images](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Neural_net_Preprocessing_images.ipynb) : This code helps you to prepare your images for the neural net, it is basicaly rescaling and reshaping. It prepares images of the IMAGES_raw folder and saved it into the IMAGES_prepared folder on your google drive. 
- Jupyter NoteBook 2 - [Neural net wood classifier](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Neural_Net_Wood_Classifier.ipynb) : This code loads a convolutional neural network that has been trained to do binary classification on wood, it loads your image and estimates if your image represents clearwood or defect. 
- GitHub Page - [Wood Classifier Tutorial](https://arthurcalvi.github.io/Classifieur-Bois/) : This page contains one tutorial to clone this github repository to your own google drive and afterwhile easily use the jupyter notebooks. 
- Dataset - [Binary Dataset](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Binary_dataset_256.rar) : This is a 500 images dataset containing images of clearwood and 5 different defects which are : live and dead knot, pitch pocket, stain and split. The dimensions of the images are 256x256 px. The dataset contains more than 200 different species.
- Keras Neural net trained model [Wood classifier KERAS](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/MODEL_CNN1_bs32_ep100_augTrue_t1593511641.h5) : This keras convolutional neural network have been trained on the binary dataset. The architecture, the weights and the hyperparameters have been saved. Its Preicision is about 94%. 
- Python functions - [Custom functions](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/custom_functions_v1.py) : This python code contains several functions used during the datageneration to perform : random croppping and hue changes. 
- MIT License. 
- Folder 1 - raw images : Once this folder cloned into your google drive, you will deposit your (non prepared) images in this folder on your google drive.  
- Folder 2 - prepares images : The images prepared by the Jupyter NoteBook 1 will be saved into this folder on your google drive. 

## Contact
- Arthur Calvi at arthur.calvi@ens-paris-saclay.fr
