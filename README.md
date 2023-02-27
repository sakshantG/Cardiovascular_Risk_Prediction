# Cardiovascular_Risk_Prediction
image![download](https://user-images.githubusercontent.com/120353105/218255280-da544c53-4a9c-44a8-a2b5-357211133d42.png)


# 1.INTRODUCTION:
Heart disease is the major cause of morbidity and mortality globally: it accounts for more deaths annually than any other cause. According to the WHO, an estimated 17.9 million people died from heart disease in 2016, representing 31% of all global deaths. Over three quarters of these deaths took place in low- and middle-income countries. Of all heart diseases, coronary heart disease (aka heart attack) is by far the most common and the most fatal. In the United States, for example, it is estimated that someone has a heart attack every 40 seconds and about 805,000 Americans have a heart attack every year (CDC 2019). Doctors and scientists alike have turned to machine learning (ML) techniques to develop screening tools and this is because of their superiority in pattern recognition and classification as compared to other traditional statistical approaches. In this project, I’ve built a model for predicting whether a patient has a 10-year risk of developing coronary heart disease(CHD) using different Machine Learning techniques on the Framingham, Massachusetts town dataset.

# 2.Problem Statement
The objective of the project is to come up with the machine learning model to predict whether a patient has 10-year risk of developing coronary heart disease (CHD) using the residents of the town of Framingham, Massachusetts dataset.

# 3.DATA SUMMARY
The data set is publicly available on the Kaggle website, and it is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has 10-year risk of future coronary heart disease (CHD). The data set provides the patients’ information. It includes over 4,000 records and 15 attributes. Each attribute is a potential risk factor. There are both demographic, behavioral and medical risk factors.

# Attributes:
## Demographic:

Sex: male or female("M" or "F")

Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous) Behavioral

is_smoking: whether or not the patient is a current smoker ("YES" or "NO")

Cigs Per Day: the number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarettes, even half a cigarette.)

## Medical( history)

BP Meds: whether or not the patient was on blood pressure medication (Nominal)
Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)
Prevalent Hyp: whether or not the patient was hypertensive (Nominal)
Diabetes: whether or not the patient had diabetes (Nominal)

## Medical(current)

Tot Chol: total cholesterol level (Continuous)
Sys BP: systolic blood pressure (Continuous)
Dia BP: diastolic blood pressure (Continuous)
BMI: Body Mass Index (Continuous)
Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though in fact discrete, yet are considered continuous because of large number of possible values.)
Glucose: glucose level (Continuous)
Predict variable (desired target)

10 year risk of developing coronary heart disease (CHD) — (binary: “1”, means “There is a risk”, “0” means “There is no risk”).

## 4.TOOL DEVELOPMENT
The full code for this article can be found here in github repository. It is implemented in Python and different classification algorithms are used. Below is a brief description of the general approach that I employed:

**Data cleaning and preprocessing** : Here I checked and dealt with missing and duplicate variables from the data set as these can grossly affect the performance of different machine learning algorithms (many algorithms do not tolerate missing data).

**Exploratory Data Analysis** : Here I wanted to gain important statistical insights from the data and the things that I checked for were the distributions of the different attributes, correlations of the attributes with each other and the target variable and I calculated important odds and proportions for the categorical attributes.

**Feature Selection**: Since having irrelevant features in a data set can decrease the accuracy of the models applied, I used Tree-based: SelectFromModel which is an embedded method that uses algorithms that have built-in feature selection methods which were later used to build different models.

**Model development and comparison** : I used four classification models, i.e., Logistic Regression, K-Nearest Neighbors, Decision Trees and Support Vector Machine, After which I compared the performance of the models using their accuracy and F1 scores. I then settled with the best performing model.

After training each model and tuning their hyper-parameters using grid search, I evaluated and compared their performance using the following metrics:

**The accuracy score** : which is the ratio of the number of correct predictions to the total number of input samples. It measures the tendency of an algorithm to classify data correctly.

**The F1 Score** : Which is defined as the weighted harmonic mean of the test’s precision and recall. By using both precision and recall it gives a more realistic measure of a test’s performance. (Precision, also called the positive predictive value, is the proportion of positive results that truly are positive. Recall, also called sensitivity, is the ability of a test to correctly identify positive results to get the true positive rate).

**The Area under the ROC Curve (AUC)** : Which provides an aggregate measure of performance across all possible classification thresholds. It gives the probability that the model ranks a random positive example more highly than a random negative example.

## 4.CONCLUSION

* Cardiovascular disease is a major public health problem in our country(India), often impacting the most productive years of an individual’s life. Therefore, predicting the disease before becoming infected decreases the risk of death. **This prediction is an area that is widely researched. We tried six classification modeling techniques on a real data set of residents of the town of Framingham. 
* We evaluated models using evaluation metrics and compared their performances of models so as to get the best performing model. Results showed that the **Gradient Boosting** model has the **best accuracy of 88%**, whereas Logistic regression being the least accurate model. 
* We also used ROC curve analysis to evaluate models and found that again **Gradient Boosting model has best auc score of 0.951** which is pretty good. 
* The GradientBoostingClassifier is found to be the best model. Therefore, the **Gradient Boosting model can be used to predict risk of CHD**. 
* Variable importance analysis showed that age, systolic BP, total cholesterol and glucose(diabetes) are the most influential features to predict whether the patient has a 10-year risk of future coronary heart disease. 

