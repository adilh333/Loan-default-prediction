# Loan Default Prediction Model

A machine learning project that predicts loan defaults using multiple algorithms including Logistic Regression, Random Forest, and XGBoost. The model is designed to help financial institutions assess credit risk and make informed lending decisions.

## 📊 Project Overview

This project analyzes loan data to predict whether a borrower will default on their loan. The dataset contains information about employment status, bank balance, annual salary, and other financial indicators. The model achieves high recall scores to minimize false negatives (missed defaults), which is crucial for risk management.

## 🎯 Key Features

- **Multiple ML Algorithms**: Implements Logistic Regression, Random Forest, and XGBoost
- **Class Imbalance Handling**: Uses balanced class weights and appropriate evaluation metrics
- **Feature Engineering**: Creates debt-to-income ratio for better predictions
- **Comprehensive Evaluation**: Includes accuracy, precision, recall, F1-score, and ROC-AUC metrics
- **Visualization**: Provides feature importance plots and ROC curve comparisons

## 📈 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score | ROC AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.854 | 0.172 | **0.881** | 0.288 | 0.949 |
| Random Forest | 0.866 | 0.179 | 0.836 | 0.295 | 0.935 |
| XGBoost | 0.845 | 0.165 | **0.896** | 0.279 | 0.939 |

**Key Insights:**
- XGBoost achieves the highest recall (89.6%), crucial for minimizing missed defaults
- All models show strong ROC-AUC scores (>0.93), indicating excellent discrimination ability
- The dataset has a 3.33% default rate, making it highly imbalanced

## 🛠️ Technical Details

### Dataset
- **Size**: 10,000 records
- **Features**: Employment Status, Bank Balance, Annual Salary, Debt-to-Income Ratio
- **Target**: Binary classification (Defaulted: Yes/No)
- **Class Distribution**: 96.67% Non-default, 3.33% Default

### Features Used
1. **Employment_Status**: Whether the borrower is employed
2. **Bank_Balance**: Current bank account balance
3. **Annual_Salary**: Yearly income
4. **Debt_to_Income**: Calculated ratio of bank balance to annual salary

### Algorithms Implemented
1. **Logistic Regression**: Linear model with balanced class weights
2. **Random Forest**: Ensemble method with 150 trees, max depth 5
3. **XGBoost**: Gradient boosting with early stopping and class balancing

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### Usage
1. Clone the repository:
```bash
git clone https://github.com/adilh333/Load-default-prediction.git
cd Load-default-prediction
```

2. Place your dataset (`Default_Fin.csv`) in the project directory

3. Run the Jupyter notebook:
```bash
jupyter notebook Appl_AI.ipynb
```

## 📁 Project Structure

```
Load-default-prediction/
├── Appl_AI.ipynb          # Main Jupyter notebook with analysis
├── Default_Fin.csv        # Dataset (not included in repo due to size)
├── README.md              # This file
└── .gitignore            # Git ignore file
```

## 🔍 Key Findings

1. **Feature Importance**: Bank balance and annual salary are the most predictive features
2. **Model Selection**: XGBoost performs best for recall, while Random Forest has the highest accuracy
3. **Class Imbalance**: The 3.33% default rate requires careful handling with balanced metrics
4. **Business Impact**: High recall ensures most defaults are caught, reducing financial risk

## 📊 Visualizations

The notebook includes several visualizations:
- Feature importance plots for Random Forest and XGBoost
- ROC curve comparison across all models
- Recall score comparison bar chart
- Class distribution analysis

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Adil Hussain**
- GitHub: [@adilh333](https://github.com/adilh333)

## 📞 Contact

If you have any questions or suggestions, please feel free to reach out or open an issue in this repository.

---

**Note**: This model is for educational and research purposes. For production use in financial services, additional validation, regulatory compliance, and risk assessment would be required.
