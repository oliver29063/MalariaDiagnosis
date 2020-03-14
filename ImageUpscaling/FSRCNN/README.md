## OVERVIEW
In this folder, we store the results of testing different FSRCNN models with varying numbers of mapping layers (m), high resolution feature dimensions (d), and low resolution feature dimensions (s). More specifically, we test models with 2, 3 or 4 mapping layers, 48 or 56 high resolution feature dimensions, and 12 or 16 low resolution feature dimensions. The "FSRCNN Architecture Experiments.ipynb" file is fairly-self explanatory once you open the code. This is where we ran our experiments to obtain the CSV files located within this folder. Note that upon running the code, you will receive slightly different numbers in the CSV file due to a different randomly cross-validation split, but the general values and trends should be consistent.

## TRAINING AND TESTING CONDITIONS
When training the FSRCNN model, five-fold cross validation across the full dataset was used. MSE was calculated during the training of the model, while PSNR was calculated manually with the equation below, where $I$ is the maximum pixel intensity (I=256 in our images):

PSNR = 10 log_{10}(I^2/MSE)

## INTERPRETTING CSV FILES
Each CSV file has the title format of "d_s_mMaps_TrainLoss.csv" for the FSRCNN training loss and "d_s_mMaps_TestLoss.csv" for the FSRCNN testing loss. Within each file, each row is a different cross-validation set, while each column is a sequential epoch. For example, a file called "56_12_3Maps_TrainLoss.csv" with the value of 138.6275 in the first row and third column: The omdel training loss MSE is 138.6275 in the first cross-validation set on the third epoch, for a FSRCNN model with 3 mapping layers, a high resolution feature dimension of 56, and a low resolution feature dimension of 12.
