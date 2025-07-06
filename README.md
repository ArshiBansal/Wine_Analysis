<h1 align="center">🍷 Red Wine Quality Predictor & Analytics</h1>
---
# Overview 📊

This Streamlit-based web application offers a robust platform for analyzing and predicting red wine quality using machine learning. Powered by the UCI Red Wine Quality dataset, it provides interactive visualizations, model performance metrics, feature importance insights, and quality predictions based on physicochemical properties. Ideal for winemakers, sommeliers, and wine enthusiasts seeking data-driven insights.

---

# Features ⚡

- 📈 Market Overview: Visualize quality distributions, feature comparisons, and metrics like average quality and alcohol content
- 🔮 Quality Predictions: Predict wine quality (3–8) using a Random Forest Classifier
- 📊 Visualizations: Interactive histograms, box plots, KDE plots, and correlation matrices
- 🧠 Model Performance: Assess accuracy, precision, recall, F1-score, and confusion matrices
- 💡 Advanced Insights: Explore feature importance, SHAP analysis, raw data, and export options
- 🎛️ Custom Filters: Filter by quality, alcohol, volatile acidity, sulphates, citric acid, pH, and density
- 🎨 Theme Support: Choose Light, Dark, or Modern Blue themes for a tailored experience
- 🍷 Recommendations: Identify high-quality wines based on user-defined quality thresholds

---

# Technologies Used 🛠️

### 🐍 Python Libraries:

- Streamlit – Interactive UI framework
- Pandas, NumPy – Data manipulation and processing
- Plotly, Seaborn, Matplotlib – Data visualizations
- Scikit-learn – Machine learning and preprocessing
- SHAP – Model interpretability and feature importance

### 📦 Machine Learning Models:

-Random Forest Classifier – 100 estimators for quality prediction

### 🔄 Data Processing:

- `@st.cache_data`, `@st.cache_resource` – Efficient caching for data and models
- StandardScaler – Feature scaling
- Train-test split – 80-20 split with stratification

### 🧾 Logging:

- Python’s `logging` module for tracking and debugging  

---

# Installation 🧩

```bash
git clone https://github.com/ArshiBansal/red-wine-quality-predictor.git
cd red-wine-quality-predictor
```

---

# Data Requirements 📂

- Dataset: `winequality-red.csv` (UCI Red Wine Quality dataset) 
- **Key Columns**:  
  - fixed acidity
  - volatile acidity
  - citric acid
  - residual sugar
  - chlorides
  - free sulfur dioxide
  - total sulfur dioxide
  - density
  - pH
  - sulphates
  - alcohol
  - quality

### 🧠 Feature Engineering Includes:
- `Sales Ratio` – Ratio of Sale Amount to Assessed Value  
- `PriceToYearlyMedian` – Comparison to annual town median  
- `TownPricePremium` – Premium over town average  
- `PotentialFlip` – Flip potential flag for investments  

---

# Usage Guide 🚀

 **Launch App**:  
  ```bash
  streamlit run app.py
  ```
 ### 🔎 Apply Filters

Use the sidebar to filter the dataset by:

🍷 Quality Range (3–8)
🍸 Alcohol (%)
⚗️ Volatile Acidity (g/L)
🧪 Sulphates (g/L)
🍋 Citric Acid (g/L)
⚖️ pH
💧 Density (g/cm³)
Click Apply Filters to update or Reset Filters to revert to defaults

### 🧭 Explore Tabs

📈 Market Overview – View quality distributions and feature impacts via histograms, box plots, or KDE plots
🔮 Quality Prediction – Input physicochemical properties to predict wine quality and see similar wines
📉 Model Performance – Review accuracy, precision, recall, F1-score, and confusion matrices
💡 Advanced Insights – Explore raw data, summary statistics, correlation matrices, and download data
🍷 Recommendations – Set a quality threshold for high-quality wine recommendations

### 🧪 Train Models
Click the Train Model button to train the Random Forest Classifier on the filtered dataset. Results are cached for efficiency.

### 📥 Download
Export filtered data as a .csv file from the Advanced Insights tab.

---

# Notes 📝

- 📦 **Caching**  
  Cached dataset stored at: `./cache/processed_real_estate_data.pkl` for faster load times  

- 🧭 **Coordinates**  
  If `Location` is missing, fallback lat/lon values are auto-generated (e.g., within Connecticut)

- 🔢 **Training Requirements**  
  At least **50 valid records** required to enable training

- 🎨 **Themes**  
  Users can select **Light**, **Dark**, or **Modern Blue** UI themes via sidebar

- 🧼 **Error Handling**  
  - Configured with Python’s `logging` module for diagnostics  
  - Graceful fallback alerts for missing columns or corrupt records  

---

# Limitations ⚠️

i. Requires a valid winequality-red.csv with all essential columns.

ii. Model performance varies with filtered dataset size and quality.

iii. SHAP analysis can be computationally intensive for large datasets.

iv. Predictions are constrained to the dataset’s quality scale (3–8).

v. No real-time data updates or external API integration.

---

# Future Improvements 🔮

- 🔄 Support additional datasets (e.g., white wine quality).
- ⚙️ Add hyperparameter tuning for the Random Forest Classifier.
- 📊 Include more visualization types (e.g., scatter plots, pair plots).
- 🌐 Integrate real-time data via APIs for dynamic updates.
- 🔍 Enhance recommendations with clustering or similarity metrics.
- 🔐 Add user authentication for saving filter preferences.
