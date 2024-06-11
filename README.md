# shodh-ai-task

### Problem Statement 1: 
The file "Sales_Dialogues_Dataset.md" contains approximately 110 dialogue sets that simulate conversations in a sales context. These dialogues demonstrate a deep understanding of the product or service being offered. They culminate in simulated sales scenarios, where the dialogue aims to lead the potential customer towards making a purchase.

### Problem Statement 1: 
Documentation for MNIST Classification Model (shodh_ai_mnist_classification.ipynb)

Model Architecture
The model is designed using the TensorFlow Keras API and consists of a convolutional neural network (CNN) tailored for handwritten digit recognition on the MNIST dataset. The architecture includes:

Three convolutional layers with 32, 64, and 64 filters respectively, each followed by a 2x2 max-pooling layer. Each convolutional layer uses a 3x3 kernel and ReLU activation.
After the convolutional and pooling layers, the network flattens the data and feeds it into a dense layer of 64 neurons with ReLU activation, followed by a dropout layer with a dropout rate of 0.5 to prevent overfitting.
The output layer is a dense layer with 10 neurons (one for each digit 0-9) using the softmax activation function to output probability distributions over the 10 classes.
Training Process
The model was compiled with the Adam optimizer and categoricalcrossentropy as the loss function. The metrics for evaluation were accuracy.

Training involved a batch size of 32 and was set to run for a maximum of 10 epochs.
Validation was performed on 10% of the training data.
Early stopping was employed to terminate training if the validation loss did not improve for three consecutive epochs, to avoid overfitting.
Additionally, weights from the first convolutional layer were recorded after each epoch for visualization purposes.
Results
The model achieved high accuracy on the test dataset, indicative of its effectiveness in recognizing handwritten digits from the MNIST dataset. Plots were provided to show the progression of accuracy and loss across training epochs for both training and validation data.

Visualization Interface
Model Metrics Plot: After training, plots for accuracy and loss over epochs are shown, providing insights into the model’s performance over time. These plots help identify if the model is learning effectively or if it is overfitting or underfitting.
Weights Visualization: Visualizes the filters from the first convolutional layer after each epoch. This helps to understand how the model's features evolve over time.

Confusion Matrix: After making predictions on the test set, a confusion matrix is plotted to evaluate the model's performance across all classes, highlighting any particular digits for which the model may be confusing one for another.

To predict the digit from an image file:
Call the predict_digit function with the path to the image file as an argument.
The function will display the image, preprocess it, make a prediction using the trained model, and output the predicted digit.
