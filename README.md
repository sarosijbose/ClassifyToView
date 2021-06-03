# ClassifyToView: Model and visualization code for detecting diseases in Leaf species

## Description:-
This repository contains code for classifying various diseases in plant leaves based on the [AlexNet](https://papers.nips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf) Architecture whose pre-trained weights are used. The model is then further Fine-tuned and the best weights saved from each iteration. It is then tested over the test data where it achieves an accuracy of almost 97%. The predictions for each species of leaf are then written to a csv file which is then later used in the visualization tool [FiftyOne](https://voxel51.com/fiftyone/). The code for loading and visualizing the dataset, the positive and the negative labels is also provided. The [FiftyOne App](https://voxel51.com/docs/fiftyone/user_guide/app.html) then allows the user to evaluate the quality of samples, predictions of the model, dstribution of the dataset etc. Users can also further use some of FiftyOne's powerful in-house tools such as the [FiftyOne Brain](https://pypi.org/project/fiftyone-brain/) and the [Model Zoo](https://voxel51.com/docs/fiftyone/user_guide/model_zoo/models.html) for further predictions and refining of the data pre-loaded in the launched App with the help of the given code. The dataset used here is the [New Plant Diseases Dataset](https://www.kaggle.com/vipoooool/new-plant-diseases-dataset) containing 38 classes and over 87000 images on which the models are based.

## Project Setup:-
### 1. Download the Dataset and modify it.

Download the dataset [here](https://www.kaggle.com/vipoooool/new-plant-diseases-dataset).

In the ```train```, ```test``` and ```valid``` folders, remove the ```tomato``` leaf species folders. This is done for two reasons.

* The tomato species alone accounts for over 1/3 of the test data. This results in a problem with the predictions obtained in the csv file since that file is used for visualizations in the App. This prevents the data which is visualized there from being extremely skewed.
* As a result of this exclusion, it has to be removed from the valid and test folders as well.

NOTE: Inside the ```train``` and ```valid``` folders, the name of the folders (the various species) have to be in alphabetical order.

### 2. Clone the Repository.
```bash
git clone https://github.com/sarobml2000/ClassifyToView.git
```
### 3. FineTune the model and generate predictions.

Launch the _Leaf_Disease_Classification_Model.ipynb_ file inside the _Code_ folder.
```bash
cd Code
jupyter notebook Leaf_Disease_Classification_Model.ipynb
```
The predictions on the test data will be written to the csv file.
The pre-trained weights for the AlexNet architecture can be found [here](https://drive.google.com/file/d/1iP2E2Didog_yPk-6s1Idlxz0Bz4Xkm3i/view?usp=sharing)

### 4. Visualize with FiftyOne.
Launch the _Visualizations_leaf_diseases.ipynb_ file inside the _Code_ folder.
```bash
cd Code
jupyter notebook Visualizations_leaf_diseases.ipynb
```
Here, the contents of the ```.csv``` file were re-written into this [excel file](https://github.com/sarobml2000/Leaf-Disease-Classification/blob/main/Pred_Classes.xlsx) for easier handling and loading. 
The FiftyOne App session will be launched inside the cell of the notebook which can then be used for various purposes as outlined above.

## Hardware Used:-
OS: Windows 10 Home.  
CPU: Intel i5 8th generation.  
GPU: NVIDIA GeForce 940 MX.  
RAM: 8 GB.

_Dataset Credit_: [Samir Bhattarai](https://www.kaggle.com/vipoooool)
