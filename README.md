# Fraud Detection for E-commerce and Banking Transactions

A machine learning project for detecting fraudulent transactions in e-commerce and banking systems using various classification algorithms and data preprocessing techniques.

## Project Structure

```
fraud-detection-modeling-ecommerce-banking-transactions/
├── data/
│   ├── raw/                    # Original datasets
│   │   ├── creditcard.csv
│   │   ├── Fraud_Data.csv
│   │   └── IpAddress_to_Country.csv
│   └── processed/              # Cleaned and preprocessed data
│       ├── feature_info.json
│       ├── fraud_data_cleaned.csv
│       ├── label_encoders.pkl
│       ├── scaler.pkl
│       └── train/test splits
├── notebooks/
│   └── 01_data_analysis.ipynb  # Exploratory data analysis
├── scripts/
│   ├── __init__.py
│   └── preprocess.py           # Data preprocessing utilities
└── README.md
```

## Features

- **Data Preprocessing**: Comprehensive data cleaning and feature engineering
- **Feature Engineering**: 
  - Time-based features (signup/purchase hours, day of week)
  - IP address to country mapping
  - Age grouping and categorical encoding
  - Time difference calculations
- **Class Imbalance Handling**: SMOTE (Synthetic Minority Oversampling Technique)
- **Scaling**: StandardScaler for numerical features
- **Exploratory Data Analysis**: Detailed analysis in Jupyter notebooks

## Dataset Information

The project uses multiple datasets:
- **Fraud_Data.csv**: Main transaction data with user information
- **IpAddress_to_Country.csv**: IP address to country mapping
- **creditcard.csv**: Additional credit card transaction data

### Key Features
- `user_id`: Unique user identifier
- `age`: User age
- `purchase_value`: Transaction amount
- `ip_int`: IP address (integer format)
- `signup_time`/`purchase_time`: Timestamp features
- `sex`, `age_group`, `purchase_category`: Categorical features
- `country`: User's country (derived from IP)

## Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
imbalanced-learn
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/fraud-detection-modeling-ecommerce-banking-transactions.git
cd fraud-detection-modeling-ecommerce-banking-transactions
```

2. Install required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

## Usage

### Data Analysis
Start with the exploratory data analysis notebook:
```bash
jupyter notebook notebooks/01_data_analysis.ipynb
```

### Data Preprocessing
Use the preprocessing script for data preparation:
```python
from scripts.preprocess import preprocess_data
# Add your preprocessing code here
```

## Data Processing Pipeline

1. **Data Loading**: Load raw datasets from `data/raw/`
2. **Data Cleaning**: Handle missing values and data quality issues
3. **Feature Engineering**: Create time-based and derived features
4. **Encoding**: Label encoding for categorical variables
5. **Scaling**: StandardScaler for numerical features
6. **Balancing**: SMOTE for handling class imbalance
7. **Train/Test Split**: Prepare data for modeling

## Model Performance

The project implements various classification algorithms for fraud detection:
- Logistic Regression
- Random Forest
- Support Vector Machine
- Neural Networks

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Dataset sources and contributors
- Scikit-learn and imbalanced-learn libraries
- Jupyter notebook community