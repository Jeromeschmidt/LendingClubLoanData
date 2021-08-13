# LendingClubLoanData

### Notes and Assumptions:

- Goal: Classify different loans into grades based on included features.

- Due to Google Colab resource limits the following assumptions were made
  - Due to long training times, I made the assumption that we do not need to interpret feature importance.
  - Looking to classify high grade (A,B,C) vs low grade loans (D,E,F,G) instead of each individual grade for ML methods.
  - Predict specific grade(A,B,C,...) for Neural Networks method.

#### *Update Notes:*

- Added Deep Neural Network with Keras.
- Keras model predicts specific grade(A,B,C,...) instead of high grade vs. low grade. To do this with ML methods drastically increased training time.
- Created separate feature engineering process for Deep Learning model to optimize performance. Added One-hot encoding for non-ordinal variables
- Kept similar feature engineering process for Machine Learning methods to keep training time low.

#### Next Improvements:
- Finish implementing TFX pipeline
- Improve Feature Engineering for ML data


## Project Structure:

- Feature Engineering
  - Separate data preparation for machine learning and deep learning methods

- PCA
  - Performed PCA to reduce training time for machine learning methods

- Machine Learning Models Included:
    - K Neighbors Classifier
    - Decision Tree
    - SGD Classifier
    - XGBoost
    - Random Forest Classifier
    - MLP Classifier


### Neural Network Design Choices:
Activation Function: RELU
- Fast training and not prone to vanishing gradients

Optimizer: Adam
- Fast optimizer to find local minimum

Loss: sparse_categorical_crossentropy
- Since not all of our features are one-hot encoded


## Accuracy Comparison:

Machine Learning Model Performance:

![Machine Learning Models Accuracy](/assets/images/ml_accuracy.png)

| Algorithm | Accuracy |
| ----------- | ----------- |
| K Neighbors Classifier | 0.7244905637958691 |
| Decision Tree | 0.6494445214567202 |
| SGD Classifier | 0.7654157672733034 |
| XGBoost |  0.7655939956829119 |
| Random Forest Classifier | 0.76415628651207 |
| MLP Classifier | 0.765427649167277 |


Deep Learning Model Performance:

![Neural Network Loss](/assets/images/nn_loss.png)

![Neural Network Accuracy](/assets/images/nn_accuracy.png)

| Algorithm | Loss | Accuracy |
| ----------- | ----------- | ----------- |
| Neural Network | 0.04266935586929321 | 0.9847416281700134 |

## Results:
Since our Neural Network outperformed our tree based ML algorithms(~98.8% vs ~76.4%), a neural network would be the most effective approach for this dataset. Also, the neural network classified specific graded where the ML methods only classified high vs low grade loans.

Further improvements and things to look at:

Different model structure
Try SGD optimizer
