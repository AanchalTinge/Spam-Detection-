
# Spam Detection Project

## Overview

This project aims to build a spam detection system using machine learning. It classifies messages into two categories: "Spam" or "Ham" (non-spam). The project uses a dataset of labeled messages, preprocesses the text data, trains a logistic regression model, and evaluates its performance.

## Dependencies

The project requires the following Python packages:

- `pandas` for data manipulation
- `matplotlib` for plotting
- `seaborn` for visualization
- `scikit-learn` for machine learning

You can install the required packages using pip:

```bash
pip install pandas matplotlib seaborn scikit-learn
```

## Dataset

The dataset used in this project is `spam.csv`, which contains labeled messages. The dataset should be placed in the same directory as the script. The dataset should have the following columns:
- `label`: Indicates whether the message is spam (`spam`) or not (`ham`).
- `message`: The text of the message.

## Code Description

1. **Data Loading and Preprocessing**
   - Loads the dataset from `spam.csv`.
   - Drops unnecessary columns and renames remaining columns.
   - Maps labels to binary values (0 for 'ham', 1 for 'spam').

2. **Visualization**
   - Displays a pie chart showing the distribution of spam and ham messages.

3. **Data Splitting**
   - Splits the dataset into training and testing sets.

4. **Feature Extraction**
   - Initializes and applies TF-IDF Vectorizer to convert text data into numerical format.

5. **Model Training**
   - Trains a Logistic Regression model using the training data.

6. **Evaluation**
   - Evaluates the model's performance using accuracy, classification report, confusion matrix, and ROC curve.

7. **Testing**
   - Tests the spam detection function with a few sample messages.

## Usage

To run the script, execute the following command in your terminal:

```bash
python spam_detection.py
```

### Example Output

The script will print the accuracy of the model and a classification report. It will also display plots for the confusion matrix and ROC curve. Additionally, it will print predictions for a set of test messages.

### Testing Messages

The following messages are used for testing the spam detection function:

1. "Congratulations! You've won a free ticket to the Bahamas. Call now!"
2. "Reminder: Your appointment is scheduled for tomorrow at 10 AM."
3. "URGENT! Your account has been compromised. Please contact support immediately."
4. "Hey, are we still meeting for lunch tomorrow?"
5. "You have received a bonus of $500. Click here to claim your prize."

## Example Output

```
Accuracy: 0.98
              precision    recall  f1-score   support

         ham       0.98      0.98      0.98       145
        spam       0.98      0.98      0.98        55

    accuracy                           0.98       200
   macro avg       0.98      0.98      0.98       200
weighted avg       0.98      0.98      0.98       200

Confusion Matrix:
[[143   2]
 [  2  53]]

ROC Curve:
AUC: 0.99

Message 1: Congratulations! You've won a free ticket to the Bahamas. Call now!
Prediction: Spam

Message 2: Reminder: Your appointment is scheduled for tomorrow at 10 AM.
Prediction: Ham

Message 3: URGENT! Your account has been compromised. Please contact support immediately.
Prediction: Spam

Message 4: Hey, are we still meeting for lunch tomorrow?
Prediction: Ham

Message 5: You have received a bonus of $500. Click here to claim your prize.
Prediction: Spam
```

## Notes

- Ensure that the `spam.csv` dataset file is present in the same directory as the script.
- The accuracy and performance metrics may vary depending on the dataset and model configuration.
