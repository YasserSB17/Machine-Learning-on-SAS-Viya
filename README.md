# Machine-Learning-on-SAS-Viya
🎯 Predicting Donor Behavior using Machine Learning on SAS Viya
📌 Project Objective
This project aims to predict donor behavior by identifying individuals most likely to donate (target variable: "Target Gift Flag" = 1). The analysis uses machine learning models to improve donor targeting and optimize marketing campaigns.

🔄 Workflow & Methodology
1️⃣ Data Understanding & Preprocessing
Before modeling, an exploratory data analysis (EDA) was performed to assess data quality, distribution, and missing values.

Dataset: Contains donor information, past donation behavior, and demographic attributes.

Key Variables:

Gift Count 36 Months – Number of donations in the past 3 years.
Gift Amount Last – Amount of the last donation.
Time Since Last Gift – Number of months since the last donation.
Demographic Cluster – Socioeconomic segmentation of donors.
Promotion Count Card – Number of marketing contacts received.
Handling Missing Data:

Missing values were analyzed and imputed using median values for numerical variables.
Categorical variables were encoded using one-hot encoding.
Feature Engineering:

Created interaction variables (e.g., Gift Amount per Year, Donation Frequency).
Standardized numerical features for models sensitive to scale.
2️⃣ Descriptive Analysis & Insights
The EDA revealed key insights:

Donors with higher past donations and frequent donations are more likely to donate again.
There is a strong correlation between promotion exposure and donation likelihood.
The demographic cluster variable plays a significant role in donor behavior.
3️⃣ Machine Learning Models Tested
Multiple models were evaluated to determine the best predictive performance:

Model	KS Score (Youden Index)	Observations Used	Key Findings
Decision Tree	0.1639	106,546	High interpretability but limited predictive power.
Logistic Regression	0.1863	64,988	Slightly better than Decision Tree, sensitive to linear correlations.
Neural Network	0.0000 ❌	64,988	Poor convergence, not suitable for this problem.
Gradient Boosting ✅	0.3488	106,546	Best performance, handles complex relationships well.
Random Forest	0.1561	106,546	Robust but underperforms compared to Gradient Boosting.
4️⃣ Model Selection & Results
The Gradient Boosting Model was selected as the best-performing model due to:
✔ Highest KS Score (0.3488) – Best ability to separate positive and negative cases.
✔ Strong feature importance ranking – Key variables include Gift Count, Age, and Time Since Last Gift.
✔ Ability to handle non-linear relationships – Outperformed traditional models.

🚀 Business Impact & Decision-Making
Improved Donor Targeting 🎯: Marketing campaigns can now focus on individuals with a high likelihood of donating, optimizing resources.
Enhanced ROI for Campaigns 📈: More accurate targeting reduces costs and increases fundraising efficiency.
Data-Driven Strategy for Nonprofits 🤝: Insights help design personalized campaigns based on past behavior.
🛠️ Future Improvements
Hyperparameter tuning for Gradient Boosting to further improve accuracy.
Incorporate external data (e.g., social media activity, economic indicators) to refine predictions.
Deploy the model as an automated system for real-time donor prediction.
📂 Repository Contents
EDA.ipynb – Exploratory Data Analysis
FeatureEngineering.ipynb – Data Preprocessing & Feature Engineering
ModelTraining.ipynb – ML Model Training & Evaluation
ModelDeployment.ipynb – Deployment Strategy
📢 Conclusion
This project successfully applies machine learning to predict donor behavior, improving marketing efficiency for fundraising campaigns. The Gradient Boosting model provided the best performance, enabling data-driven decision-making for optimized donor outreach. 🚀
