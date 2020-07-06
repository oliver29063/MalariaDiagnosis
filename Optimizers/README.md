## OVERVIEW
In this folder, we store the results of testing different optimizers and learning rates for the VGG16 model. All other hyperparameters were the same during training.

## TRAINING AND TESTING CONDITIONS
In order to reduce computational burden, the performance of each model was evaluated on a subset of 10,000 images with balanced classes between uninfected and parasitized red blood cells. Five-fold cross-validation was performed, in which the mean and 95% confidence intervals are displayed on the figures below. After the convolutional layers, there were two fully connected dense layers with 1024 ReLU nodes each and 0.5 dropout. The batch size was set to 64. The models were trained for 50 epochs. A categorical cross-entropy loss function was used. Learning rates of 1e-6, 1e-5, 1e-4, and 1e-3 were tested on the followning optimizers: SGD w/ Nesterov, Adam, Nadam, RMSProp, and AdaMax.

## INTERPRETTING FILES
- General: Each row is a different cross-validation set.
- Optimizer_LR_TestAcc: Validation accuracy of neural network. Each column is a sequential epoch.
- Optimizer_LR_TestLoss: Validation loss of neural network. Each column is a sequential epoch.
- Optimizer_LR_TrainAcc: Testing accuracy of neural network. Each column is a sequential epoch.
- Optimizer_LR_TrainLoss: Testing loss of neural network. Each column is a sequential epoch.
- Optimizer_LR_Thresholds: Probability thresholds used to calculate each corresponding TPR and FPR value
- Optimizer_LR_TPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "BatchSize_Thresolds.csv".
- Optimizer_LR_FPR: True positive rate for each corresponding threshold. Column indices correspond with column indices in "BatchSize_Thresolds.csv".

