# LendingClubLoanData

### Notes and Assumptions:

- Goal: Classify different loans into grades based on included features.

- Due to Google Colab resource limits the following assumptions were made
  - Due to long training times, I made the assumption that we do not need to interpret feature importance.
  - Looking to classify high grade (A,B,C) vs low grade loans (D,E,F,G) instead of each individual grade for ML methods.
  - Predict specific grade(A,B,C,...) for Neural Networks method.

- Next Improvements:
  - Finish implementing TFX pipeline
  - Improve Feature Engineering for ML data

#### *Update Notes:*

- Added Deep Neural Network with Keras.
- Keras model predicts specific grade(A,B,C,...) instead of high grade vs. low grade. To do this with ML methods drastically increased training time.
- Created seperate feature engineering process for Deep Learning model to optimize performance. Added One-hot encoding for non-ordinal variables
- Kept similiar feature engineering process for Machine Learning methods to keep training time low.


## Project Structure:

- Feature Engineering
  - Seperate data preparation for machine learning and deep learning methods

- PCA
  - Perforned PCA to reduce training time for machine learning methods

- Machine Learning Model Performance:

## Accuracy:

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
