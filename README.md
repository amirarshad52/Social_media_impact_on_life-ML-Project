
# Impact of Social Media on Life
## Machine Learning Project — BSAI 5B | Group 2

A Supervised Machine Learning project that analyzes student-related social media data and predicts its overall impact as **Beneficial, Neutral, or Negative**.

---

## Project Information

| Detail | Information |
|---|---|
| Project Title | Impact of Social Media on Life |
| Program | Bachelor of Science in Artificial Intelligence (BSAI) |
| Class | BSAI 5B |
| Group | Group 2 |
| Project Type | Supervised Machine Learning |
| Classification Type | Multiclass Classification |
| Best Model | Gradient Boosting Classifier |

---

## 1. Introduction

Social media has become an important part of students' daily lives. Platforms such as Instagram, TikTok, YouTube, and other social networking applications influence communication, entertainment, learning habits, and daily routines.

Although social media provides educational and communication opportunities, excessive or inappropriate usage may also be associated with sleep problems, stress, reduced study time, and academic challenges.

This project uses machine learning techniques to analyze student-related social media data and classify its overall impact into three categories:

- Beneficial
- Neutral
- Negative

## 2. Problem Statement

Students use social media for different purposes and durations. Its impact may vary according to usage patterns, academic activities, sleep quality, and other factors.

The main problem addressed in this project is to use machine learning algorithms to identify patterns in student data and predict the overall impact category of social media usage.

## 3. Project Aim

The main aim is to develop and evaluate a machine learning classification system that predicts the overall impact of social media on students' lives using relevant student-related features.

## 4. Project Objectives

1. Obtain and understand a suitable student-focused social media dataset.
2. Explore the dataset and identify relevant features.
3. Perform data cleaning and preprocessing.
4. Conduct exploratory data analysis (EDA) using statistical summaries and visualizations.
5. Train multiple machine learning classification algorithms.
6. Evaluate and compare the performance of trained models.
7. Select the best-performing model based on evaluation metrics.
8. Save the trained model using the Joblib library for future reuse.

---

## 5. Dataset Information

The project uses the Kaggle dataset titled **Impact of Social Media on Life**.

| Dataset Detail | Description |
|---|---|
| Dataset Source | Kaggle |
| Dataset Name | Impact of Social Media on Life |
| Total Records | 4,500 |
| Target Column | `Overall_Impact` |
| Classification Type | Multiclass Classification |
| Target Classes | Beneficial, Neutral, Negative |

### Dataset Features

The dataset contains student-related information, including:

- Age
- Gender
- Academic Level
- Most Used Social Media Platform
- Daily Usage
- Sleep Quality
- Device
- Mental Health-related scores
- Conflicts
- Academic Impact
- Usage Frequency
- Stress Level
- Study Hours
- GPA
- Overall Impact (Target Variable)

### Dataset URL

