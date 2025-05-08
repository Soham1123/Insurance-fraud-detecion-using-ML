
# 🛡️ Insurance Fraud Detection System

This project implements a machine learning system to detect fraudulent insurance claims using a combination of classification models. It provides both a CLI and a Gradio-based web interface for ease of use.

## 📂 Project Structure

```
.
├── preprocess.py           # Data preprocessing script
├── predict.py              # Main prediction and UI script
├── models/                 # Trained models (KMeans, SVM, XGBoost)
│   └── metadata.sav        # Metadata including encoders, scaler, best model
├── data/
│   └── insurance_claims.csv  # Sample input data
├── processed/              # Output of preprocessed files
└── predictions.csv         # Output predictions
```

## ⚙️ Features

- **Preprocessing**: Cleans data, encodes categorical features, and scales numeric ones.
- **Models**: Trained on real-world insurance claim data using:
  - KMeans (unsupervised baseline)
  - Support Vector Machine (SVM)
  - XGBoost (best-performing model)
- **Model Selection**: Automatically uses the best model for predictions.
- **Gradio Interface**: Upload CSVs and get predictions with confidence scores.
- **CLI Mode**: For advanced or scripted usage.

## 🚀 Getting Started

### 1. Requirements

Install dependencies using:

```bash
pip install pandas numpy scikit-learn xgboost gradio joblib
```

### 2. Preprocess Your Data

```bash
python preprocess.py
```

This will generate a scaled CSV in the `processed/` directory.

### 3. Predict Using CLI

```bash
python predict.py
```

This will process `insurance_claims.csv` and save predictions to `predictions.csv`.

### 4. Use the Web Interface

```bash
python predict.py
```

Gradio will launch in your browser. Upload a CSV to get predictions and download results.

## 📊 Sample Output

The predictions include:

- `Predicted_Fraud`: Yes/No
- `Confidence`: Model's confidence (if available)

Example:

| PolicyType | Age | Predicted_Fraud | Confidence |
|------------|-----|------------------|------------|
| Sedan      | 45  | Yes              | 0.87       |
| SUV        | 35  | No               | 0.92       |

## 📁 Metadata

The system uses `metadata.sav` to load:

- Trained models
- Label encoders
- Standard scaler
- Best model info

## 👨‍💻 Author

Soham Choudhari  
B.Tech - Artificial Intelligence  
Email: sohamchoudhari1123@gmail.com

## 📜 License

This project is for educational and research purposes.
