# Niyo-Bootcamp---Final-Project
Data Analytics - Final Project_End-to-End Analysis Applying All Tools

**Introduction**
Welcome to the Cardiovascular Disease Predictor project. This repository is dedicated to creating an analysis that can eventually be used as a basis for building a predictive model to assess the risk of cardiovascular disease (CVD) using various risk factors. The goal is to enable early detection and intervention, potentially saving lives and improving the quality of life for those at risk.

**About Me**
My name is Savina, and I have a background in Biomedical Science. Transitioning from Biomedical Science to Data Analysis was driven by my desire to make a broader impact in the medical field, particularly in research and development. Combining my scientific knowledge with data analysis skills, I aim to uncover valuable insights that lead to breakthroughs in medical science, improving patient outcomes and quality of life. This project aligns with my career goals of contributing to significant medical advancements, especially in cancer research and related fields.

**Project Overview
Topic:
Cardiovascular Disease Predictor**

**Problem Statement**
Cardiovascular disease (CVD) is a leading cause of death globally, with millions affected. Early detection is crucial to prevent severe health complications like strokes and heart attacks. The project aims to address the limited ability to detect and predict CVD early.

**Aim and Importance**
The primary aim is to create a predictive model that can assess CVD risk based on various factors. The importance of this project includes:

Reducing Mortality: Early detection can significantly lower mortality rates.
Improving Quality of Life: Early intervention can prevent serious health complications.
Addressing Health Disparities: Focus on reducing CVD risk among different demographic groups, particularly ethnic minorities.
Informing Public Health Policy: Identify key risk factors to contribute to public health strategies.
Sybil Jones Story
This project is inspired by Sybil Jones, a mother of three, whose life was impacted by an undiagnosed cardiovascular disease. Sybil's story underscores the importance of early detection and the potential life-saving benefits of predictive modeling in healthcare.

**Data Preparation**
Data Cleaning: Dropped the existing 'CVD' table and created a new one with specific fields such as general health, heart disease, age category, etc. Imported data from 'CVD_dataset_uncleaned.csv', cleaned the dataset by removing unwanted rows based on conditions in the 'diabetes' field, and exported the cleaned data to 'CVD_dataset_cleaned.csv'.
Data Processing: Initialized a Spark session, imported the cleaned data into a Spark dataframe, created a temporary Spark view, and cached it for optimized SQL queries.
Data Analysis: Used Spark SQL to analyze factors related to heart disease, including age, sex, general health, BMI, exercise, and more.
Data Visualization
Visualized findings using Plotly to create bar charts, pie charts, and line charts. Key insights include:

Increased heart disease risk with age, higher prevalence among males, and correlations with factors like smoking history and diabetes.
Identified trends in checkup frequency and general health ratings.
Example code for a bar chart visualization:

fig = px.bar(
    health_pandas_df,
    x='general_health',
    y='heart_disease_percentage',
    title='<b>Heart Disease Prevalence by General Health over Lifetime</b>',
    labels={'general_health': 'General Health', 'heart_disease_percentage': 'Heart Disease Prevalence (%)'},
    color='general_health',
    color_discrete_sequence=['#CD5C5C', '#8D021F'],
    category_orders={"general_health": ["Poor", "Fair", "Good", "Very Good", "Excellent"]},
    template='simple_white',
)

fig.update_layout(title_font=dict(size=28), xaxis_title_font=dict(size=16), yaxis_title_font=dict(size=16), xaxis_tickfont=dict(size=12), yaxis_tickfont=dict(size=12))
fig.show()

**Insights**
- Age-Related Trends: Risk of heart disease increases significantly with age, peaking in the 80+ age group.
- Gender Disparities: Males have a 1.5 times higher risk of heart disease compared to females.
- Lifestyle Factors: Regular exercise reduces risk, while smoking history increases it.
- Health Checkups: Frequent health checkups correlate with lower heart disease risk.
  
**Challenges and Recommendations**

**Challenges**
- Data Imbalance: Addressed imbalance between cases with and without heart disease using data cleaning and balancing techniques.
- Data Limitations: Geographic limitation to the United States and missing/inconsistent values required extra cleaning.
  
**Recommendations**
- Promote Regular Health Checkups: Encourage regular checkups for early detection and intervention.
- Target Lifestyle Factors: Public health campaigns to promote healthy lifestyle choices.
- Gender-Specific Strategies: Tailored prevention strategies for higher-risk groups.
- Expand Data Sources: Include broader geographic data to improve model generalization.
  
**Conclusion**
This project aims to create a significant impact on public health by developing a predictive model for cardiovascular disease, addressing one of the most critical medical issues of our time.
