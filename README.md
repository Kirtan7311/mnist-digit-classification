# MNIST Digit Classification

This repository contains code for training a neural network to classify MNIST digits using TensorFlow and Keras. The model is built and trained on the MNIST dataset, which consists of 60,000 training images and 10,000 test images of handwritten digits from 0 to 9.

## Requirements

The following Python libraries are required to run the code:

- TensorFlow
- Matplotlib
- Scikit-learn

You can install these libraries using the following command:
```bash
pip install -r requirements.txt
```
## Data Preprocessing
The MNIST dataset is loaded and normalized to scale the pixel values to the range [0, 1].

## Model Architecture

The neural network model for MNIST digit classification is built using the Sequential API from Keras. Below is a detailed description of each layer in the model architecture:

1. **Input Layer**:
   - **Shape**: (28, 28)
   - The input layer accepts grayscale images of handwritten digits, each with dimensions 28x28 pixels.

2. **Flatten Layer**:
   - **Function**: Converts the 2D input images into 1D vectors.
   - This layer is essential for transitioning from the 2D image format to a format that can be processed by dense (fully connected) layers.

3. **Dense Layer 1**:
   - **Neurons**: 128
   - **Activation Function**: ReLU (Rectified Linear Unit)
   - This fully connected layer has 128 neurons and uses the ReLU activation function to introduce non-linearity into the model, allowing it to learn more complex patterns.

4. **Dropout Layer**:
   - **Dropout Rate**: 0.2 (20%)
   - The dropout layer is added to prevent overfitting. It randomly sets 20% of the input units to 0 during training, which helps the model generalize better to new data.

5. **Dense Layer 2**:
   - **Neurons**: 10
   - **Activation Function**: Softmax
   - This is the output layer with 10 neurons, each representing a digit class (0-9). The softmax activation function is used to convert the output to a probability distribution over the 10 digit classes.

## Training
The model is compiled using the sparse categorical cross-entropy loss function and the Adam optimizer. It is trained for 20 epochs with a validation split of 20%. The training accuracy and validation accuracy are plotted to visualize the training process.

### Results
The trained MNIST classifier model was evaluated on a test dataset to determine its performance. The following metrics were used to assess the model's effectiveness:

1. **Accuracy**:
   - The accuracy of the model indicates the percentage of correctly classified messages out of the total messages in the test dataset.

The model achieved the following results on the test dataset:

- **Accuracy**: 97.91%

These results demonstrate that the MNIST classifier is capable of accurately identifying digits. The model's performance can be further improved by tuning hyperparameters.

## Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/Kirtan7311/mnist-digit-classification.git
    ```

2. Navigate to the project directory:
    ```bash
    cd mnist-digit-classification
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Run the application:
    ```bash
    python mnist_model_training.py
    ```

## Contributing
Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

Please make sure your code follows the project's coding style and includes relevant tests. We appreciate your contributions and will review pull requests promptly.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

Thank you all for your support!