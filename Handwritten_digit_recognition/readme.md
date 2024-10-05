Handwritten Digit Recognition
This project implements a handwritten digit recognition system using a Convolutional Neural Network (CNN) with Keras on the MNIST dataset. The model is trained to classify images of handwritten digits (0-9) and can predict digits from new images.

Table of Contents
1. Installation
2. Data Description
3. Project Structure
4. Steps
5. Model Architecture
6. Data Augmentation
7. Results
8. Usage
9. License
1. Installation
-** To run this project, ensure you have the following Python packages installed:

bash
Copy code
pip install keras opencv-python matplotlib numpy tensorflow
2. Data Description
The dataset used in this project is the MNIST handwritten digit dataset, which consists of 60,000 training images and 10,000 testing images of handwritten digits. Each image is 28x28 pixels.

3. Project Structure
bash
Copy code
.
├── mnist_digits_recognition.py  # Python script for digit recognition
├── 1.png                        # Sample image of handwritten digit
├── 2.png                        # Sample image of handwritten digit
├── 3.png                        # Sample image of handwritten digit
├── 4.png                        # Sample image of handwritten digit
├── 5.png                        # Sample image of handwritten digit
└── README.md                    # Project documentation
4. Steps
Import Libraries: Import necessary libraries such as Keras, OpenCV, and Matplotlib.
Load Data: Load the MNIST dataset using Keras.
#Preprocess Data:
- **Reshape the training and testing images to include the channel dimension.
- **Normalize the pixel values to the range [0, 1].
- **Convert the class labels to categorical format.
# Create the Model:
- **Build a CNN model with convolutional layers followed by batch normalization and dropout layers.
- **Add dense layers for classification with L2 regularization.
- **Compile the Model: Compile the model using categorical crossentropy loss and the Adam optimizer with a custom learning rate.
- **Data Augmentation: Use ImageDataGenerator for data augmentation to improve model generalization.
- **Train the Model: Fit the model on the augmented training data and validate it on the test data.
# Make Predictions:
- **Load new handwritten digit images.
- **Invert the image colors for better prediction accuracy.
- **Resize and preprocess the images to match the model's input shape.
- **Predict the digits using the trained model.
5. Model Architecture
- **The model architecture consists of:

- **Convolutional Layers: Three Conv2D layers with ReLU activation, followed by batch normalization.
- **Pooling Layer: One MaxPooling2D layer to reduce dimensionality.
- **Dropout Layers: Two Dropout layers to prevent overfitting.
- **Fully Connected Layers: Three Dense layers with 256 neurons each and L2 regularization.
6. Data Augmentation
- **Data augmentation techniques used in this project include:

Rotation
Zoom
Width and height shifts
These augmentations help improve the model's ability to generalize to unseen data.

7. Results
- **The model is trained for 2 epochs with a batch size of 128. The training and validation accuracy will be displayed during the training process.

8. Usage
- **To run the digit recognition script, ensure you have the sample images (1.png, 2.png, 3.png, 4.png, 5.png) in the same directory. Execute the following command:

bash
Copy code
- **python mnist_digits_recognition.py
- **The script will print the predicted digit for each image and display the images.

License
This project is licensed under the MIT License - see the LICENSE file for details.

