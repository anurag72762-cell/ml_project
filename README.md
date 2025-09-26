# 🏥 Health Insurance Premium Predictor

An intelligent and interactive web application built with **Streamlit** that predicts individual health insurance premiums using machine learning models. It analyzes user inputs like age, BMI, smoking status, income, and more to estimate the expected premium. A dual-model strategy ensures higher prediction accuracy by tailoring the algorithm to the user’s age group.

---

## 🌐 Live App  
👉 Try it live: [**Health Insurance Premium Predictor**](https://healthcare-insurance-prediction.streamlit.app/)

---

## 🔍 Key Features

- ✅ Clean, user-friendly Streamlit interface  
- 📈 Predicts insurance premium instantly using user-provided details  
- 🧠 Dual-model system for improved accuracy:  
  - **Linear Regression** for users aged ≤ 25  
  - **XGBoost Regressor** for users aged > 25  
- 📦 Pre-trained models and scalers for fast, real-time predictions  
- 🔎 Exploratory Data Analysis (EDA) & data preprocessing included in development phase  
- 🧪 Hyperparameter tuning and model evaluation  
- 🧩 No backend server or database required – lightweight and easy to run locally

---

## ⚙️ Tech Stack

- **Frontend & Deployment**: Streamlit  
- **Machine Learning**: Scikit-Learn, XGBoost  
- **Data & Visualization**: Pandas, NumPy, Matplotlib, Seaborn  
- **Model Persistence**: Joblib

---

## 📂 Project Structure

```
Health_Insurance_Cost_Predictor/
│
├── artifacts/                      # Serialized models and scalers
│   ├── model_rest.joblib           # XGBoost model for age > 25
│   ├── model_young.joblib          # Linear Regression model for age ≤ 25
│   ├── scaler_rest.joblib          # Scaler for general population
│   └── scaler_young.joblib         # Scaler for younger population
│
├── LICENSE                         # Apache License
├── README.md                       # Project documentation
├── main.py                         # Streamlit app interface
├── prediction_helper.py            # Prediction logic
└── requirements.txt                # Required Python packages
```

---

## 📊 Machine Learning Workflow

1. **Dataset**  
   - Public dataset with demographic and health-related features used to estimate insurance costs.

2. **EDA & Feature Engineering**  
   - Distribution analysis, correlation checks  
   - Handling missing values and encoding categorical variables

3. **Model Building & Selection**  
   - Trained multiple ML algorithms (Linear Regression, XGBoost, Random Forest)  
   - Selected the best models based on RMSE, MAE  
   - Applied segmentation:
     - Age ≤ 25 → Linear Regression
     - Age > 25 → XGBoost

4. **Model Deployment**  
   - Serialized models and scalers using `joblib`  
   - Integrated with Streamlit for real-time prediction

---

## 🧠 Input Features Used

- Age (in years)  
- Gender (Male/Female)  
- Marital Status  
- Income (in Lakhs)  
- Employment Status  
- Number of Dependents  
- Smoking Status  
- BMI Category (Underweight, Normal, Overweight, Obese)  
- Genetical Risk (0–3 scale)  
- Insurance Plan Type (Bronze/Silver/Gold)  
- Region (Northeast, Northwest, Southeast, Southwest)  
- Medical History (Has Disease / No Disease)

---

## 🚀 How to Run Locally

### Prerequisites  
- Python 3.8+

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/your-username/Health-Insurance-Premium-Predictor.git
cd Health-Insurance-Premium-Predictor

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the Streamlit app
streamlit run main.py
```

---

## 📄 License

This project is licensed under the **Apache License 2.0**. See the [LICENSE](./LICENSE) file for more information.

---

### 💡 Final Note

> “Don’t guess—predict. Discover your insurance premium with smart insights.”
