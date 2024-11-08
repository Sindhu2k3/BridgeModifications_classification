# KW51 Bridge Modifications Classification

This project classifies time series data from the KW51 bridge before and after structural modifications using image classification techniques with a convolutional neural network (CNN).

## Project Description

The KW51 bridge underwent retrofitting to enhance its structural integrity. To evaluate the effects, time series data was collected both **before** and **after** the modifications:
- **Normal Bridge**: Data collected from the bridge before modifications.
- **Retrofitted Bridge**: Data collected after modifications.

The data was transformed into images and classified using a CNN model based on GoogleNet architecture, fine-tuned for this binary classification task.

## Dataset

The dataset consists of two folders:
- `train`: Training images for both classes.
- `test`: Testing images for both classes.

**Note**: The datasets are hosted externally due to GitHub's file size limits.

- [Download `tre.zip` and `amb.zip` from Google Drive](https://drive.google.com/drive/folders/1vPwom8AetBAnPkCyaNuyQ8Wgo00WNjWN?usp=drive_link)



## Model Architecture

The model is based on GoogleNet, with modifications:
- The final fully connected layer is adjusted to output two classes, corresponding to the Normal and Retrofitted bridge states.

## Installation and Setup

1. **Extract the Dataset**: After downloading the zipfile, extract it in the main project directory.
2. **Environment**: Ensure the following libraries are available:
   - PyTorch
   - Torchvision
   - Matplotlib
   - scikit-learn
   - Google Colab (if running on Colab)

3. **Run the Notebook**:
   - Open and execute the Colab notebook to train and evaluate the model.

## Training and Evaluation

### Training
The model is trained using Cross-Entropy loss and the Adam optimizer over 20 epochs. During each epoch, the training loss and accuracy are computed and displayed.

### Validation
After each epoch, the model is evaluated on the test set. Validation loss and accuracy are also computed and displayed.

### Results
The model's performance on the test set is visualized with a confusion matrix, showing the classification accuracy for each bridge state.

## Confusion Matrix

A confusion matrix is generated to evaluate the model’s performance, illustrating the true and predicted classifications for both classes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
