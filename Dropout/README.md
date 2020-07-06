## OVERVIEW
In this folder, we store the results of testing different dropout rates for the VGG16 model. All other hyperparameters were the same during training.

## TRAINING AND TESTING CONDITIONS
In order to reduce computational burden, the performance of each model was evaluated on a subset of 10,000 images with balanced classes between uninfected and parasitized red blood cells. Five-fold cross-validation was performed, in which the mean and 95% confidence intervals are displayed on the figures below. An Adam optimizer with a small learning rate of 1e-6 was used. After the convolutional layers, there were two fully connected dense layers 1024 ReLU nodes each. The batch size was set to 64 and the models were trained for 40 epochs. A categorical cross-entropy loss function was used. The dropout rates tested were 0.25, 0.50, and 0.75. 

## INTERPRETTING FILES
- General: Each row is a different cross-validation set.
- DropoutRate_TestAcc: Validation accuracy of neural network. Each column is a sequential epoch.
- DropoutRate_TestLoss: Validation loss of neural network. Each column is a sequential epoch.
- DropoutRate_TrainAcc: Testing accuracy of neural network. Each column is a sequential epoch.
- DropoutRate_TrainLoss: Testing loss of neural network. Each column is a sequential epoch.
- DropoutRate_Thresholds: Probability thresholds used to calculate each corresponding TPR and FPR value
- DropoutRate_TPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "Node1_Node2_Thresolds.csv".
- DropoutRate_FPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "Node1_Node2_Thresolds.csv".
