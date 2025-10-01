<h1 align="center">📉 Customer Churn Prediction</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Machine%20Learning-Classification-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Accuracy-82%25-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Deployed%20With-Streamlit-red?style=for-the-badge" />
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
This project predicts whether a customer will <strong>churn (leave the company)</strong> or remain, based on demographics, account information, and service usage patterns.  
The system is powered by <strong>machine learning classification models</strong> and deployed with <strong>Streamlit</strong> for interactivity.
</p>

---

<h2>🗃️ Dataset Summary</h2>

<ul>
  <li><strong>Total Records:</strong> ~7,043</li>
  <li><strong>Total Features Used:</strong> 20+</li>
  <li><strong>Target Variable:</strong> Churn (Yes / No)</li>
  <li><strong>Missing Values:</strong> Cleaned and imputed</li>
</ul>

<h3>🔑 Input Features</h3>

<table>
  <thead>
    <tr>
      <th>Feature</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>gender</td><td>Male / Female</td></tr>
    <tr><td>SeniorCitizen</td><td>0 / 1 (binary)</td></tr>
    <tr><td>Partner</td><td>Yes / No</td></tr>
    <tr><td>Dependents</td><td>Yes / No</td></tr>
    <tr><td>tenure</td><td>Number of months with company</td></tr>
    <tr><td>PhoneService</td><td>Yes / No</td></tr>
    <tr><td>MultipleLines</td><td>Yes / No / No phone service</td></tr>
    <tr><td>InternetService</td><td>DSL / Fiber optic / No</td></tr>
    <tr><td>OnlineSecurity</td><td>Yes / No / No internet service</td></tr>
    <tr><td>OnlineBackup</td><td>Yes / No / No internet service</td></tr>
    <tr><td>TechSupport</td><td>Yes / No / No internet service</td></tr>
    <tr><td>StreamingTV</td><td>Yes / No / No internet service</td></tr>
    <tr><td>StreamingMovies</td><td>Yes / No / No internet service</td></tr>
    <tr><td>Contract</td><td>Month-to-month / One year / Two year</td></tr>
    <tr><td>PaperlessBilling</td><td>Yes / No</td></tr>
    <tr><td>PaymentMethod</td><td>Electronic check / Others</td></tr>
    <tr><td>MonthlyCharges</td><td>Customer's monthly bill</td></tr>
    <tr><td>TotalCharges</td><td>Total amount billed</td></tr>
  </tbody>
</table>

---

<h2>📊 Exploratory Data Analysis</h2>

<ul>
  <li>Higher churn among <strong>month-to-month contracts</strong></li>
  <li><strong>Fiber optic</strong> customers churn more than DSL</li>
  <li>Customers with <strong>higher monthly charges</strong> tend to churn more</li>
  <li>Visuals include countplots, histograms, bar charts, and correlation heatmaps</li>
</ul>

---

<h2>⚙️ Data Preprocessing</h2>

<ul>
  <li>Encoded categorical variables (Label Encoding / OneHot)</li>
  <li>Handled missing values (TotalCharges → numeric conversion)</li>
  <li>Scaled numerical features with <strong>StandardScaler</strong></li>
  <li>Balanced classes using <strong>SMOTE</strong></li>
</ul>

---

<h2>🧠 Model Training</h2>

<ul>
  <li><strong>Train/Test Split:</strong> 80% / 20%</li>
  <li><strong>Models Tested:</strong></li>
  <ul>
    <li>✔️ Logistic Regression</li>
    <li>🌲 Decision Tree</li>
    <li>🌳 Random Forest</li>
    <li>🤖 KNN</li>
    <li>🧬 XGBoost</li>
  </ul>
  <li><strong>Best Accuracy:</strong> <code>82%</code> with Random Forest</li>
</ul>

---

<h2>🌐 Streamlit Web Application</h2>

<ul>
  <li>User-friendly churn prediction form</li>
  <li>Interactive feature inputs for real-time prediction</li>
  <li>Visual results: "Customer Likely to Churn" / "Customer Retained"</li>
</ul>

<h3>🚀 Run Locally</h3>

```bash
# Clone repo
git clone https://github.com/your-username/customer-churn-prediction.git
cd customer-churn-prediction

# Install dependencies
pip install -r requirements.txt

# Start the app
streamlit run app.py
