##OVERVIEW
In this folder, we store the results of testing different pre-trained convolutional neural network models. These pre-trained convolutional neural network architectures were trained with the same dense layer structures and training conditions. 

##TESTING CONDITIONS
In order to reduce computational burden, the performance of each model was evaluated on a subset of 10,000 images with balanced classes between uninfected and parasitized red blood cells. Five-fold cross-validation was performed, in which the mean and 95% confidence intervals are displayed on the figures below. An Adam optimizer with a small learning rate of 1e-6 was used. After the convolutional layers, there were two fully connected dense layers with 512 ReLU nodes each and 0.5 dropout. The batch size was set to 64 and the models were trained for 75 epochs. A categorical cross-entropy loss function was used.

##INTERPRETTING FILES
General: Each row is a different cross-validation set.
ModelName_TestAcc: Validation accuracy of neural network. Each column is a sequential epoch.
ModelName_TestLoss: Validation loss of neural network. Each column is a sequential epoch.
ModelName_TrainAcc: Testing accuracy of neural network. Each column is a sequential epoch.
ModelName_TrainLoss: Testing loss of neural network. Each column is a sequential epoch.
ModelName_Thresholds: Probability thresholds used to calculate each corresponding TPR and FPR value
ModelName_TPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "ModelName_Thresolds.csv".
ModelName_FPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "ModelName_Thresolds.csv".
