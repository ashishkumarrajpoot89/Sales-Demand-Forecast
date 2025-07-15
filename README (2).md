# 🛒 Sales Prediction Model for Retail Products

## 📌 Problem Statement
Build a predictive model to estimate the **sales of each product** at a particular store using historical sales data.

---

## 🏗️ Project Architecture

The end-to-end pipeline includes:
- Data validation and preprocessing
- Database storage and management
- Model training using clustering and regression
- Deployment via Pivotal Web Services

---

## 🧾 Dataset Description

| Feature | Description |
|--------|-------------|
| `Item_Identifier` | Unique product ID |
| `Item_Weight` | Weight of the product |
| `Item_Fat_Content` | Low fat or not |
| `Item_Visibility` | % of display area for the product |
| `Item_Type` | Category of the product |
| `Item_MRP` | Maximum Retail Price |
| `Outlet_Identifier` | Unique store ID |
| `Outlet_Establishment_Year` | Store establishment year |
| `Outlet_Size` | Store ground area size |
| `Outlet_Location_Type` | City type where store is located |
| `Outlet_Type` | Grocery or supermarket |
| `Item_Outlet_Sales` | Target variable: Product sales in the store |

---

## 🧪 Data Validation

Performed based on the `schema` file provided by the client:

- ✅ **File Name Validation** using regex
- ✅ **Column Count Validation**
- ✅ **Column Names Validation**
- ✅ **Data Type Check**
- ✅ **Missing Value Check**

Files are sorted into:
- `Good_Data_Folder`
- `Bad_Data_Folder`

---

## 🗃️ Database Management

- Creation of SQL database
- Insertion of validated data into the `Good_Data` table
- Handling of invalid entries

---

## 🧠 Model Training Pipeline

1. **Data Export** from database to CSV
2. **Preprocessing**:
   - Null value imputation (KNN imputer)
   - Log transformation
   - Feature scaling
3. **Clustering** using KMeans + KneeLocator
4. **Model Selection** per cluster:
   - Algorithms: `Random Forest Regressor`, `Linear Regression`
   - Best model chosen via GridSearch & R² score
5. **Model Saving** for future predictions

---

## 📈 Prediction Workflow

1. Data batch from client is validated
2. Preprocessing (same as training)
3. Clustering based on trained KMeans model
4. Prediction using the corresponding cluster model
5. Output saved with original (unencoded) values in a CSV

---

## 🚀 Deployment: Pivotal Web Services

- **App Files:**
  - `main.py`: Flask app entry point
  - `predictionFromModel.py`: Handles predictions
  - `manifest.yml`: Instance/app config
  - `Procfile`: Declares app start command
  - `runtime.txt`: Python version

- **Deployment Steps:**
  1. Sign up on [Pivotal Web Services](https://pivotal.io/platform)
  2. Install Cloud Foundry CLI
  3. Use `cf login -a https://api.run.pivotal.io`
  4. Navigate to your project folder
  5. Deploy using: `cf push`

---

## 🧾 Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

---

## 🧪 Example Usage with Postman

After deployment, you can test predictions using **Postman** with the API endpoint provided by Pivotal.

---

## 📂 Project Structure

```
├── Good_Data_Folder/
├── Bad_Data_Folder/
├── database/
├── models/
├── predictionFromModel.py
├── main.py
├── manifest.yml
├── Procfile
├── requirements.txt
├── runtime.txt
└── README.md
```

---

## 📞 Contact

For questions or support, feel free to reach out via LinkedIn or GitHub Issues.