[Kaggle – Impact of Social Media on Life](https://www.kaggle.com/datasets/harishyadav0506/impact-of-social-media-on-life)

---

## 6. Project Methodology

The following workflow was used in the project.

### 6.1 Data Loading and Exploration

The dataset was loaded into Python using Pandas. Its structure, columns, data types, and statistical summaries were examined.

### 6.2 Data Cleaning and Preprocessing

The dataset was prepared for machine learning by handling data quality issues and preparing relevant features for model training.

### 6.3 Exploratory Data Analysis (EDA)

Data analysis and visualizations were used to understand patterns and relationships among student-related variables and the target classes.

### 6.4 Feature Preparation

Relevant input features were prepared for classification. The target variable was `Overall_Impact`.

### 6.5 Train-Test Split

The dataset was divided into training and testing subsets using an 80:20 split.

| Dataset Portion | Records |
|---|---:|
| Training Data (80%) | 3,600 |
| Testing Data (20%) | 900 |
| **Total** | **4,500** |

---

## 7. Machine Learning Algorithms

Three machine learning classification algorithms were implemented and compared.

### 7.1 Logistic Regression

Used as a classification approach to predict the target categories.

### 7.2 Random Forest Classifier

Uses multiple decision trees to produce classification predictions.

### 7.3 Gradient Boosting Classifier

Builds an ensemble of sequentially improved decision trees.

---

## 8. Model Evaluation and Actual Results

The trained models were evaluated using Test Accuracy and Macro F1-score.

### Model Comparison

| Algorithm | Test Accuracy | Test Macro F1 |
|---|---:|---:|
| Logistic Regression | 97.00% | 93.37% |
| Random Forest | 96.67% | 91.87% |
| **Gradient Boosting** | **97.33%** | **93.53%** |

### Selected Best Model: Gradient Boosting Classifier

The Gradient Boosting model achieved the highest test accuracy of **97.33%** and Macro F1-score of **93.53%** among the three evaluated models.

### Cross-Validation

Five-fold cross-validation was also performed to assess model performance across different data splits.

- Cross-Validation Method: 5-Fold
- Average Macro F1-score: **94.37%**

Cross-validation provides an additional measure of model performance beyond a single train-test split.

---

## 9. Model Saving Using Joblib

After selecting Gradient Boosting as the best-performing model, the trained model pipeline was saved using the Joblib Python library.

### Saved Model File

`Social_Media_Impact_Best_Model.pkl`

Joblib allows the trained model to be stored and loaded again without repeating the entire training process.

The saved model can be reused for future predictions and can serve as the model artifact for a future deployment stage.

### Save Model Example

```python
import joblib

joblib.dump(
    best_pipeline,
    "Social_Media_Impact_Best_Model.pkl"
)
```

### Load Saved Model Example

```python
import joblib

loaded_model = joblib.load(
    "Social_Media_Impact_Best_Model.pkl"
)
```

---

## 10. Completed Project Work

The following tasks have been completed:

- Dataset selection and loading.
- Dataset exploration and analysis.
- Data cleaning and preprocessing.
- Exploratory data analysis and visualizations.
- Feature preparation.
- Training and testing data separation.
- Training of Logistic Regression, Random Forest, and Gradient Boosting.
- Model comparison using evaluation metrics.
- Five-fold cross-validation.
- Selection of the Gradient Boosting model.
- Saving the trained model using Joblib.
- Maintaining the project notebook, dataset, and saved model in the GitHub repository.

---

## 11. Expected Outcomes and Project Benefits

The project demonstrates how machine learning can be applied to student-related social media data.

Expected benefits include:

- Identifying patterns associated with social media usage.
- Predicting the overall impact category using a trained classifier.
- Comparing different classification algorithms.
- Preserving the best-performing model for future use.
- Providing a foundation for a future prediction application.

---

## 12. Limitations

- The model's predictions depend on the quality and representativeness of the available dataset.
- The dataset may contain class imbalance, which can affect performance across individual classes.
- Machine learning predictions identify patterns and associations; they do not establish that social media directly causes a particular outcome.
- The model should not be treated as a medical or psychological diagnostic tool.
- A live web application or production deployment is not claimed as completed in this submission.

---

## 13. Future Enhancements

The project can be extended in the future through:

1. Developing a web-based interface for entering student information and receiving predictions.
2. Deploying the trained model through a suitable application framework.
3. Testing the model with additional datasets.
4. Monitoring model performance and retraining when appropriate.
5. Improving performance on underrepresented target classes.

---

## 14. Tools and Technologies

| Tool / Library | Purpose |
|---|---|
| Python | Programming Language |
| Jupyter Notebook | Project Development |
| Pandas | Data Handling |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| Seaborn | Statistical Visualization |
| Scikit-learn | Machine Learning and Evaluation |
| Joblib | Saving and Loading the Trained Model |
| GitHub | Project Version Control and Hosting |
| Kaggle | Dataset Source |

---

## 15. GitHub Project Repository

The project files are maintained in the following GitHub repository.

**Repository Name:** Social_media_impact_on_life-ML-Project

**GitHub URL:**

[View Project Repository](https://github.com/amirarshad52/Social_media_impact_on_life-ML-Project)

The repository contains the project notebook, dataset, saved Joblib model, and project documentation.

---

## 16. Conclusion

The project demonstrates the application of supervised machine learning to analyze and classify the overall impact of social media on students' lives.

Three classification algorithms were trained and evaluated. Among them, Gradient Boosting achieved the best test accuracy of **97.33%** and Macro F1-score of **93.53%**.

The selected model was saved using Joblib, making it reusable for future predictions and further development.

This project provides practical experience in data analysis, preprocessing, machine learning model development, evaluation, model comparison, and model persistence.

---

## 17. References

1. **Kaggle Dataset – Impact of Social Media on Life**  
   https://www.kaggle.com/datasets/harishyadav0506/impact-of-social-media-on-life

2. **GitHub Project Repository**  
   https://github.com/amirarshad52/Social_media_impact_on_life-ML-Project

3. **Scikit-learn Documentation**  
   https://scikit-learn.org/

4. **Joblib Documentation**  
   https://joblib.readthedocs.io/

---

**Project:** Impact of Social Media on Life  
**Program:** BSAI 5B  
**Group:** Group 2
