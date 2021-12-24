# CNN_Oxford-IIIT-Pet_ DataSet
Oxford-IIIT-Pet_Image dataset classification model
## Dataset
The dataset for this project can be downloaded from any of the following links:
* [The Oxford-IIIT Pet Dataset](https://www.robots.ox.ac.uk/~vgg/data/pets/)
* [Kaggle](https://www.kaggle.com/tanlikesmath/the-oxfordiiit-pet-dataset)

This dataset consists of 7390 images of pets spanning 37 classes with about 200 images per class. The images vary vastly in size, aspect ratio, pose, lightning, etc. All images in the dataset are within the same folder and the associated class information for each image is present in the file name itself.

## Project Requirements
The external libraries required for running _**Train.ipynb**_ are:
1. numpy
2. matplotlib
3. sklearn/scikit-learn
4. tensorflow (Version 2.7.0 used)
5. tqdm (Optional. If unavailable, make changes accordingly)

## Data Preprocessing

- Firstly, the class names of all images were extracted from the image file names to create the target variable.
- The dataset was then divided into **train**, **validation** and **test** datasets. **10% of the entire dataset was used as a test dataset and 10% of the remaining as the validation dataset.**
- Since all images have different sizes and aspect ratios, **the images were loaded with fixed 256*256 resolution with padding**. The padding helps prevent distortion due to stretching or shrinking of images when changing its aspect ratio.
- Keras' **ImageDataGenerator** was used for image augmentation during training with small values for rotation, shift, shear, zoom etc.

## Model
The model used is a deep Convolutional Neural Network and was created using tensorflow.keras Sequential API.

The different layers used in this model are as follows:
- Input 
- Convolution 2D
- Max Pooling 2D
- Batch Normalization
- Dropout

#Note: Due to Time limit in Google colab GPU usage i have made Epochs=50 increase it if you want more accuray
