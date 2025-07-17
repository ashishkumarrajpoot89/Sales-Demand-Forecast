# 🛒 Sales Demand Forecast

This project aims to build a robust, end-to-end machine learning pipeline to forecast product sales demand. Leveraging advanced data preprocessing, feature engineering, model training, evaluation, and deployment, this system enables businesses to predict future demand and make data-driven inventory and supply chain decisions.

---

## 📌 Problem Statement

The objective is to predict future sales demand for products based on historical data. By forecasting sales, businesses can reduce overstock, prevent stockouts, and optimize their inventory management strategy.

---

## 📂 Folder Structure

```
Sales-Demand-Forecast/
│
├── application_logging/             # Logging for training and prediction
├── best_model_finder/               # Model selection logic
├── data_files/                      # Input dataset files
├── data_ingestion/                  # Data loading modules
├── data_preprocessing/             # Data cleaning and transformation
├── file_operations/                # Model save/load utilities
├── models/                          # Trained ML models
├── preprocessing_data/             # Feature engineering scripts
│
├── Training_Batch_Files/           # New training data files
├── Training_Raw_data_validation/   # Raw training data validation
├── DataTypeValidation_Insertion_Training/
├── Training_FileFromDB/
├── Training_Database/
├── TrainingArchiveBadData/
├── Training_Logs/
│
├── Prediction_Batch_files/         # New prediction data files
├── Prediction_Raw_Data_Validation/ # Raw prediction data validation
├── DataTypeValidation_Insertion_Prediction/
├── Prediction_FileFromDB/
├── Prediction_Database/
├── PredictionArchivedBadData/
├── Prediction_Logs/
├── Prediction_Output_File/
│
├── main.py                          # Training script
├── predictFromModel.py             # Inference script
├── trainingModel.py                # Model training orchestration
├── prediction_Validation_Insertion.py
├── training_Validation_Insertion.py
│
├── schema_training.json            # Training data schema
├── schema_prediction.json          # Prediction data schema
├── Procfile / runtime.txt / manifest.yml  # Deployment configs
├── flask_monitoringdashboard.db    # Flask dashboard DB
├── README.md
└── .gitignore
```

---

## ⚙️ Setup and Installation

1. **Clone the Repository**

```bash
git clone https://github.com/ashishkumarrajpoot89/Sales-Demand-Forecast.git
cd Sales-Demand-Forecast
```

2. **Create a Virtual Environment**

```bash
python -m venv venv
source venv/bin/activate   # for Linux/Mac
venv\Scripts\activate      # for Windows
```

3. **Install Dependencies**

```bash
pip install -r requirements.txt
```

4. **Run Training**

```bash
python main.py
```

5. **Run Prediction**

```bash
python predictFromModel.py
```

---

## 🔍 Project Highlights

* **Data Validation**: Schema-based validation of training and prediction files.
* **Data Transformation**: Null handling, categorical encoding, and scaling.
* **Model Selection**: Automatic best model selection using evaluation metrics.
* **Logging**: Every operation is logged for traceability.
* **Deployment Ready**: Includes `Procfile`, `runtime.txt`, and dashboard DB for cloud hosting (e.g., Heroku).

---

## 📈 Tech Stack

* **Python**
* **Scikit-learn**
* **Pandas, NumPy**
* **Flask** (for deployment)
* **Logging & Monitoring**
* **Heroku (Deployment-Ready)**

---

## 🤝 Contribution

Feel free to fork this repo, raise issues, or submit PRs. For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is open-source and free to use under the [MIT License](LICENSE).
