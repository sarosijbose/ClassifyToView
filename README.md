# Leaf-Disease-Classification: Model and visualization code for detecting diseases in Leafs

## Description:-
This repository contains code for classifying various diseases in plant leaves based on the [AlexNet](https://papers.nips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf) Architecture whose pre-trained weights are used. The model is then further Fine-tuned and the best weights saved from each iteration. It is then tested over the test data where it achieves an accuracy of almost 97%. The predictions for each species of leaf are then written to a csv file which is then later used in the visualization tool [FiftyOne](https://voxel51.com/fiftyone/). The code for loading and visualizing the dataset, the positive and the negative labels is also provided. The [FiftyOne App](https://voxel51.com/docs/fiftyone/user_guide/app.html) then allows the user to evaluate the quality of samples, predictions of the model, dstribution of the dataset etc. Users can also further use some of FiftyOne's powerful in-house tools such as the [FiftyOne Brain](https://pypi.org/project/fiftyone-brain/) and the [Model Zoo](https://voxel51.com/docs/fiftyone/user_guide/model_zoo/models.html) for further predictions and refining of the data pre-loaded in the launched App with the help of the given code. The dataset used here is the [New Plant Diseases Dataset](https://www.kaggle.com/vipoooool/new-plant-diseases-dataset) on which some further modifications was done which will be described below.

## Project Setup:-
### 1. Download the Dataset and modify it.

### 2. Clone the Repository.
```bash
git clone https://github.com/sarobml2000/Leaf-Disease-Classification.git
```
### 3. FineTune the model.

### 4. Visualize with FiftyOne.



