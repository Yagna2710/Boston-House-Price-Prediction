# Boston-House-Price-Prediction
A machine learning project to predict Boston house prices using various regression models.
Introduction
The objective of this project is to design and implement a regression model to accurately predict Boston house prices using a dataset containing various attributes such as the number of rooms, crime rates, and other relevant factors. This project follows a structured approach involving data preprocessing, model selection, training, evaluation, and fine-tuning.
________________________________________
1. Data Preprocessing
The dataset was loaded and examined for missing values and outliers. The key steps taken include:
•	Handling Missing Values: Missing values were filled with the mean of the respective columns to maintain consistency across the dataset.
•	Outlier Detection and Removal: Outliers in the target variable ('MEDV') were identified and removed using the Interquartile Range (IQR) method to ensure a more reliable model.
•	Feature Engineering: A new feature 'LSTAT_SQ' (square of 'LSTAT') was created to enhance the model's predictive ability.
•	Feature Scaling: Data was scaled using StandardScaler to ensure uniformity across all features.
________________________________________
2. Model Selection & Training
Various regression models were evaluated to determine their predictive performance:
•	Linear Regression
•	Decision Tree Regressor
•	Gradient Boosting Regressor
•	Random Forest Regressor
________________________________________
3. Evaluation
The models were evaluated using Mean Squared Error (MSE) and R² Score. The results are summarized below:
Model	Mean Squared Error (MSE)	R² Score
Linear Regression	22.566	0.7263
Decision Tree Regressor	18.834	0.7631
Gradient Boosting Regressor	12.562	0.8476
Best Gradient Boosting (Tuned)	10.467	0.8694
Random Forest Regressor	11.758	0.8582
From the above results, it is evident that the Gradient Boosting Regressor (after hyperparameter tuning) performs the best with an MSE of 10.467 and an R² Score of 0.8694.
________________________________________
4. Fine-Tuning
The Gradient Boosting Regressor was fine-tuned using GridSearchCV with the following hyperparameters:
•	Number of Estimators: 100, 200, 300
•	Learning Rate: 0.01, 0.1, 0.2
•	Max Depth: 3, 4, 5
The best model was identified with:
•	Number of Estimators: 200
•	Learning Rate: 0.1
•	Max Depth: 4
________________________________________
5. Feature Importance
The feature importances were analyzed using the Random Forest model. The most significant features influencing house prices include:
•	RM (Average number of rooms per dwelling)
•	LSTAT (Percentage of lower status population)
•	PTRATIO (Pupil-teacher ratio by town)
These features were found to have the greatest impact on predicting the target variable ('MEDV').
________________________________________
6. Visualization
The model performance comparison was visualized using bar plots for MSE and R² Scores. It clearly shows that the Best Gradient Boosting Model achieved the highest performance metrics.
________________________________________
7. Real-World Applications
The developed models can be utilized by real estate agencies to predict house prices based on various features such as the number of rooms, crime rates, distance to employment centers, etc. This assists in:
•	Setting appropriate prices for properties.
•	Making informed decisions regarding property investments.
•	Developing pricing strategies for new real estate developments.
________________________________________
8. Conclusion
The Gradient Boosting Regressor proved to be the most effective model for predicting house prices, demonstrating strong performance after fine-tuning. This approach provides a robust solution for predictive analysis in the real estate domain, facilitating better decision-making and market analysis.                                 
 
