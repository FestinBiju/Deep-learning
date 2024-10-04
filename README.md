
# PROJECT 1 :Handwritten Digit Recognition with MNIST
This project uses the popular MNIST dataset of handwritten numbers to create a model that can recognize digits from 0 to 9. The process includes exploring the data, cleaning it, and preparing it for training a machine learning model to accurately recognize these handwritten digits.

## About the Dataset
We’re using the MNIST dataset, which includes:

- 60,000 training images of handwritten digits
- 10,000 test images to check the model's performance
Each image is 28x28 pixels, making it easy to work with for beginners and experienced users alike.

## Steps in This Project
### 1. Exploratory Data Analysis (EDA)
In this step, we explore the data by:

- Viewing sample images to get a feel for the data.
- Checking pixel intensity values to see patterns and understand image brightness.
- Ensuring each digit from 0-9 is represented in a balanced way, making sure no numbers are missing.
### 2. Data Cleaning
We make sure the data is ready for use by:

- Verifying that all images are complete and not corrupted.
- Scaling pixel values from 0 to 1 to simplify the model’s job of understanding the images.
- Trimming unnecessary space around the digits to improve recognition accuracy.
### 3. Data Preparation
To prepare the data for our model, we:

- Flatten each image into a 1D array that the model can read.
- Encode the digit labels (0-9) in a way the model understands.
- Split the data into training, validation, and test sets.
### 4. Model Training
We then:

- Choose a model—typically a Convolutional Neural Network (CNN)—which is good at identifying patterns in images.
- Train the model on the training set and monitor its progress on the validation set.
- Test the model on the test set to see how accurately it recognizes digits.
