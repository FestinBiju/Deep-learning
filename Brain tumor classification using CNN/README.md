# Brain Tumor Classification Using CNN
This project focuses on classifying brain MRI images to detect the presence of a brain tumor. It uses a **_Convolutional Neural Network_** (CNN) to distinguish between images labeled as "Tumor" or "No Tumor." The dataset is sourced from Kaggle, and this project demonstrates a basic approach to training a deep learning model to perform binary image classification.

## Dataset
The dataset used in this project is from Kaggle, specifically the Brain MRI Images for Brain Tumor Detection dataset. It consists of MRI scans divided into two categories:

- Yes (Images that contain a brain tumor)
- No (Images that do not contain a brain tumor)

### Dataset Structure:
Training Images: MRI scans are stored in two directories: yes/ and no/.
Images are resized to 128x128 pixels for simplicity.

# Steps in This Project
## 1. Data Preprocessing
The dataset is preprocessed by:

- Rescaling the images: Pixel values are normalized to the range [0, 1].
- Resizing: Images are resized to 128x128 pixels for uniform input to the CNN.
- Splitting the data: The dataset is split into training (80%) and validation (20%) sets using the ImageDataGenerator class from Keras.
## 2. CNN Model Architecture
A simple Convolutional Neural Network is used with the following layers:

- Convolutional layers: 3 Conv2D layers for feature extraction with ReLU activation.
- MaxPooling layers: Used after each convolutional layer to down-sample the feature maps.
- Dense layers: A fully connected layer with 128 neurons.
- Dropout layer: Applied before the final output to reduce overfitting.
- Output layer: A single neuron with a sigmoid activation for binary classification (tumor vs no tumor).
## 3. Model Compilation and Training
- Loss Function: Binary cross-entropy, as this is a binary classification problem.
- Optimizer: Adam optimizer with a learning rate of 0.001.
- Metrics: Accuracy is used to evaluate the model's performance during training.
The model is trained for 10 epochs with a batch size of 32, using a validation set to monitor accuracy and loss.

## 4. Model Evaluation
After training, the model is evaluated on the validation set, and the following metrics are reported:

- Validation Loss
- Validation Accuracy
## 5. Visualizing Results
- Training History: A plot of accuracy and loss over epochs for both the training and validation sets.
- Predictions: A visualization of a few random images from the validation set with both the true labels and the predicted labels shown.

## To run the project, follow these steps:
### Step 1: Install Requirements
- First, install the required Python libraries. This project uses TensorFlow, Keras, and Matplotlib:

`pip install tensorflow matplotlib kaggle`
## Step 2: Kaggle API Setup
Download the dataset using the Kaggle API. Make sure you have set up your Kaggle API key and downloaded the dataset:
`kaggle datasets download -d navoneel/brain-mri-images-for-brain-tumor-detection`

`unzip brain-mri-images-for-brain-tumor-detection.zip -d brain_tumor_dataset`
## Step 3: Run the Python Script
Run the script `brain_tumor_classification.py` or the provided Jupyter notebook to train and evaluate the model.

# Visualization
## Training and Validation Accuracy and Loss
The training history is plotted to visualize how well the model is learning over time.

## Sample Predictions
The model’s predictions on a few validation images are visualized with both the true labels and the predicted labels displayed.

## Acknowledgments
- Dataset: The dataset was sourced from Kaggle.
- Inspiration: This project is inspired by the importance of early detection of brain tumors using MRI scans.
