# Arabic-Handwritten-Words-Recognition

# Image Classification Model: 
“Arabic-Handwritten-Words-Classification”
## 1. Model Architecture and Design
* Objective: Classify Arabic words from a set of known words, the good handwritten words by user should be predicted correctly by the Model.
* Architecture:
  * Input layer: RGB images of size 150x150 pixels.
  * Convolutional layers (4 layers):
    * 64 filters, kernel size 3x3, ReLU activation.
    * 64 filters, kernel size 3x3, ReLU activation.
    * 128 filters, kernel size 3x3, ReLU activation.
    * 128 filters, kernel size 3x3, ReLU activation.
  * Max-pooling layers (2 layers):
    * Pool size 2x2.
  * Flatten layer.
    * Fully connected layers (2 layers):
    * 512 neurons, ReLU activation.
    * 53 neurons (output), softmax activation.
## 2. Hyperparameters
  * Learning rate: 0.01
  * Batch size: 20
  * Optimizer: RMSProp
## 3. Dataset Details
  * Dataset: Handwritten Arabic words (53 words) 
    * Each word dataset has the following:
      * Different handwriting style.
      * The same word written by optical characters.
      * Different computer Arabic fonts.
    * [Dataset used](https://github.com/MuhammadWael/Arabic-words-dataset)
* Preprocessing:
  * Resize images to 150x150 pixels.
  * Normalize pixel values to [0, 1].
  * Random data augmentation is not used.
## 4. Training Process
  * Training:
    * Train for 10 epochs.
    * Early stopping based on validation loss.
   
  * Loss Function: Categorical cross-entropy.
  * Metrics: Training Accuracy: %99.34  Validation accuracy: %96.57
## 6. Evaluation Metrics
  * Accuracy on a separate test set of 25 images was %84
    ![image](https://i.imgur.com/CU0YffC.png)
## Contributors:
* [Muhammad Wael](https://github.com/MuhammadWael)
* [Abdelrahman Sabry](https://github.com/sabrysm)
