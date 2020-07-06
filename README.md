# MalariaDiagnosis
This GitHub repository contains the source code for the PeerJ manuscript submission titled **"Convolutional Neural Networks to Automate the Screening of Malaria in Low-Resource Countries**". In order to best delineate which Jupyter Notebooks are used in each part of the manuscript, we will list them by sections and subsections of the manuscript. These notebook were run on either: (1) Google Colab, (2) Google Cloud Computing Platform, or (3) a personal laptop with CUDA GPA. Each notebook will specify which platform was used and list the versions of every Python package in use. 

In order to replicate the results, we first recommend setting the number of training epochs to 1 to ensure that the notebooks function correctly. Then the epoch count can be changed back to run the full training process, which can take quite some time. Please note that the results will slightly vary from the provided \*.csv files, but should give closely similar results. 

## Results

### Red Blood Cell Object Detection

### Malaria Classification Model

#### Evaluating Pre-Trained Neural Network Architectures

#### Optimizing Classification Layers
In this section, we determine the optimal dropout rate, number of nodes in the dense layers, and the activation function. The raw data of these results can be found at **MalariaDiagnosis/Dropout**, **MalariaDiagnosis/DenseNodes**, and **MalariaDiagnosis/ActivationFunctions**. The notebook used to gather these results can be found in this same folder at **Architecture Training for Classification.ipynb**. In order to generate the data shown Figure 3, we use the notebook **Classification Architecture Evaluation.ipynb**.
  
Online Google Colab versions are available:
- Architecture Training for Classification.ipynb: https://colab.research.google.com/drive/1F8x74o6_3jykbbVpXUktouWKDOGydi5j?usp=sharing
- Classification Architecture Evaluation.ipynb: https://colab.research.google.com/drive/1kqDQYJWPtIqQbVs_U0AwysL832Tn-JVa?usp=sharing

#### Fine-Tuning Training Hyperparameters

### Image Resolution Upscaling

### Integration of CNNs on Mobile Platform

## Discussion
