
# ![1613885918](https://github.com/user-attachments/assets/5793ce83-645c-4f41-b41c-969de0018d66)
Smart Justice: Predictive Analytics for Recidivism and Violent Behavior
## Introduction 
Imagine being judged not just by your past actions but by an algorithm predicting your future behavior. This is the reality in many courtrooms today, where a tool known as COMPAS(Correctional Offender Management Profiling for Alternative Sanctions) helps determine whether someone is likely to re-offend. Used in critical decisions like bail, sentencing, and parole, COMPAS plays a significant role in shaping the lives of thousands in the United States of America. But how does it work, and what does its influence mean for justice and fairness? Let's dive into the world of COMPAS to understand its impact and the controversies surrounding it.

## Contributers
Project Leader: Houssam Saleh Alrifaii 
Team Members: Mariana Saleh Alrifaii


![](docs/prison.webp)
## Project overview 
The Smart Justice project is a data analysis project focused on predicting recidivism within the criminal justice system. Using a comprehensive dataset,With more than 18000 rows and 40 columns, this project seeks to explores patterns in re-offending, assesses risk factors, and investigates potential biases in risk assessment tools like COMPAS. The insights generated aim to support fair and informed decision-making in areas such as pretrial release, sentencing, and parole.
## Features
### .Data Preprocessing:
Converts and cleans data related to offenders, including handling dates, categorizing age groups, and managing missing values.
### .Risk Assessment:
Analyzes risk factors and generates insights based on the COMPAS risk assessment tool, focusing on general and violent recidivism.
### .Visualization:
Provides graphical representations of data trends, risk distributions, and recidivism patterns.
### .Predictive Modeling: 
Implements machine learning models to predict the likelihood of recidivism based on various risk factors.
### .Bias Analysis:
Investigates potential biases in risk assessments, particularly concerning race and age, to ensure fair treatment in the justice system.
## Dataset 
**Demographics:** ID, FirstName,FullName, LastName, Gender, DateOfBirth, Age, age_category, Race

**Criminal History:** JuvenileFelonyCount, JuvenileMisdemeanorCount, JuvenileOtherCount, PriorsCount

**Risk Assessment:** RiskScore, RiskScoreText, AssessmentType, ViolentRiskAssessmentType, ViolentRiskScoreText

**Judicial Data:** JailEntry, JailExit, DaysBetweenScreeningAndArrest, ChargeDegree, ChargeDescription, RecedevismChargeDegree, DaysFromRecidivismArrest, RecidivismOffenseDate, RecidivismChargeDescription, RecidivismJailEntryDate, ViolentRecidivismChargeDegree, ViolentRecidivismOffenseDate, ViolentRecidivismChargeDescription

**Outcome Variables:** Recidivisim, ViolentRecidivism, Event

**Additional Information:** DaysBetweenScreeningAndArrest, ScreeningDate

## Data Dictionary:
|     Variable           | Description                                 | 
|:------------------------:|---------------------------------------------|
| ID                     |A unique identifier                          |
| FullName               |A full name of individual                    |
| FirstName              |A first name of the individual               |
| LastName                |A last name of the individual                |
|       Gender              |the gender(male or female)                   |
| DateOfBirth                    | Date of birth                               |
| Age                    | the age of the individual                   | 
| age_category           | the age group (>45 ,45> >25, <25)           |
| Race                   | the ethnicity of the individual             |
| JuvenileenilefelonyCount          |the Count of Juvenileenile felony charges         |
| RiskScore           |A risk assessment score                      |
| JuvenileenilemisdemanorCount         |The Count of Juvenileenile misdemeanor            |
| JuvenileenileOtherCount        |The Count of other Juvenileenile offenses (minors)|
| PriorOffenceCount           |The total number of prior criminal charges   |
| DaysbetweenScreeningAndArrest|number of days between arrest an assessment  |
| JailEntryDate              |The date  admitted to jail                   |
| JailExitDate             |The date released from jail                  |
| DaysfromCompasScreening     |Days between COMPAS and relevent event       |
| ChargeDegree        |The severity of the criminal charge          |
| ChargeDescription          |A description of the criminal charge         |
| Recidivism               |Indicates if committed another crime after   | 
| RecedevismChargeDegree        |The severity of the most recent  charge      |
| DaysFromRecedivismArrest     |days from the recent arrest to other event   |
| RecedevismOffenseDate         |The date of the most recent offense          |
| RecedevismChargeDescription          |A description of the most recent charge      |
| RecedevismJailEntryDate              |The date of admission to jail                |
| ViolentRecidivism      |commited violent crime after initial offense |
| ViolentRecidivismChargedegree       |The severity of the charge                   |
| ViolentRecidivismOffenseDate        |The date of the most recent violent offense  |
| ViolentRecidivismChargeDescription        |A description of the recent violent charge   |
| AssessmentType     |The type of risk assessment performed        |
| RiskScoreText             | A textual interpretation of the decile score|
| ScreeningDate         |screening was conducted date                 |
| ViolentRiskAssessmentType   |The type of assessment related to violent    |
|ViolentRiskScore |the score in which the individual is violent |
|ViolentRiskScoreText|the violence Degree of the individual|
| Event                  | An event that occurred                      |


![](docs/Compas.png)

## Steps Taken To Train The Model :
**1.     Data Preparation :**
- Collected and preprocessed the data, ensuring that demographic features (e.g., age, gender) and past records were cleaned, encoded, and normalized where necessary. 
- Split the dataset into training and testing sets, typically using an 80-20 or 70-30 ratio, to ensure the model generalizes well to unseen data. 

**2.  Model Selection:**
-	Initially experimented with several classification algorithms (e.g., logistic regression, decision trees, random forest, support vector machines) and regression algorithms (e.g., linear regression, ridge regression).
-  	Based on initial performance, focused on a classification algorithm (e.g., random forest or logistic regression) since the task is predicting categorical risk scores.

**3. Training Process:**
-	Trained the model using the selected algorithm(s) on the training data.
-	Applied cross-validation (e.g., k-fold cross-validation) to prevent overfitting and to tune hyperparameters effectively across multiple splits of the dataset.

## Key Objectives of the Project
### The key objectives of this project are:

**1.	Develop a Predictive Models:** Build and train a classification and regression models that can accurately predict  based on available data.

**2.	Utilize Demographic and Historical Data:** Incorporate demographic information such as age and gender, along with past behavioral records, into the model to enhance prediction accuracy.

**3.	Evaluate Model Performance:**
 Assess the model’s accuracy and identify the most important factors contributing to violent risk prediction.

**4.	Address Bias and Fairness:**
 Ensure that the model is fair and minimizes bias, particularly regarding demographic variables like gender and age, which could disproportionately affect certain groups.


## Impact:
Through exploratory data analysis, several key insights were discovered. Notably,
