# 🫀 Heart Disease Risk Analysis

Heart disease remains one of the leading causes of death globally. his project explores patterns and associations among lifestyle factors and health metrics to understand their role in heart disease risk and uncover insightful trends. While correlation does not imply causation, the findings highlight how certain factors interact, paving the way for early intervention and public education on heart health.

## Using real-world datasets from:

1) [The Behavioral Risk Factor Surveillance System (BRFSS), futher operated by the Center for Disease Control (CDC) & The World Health Organization (WHO)](https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset?select=CVD_cleaned.csv).
   
2) [University of California at Irvine (UCI) Machine Learning Repository (Cleveland’s Database)](https://archive.ics.uci.edu/dataset/45/heart+disease).

# Dataset 1 (BRFSS): 

This dataset includes a lot of variables that seem to play a critical role in influencing the development of CVD. These include various factors such as general health, checkup frequency, BMI, physical activity, presence of other disease or mental health disorders, smoking history, alcohol consumption, and other dietary variables, including even demographic variables such as age, height, and gender.

## 🧹 Data Cleaning & Preprocessing

The BRFSS dataset was cleaned and preprocessed using R with the following steps:

• **Diabetes Reclassification:** Simplified the "Diabetes" column to "Yes" or "No."

• **Patient Indexing:** Added "Patient_ID" for consistent tracking.

• **Binary Conversion:** Recoded binary variables (Yes/No) to numerical (1/0).

• **Standardized Consumption:** Converted all intake values to a monthly scale.

• **Categorical Factors** Recoded variables like "General_Health" and "Age_Category" as ordered factors.

• **BMI Categorization:** Grouped BMI into categories: Underweight, Normal, Overweight, and Obesity.

## 🔍 Correlation Insights

• BMI & Weight: Strong positive correlation (0.86), as expected, with both showing weak positive correlations with heart disease.

• Age & Heart Disease: Moderate positive correlation (0.23), indicating an increased likelihood of heart disease with age.

• Age & Other Conditions: Positive correlations with arthritis (0.37), other cancer (0.20), and diabetes (0.17), common in older individuals.

• Checkups & Health: Regular checkups correlate positively (0.16) with better general health.

• General Health & Heart Disease: Moderate negative correlation (-0.26), suggesting poorer health is linked to higher heart disease risk.

• Exercise & Heart Disease: Negative correlation (-0.10), indicating regular exercise may reduce heart disease risk.

![Heatmap](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/cc08e03629559f8ceed576c10726fd19d96f1570/BRFSS%20Tableau%20Visuals/Correlation%20to%20Target%20Variable.png)

## Below are some of the most important visuals created using Tableau that helped me derive valuable insights:

• **Age & Heart Disease Risk:**

![image1](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/90bdfa408d01ee0b1e04790c5c551366c3a6f82e/BRFSS%20Tableau%20Visuals/Age%20%26%20Heart%20Disease.png)


• **Age & Other Chronic Diseases Risk:**

![image2](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/90bdfa408d01ee0b1e04790c5c551366c3a6f82e/BRFSS%20Tableau%20Visuals/Other%20Chronic%20Diseases%20%26%20Age.png)


• **Smoking In Relation to Age  & Heart Disease Risk:**

![image3](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/90bdfa408d01ee0b1e04790c5c551366c3a6f82e/BRFSS%20Tableau%20Visuals/Smoking%20in%20relation%20to%20Age%20%26%20Heart%20Disease%20.png)


• **BMI & Heart Disease Risk:**

![image4](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/90bdfa408d01ee0b1e04790c5c551366c3a6f82e/BRFSS%20Tableau%20Visuals/BMI%20%26%20Heart%20Disease.png)


• **BMI In Relation to Diabetes & Age:**

![image5](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/90bdfa408d01ee0b1e04790c5c551366c3a6f82e/BRFSS%20Tableau%20Visuals/Diabetes%20in%20relation%20to%20Age%20%26%20BMI.png)


• **Fried Food Consumption in Relation to BMI & Heart Disease:**

![image6](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/659cbdb2b4016b335d084ec40ee8514244303cd8/BRFSS%20Tableau%20Visuals/Fried%20Food%20%26%20BMI%20in%20relation%20to%20Heart%20Disease.png)


• **Alcohol Consumption in Relation to Gender, Age & Heart Disease Risk:**

![image7](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/90bdfa408d01ee0b1e04790c5c551366c3a6f82e/BRFSS%20Tableau%20Visuals/Alcohol%20%26%20Heart%20Disease.png)


• **Exercise In Relation to Age  & Heart Disease Risk:**

![image8](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/90bdfa408d01ee0b1e04790c5c551366c3a6f82e/BRFSS%20Tableau%20Visuals/Exercise%20%26%20Heart%20Disease.png)

## 📈 Statistical Significance Analysis

• **Chi-Square Test:** Found significant associations between heart disease and variables like age, general health, exercise habits, smoking history, and gender based on p-values.

• **ANOVA Test:** Showed significant differences in how age, general health, and checkup frequency influence BMI, indirectly affecting heart disease risk.

## Below is a screenshot of the final dashboard created in Tableau. It is interactive as to allow the end-user to extract insights that might be useful to his/her case.

You can access it after signing in through this public Tableau [link](https://public.tableau.com/views/HeartDiseaseRiskFactorsDashboard/New?:language=en-US&:display_count=n&:origin=viz_share_link).

![Interactive Dashboard](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/086b77ee4e08bb3e3733feae7115e4616ee09bf3/Final%20Dashboard/Dashboard%20Screenshot.png)

# Dataset 2 (UCI): 

This dataset complements the BRFSS data and includes medical terminology and factors that are known to influence CVD such as bloos pressure, cholestrol, chest pain, max heart rate, sugar level, artery blockage, etc.

## 🧹 Data Cleaning & Preprocessing

• Imputation of missing (NA) values with the mean. 

• Modified the features names to terms that are easier and more clear for the general public to grasp using R programming.

## 🔍 Correlation Insights 

### With Target Variable, Heart Disease: 

![Corr1](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/c5abed38d71702fb2401b5060b0c58b42c686cee/UCI%20Visuals/Correlation%20of%20Features%20with%20Heart%20Disease.png)

### Overall Heatmap:

![Corr2](https://github.com/AyahIbrahim/heart-disease-risk-analysis/blob/c5abed38d71702fb2401b5060b0c58b42c686cee/UCI%20Visuals/Heatmap.png)

I found the insights below to be useful:

• Maximum Heart Rate Achieved has a negative correlation (-0.42) with heart disease, indicating that a higher maximum heart rate achieved is associated with a lower likelihood of heart disease.

• Exercise ST segment Depression Value shows a moderate positive correlation (0.50) with heart disease, meaning that higher ST segment depression is associated with a higher likelihood of heart disease.

• Slope Peak Exercise ST segment Value and Unblocked Coronary Arteries also show positive correlations (0.38 and 0.52, respectively) with heart disease.

• Unblocked Coronary Arteries have a strong positive correlation (0.36) with age, indicating that older participants tend to have more unblocked coronary arteries.

• Aging also seems to lead to higher cholestrol, bloos pressure, and sugar levels.

• Thalassemia Type shows strong positive correlations with Chest Pain Type (0.26) and Unblocked Coronary Arteries (0.29), suggesting some association between these conditions.




