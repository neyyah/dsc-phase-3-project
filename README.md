
![magnet customers](https://github.com/neyyah/dsc-phase-3-project/assets/151524110/27d96704-cfca-4d2c-b5d7-713038850b2e)

## PROJECT OVERVIEW

The project's aim is to develop a machine learning model to predict customer churn for SyriaTel, a telecommunications company. The dataset includes various features such as customer service calls, total day charge, and total day minutes. The objective is to create a model that will accurately identify customers who are likely to churn, allowing the company to implement targeted retention strategies.

## BUSINESS UNDERSTANDING
The project focuses on predicting customer churn for SyriaTel, a telecommunications company. Churn prediction is crucial for telecom companies as retaining customers is significantly cheaper than acquiring new ones. Identifying customers who are likely to churn allows the company to implement proactive retention strategies, such as offering discounts or personalized services, to reduce churn rates and maintain revenue.Stakeholders within the telecommunications industry, including marketing and sales teams, customer service departments, and SyriaTel telcom company, stand to benefit substantially from the outcomes of the project

## DATA UNDERSTANDING
The dataset originates from SyriaTel Telecommunication company and was obtained from Kaggle [here](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset). It comprises 21 columns and 3333 rows. The columns have various attributes related to customer demographics, service usage, and churn behavior. The rows correspond to a recorded customer. The dataset encompasses both continuous and categorical variables. The target variable identified is "churn," with the remaining variables serving as predictors.

## DATA PREPARATION
In this stage, data is cleaned,transformed, and preprocessed to make it suitable for analysis. 

### Data Cleaning and Inspection:

The SyriaTel dataset underwent an initial inspection which revealed that it was clean, requiring no further cleaning steps.

### Exploratory Data Analysis (EDA):

- During EDA, thorough analyses were conducted on both feature and categorical data to gain insights into the dataset's composition.
- Correlation analyses were performed to identify relationships between features and the churn variable, highlighting significant correlations with customer service calls, total day minutes, and total day charge.
- Outliers were detected during the EDA process, although they were retained due to their potential importance in the analysis.

### Data Preprocessing:

- Categorical data underwent encoding to convert them into a numerical format suitable for analysis.
- Numeric features were scaled to standardize their values, ensuring consistency across the dataset.
- The dataset was split into training and testing sets to facilitate model training and evaluation.
- To address class imbalance, Synthetic Minority Over-sampling Technique (SMOTE) was applied to the dataset, ensuring a more balanced representation of both churn and non-churn instances in the training data.

## MODELING
Four models were employed in the analysis: Logistic Regression, Decision Tree, Random Forest, and XGBoost. Here are the results for each model:

### Logistic Regression:

- Precision: The model correctly identified 39% of predicted churn cases out of all positive predictions.
- Recall: It captured 77% of actual churn cases, highlighting its ability to identify churn instances.
- Accuracy: Overall accuracy was 78%, meaning it correctly predicted 78% of instances in the test set.

### Decision Tree:

- Precision: For class 0 (no churn), precision was 96%, while for class 1 (churn), it was 64%.
- Recall: It achieved a recall of 92% for class 0 and 78% for class 1.
- Accuracy: Overall accuracy was 90%.

### Random Forest:

- Precision: Precision for class 0 remained at 96%, while for class 1, it improved from 64% to 85%.
- Recall: Recall for class 0 improved from 92% to 98%, indicating better identification of non-churn cases. Recall for class 1 remained stable at 79%.
- Accuracy: Accuracy increased from 90% to 95%

### XGBoost:

- Precision: Precision for class 0 remained at 96%, while for class 1, it improved from 85% to 89%.
- Recall: Recall for class 0 remained the same at 98%, while for class 1, it was relatively stable at 79%.
- Accuracy: Accuracy remained the same at 95%.
- To enhance performance, model tuning was considered.

### Hyperparameter Tuning
Hyperparameter tuning was performed using GridSearchCV to optimize the Random Forest model and XGBoost Model.

### Random Forest(Tuned)
- Precision for class 0 (non-churn) was 0.97, and for class 1 (churn) it was 0.84.
- Recall for class 0 was 0.97, and for class 1 it was 0.82.
- ROC AUC: The area under the ROC curve (ROC AUC) is 0.94, which represents the model's ability to distinguish between positive and negative classes.

### XGBoost(Tuned)
- Precision of 0.97 for non-churn customers (class 0) and 0.85 for churn customers (class 1).
- Recall scores of 0.98 for class 0 and 0.80 for class 1.
- Overall accuracy stood at 0.95.

### EVALUATION
- ROC AUC curves were plotted to assess model performance.
- Random Forest and XGBoost achieved an AUC of 0.93indicating good performance
- Logistic Regression had an AUC of 0.836, while Decision Tree achieved 0.852.
- After tuning , Random Forest performed the best, achieving a recall of 82%, surpassing the 80% target set for the model and an AUC of 0.94.
- XGBoost achieved a recall of 80% and an overall accuracy of 95%.

From the dataset,the top  features are:
- Customer service calls
- Total day charge
- Total day minutes
- Total eve minutes

## CONCLUSION
- Customers who made three calls to customer service exhibited the lowest churn rate, suggesting that this level of interaction may indicate satisfaction or issue resolution.
- Conversely, as the number of customer service calls increases, churn rates tend to rise, indicating potential dissatisfaction or unresolved issues.
- Churned customers tend to have higher average total day minutes of approximately 206.91 compared to non-churned customers, implying that customers with higher daytime usage are more likely to churn.
- Similarly, churned customers exhibit a higher average total day charge of around 35.81 compared to non-churned customers, suggesting that customers with higher charges for daytime usage are more likely to churn.
- Customers with internation plan have lower churn rate
- The tuned Random Forest model demonstrated the best performance, exceeding the target recall of 80%.

## RECOMMENDATIONS
To enhance customer retention at SyriaTel, it's crucial to integrate the machine learning model for real-time predictions. Continuous real-time monitoring ensures that the model continuously learns and enhances its accuracy over time. By utilizing feature importance, valuable insights can be derived to identify areas for service enhancements and personalize retention initiatives.

- Implement loyalty programs to reward frequent users or incentives to high-usage customers to improve retention and reduce churn among this segment.
- Implement proactive customer service strategies by Using surveys, reviews, and feedback forms to understand customer satisfaction and areas for improvement, particularly for customers who have made multiple calls to customer service.
- Company should look into the call charge rates in comparison to the competitors, and consider if they should lower the charges of calls per minute. This can prevent other customers from churning.
- Improve the features with lower importance but still relevant to reduce churn. These features may have potential for improvement or further analysis.
- SyriaTel should encourage its customers to take up international plan as the customers within international plan have low churn rate.
- Utilize the tuned Random Forest model to predict and mitigate churn effectively.




























