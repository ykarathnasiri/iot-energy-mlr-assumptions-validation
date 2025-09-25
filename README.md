# IoT Energy Consumption Prediction using Multiple Linear Regression

A comprehensive analysis of IoT sensor data to predict energy consumption changes using Multiple Linear Regression (MLR) with thorough assumption validation.

## 👥 Team Members
- W.A.C Fernando - 26545  
- R.T Dulmina - 27999  
- S.I.M.S Wimalasiri - 29785  
- M.A.P.M Premasiri - 26033  
- Y.K.A Rathnasiri - 27413

## 📋 Project Overview

This project analyzes an **IoT-based dataset** that records environmental and operational changes measured by sensors. The main objective is to understand how environmental factors influence energy consumption in IoT systems and build a reliable predictive model.

### Dataset Variables
- **Temperature Change (°C)** – variation in surrounding temperature  
- **Pressure Change (hPa)** – fluctuation in air pressure levels  
- **Speed Change (km/h)** – change in movement or flow speed  
- **Energy Change (kWh)** – variation in energy consumption (dependent variable)

## 🎯 Objectives

1. **Build a Multiple Linear Regression model** to predict energy consumption changes
2. **Validate all MLR assumptions** to ensure model reliability and accuracy
3. **Provide insights** for energy monitoring and optimization in IoT systems
4. **Create a reusable framework** for IoT energy prediction

## 📊 MLR Assumptions Validated

This project comprehensively tests all five key assumptions of Multiple Linear Regression:

### 1. **Linearity**
- **What it means**: Predictors should have a linear relationship with the dependent variable
- **Testing method**: Residuals vs Fitted values plot
- **Importance**: Ensures accurate coefficient interpretation
- **Fix if violated**: Apply transformations (log, polynomial) or use robust regression

### 2. **Independence**
- **What it means**: Each observation should be independent of others
- **Testing method**: Durbin-Watson test
- **Importance**: Prevents false correlation detection
- **Fix if violated**: Use time-series or GLS models

### 3. **Homoscedasticity**
- **What it means**: Residuals should have constant variance across all predicted values
- **Testing method**: Breusch-Pagan test and Scale-Location plot
- **Importance**: Ensures unbiased standard errors and reliable statistical inference
- **Fix if violated**: Apply transformations or use heteroscedasticity-robust errors

### 4. **Normality of Residuals**
- **What it means**: Residuals should follow a normal distribution
- **Testing method**: Shapiro-Wilk test, Q-Q plots, and histograms
- **Importance**: Validates confidence intervals and hypothesis tests
- **Fix if violated**: Transform data or apply non-parametric methods

### 5. **No Multicollinearity**
- **What it means**: Independent variables should not be highly correlated
- **Testing method**: Variance Inflation Factor (VIF)
- **Importance**: Ensures stable coefficients and clear variable effects
- **Fix if violated**: Remove/combine correlated predictors or use PCA

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **matplotlib & seaborn** - Data visualization
- **statsmodels** - Statistical modeling and assumption testing
- **scipy** - Statistical tests
- **pickle** - Model serialization

## 📁 Project Structure

```
IoT_Energy_Regression_Analysis/
├── IoT_Energy_Regression_Analysis.ipynb  # Main analysis notebook
├── dataset/
│   └── iot_dataset.csv                   # IoT sensor data
├── model/
│   └── iot_energy_model.pkl             # Trained MLR model
└── README.md                            # Project documentation
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn statsmodels scipy
```

### Running the Analysis

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd IoT_Energy_Regression_Analysis
   ```

2. **Open the Jupyter notebook**
   ```bash
   jupyter notebook IoT_Energy_Regression_Analysis.ipynb
   ```

3. **Run all cells** to reproduce the complete analysis

## 📈 Key Results

The analysis provides:

- **Model Performance Metrics**: R-squared, F-statistic, and coefficient significance
- **Assumption Validation Results**: Pass/fail status for each MLR assumption
- **Visual Diagnostics**: Comprehensive plots for assumption checking
- **Predictive Capability**: Trained model for new energy consumption predictions
- **Statistical Insights**: Understanding of how environmental factors affect energy usage

## 🔍 Analysis Workflow

1. **Data Loading & Preprocessing**
   - Load IoT dataset
   - Handle missing values
   - Rename columns for clarity

2. **Exploratory Data Analysis**
   - Distribution analysis
   - Correlation matrix
   - Summary statistics

3. **Model Training**
   - Fit Multiple Linear Regression model
   - Generate model summary

4. **Comprehensive Assumption Testing**
   - Linearity check with residual plots
   - Independence test using Durbin-Watson
   - Homoscedasticity test with Breusch-Pagan
   - Normality test with Shapiro-Wilk
   - Multicollinearity check with VIF

5. **Model Validation & Predictions**
   - Final assumption summary
   - Sample predictions
   - Model serialization

## 📊 Model Interpretation

The MLR model equation:
```
Energy_Change = β₀ + β₁(Temperature_Change) + β₂(Pressure_Change) + β₃(Speed_Change) + ε
```

Each coefficient represents the expected change in energy consumption for a one-unit change in the corresponding predictor, holding other variables constant.

## 🎯 Business Applications

- **Energy Management**: Predict energy needs based on environmental conditions
- **IoT Optimization**: Optimize sensor deployment and energy efficiency
- **Predictive Maintenance**: Anticipate energy consumption patterns
- **Cost Reduction**: Better energy planning and resource allocation

## 🔮 Future Enhancements

- **Time Series Analysis**: Incorporate temporal patterns
- **Feature Engineering**: Create interaction terms and polynomial features
- **Advanced Models**: Compare with Random Forest, SVM, or Neural Networks
- **Real-time Prediction**: Deploy model for live IoT data streams
- **Cross-validation**: Implement k-fold validation for robust performance assessment

## 📝 License

This project is created for educational purposes as part of a Big Data course analysis.

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for improvements or extensions to the analysis.

## 📞 Contact

For questions or suggestions, please reach out to any of the team members listed above.

---

**Note**: This project demonstrates best practices in statistical modeling by thoroughly validating all MLR assumptions, ensuring the reliability and interpretability of the predictive model.
