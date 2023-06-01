# Hi! Paris technical assignment

Both the notebooks have been edited using Google Colab 
to leverage the Google GPU resources. Therefore, it is required to 
modify some file paths and some constants to execute it in any other environment

## Image classification 

The data have been stored in Google Drive and retrieved in Google Colab,
it will require to do the same to re-execute the notebook in Colab.

Tensorflow and Keras are leveraged for the neural network implementation. 

### Methodology

- Image vectorization and normalization
- Data exploration (no difference are guessable between classes by looking at the images)
- Training set balancing 
- Creation of a test set with labels using a subsample of the validation set
- Data Augmentation to rotate / zoom on images using ImageDataGenerator and hedge against overfitting
- Transfer Learning to use the imagenet weights of pretrained VGG16 and Xception architecture
- Several custom architectures
- Callbacks to keep the model of the best epoch and to make the learning rate decrease depending on the epoch
- Evaluation using accuracy, confusion matrix, F1 score and ROC curve, discriminating on the gender to see if 
it's playing a significant role in the classification

The different results obtained with the different models are barely better than the random classifier.
Moreover, the difference of performance depending on the gender can not be surely attributed to the characteristics of each class as wae don't know which they are.
Hence, we don't know if there is a real difference between the classes.

### Further improvements

A deep dive into the trained filters using grad cam algorithm could help indentify what are the 
features of each class if such classes are different. 


## Text generation

As for the image classification task, the data has been stored in Google Drive and 
the notebook has been executed in Google Colab. 

Tensorflow and Keras are also used in this part. 

### Methodology 

#### RNN implementation using tensorflow 

I have used tensorflow to process the data (tokenization) and I have chosen 
to implement a character based text generation model. 

I have tried several architecture with several number of LSTM layers with different dimensions. 
I have also modified the temperature parameter several times. 

The results are not convincing with this method as the generated words don't exist and therefore the sentences don't have any meaning.
That's may be due to the lack of data. 


#### Transfer Learning using pre-trained GPT model

In this section I have used KerasNLP to load GPT model in order to 
fine tune it with the mody dick data. 

After the fine tuning, the results are quite good and they are well reflecting the 
moby dick data training.

Transfer Learning seems to be the best methodology for this kind of task.

### Further improvements

Other architecture would have been tested with other kind of RNN units like GRU.

The amount of data could be increased and the task could be precised to make a more specialised 
text generation algorithm.

Most recent model like GPT4 could be used to make it more performant.









