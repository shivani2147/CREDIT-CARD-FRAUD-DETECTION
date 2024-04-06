# Credit Card Fraud Detection

- It's a collection of information about credit card transactions made by people in Europe during two days in September 2013.
- Only a tiny portion / fraction (0.17%) of transactions are fraudulent
- Details include Transaction Time, Amount Spent and the Value that indicates whether a transaction was fraud or not.
- Researchers use this dataset to create tools that can identify rare Fraudulent transactions.

---
### Columns Include : 
- It's a Deep Learning based project
- Time --> Number of seconds elapsed between this transaction and the first transaction in the dataset.
- V1 to V28 (Numerical Features)
- Amount --> Transaction amount.
- Class (Target) --> 1 for Fraudulent Transactions, 0 otherwise (Legitimate)

---
### Steps of the Project : 
1. The dataset consists of 2,84,807 records and 31 features, with "Class" as the target feature.
2. No null values were detected.
3. The dataset was split into Input features and Output target
4. Data was split into 70% Training and 30% Testing sets.
5. Distribution of fraud and legitimate transactions:
    - Fraudulent transactions: 0.17%
    - Legitimate transactions: 99.83%
6. The data is highly unbalanced, with a significant difference between class 0 and class 1.
    - Applied RandomOverSampler() technique to address the imbalance.
7. Neural Network Model
    - Model with 2 Hidden layers (units - 64, 32)
    - Compile the model with "Adam" optimizer and "binary_crossentropy" Loss
    - Trained the model for 100 epochs with a batch size of 32.
    - Visualise Training and Testing Error (loss), Training and Testing Accuracy
    - Made predictions using the model.
    - Evaluated the model using classification_report and confusion_matrix.
    - Achieved an accuracy percentage of 85.93%.
    - Visualize 'Correct Prediction' and 'Incorrect Prediction'
8. Dropout
    - Model with 3 Hidden layers (units - 128, 64, 32)
    - Compiled the model
    - Trained the model for 10 epochs with a batch size of 32.
    - ----- Performed the same steps till model evaluation -----
    - Achieved an accuracy percentage of 90.65%.
    - Visualize 'Correct Prediction' and 'Incorrect Prediction'
9. EarlyStopping
    - Model with 2 Hidden layers (units - 64, 32)
    - Compiled the model
    - Created callback with parameters (monitor, min_delta, patience, verbose)
    - Trained the model for 2000 epochs.
    - ----- Performed the same steps till model evaluation -----
    - Achieved an accuracy percentage of 88.16%.
    - Visualize 'Correct Prediction' and 'Incorrect Prediction'.
