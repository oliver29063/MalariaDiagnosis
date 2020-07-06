## OVERVIEW
In this folder, we store the results of testing different batch sizes for the VGG16 model. All other hyperparameters were the same during training.

## TRAINING AND TESTING CONDITIONS
In order to reduce computational burden, the performance of each model was evaluated on a subset of 10,000 images with balanced classes between uninfected and parasitized red blood cells. Five-fold cross-validation was performed, in which the mean and 95% confidence intervals are displayed on the figures below. An SGD w/ Nesterov optimizer with a small learning rate of 1e-5 was used. After the convolutional layers, there were two fully connected dense layers with 1024 ReLU nodes each and 0.5 dropout. The batch size was set to: 4, 8, 16, 32, 64, 128, and 256. The models were trained for 50 epochs. A categorical cross-entropy loss function was used.

## INTERPRETTING FILES
- General: Each row is a different cross-validation set.
- BatchSize_TestAcc: Validation accuracy of neural network. Each column is a sequential epoch.
- BatchSize_TestLoss: Validation loss of neural network. Each column is a sequential epoch.
- BatchSize_TrainAcc: Testing accuracy of neural network. Each column is a sequential epoch.
- BatchSize_TrainLoss: Testing loss of neural network. Each column is a sequential epoch.
- BatchSize_Thresholds: Probability thresholds used to calculate each corresponding TPR and FPR value
- BatchSize_TPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "BatchSize_Thresolds.csv".
- BatchSize_FPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "BatchSize_Thresolds.csv".
