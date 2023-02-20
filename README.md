# calculate-Inception-Score-for-CIFAR-10-in-Keras
This code calculates the Inception Score for the CIFAR-10 dataset using Keras with InceptionV3 model. The Inception Score is a metric to evaluate the quality of generated images from a generative model.This code calculates the Inception Score for the CIFAR-10 dataset using Keras with InceptionV3 model. The Inception Score is a metric to evaluate the quality of generated images from a generative model. It measures how well the generated images match the real images in the dataset in terms of their diversity and quality.

The code loads CIFAR-10 dataset and shuffles the images. It uses the InceptionV3 model to calculate the Inception Score for a subset of images. The images are split into n_split parts, and the Inception Score is calculated for each split, and then the average and standard deviation of the Inception Scores are computed. The code also includes a function to scale an array of images to a new shape using nearest neighbor interpolation.

To run the code, simply execute the Python script. The output will show the shape of the loaded images and the calculated Inception Score with its standard deviation.
Note: This code assumes that Keras and its dependencies are installed, as well as scikit-image and numpy libraries.

# Prerequisites
This code requires Keras and TensorFlow to be installed.
The code uses the Cifar-10 dataset, which can be loaded using the cifar10.load_data() function provided by Keras.

# How to Use
Install the required libraries and packages.
Load the Cifar-10 dataset using cifar10.load_data() and shuffle the images.
Select a subset of images for calculating the Inception Score. This code uses 5000 images, but you can change this number as per your requirement.
Call the calculate_inception_score() function with the selected images as input. This function returns the average and standard deviation of the Inception Score for the given set of images.
Print the results returned by the calculate_inception_score() function.

# Function Description
scale_images(images, new_shape) function takes an array of images and scales them to a new size. It uses the resize() function from skimage.transform module for resizing the images.
calculate_inception_score(images, n_split=10, eps=1E-16) function calculates the Inception Score for a set of images. It loads a pre-trained Inception V3 model and uses it to predict the class probabilities for each image. It then calculates the Inception Score using the KL divergence between the predicted class probabilities and the overall class probabilities. It returns the average and standard deviation of the Inception Score for the given set of images. The n_split parameter specifies the number of splits of images/predictions to use in the calculation, and the eps parameter is a small constant added to prevent division by zero.

# References
Salimans, T., Goodfellow, I., Zaremba, W., Cheung, V., Radford, A., & Chen, X. (2016). Improved techniques for training GANs. In Advances in neural information processing systems (pp. 2234-2242).
TensorFlow Documentation: https://www.tensorflow.org/api_docs/python/tf
Keras Documentation: https://keras.io/
