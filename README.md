# MalariaDiagnosis
This GitHub repository contains the source code for the PeerJ manuscript submission titled **"Convolutional Neural Networks to Automate the Screening of Malaria in Low-Resource Countries**". In order to best delineate which Jupyter Notebooks are used in each part of the manuscript, we will list them by sections and subsections of the manuscript. These notebook were run on either: (1) Google Colab, (2) Google Cloud Computing Platform, or (3) a personal laptop with CUDA GPA. Each notebook will specify which platform was used and list the versions of every Python package in use. 

In order to replicate the results, we first recommend setting the number of training epochs to 10 (or another low amount) to ensure that the notebooks function correctly. Then the epoch count can be changed back to run the full training process, which can take quite some time. Please note that the results will slightly vary from the provided \*.csv files, but should give closely similar results. 

## Replicating the Results w/ Jupyter Notebooks

### Malaria Classification Model

#### Evaluating Pre-Trained Neural Network Architectures
In this section, we determine the best preliminary pre-trained CNN architecture to move forward with. The raw data of these results can be found at **MalariaDiagnosis/ArchitectureResults**. The notebook used to gather these results can be found in this same folder at **Architecture Testing.ipynb**. In order to generate the data shown in Figure 2, we use the notebook **Architecture Evaluation.ipynb". 

Only Google Colab versions are available:
- Architecture Evaluation.ipynb: https://colab.research.google.com/drive/1IahTdafeEFg4DdnHI2IitlaH0d5RfRZJ?usp=sharing
- Architecture Testing.ipynb: https://colab.research.google.com/drive/1dzrXUnkqsWAkLNNIIaZwx4YYy0LOOcwV?usp=sharing

#### Optimizing Classification Layers
In this section, we determine the optimal dropout rate, number of nodes in the dense layers, and the activation function. The raw data of these results can be found at **MalariaDiagnosis/Dropout**, **MalariaDiagnosis/DenseNodes**, and **MalariaDiagnosis/ActivationFunctions**. The notebook used to gather these results can be found in this same folder at **Architecture Training for Classification.ipynb**. In order to generate the data shown Figure 3, we use the notebook **Classification Architecture Evaluation.ipynb**.
  
Online Google Colab versions are available:
- Architecture Training for Classification.ipynb: https://colab.research.google.com/drive/1F8x74o6_3jykbbVpXUktouWKDOGydi5j?usp=sharing
- Classification Architecture Evaluation.ipynb: https://colab.research.google.com/drive/1kqDQYJWPtIqQbVs_U0AwysL832Tn-JVa?usp=sharing

#### Fine-Tuning Training Hyperparameters
In this section, we determine the optimal optimizer type, learning rate, and batch size. The raw data of these results can be found at **MalariaDiagnosis/Optimizers** and **MalariaDiagnosis/BatchSize**. The notebook used to gather these results can be found in this same folder at **Architecture Training for Optimizers.ipynb**. In order to generate the data shown in Figure 4, we use the notebook **Optimizer Architecture Evaluation.ipynb**. 

Online Google Colab versions are available: 
- Architecture Training for Optimizers.ipynb: https://colab.research.google.com/drive/1cjaYpPl_OdfnDsxZPb6wrHNeHFb3F9C9?usp=sharing
- Optimizer Architecture Evaluation.ipynb: https://colab.research.google.com/drive/106qRc7l45pAER0PfhTiJzlMMEJxI3G5P?usp=sharing

### Image Resolution Upscaling
In this section, we determine the optimal number of mapping layers, high feature dimension space, and low feature dimension space for our FSRCNN model. The raw data of this results can be found at **MalariaDiagonsis/Upscaling/FSRCNN**. The notebook used to gather these results can be found in this same folder at **FSRCNN Training.ipynb**. The values were manually analyzed to create Table 4. To generate the results for Table 5, the images can be directly exported and run through the model with the correct hyperparameters - which can be copied, pasted, and adjusted from any of the \*.ipynb files training the VGG16 CNN.

Online Google Colab versions are available: 
- FSRCNN Training.ipynb: https://colab.research.google.com/drive/1tg5uY-tL0eCj_ikR-PNAQDBdr1SlHC73?usp=sharing

### Red Blood Cell Object Detection
In this section, we generate the SSD300 object detection model, whose results are shown on Table 2 of the manuscript. The notebook used is found in this same folder at **SSD300 Object Detection.ipynb**. This notebook **MUST** be run on the Google Cloud Computing Platform with either of the two specifications mentioned in the manuscript. 
