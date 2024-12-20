# Homesite-Insurance-Quote-Conversion

# Overview

Before asking someone out or attempting skydiving, it’s wise to gauge your chances of success. Similarly, quoting home insurance prices to potential customers requires a good prediction of conversion likelihood. Homesite, a top provider of homeowners insurance, currently lacks a dynamic model to predict whether a quoted price will lead to a purchase.
With anonymized data on customer behavior, sales activity, property details, and coverage information, Homesite aims to predict which customers are likely to purchase a given quote. Accurate predictions would enable Homesite to assess the effects of pricing adjustments and maintain a well-balanced customer portfolio.

# Key Features
1.	Data Preprocessing:
	•	Managed class imbalance using SMOTE, balancing the dataset.
	•	Scaled features with StandardScaler to improve model convergence.
	•	Split the data into training, validation, and test sets for evaluation.
2.	Model Development:
	•	Implemented five classifiers:
	•	Multilayer Perceptron (MLP)
	•	Support Vector Machine (SVM)
	•	Decision Tree
	•	Random Forest
	•	K-Nearest Neighbors (KNN)
	•	Evaluated models on metrics such as accuracy, F1-score, and AUC.
3.	Stacking and Hyperparameter Tuning:
	•	Built a one-layer stacking model combining predictions from all classifiers.
	•	Used RandomizedSearchCV for tuning hyperparameters of the stacked model’s final estimator.
	•	Compared base models and stacking performance on validation data.
4.	Kaggle Submission:
	•	Predictions were aligned with test data for submission.
	•	Submitted the stacked model’s output to Kaggle.

# Technologies Used
1.	Programming Language:
	•	Python
2.	Libraries:
	•	Data Handling: pandas, numpy
	•	Preprocessing: StandardScaler, SMOTE
	•	Modeling: MLPClassifier, SVC, DecisionTreeClassifier, RandomForestClassifier, KNeighborsClassifier, StackingClassifier
	•	Evaluation: classification_report, roc_auc_score
	•	Hyperparameter Tuning: RandomizedSearchCV

# Datasets
https://www.kaggle.com/c/homesite-quote-conversion/data


# Key Insights
1.	SMOTE for Class Imbalance:
	•	SMOTE successfully balanced the minority class and improved performance on minority class predictions.
2.	Model Evaluation:
	•	Best-performing base models:
	•	MLP achieved the highest accuracy (87%).
	•	Random Forest had the best AUC (93.92%).
	•	KNN and SGDClassifier showed relatively poor performance on the dataset.
3.	Stacking Model:
	•	The stacked model demonstrated robust performance by combining the strengths of individual classifiers.
	•	Achieved an accuracy of 82.50% and an AUC of 39.84% on the validation set.
4.	Hyperparameter Tuning:
	•	RandomizedSearchCV efficiently improved the stacked model’s final estimator.
5.	Kaggle Submission:
	•	Predictions were generated and saved in a Kaggle-compatible format.


