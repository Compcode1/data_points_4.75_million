This notebook expands on a previously created novel synthetic dataset of 250,000 rows by inserting additional attributes related to health and lifestyle. The expanded dataset now includes several new columns and computations, offering a richer basis for statistical analysis and machine learning applications.

#### Data Enrichment
New columns are generated based on a variety of health risk factors, including:

- **Smoking Habits**: (Smoker, Former Smoker, Non-Smoker).
- **Alcohol Consumption**: (Non-Drinker, Moderate Drinker, Heavy/Binge Drinker).
- **Exercise Patterns**: (Meets Both Guidelines, Meets Aerobic Only, Insufficiently Active, Inactive).
- **Sleep Deprivation**: (Adequate Sleep, Less than 7 Hours, Chronic Sleep Deprivation).
- **Other Health Conditions**: Columns for conditions such as Metabolic Syndrome, COPD, Cancer, Diabetes, and Heart Disease were also included.

#### Health Condition Assignment
Algorithms were designed to assign binary outcomes for a number of health conditions:

- **Diabetes**: Assigned based on age groups and fasting blood glucose (FBG) thresholds. Younger individuals require higher FBG levels for a diabetes diagnosis, while older individuals have a lower FBG threshold.
- **Cancer**: Assigned with a base probability for individuals over 65, with smoking and BMI > 37 as contributing risk factors.
- **Heart Disease**: Probability of heart disease is increased by risk factors such as BMI, alcohol consumption, high fasting blood glucose, and smoking.
- **Metabolic Syndrome**: Assigned based on the presence of at least three risk factors, including high blood pressure, high triglycerides, low HDL, high fasting blood glucose, and high waist circumference.
- **COPD**: Assigned to smokers over age 45, with increased probabilities for smokers over age 60.

#### Physical Exam Score Calculation
A custom **Physical Exam Score** is calculated for each individual, starting with an age-based base score:

- **Base Score**: Determined by age, with younger individuals receiving a higher score.
- **Adjustments**: Reductions are applied based on negative health factors like smoking, alcohol consumption, inactivity, sleep deprivation, and conditions like heart disease, cancer, COPD, and diabetes. Each risk factor subtracts a specific percentage from the base score.

#### Statistical Summaries
The notebook computes key statistics, such as the percentage of individuals with diabetes, cancer, COPD, heart disease, and metabolic syndrome. In addition, a breakdown of physical exam scores by age group is provided.
