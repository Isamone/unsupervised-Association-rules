Project Objective
The goal of this project is to analyze the Customer Purchases History dataset (provided by Kaggle) in order to discover association rules that can help supermarket owners develop better marketing strategies and improve overall sales.

📦 Dataset Overview
Name: Customer Purchases History

Source: Kaggle

Structure: Each row represents a customer's purchase history (i.e., items bought together in a single transaction).

Toy Example:

python
Copy
Edit
toy_dataset = [
    ['Skirt', 'Sneakers', 'Scarf', 'Pants', 'Hat'],
    ['Sunglasses', 'Skirt', 'Sneakers', 'Pants', 'Hat'],
    ['Dress', 'Sandals', 'Scarf', 'Pants', 'Heels'],
    ['Dress', 'Necklace', 'Earrings', 'Scarf', 'Hat', 'Heels'],
    ['Earrings', 'Skirt', 'Scarf', 'Shirt', 'Pants']
]
Dataset Link: 🔗 Download Dataset

🧾 Instructions & Pipeline
🔹 1. Import Data and Perform Basic Exploration
Load the dataset using pandas.

Inspect basic structure: shape, data types, and sample rows.

Generate summary statistics.

🔹 2. Data Preparation
Handle missing or corrupted values

Remove duplicates (e.g., repeated items in the same transaction)

Encode categorical features if needed (for models like SVM)

Handle outliers (not always applicable in market basket data)

Transaction Encoding: Convert transactions to one-hot encoded format (for association rule mining or modeling)

🔹 3. Association Rule Mining
Apply Apriori algorithm to extract frequent itemsets.

Use mlxtend.frequent_patterns.apriori and association_rules.

Calculate:

Support: How often an itemset appears.

Confidence: How often the rule has been true.

Lift: Strength of association.

🔹 4. SVM Classification (if applicable)
If you introduce a target variable (e.g., high vs low basket value), you can:

Split dataset using train_test_split

Train an SVM classifier using sklearn.svm.SVC

Evaluate using:

Accuracy

Confusion Matrix

Precision/Recall/F1 Score

📊 Evaluation & Visualization
Plot frequent itemsets using bar plots.

Visualize association rules using network graphs or heatmaps (lift vs confidence).

If SVM applied: plot decision boundaries (if using 2D features).

