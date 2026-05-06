# Credit Card Fraud Detection

This project implements multiple machine learning models to detect fraudulent credit card transactions. The project includes various approaches including Random Forests, Isolation Forests, Decision Trees, and Hidden Markov Models.

## Project Structure

```
.
├── data/                       # Dataset directory
│   ├── creditcard.csv         # Credit Card Fraud Detection dataset (to be downloaded)
│   └── fraudTrain.csv         # Synthetic Financial dataset (to be downloaded)
│
├── eda & preprocessing/        # EDA and data preprocessing notebooks
│   ├── EdaPreprocessing1.ipynb
│   └── EdaPreprocessing2.ipynb
│
├── analysis1.ipynb            # Analysis notebook using various models
├── analysis2.ipynb           # Additional analysis notebook
├── clustering.py             # Implementation of clustering algorithms (KMeans, DBSCAN, CLINK)
├── config.py                 # Configuration parameters
├── decisionTree.py          # Custom Decision Tree implementation
├── hidden_markov_main.py    # Main script for Hidden Markov Model
├── hidden_markov_model.py   # HMM implementation for fraud detection
├── isolationForest_1.ipynb  # Isolation Forest implementation and analysis
├── isolationForest_2.ipynb  # Additional Isolation Forest analysis
├── RandomForest1.ipynb      # Random Forest implementation and analysis
├── RandomForest2.ipynb      # Additional Random Forest analysis
├── randomForestt.py         # Custom Random Forest implementation
│
├── requirements.txt         # Project dependencies
├── .gitignore              # Git ignore file
└── README.md               # Project documentation
```

## Features

- **Multiple Models**: Implementation of various machine learning models for fraud detection:
  - Random Forest
  - Isolation Forest
  - Decision Tree
  - Hidden Markov Model
  
- **Custom Implementations**: Hand-crafted implementations of:
  - Decision Trees
  - Random Forests
  - Clustering Algorithms

- **Comprehensive Analysis**: Detailed analysis notebooks with:
  - Data preprocessing
  - Exploratory Data Analysis (EDA)
  - Model training and evaluation
  - Performance metrics visualization

## Requirements

- Python 3.7+
- Required packages listed in `requirements.txt`

## Datasets Required

This project requires the following datasets that are not included in the repository due to size and privacy considerations. After downloading, place them in the `data` directory as follows:

```
data/
├── creditcard.csv           # Dataset 1: Credit Card Fraud Detection dataset
├── fraudTrain.csv          # Dataset 2: Synthetic Financial Datasets (Training set)
└── fraudTest.csv           # Dataset 2: Synthetic Financial Datasets (Test set)
```

1. Credit Card Fraud Detection dataset from Kaggle:
   - Contains features V1-V30, Amount, and Class
   - Download from [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
   - Rename if needed to `creditcard.csv`
   - Place in the `data` directory

2. Synthetic Financial Datasets for Fraud Detection:
   - Download from [Kaggle Synthetic Financial Datasets For Fraud Detection](https://www.kaggle.com/kartik2112/fraud-detection)
   - Contains detailed transaction data including customer details, location, and merchant information
   - Download both files:
     * `fraudTrain.csv`: Training dataset
     * `fraudTest.csv`: Test dataset
   - Place both files in the `data` directory

Note: Make sure both files are placed directly in the `data` directory as shown in the structure above.

## Installation

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd credit-card-fraud-detection
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### 1. Data Preprocessing and EDA
- Run the notebooks in the `eda & preprocessing` folder:
  ```bash
  jupyter notebook "eda & preprocessing/EdaPreprocessing1.ipynb"
  ```

### 2. Running Different Models

#### Random Forest
```bash
jupyter notebook RandomForest1.ipynb
```
- Configurable parameters in the notebook:
  - Number of trees (50, 100, 150)
  - Minimum samples split (2, 5, 10)
  - Minimum samples leaf (1, 2, 5)

#### Isolation Forest
```bash
jupyter notebook isolationForest_1.ipynb
```
- Implements anomaly detection using Isolation Forest algorithm

#### Hidden Markov Model
```bash
python hidden_markov_main.py
```
- Uses HMM for sequence-based fraud detection
- Configure parameters in `config.py`

### 3. Model Evaluation

Each notebook includes comprehensive evaluation metrics:
- Accuracy
- Precision-Recall curves
- F1 Score
- Area Under Precision-Recall Curve (AUPR)

## Model Performance

The models have been evaluated on standard credit card fraud datasets. Key performance metrics:

- Random Forest:
  - High precision and recall balance
  - Good handling of imbalanced data using SMOTE

- Isolation Forest:
  - Effective at detecting anomalies
  - Unsupervised learning approach

- Hidden Markov Model:
  - Sequence-based detection
  - Good for temporal pattern recognition

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.