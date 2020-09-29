## Filtering the false Positives, why?

In our case, a false positive is an image of clearwood detected by the detection algorithm as an image of wood which contains a defect *(live or dead knot, pitch pocket, split or stain)*. The detection algorithm is used to classify woodboard, woodbeam, ... Thus, a false positive could lead to a negative classification error and then to an economic loss for the manufacturer. As contrary, a false negative is an image of a wood defect that has been detected by the algorithm as clearwood. A false negative could lead to a positive classification error and thus to customer risk. Unfortunately, decreasing the rate of false negatives could only be done by improving the core of the detection algorithm. However, decreasing the rate of false positive is easier : you just have to add a filter after the detection which remove the false positives. In this website, I provide a simple binary classifier *(Neural network)* which is able to distinguish clearwood from defects and which can be used as a false positive filter.

<p align="center">
<img src="Images/process.PNG" alt="Wood Process" width="300"/>
</p>

## The Filter

The filter is a convolutional neural network acting like a binary classifier. The architecture of the neural network is almost the same as Yann Lecun one. It is composed by 8 hidden layers, 3x3 kernel for convolution layer and 2x2 kernel for pooling layer. This neural network has approximatively 600k parameters. The both low complexity and low number of parameters of the net facilitate its training on a small dataset.

<p align="center">
<img src="Images/arch.PNG" alt="Neural Network Architecture" width="400"/>
</p>

## The training dataset

The training dataset is composed by 400 images downloaded on google images. Half of these images are clearwood and the other half contains 5 different types of defect : *(1) Live knot, (2) dead knot, (3) stain, (4) pitch pocket, (5) stain*. Those 5 categories of defect have been chosen because firstly they are the most common defects encountered and secondly they are the defects used by the *Eurocode* to visually estimate the mechanical properties of wood.

<p align="center">
<img src="Images/défauts.PNG" alt="Defect categories" width="300"/>
</p>

As the purpose of this project is to create a starting point to automatic wood classification, the dataset contains more than 200 different wood species. This parameter is important because according to the nature of the wood : hardwood of softwood and also the species the aspect of the defects could vary. Therefore, I tried to create the more unbiased dataset I could to provide a binary classifier which performs well on every species of wood. Afterwhile, you can create a dataset with only one specie of wood and then train the neural net on this particular dataset in order to be more accurate on this very specie.

<p align="center">
<img src="Images/images.PNG" alt="Sample of the training dataset" width="500"/>
</p>

## What for and How to use it ? 

# Predict nature of wood images : defect or clearwood 
  
1. Where can I add images for prediction? 

In order to predict the nature of a particular image, you should add this image to a specific folder on your google drive. Why on google drive? Because codes are hosted on google colaboratory and thoses codes will be cloned on your google drive. This will create folders on your google drive where images can be uploaded and then easily processed by the neural network.

*Tutorial : How to configure your google drive :*

  -   Please create a folder named "Project_google_colab" in My Drive/.
<p align="center">
<img src="Images/tuto_drive.PNG" alt="Google Drive tutorial" width="700"/>
</p>

  -   Launch this *Jupyter* notebook on google colab : [Jupyter Notebook](https://github.com/ArthurCalvi/Classifieur-Bois/blob/master/Classification_du_bois_pr%C3%A9paration_des_images.ipynb).
<p align="center">
<img src="Images/tuto_colab.PNG" alt="Colab tutorial" width="700"/>
</p>

Your google drive should be configured by now. Open the folder "Project_google_colab", a new folder named "Classifieur-Bois" should be here. Open it! This folder contains 4 folders. You can directly upload your images in the folder "IMAGES_brutes". 

<p align="center">
<img src="Images/tuto_add_images.PNG" alt="add images tutorial" width="700"/>
</p>

2. How to preprocess images for the neural net? 

3. How can I predict the nature of thoses images? 

## HELP
Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ArthurCalvi/Classifieur-Bois/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
