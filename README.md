🏠 Home Loan Default Prediction
____________________________________
This project focuses on predicting whether a home loan applicant will default on their loan. The primary challenge was handling a highly imbalanced dataset and integrating information from 7 different sources to build a reliable risk assessment model.

🚀 Project Overview
_________________________________
- Objective: Identify potential defaulters to minimize financial loss for the bank.

- Key Challenge: Only ~8% of the data represented defaulters, making it an "Imbalanced Classification" problem.

- The Journey: From merging 7 complex files to tuning advanced XGBoost models.

🛠️ Step 1: Data Integration (Merging 7 CSVs)
_______________________________________________
- The data was spread across 7 different files (like application_train, bureau, previous_application, etc.).

- Process: Linked all files using unique identifiers (like SK_ID_CURR).

- Result: Created a single comprehensive master dataset containing the complete history of applicants.

🧹 Step 2: Data Cleaning & Preprocessing
______________________________________________
- Null Values: Handled a massive amount of missing data using strategic imputation (filling values based on column type).

- Scaling: Applied Min-Max Scaling to ensure all numerical features are on the same scale for the algorithms.

- Categorical Encoding: Converted text data into numbers so the models could understand them.

📊 Step 3: EDA & Insights (Graphs)
__________________________________________
- We used Matplotlib and Seaborn to visualize the data:

- Class Imbalance: Bar charts showed the extreme gap between "Repayers" and "Defaulters."

- Correlation Heatmaps: Identified which features (like Income, Age, or Credit Amount) had the strongest connection to loan default.

- Distribution Plots: Analyzed how different age groups or income levels behave regarding defaults.

🤖 Step 4: Model Building & Handling Imbalance
_________________________________________________

- We compared multiple models to see which one handles risk the best:

- Logistic Regression: Our baseline (High accuracy, but missed almost all defaulters).

- Decision Tree & Random Forest: Better, but struggled with the minority class.

- The Solution: Used XGBoost with scale_pos_weight to give more importance to the defaulters.

📈 Step 5: Optimization & Final Result
_________________________________________
- Hyperparameter Tuning: Tuned learning_rate and max_depth to prevent overfitting.

- Threshold Adjustment: Changed the classification threshold to 0.656 to reach the best balance between Recall and Precision.

- Final Performance: Successfully increased the model's ability to catch defaulters by 14 times compared to the baseline model.

🛠️ Tech Stack Used
____________________
- Language: Python

- Libraries: Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn

- Environment: Jupyter Notebook

🏁 Conclusion
_____________________
- The final Weighted XGBoost Model is highly effective at identifying high-risk home loan applications, providing a powerful tool for the bank's risk management team.

AUTHOR :- SHUDHANSHU RANJAN
