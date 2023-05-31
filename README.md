# Assignment Overview

Both the notebooks have been edited using Google Colab 
to leverage the Google GPU resources. Therefore, it might require to 
modify some file paths and some constants to execute it in any other environment

## Image classification 

The data have been stored in Google Drive and retrieved in Google Colab,
it will require to do the same to re-execute the notebook in Colab

### Methodology

I have used the following methodology : 

- Image vectorization and normalization
- Data exploration
- Training set balancing 
- Creation of a test set with labels using a subsample of the validation set
- Data Augmentation to rotate / zoom on images using ImageDataGenerator and hedge against overfitting
- Transfer Learning to use the imagenet weights of pretrained VGG16 architecture
- Callbacks to keep the model of the best epoch and to make the learning rate decrease depending on the epoch
- Evaluation using accuracy, confusion matrix, F1 score and ROC curve

The results are not convincing therefore I am not sure if there is a real difference between the classes or 
if the amount of data is not enough

## Text generation





