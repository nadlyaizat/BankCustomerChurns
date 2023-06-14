# Bank Customer Churns
Analysis on the factors influencing customer churn in the banking industry.

## Bank Customer Data for Customer Churn

### Introduction

Churn, in the context of the banking industry, refers to the phenomenon where customers discontinue their relationship with a bank or financial institution. Understanding the factors that influence customer churn is crucial for banks to effectively retain their customers and develop strategies to minimize attrition.

The aim of this project is to analyze bank customer data and uncover the key factors that contribute to customer churn. By examining various attributes such as credit scores, account balances, and salaries, we can identify patterns and correlations that help us understand why customers decide to leave the bank.

### Hypothesis

Our hypothesis suggests that customers with lower credit scores, lower account balances, and lower salaries are more likely to churn from the bank. By exploring the dataset and conducting statistical analyses, we aim to validate or refute this hypothesis, gaining insights into the factors that play a significant role in customer churn.

### Acknowledgements

It is widely recognized that acquiring new customers is considerably more expensive than retaining existing ones. For this reason, it is advantageous for banks to proactively identify the reasons behind customer churn and take appropriate measures to mitigate it. By preventing churn, banks can allocate resources towards developing loyalty programs and retention campaigns that aim to retain as many customers as possible.

This project leverages bank customer data to contribute to the understanding of customer churn in the banking industry, ultimately providing valuable insights for banks and financial institutions in their efforts to improve customer retention strategies.

## Analysis on Factors Influencing Customer Churn in the Banking Industry

In this section, we will explore the factors that influence customer churn in the banking industry. Our aim is to understand the relationship between various factors and customer churn. We start by stating our hypothesis that customers with lower credit scores, lower account balances, and lower salaries are more likely to churn from the bank.

### Dataset and Data Exploration

To begin our analysis, we import the necessary libraries and load the dataset. The dataset contains information about bank customers, including their demographic details, account balances, credit scores, and churn status. After loading the dataset, we explore its structure and drop irrelevant columns.

Next, we preprocess the data by checking for missing values and converting categorical variables to numerical ones using one-hot encoding. This prepares the dataset for further analysis.

### Exploratory Data Analysis

We perform exploratory data analysis to gain insights into the relationship between different variables and customer churn. We start by visualizing the distribution of the target variable, which indicates the number of customers who have churned and those who have not.

![image](https://github.com/nadlyaizat/BankCustomerChurns/assets/127640970/26a517b9-9862-4388-9812-5781a8e3052a)

Interpreting the plot:
- 0: Represents customers who have not left the bank.
- 1: Represents customers who have left the bank.

From the countplot, we observe the distribution of churned and non-churned customers.

We then proceed to visualize the correlation matrix to understand the relationships between different features. The correlation matrix helps us identify any significant correlations between variables.

![image](https://github.com/nadlyaizat/BankCustomerChurns/assets/127640970/e150baec-da6c-4d54-8dde-fdcf559d2013)

Interpreting the heatmap:
- Color: The color scale represents the correlation coefficient, ranging from negative correlation (blue) to positive correlation (red). Darker shades indicate stronger correlations.
- Annotations: Numerical values displayed in each square represent the correlation coefficient. Positive values indicate positive correlation, negative values indicate negative correlation, and values close to zero indicate weak or no correlation.

The heatmap reveals the correlations between features such as credit score, balance, estimated salary, and churn.

Additionally, we investigate the relationship between features (credit score, balance, and estimated salary) and churn using box plots.

![image](https://github.com/nadlyaizat/BankCustomerChurns/assets/127640970/8d82761e-99e2-45f5-a1f9-7981a642d02a)

![image](https://github.com/nadlyaizat/BankCustomerChurns/assets/127640970/cfc75ea0-c63c-4d91-b010-b66dd92d32e4)

![image](https://github.com/nadlyaizat/BankCustomerChurns/assets/127640970/33079d41-8b63-4b39-afec-5930b84cb9f1)

Interpreting the box plots:
- Credit Score: Customers who left the bank tend to have slightly lower credit scores compared to those who stayed.
- Balance: Customers who left the bank tend to have slightly higher median account balances compared to those who stayed.
- Estimated Salary: There is no significant difference in estimated salaries between customers who left and those who stayed.

Based on these observations, it appears that account balance plays a role in customers' decisions to leave or stay with the bank. Customers who left had slightly higher median balances, while those who stayed had a wider range of balances. This is further confirmed by the correlation coefficient in the heatmap, which shows the highest correlation between churn and account balance.

### Building a Predictive Model

Next, we split the data into training and testing sets to build and evaluate a predictive model. We use logistic regression as our modeling technique to predict customer churn based on the selected features.

After training the model, we make predictions on the test set and evaluate its performance using various metrics such as accuracy, precision, recall, and F1-score.

### Interpretation of Results

To interpret the logistic regression model's results, we extract the coefficients associated with each feature. The coefficients provide insights into how each factor contributes to the likelihood of churn.

From the coefficients, we observe the following:
- Credit Score: Customers with lower credit scores are more likely to leave the bank.
- Balance: Customers with higher account balances are less likely to leave.
- Salary: Customers with lower salaries are more likely to leave.

These findings align with our initial hypothesis and suggest that credit score, account balance, and salary indeed have an impact
on customer churn.

### Additional Result Interpretations

In addition to the main factors, we also consider other features' coefficients related to customer demographics and card types. These coefficients indicate the influence of factors such as age, tenure, number of products, customer satisfaction, country (geography), gender, and card type on customer churn.

Based on these coefficients, we find that:
- Older customers and those with longer tenure are less likely to leave the bank.
- Customers with higher account balances, more products, and active membership are less likely to churn.
- Higher customer satisfaction scores and point earnings decrease the likelihood of churn.
- Customers who have registered a complaint are more likely to leave the bank.
- Geography-wise, customers from Germany are more likely to churn compared to other countries, while customers from Spain are less likely to churn.
- Male customers have a slightly higher likelihood of churn compared to female customers.
- Customers with gold or platinum cards are less likely to leave, while those with silver cards are slightly more likely to churn.

These coefficients help us understand the importance and direction of each factor in predicting customer churn. By analyzing them, we can identify which factors have the strongest impact on whether a customer will leave the bank or not, guiding the bank's strategies to retain customers.

## Conclusion

In conclusion, our analysis aimed to understand the factors influencing customer churn in the banking industry, specifically focusing on the hypothesis that customers with lower credit scores, lower account balances, and lower salaries are more likely to churn from the bank.

Our findings indicate that credit score, account balance, and salary do indeed play a role in customer churn. Customers with lower credit scores, lower account balances, and lower salaries are more likely to leave the bank. Additionally, other factors such as age, tenure, number of products, customer satisfaction, geography, gender, and card type also influence customer churn to varying degrees.

These insights can assist banks in developing targeted strategies to retain customers and implement loyalty programs that address specific factors associated with churn. By understanding the factors that influence customer churn, banks can work towards improving customer retention and overall business success.
