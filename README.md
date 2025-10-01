<h1 align="center">📉 Customer Churn Prediction (ANN)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Deep%20Learning-ANN-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Accuracy-85%25-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Framework-TensorFlow%20%7C%20Keras-red?style=for-the-badge" />
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
This project predicts whether a customer will <strong>churn (leave the company)</strong> or stay, using an <strong>Artificial Neural Network (ANN)</strong>.  
The model was built with <strong>TensorFlow/Keras</strong> and achieved an accuracy of <strong>85%</strong>.  
The project also includes data preprocessing, exploratory data analysis (EDA), and deployment-ready code.
</p>

---

<h2>🗃️ Dataset Summary</h2>

<ul>
  <li><strong>Source:</strong> <a href="https://www.kaggle.com/blastchar/telco-customer-churn">Telco Customer Churn Dataset (Kaggle)</a></li>
  <li><strong>Total Records:</strong> 7,043</li>
  <li><strong>Features:</strong> 20+ demographic & service-related features</li>
  <li><strong>Target:</strong> Churn (Yes / No)</li>
  <li><strong>Missing Values:</strong> Cleaned (e.g., TotalCharges converted to numeric)</li>
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
    <tr><td>InternetService</td><td>DSL / Fiber optic / No</td></tr>
    <tr><td>OnlineSecurity</td><td>Yes / No / No internet service</td></tr>
    <tr><td>TechSupport</td><td>Yes / No / No internet service</td></tr>
    <tr><td>Contract</td><td>Month-to-month / One year / Two year</td></tr>
    <tr><td>PaymentMethod</td><td>Electronic check / Others</td></tr>
    <tr><td>MonthlyCharges</td><td>Customer's monthly bill</td></tr>
    <tr><td>TotalCharges</td><td>Total amount billed</td></tr>
  </tbody>
</table>

---

<h2>📊 Exploratory Data Analysis</h2>

<ul>
  <li>Churn rate is higher for <strong>month-to-month contracts</strong></li>
  <li>Customers with <strong>Fiber optic</strong> Internet churn more</li>
  <li>Higher <strong>MonthlyCharges</strong> correlates with higher churn</li>
  <li>Visuals include countplots, histograms, and heatmaps</li>
</ul>

---

<h2>⚙️ Data Preprocessing</h2>

<ul>
  <li>Converted <code>TotalCharges</code> to numeric and handled nulls</li>
  <li>Encoded categorical features with <strong>LabelEncoder & OneHot</strong></li>
  <li>Standardized numerical features with <strong>StandardScaler</strong></li>
  <li>Balanced dataset using <strong>SMOTE</strong></li>
</ul>

---

<h2>🧠 Model Training (ANN)</h2>

<ul>
  <li><strong>Train/Test Split:</strong> 80% / 20%</li>
  <li><strong>Architecture:</strong></li>
  <ul>
    <li>Input layer → 20+ features</li>
    <li>Hidden layers with ReLU activation</li>
    <li>Dropout for regularization</li>
    <li>Output layer with sigmoid activation (binary classification)</li>
  </ul>
  <li><strong>Optimizer:</strong> Adam</li>
  <li><strong>Loss:</strong> Binary Crossentropy</li>
  <li><strong>Metrics:</strong> Accuracy</li>
  <li><strong>Best Accuracy:</strong> <code>85%</code></li>
</ul>

---

<h2>🌐 Streamlit Web Application (Optional)</h2>

<ul>
  <li>User form to input customer details</li>
  <li>Real-time churn prediction using ANN model</li>
  <li>Output: "Customer Likely to Churn" or "Customer Retained"</li>
</ul>

<h3>🚀 Run Locally</h3>

```bash
# Clone repo
git clone https://github.com/your-username/customer-churn-ann.git
cd customer-churn-ann

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook or Streamlit App
jupyter notebook Customer_Churn_ANN.ipynb
# OR
streamlit run app.py
