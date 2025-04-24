# Student Dropout Forecasting

## 📅 Project Overview
This project focuses on predicting student dropout using historical academic and administrative data. The dataset is obtained from the UCI Machine Learning Repository (Student Dropout and Academic Success dataset). The goal is to identify key factors influencing student retention and use predictive modeling to proactively flag at-risk students.

## ⚙️ Technologies Used
- **Python 3**
- **scikit-learn** for modeling (Logistic Regression, XGBoost, etc.)
- **matplotlib & seaborn** for data visualization
- **pandas & numpy** for data manipulation
- **ucimlrepo** for dataset loading

## 🌐 Dataset Details
- **Source**: UCI ML Repo (Dataset ID: 697)
- **Target Classes**:
  - `0` = Graduate
  - `1` = Dropout
  - `2` = Enrolled
- **Features** include academic grades, financial history (tuition payment), personal information (age, residence), and curricular progression.

---

## 🧠 Model Overview

The primary model used for prediction in this project is **XGBoost (Extreme Gradient Boosting)**, a powerful tree-based ensemble method well-known for its accuracy and efficiency on structured datasets. XGBoost excels at handling a mix of categorical and numerical features, managing missing values, and capturing non-linear relationships. It also provides feature importance scores, which make interpretation easier. However, XGBoost requires careful tuning to avoid overfitting and can be computationally expensive on very large datasets. In this project, it achieved high predictive performance and helped surface key insights about student behavior.

## 🌟 Future Work
- Incorporate time-series patterns (semester-wise GPA trends).
- Add NLP-based sentiment from student feedback.
- Use ensemble models or neural networks for improved accuracy.

---

## 📊 Visualizations

### 1. **Feature Importance Bar Chart**
>This chart shows which student factors are most important in predicting who might drop out. Taller bars mean more influence. For example, if "1st semester grades" has the highest bar, it plays the biggest role in dropout decisions according to the model. The chart highlights the top 15 predictors of student dropout. Derived from an XGBoost model, these features contribute most to the decision-making process. Key influencers include semester grades, admission performance, and tuition delay history.

### 2. **Correlation Heatmap**
> This colorful grid shows how student characteristics relate to one another. Red means two features increase together (like GPA and attendance), while blue means they move in opposite directions. It helps us see patterns and strong connections. The chart displays pairwise correlations between features. Strong linear relationships appear in red (positive) or blue (negative). This helps identify multicollinearity and features most linearly linked to dropout status.

### 3. **Violin Plot - Admission Grade vs Dropout**
> This plot looks like a mix of a box and a curve. It shows how student grades at the time of joining differ between those who graduated and those who dropped out. Narrow and low shapes mean most dropouts had lower entry grades. The plot shows the distribution of admission grades by outcome class. Dropout students tend to have lower and more concentrated grade distributions compared to those who graduate.

### 4. **Department-wise Dropout Count Plot**
> A simple bar chart showing how many students dropped out or graduated from each department. Helps spot programs with higher risk of students leaving early. The plot visualizes student outcome counts across departments. Useful for identifying high-risk programs with disproportionate dropout rates.

### 5. **Confusion Matrix**
> A grid that compares what the model predicted to what actually happened. Perfect predictions land on the diagonal. The other boxes show where the model guessed wrong. It's a useful way to measure model accuracy. It Compares model predictions against actual outcomes. Diagonal cells represent correct classifications, while off-diagonal cells show misclassifications. Useful for identifying where the model struggles.

### 6. **ROC Curves (Multiclass)**
> These curves show how good the model is at telling the difference between graduating, dropping out, and still being enrolled. Higher curves mean better performance. Each line represents one group, and the area under each curve tells us how confident the model is. ROC curves for each class (Graduate, Dropout, Enrolled) using a One-vs-Rest logistic regression. Each curve displays the model's ability to distinguish one class from the others. Higher AUC values indicate stronger performance.

---

## 🔬 Final Conclusion: Top 5 Factors Influencing Dropout
1. **Curricular Unit Grade in 1st Semester**
2. **Admission Grade**
3. **Curricular Unit Grade in 2nd Semester**
4. **Tuition Payment Delay**
5. **Age**

Academic performance, especially in the early semesters, and financial stress are primary predictors of dropout. Students who struggle early or have tuition payment delays are at high risk.

---

## ⚖️ My Recommendations

### ⏳ Short-Term Interventions
- **Early Academic Alerts**: Implement academic probation flags after 1st semester failures.
- **Targeted Counseling**: Reach out to students with low admission/semester grades.
- **Financial Aid Audits**: Provide assistance or flexible payment plans for students with delays.

### ⏱ Long-Term Strategies
- **Curriculum Reform**: Adjust course difficulty or prerequisites in high-dropout departments.
- **Predictive Dashboards**: Implement ongoing dropout risk dashboards using real-time data.
- **Mentorship Programs**: Assign mentors to freshmen identified as high risk by the model.

---

## 🌟 Future Work
- Incorporate time-series patterns (semester-wise GPA trends).
- Add NLP-based sentiment from student feedback.
- Use ensemble models or neural networks for improved accuracy.

---

## 🎓 Author
Built by a Data Science enthusiast passionate about education, early intervention, and responsible AI.