# Wood Classifier

-Introduction :

This repository contains a binary classifier which distinguish images of wood with and without defects. The classifier is a neuronal network trained on a 400 images database of nearly 200 different species of wood. Even though the database is small, it contains enought variety of wood to be a good starting point for binary classification. The neuronal network could be afterwhile trained on a particular database containing only one specy of wood and thus improving the reliability of the classification for this specy.  The database contains images of clearwood and 5 different defect : Dead and live knot, pitch pocket, split and stain. This classifier has been created to improve wood defects detection algorithm by filtering out false positives. A false positive is an image of clearwood that has been detected as a defect by the detection algorithm. False positives lead to classification errors in wood industry which often trigger client risk or economical losses for the producer, thus false positives should be filtered out. 

