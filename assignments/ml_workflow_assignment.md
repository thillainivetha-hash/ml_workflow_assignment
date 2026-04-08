# Problem Statement
- You are a junior data analyst at a retail company. Your manager hands you a dataset of past customer orders and asks you to build a model that predicts whether a customer will make a repeat purchase within 30 days.

- The dataset contains the following columns:

Column                	        Description
customer_id	Unique              customer identifier
order_count_last_90d	        Number of orders placed in the last 90 days
avg_order_value              	Average order value in INR
days_since_last_order       	Days elapsed since the customer's most recent order
repeat_purchase_flag	        1 if the customer made a repeat purchase within 30 days, 0 otherwise
discount_used_on_repeat_order	Discount applied on the repeat purchase order 


## Task 1
- Identify which column in the dataset is the label, and which column, if included as a feature, would introduce data leakage. For each, write one sentence justifying your choice.


## Task 1 answer

- **Label column:** `repeat_purchase_flag` — This is the target variable we want to predict, since it directly indicates whether a customer made a repeat purchase within 30 days.  

- **Data leakage column:** `discount_used_on_repeat_order` — Including this as a feature would introduce leakage because it reveals information that only becomes available after the repeat purchase , which is what the model is supposed to predict.


##  Task 2
- Your manager skips straight to training a gradient boosting model. Suggest two steps from the complete ML workflow that should have been completed first, and briefly explain why each step matters before jumping to a complex model.

## Task 2 answer
- **STEP 1 :**  Data Preperation and Feature engineering : Before training, the dataset should be examined for missing values, duplicates, and inconsistencies. This step ensures data quality and prevents misleading patterns that could harm model performance.
- **STEP 2 :**  Feature engineering:   Identifying relevant features and creating meaningful transformations is critical. It reduces noise, prevents overfitting, and ensures the model learns from variables that truly contribute to predicting the label.