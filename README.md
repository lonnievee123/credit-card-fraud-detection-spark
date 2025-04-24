# Credit Card Fraud Detection (Spark Project)

This project uses PySpark and SparkML to find illegal credit card operations in the Databricks Community Edition.

## 🔧 Technologies
- Databricks Community Edition
- PySpark
- SparkSQL
- SparkML (Random Forest)

## 📁 Dataset
A public dataset containing anonymized transaction data, available [on Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).  
Features are transformed via PCA and include a `Class` column (1 = fraud, 0 = non-fraud).

## 📊 Project Flow

1. **Data Loading & Cleaning**   
- Use schema inference to read a CSV file 
- The label column was cast with integer 
- To get rid of any nulls

2. **Class Balancing**
   - Decrease the number of non-fraud transactions to balance with fraud transactions
   - Increase fraud cases in order to balance the dataset (using replacement)
   - Aggregate and stratify the split in the training and the testing set

3. **Feature Engineering**
   - Apply VectorAssembler to build the features column

4. **Modeling**
   - Train RandomForestClassifier
   - Evaluate with AUC (BinaryClassificationEvaluator)
   - Display prediction vs. actual breakdown

## 📈 Result
Achieved **AUC = 1.0** due to clean balancing and fraud separation.

## 📹 Video Presentation
View the entire 10-minute guide <!-- Replace this after upload --> ">☛YouTube Link

## 👤 Author
Alon Dorfman — the only person who developed the final group project
