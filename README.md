# Maternal Health Risk Classification
An analysis of maternal risk in a developing country, Bangladesh.


## Research Question:
How can machine learning methods improve the accuracy and efficiency of maternal health risk classification during pregnancy?


## Why It’s Interesting:

According to the World Health Organization (WHO), about 810 pregnant women and 6,700 newborns die every day (WHO, 2019, 2020). Despite advancements in medical care, many maternal deaths remain preventable, especially in developing countries. 

Maternal health is a crucial aspect of public health, and accurately identifying high-risk pregnancies can significantly reduce maternal and infant mortality. Maternal risk is the likelihood of a woman experiencing adverse health outcomes during pregnancy or childbirth (Togunwa, Babatunde, Abdullah, 2023).

Deep learning-based models offer a data-driven method to classify maternal health risks with high accuracy, aiding healthcare professionals in early intervention.


## Conclusions:

Our best performing model found that systolic blood pressure (an indication of gestational diabetes), blood sugar, and body temperature were important feature contributions to maternal health risk, aligning with medical understanding.


## Dataset:

Source: UCI Machine Learning Repository
Origin: IoT monitoring systems in rural Bangladesh

The maternal health risk dataset that we are using is from the UCI machine learning repository and was collected from different hospitals, community clinics, and maternal health care centers from rural areas of Bangladesh through an IoT risk monitoring system. There are six predictor variables: age, systolic blood pressure, diastolic blood pressure, blood sugar, body temperature, and heart rate. The target variable is risk level, ranging from low, mid, and high risk. 

Other risk factors can include having given birth before, history of disorder during pregnancy, and miscarriage, which are not contained in our analysis (Raza, Siddiqui, Munir, et al 2022). 

Size:
1017 Samples, 7 features 

Variables:
Features: Age, SystolicBP, DiastolicBP, Blood Sugar, Body Temp, Heart Rate
Target: RiskLevel (Low, Mid, High)

<img width="557" alt="image" src="https://github.com/user-attachments/assets/680bf83a-2296-4cb3-8e21-0567be0c87ea" />


### Risk Level Distribution

We had an imbalanced dataset, with most of our samples being low risk patients. We corrected for this using SMOTE (synthetic minority oversampling technique).

<img width="852" alt="Screenshot 2025-04-03 at 7 20 30 PM" src="https://github.com/user-attachments/assets/899ba6b3-f2ae-45ca-bcdd-dd0d3086bae3" />


### Feature Importance

When analyzing the model, we found that SystolicBP and Blood Sugar are the top contributors.
These align with medical understanding such as blood pressure and glucose are key indicators of maternal risk.
The model's interpretability helps reinforce trust and usability in healthcare settings.

<img width="540" alt="Screenshot 2025-05-01 at 5 17 47 AM" src="https://github.com/user-attachments/assets/fa9cf020-6d45-45b3-8cfd-2361ecfe7117" />


### Algorithms

We used several algorithms, including random forest and neural networks.

<img width="828" alt="Screenshot 2025-04-03 at 7 20 45 PM" src="https://github.com/user-attachments/assets/819ee15a-9213-448b-bafe-bd184793b6e0" />

### Model Results

The logistic regression model gave us a training and test accuracy off 67% and a test accuracy of 64%.
The SVC model had a training accuracy of 74% and test accuracy of 69%. 
The random forest model performed very well on the training data with 80% accuracy and 76% on test.
The artificial neural network performed the most balanced, with a training accuracy of 73% and a test accuracy of 72%.

<img width="385" alt="Screenshot 2025-05-01 at 5 17 58 AM" src="https://github.com/user-attachments/assets/685e4bab-4df2-4c01-8071-8f8c38e4aaa2" />


