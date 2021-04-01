Credit Card Defaulting Potential

This default detection problem involves modeling past credit card loans with the knowledge of the ones that were defaulted on. The purpose of this project is to identify the variables that are indicators of potential default. Using this dataset, I will develop a predictive model that determines the likelihood of payment issues based on the features most correlated with defaulting. Do all borrowers share common features associated with default? Do borrowers with payment issues have red flags exclusive to them? The end goal is to use a robust model as part of a risk assessment before potential customers are sanctioned a loan from a financial institution. 

The Data

There are over 30,000 rows and 122 columns. The features include loan type, income total credit amount, and other various socioeconomic questions.

https://www.kaggle.com/mishra5001/credit-card


Method

Models and Metrics:

This classification problem required a few tweaks to both the models and the metrics. The models built are as follows:

Support Vector Machine 
Random Forest
Logistic Regression
K_Neighbors Classifier
Decision Tree Classifier

Accuracy was a misleading measure of success due to the imbalanced data. In this situation, precision, recall, and f1 score are a better metric as explained in the results section.

Imblanced Data:

Borrowers that didn't default outnumbered the ones that did by a big margin. To generate more samples of the minority class, SMOTE and oversampling techniques were used to randomly generate minority (default) samples for the model to learn the decision boundaries.

Data Cleaning

Missing values were imputed. Columns with over 10% null values were dropped. Dates were converted to useable formats. I binned some variables such as age and income range.

EDA

Here are a few of the relationships I visualized:

![image](https://user-images.githubusercontent.com/72377927/113348499-457a7800-92fc-11eb-9126-c7e2387b2ca5.png)


![image](https://user-images.githubusercontent.com/72377927/113348420-2b409a00-92fc-11eb-8739-83f993f5961e.png)


Machine Learning:

Precision, recall and the f1 score are better indicators of performance than accuracy. While using oversampling and SMOTE to randomly increase instances of the minority class imporved metrics for the logistic regression, K-neighbors, and the decision tree models, the best model in this case is the SVM model. The SVM model gave the best scores and also provided instances of TP, FP, TN, and FN. A model that doesn't predict false positives or true positives is not very useful!

![image](https://user-images.githubusercontent.com/72377927/113348971-f254f500-92fc-11eb-96dd-24f40ecf2509.png)



