# End-to-End Supervised Machine Learning Portfolio

Welcome to my machine learning portfolio! This project is designed to be a clean, beginner-friendly, and practical demonstration of the **Data Science Lifecycle** applied to supervised learning problems. 

Instead of just throwing algorithms at data, this project walks through the entire process step-by-step: from loading data and exploring it, to preprocessing, training models, and finally understanding *why* certain models perform better than others.

## 🎯 Project Objectives

1. **Demonstrate the Data Science Lifecycle**: Show a clear progression from raw data to final insights.
2. **Cover Core Algorithms**: Implement and compare major supervised learning models (Linear/Logistic Regression, Trees, Random Forests, SVM, KNN, Naive Bayes, XGBoost).
3. **Explain Concepts Simply**: Break down complex topics like overfitting, underfitting, and the bias-variance tradeoff in plain English.
4. **Write Clean Code**: Keep the code readable, well-commented, and easy to follow for students and interviewers alike.

## 📊 Datasets Used

I chose two classic, high-quality public datasets that are realistic but clean enough to focus on learning:

1. **California Housing Prices (Regression)**
   - **Source**: 1990 US Census (via Scikit-Learn)
   - **Task**: Predict the median house value for California districts.
   - **Why this dataset?**: It requires handling outliers, feature scaling, and feature engineering. It's perfect for comparing linear models against tree-based models.

2. **Heart Disease (Classification)**
   - **Source**: UCI Machine Learning Repository
   - **Task**: Predict whether a patient has heart disease based on clinical features.
   - **Why this dataset?**: It's a critical real-world application (medical diagnosis) with a good mix of categorical and numerical features. It's great for understanding metrics like Recall and Precision.

## 📁 Folder Structure

```text
ml-portfolio/
├── data/                   # Raw and preprocessed CSV files
├── images/                 # Visualizations generated during EDA and evaluation
├── notebooks/              # The core of the project (run these in order!)
│   ├── 01_regression_eda.ipynb
│   ├── 02_regression_preprocessing.ipynb
│   ├── 03_regression_models.ipynb
│   ├── 04_classification_eda.ipynb
│   ├── 05_classification_models.ipynb
│   └── 06_final_summary.ipynb
├── .gitignore              # Keeps the repo clean
├── README.md               # You are here
└── requirements.txt        # Python dependencies
```

## 🧠 Models Implemented

### Regression Models
- **Linear Regression**: The simple baseline.
- **Ridge & Lasso Regression**: Added regularization to prevent overfitting.
- **Decision Tree Regressor**: Good for non-linear patterns, but prone to overfitting.
- **Random Forest Regressor**: An ensemble method that usually performs very well.
- **XGBoost Regressor**: Gradient boosting for maximum performance.

### Classification Models
- **Logistic Regression**: A surprisingly strong baseline for medical data.
- **K-Nearest Neighbors (KNN)**: Classifies based on similarity to nearby points.
- **Support Vector Machine (SVM)**: Finds the optimal boundary between classes.
- **Naive Bayes**: A fast, probability-based approach.
- **Decision Tree & Random Forest**: Tree-based classification.
- **XGBoost Classifier**: High-performance gradient boosting.

## 📈 Results Summary

- **Regression**: **XGBoost** and **Random Forest** significantly outperformed linear models, achieving an R² score of ~0.81. This tells us the relationship between housing features and price is highly non-linear.
- **Classification**: **Random Forest** achieved the highest accuracy (~83.6%), but simpler models like **Logistic Regression** and **SVM** were very close behind (~80-82%). In medical datasets, simple interpretable models often perform just as well as complex ones!
- **Overfitting**: We successfully managed overfitting using techniques like Train-Test Splits, Cross-Validation, and Tree Pruning.

*(Check out `notebooks/06_final_summary.ipynb` for detailed charts and a deep dive into the Bias-Variance Tradeoff!)*

## 🚀 How to Run the Project

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/ml-portfolio.git
   cd ml-portfolio
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   *Open the `notebooks/` folder and start with `01_regression_eda.ipynb`!*

## 🔮 Future Improvements

This project is designed to be expandable. In the future, I plan to add:
- **Phase 2: Unsupervised Learning**: Adding a new set of notebooks covering K-Means Clustering, PCA (Principal Component Analysis), and Anomaly Detection.
- **Hyperparameter Tuning**: Implementing `GridSearchCV` to squeeze out extra performance.
- **Model Deployment**: Wrapping the best model in a simple Streamlit web app.

---
*Built with Python, Scikit-Learn, Pandas, and Matplotlib.*
