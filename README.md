# 🌱 WattWise Smart-Charging Analysis Dashboard

An interactive Data Product Manager tool designed to analyze A/B test results for EV smart-charging features in Western European markets (Germany, France, the United Kingdom, and the Netherlands).

## 📊 Project Overview
A real-world A/B test scenario in which a "Smart Charging" AI feature is tested against a manual baseline. The app provides a full analytical pipeline, moving from raw data simulation to statistical validation and financial impact projection.

## 🚀 Key Features
* **Automated Data Synthesis**: Generates normally distributed engagement data with injected anomalies to simulate real-world sensor errors.
* **Z-Score Outlier Detection**: Implements a $|Z| > 3$ filter to ensure data integrity by removing extreme charging session errors.
* **Statistical Rigor**: Calculates p-values using a two-proportion Z-test to determine the "Success Probability" of the feature.
* **Business Impact Modeling**: Translates technical "Lift" into projected annual revenue based on European energy tariffs.
* **Qualitative Sentiment**: Generates regional Word Clouds to visualize user feedback across different markets.

## 🛠️ Tech Stack
* **Language**: Python
* **Framework**: [Streamlit](https://streamlit.io/)
* **Data Science**: Pandas, NumPy, SciPy, Statsmodels
* **Visualization**: Plotly, WordCloud
* **Deployment**: Ngrok (for secure tunneling from Google Colab)
* **Reporting**: WeasyPrint (PDF Generation)

## 📦 Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone [https://github.com/cbonnin88/wattwise-ab-analysis.git](https://github.com/cbonnin88/wattwise-ab-analysis.git)
   cd wattwise-ab-analysis


## 🧪 Methodology
### Outlier Handling
To maintain accuracy, the app uses the Z-Score method. For a normal distribution, 99.7% of data falls within 3 standard deviations. Any data point exceeding this threshold is flagged as an anomaly and removed from the statistical calculations.



### Revenue Projection
Revenue is calculated using the formula:
`Revenue = Engagement (Hours) * Charging Speed (7.4 kWh) * Energy Price (€/kWh)`
