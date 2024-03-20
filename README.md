# Function Definition:

The function reshape_image_to_three_dimension is defined to reshape a grayscale image into an RGB image format.
# Input and Output:

The function takes a grayscale image represented as a numpy array with shape (height, width) as input.
It returns the reshaped RGB image as a numpy array with shape (height, width, 3).
# Reshaping Process:

The function first adds a new dimension for the channel using np.expand_dims(image, axis=-1).
Then, it replicates the values along the new dimension to create three channels using np.repeat(image_rgb, 3, axis=-1)
# Model Training and Evaluation:

The neural network model is defined using TensorFlow and Keras, with a simple architecture consisting of a single hidden layer.
The model is compiled with the Adam optimizer, sparse categorical cross-entropy loss function, and accuracy metric.
The model is trained on the training data (X_train and y_train) for 50 epochs and validated on the validation data (X_val and y_val).
The model's performance is evaluated on the validation set, and the validation loss and accuracy are printed.
# Model Prediction:

The model is used to predict labels for the validation set (X_val).
The predicted probabilities are converted into class labels.
The model's performance is evaluated using additional metrics such as accuracy, precision, recall, and F1-score.
A confusion matrix is generated to provide further insight into the model's performance.
# Visualization:

A subset of the validation set is visualized to compare predicted labels with actual labels.
Grayscale images from the validation set are displayed along with their predicted and actual labels for visual inspection.
