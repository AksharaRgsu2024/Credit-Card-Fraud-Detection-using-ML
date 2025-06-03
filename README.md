<p> This project aims to build a machine learning model capable of accurately detecting
fraudulent credit card transactions. By leveraging historical transaction data, we apply
advanced preprocessing, feature engineering, and robust modeling techniques to classify
transactions as legitimate or fraudulent. </p>

<b> Dataset Overview </b>
<p> The dataset is got from the public kaggle dataset: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud </p>

Total Records: 284,807 transactions

Features: 31 columns, including:
- 28 PCA-transformed features (V1–V28)
- Amout
- Time
- Class

<p> The dataset is highly imbalanced, with 9983% of the transactions being legitimate, and only 0.17% are fraudulent. </p>

<b> Feature Engineering and Selection</b>
<p> The cumulative variance plot is used to select the top features contributing to 95% of the explained variance. From the plot, the optimal number of PCA features is 22.
Totally, 24 features are selected, including 'Amount' and 'Time'. </p>

<p> The hour of the day is extracted from 'Time' feature, to include cyclical time patterns in fraudulent transactions. </p> 

<b> Model Development and Testing </b>
- Resampling: Undersampling legitimate class, Oversampling fraud class with SMOTE
- Models: Random Forest, XGBoost, Gradient Boosting

<p> The Final model which gave best performance was SMOTE + Random Forest. It had highest accuracy (0.99) with balanced recall and precision.
The Recall of fraud class is 0.88 and precision of fraud class is 0.86. The Area under the Precision Recall curve (AUC) is 0.89. </p>

