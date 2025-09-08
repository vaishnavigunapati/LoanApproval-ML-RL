# 📊 Loan Approval Prediction & Policy Optimization

## 🌟 Overview
This project focuses on improving loan approval decisions using two approaches:  

1. **Deep Learning (MLP)** → Predicts whether a loan will default or be fully paid.  
2. **Offline Reinforcement Learning (RL)** → Learns a policy to approve or deny loans to maximize financial profit.  

The dataset comes from **LendingClub (2007–2018 accepted loans)**.  
Since the data is large, it’s not uploaded here — instead, you can download it from Kaggle:  
👉 [LendingClub Loan Data (Kaggle)](https://www.kaggle.com/datasets/wordsforthewise/lending-club)

---

## 📂 Project Structure

Loan-Approval-Project/
├── notebooks/
│ ├── 1_EDA_Preprocessing.ipynb # Data cleaning + feature engineering
│ ├── 2_DL_Model.ipynb # Deep Learning model (PyTorch MLP)
│ ├── 3_RL_Agent.ipynb # Offline RL agent (d3rlpy DiscreteBC)
│ └── 4_Comparison.ipynb # DL vs RL results and insights
├── dataset.ipynb # Raw dataset exploration
├── requirements.txt
└── README.md

yaml
Copy code

---

## ⚙️ Setup Instructions

1. **Clone the repo**
```bash
git clone https://github.com/your-username/loan-approval-project.git
cd loan-approval-project
Create virtual environment

bash
Copy code
python -m venv venv
Activate environment

Windows:

bash
Copy code
venv\Scripts\activate
Mac/Linux:

bash
Copy code
source venv/bin/activate
Install dependencies

bash
Copy code
pip install -r requirements.txt
Download dataset

Get accepted_2007_to_2018.csv from Kaggle.

Place it in:

bash
Copy code
Loan-Approval-Project/data/accepted_2007_to_2018.csv
🚀 How to Run
🔍 Step 1: Exploratory Data Analysis (EDA)
Run:

bash
Copy code
jupyter notebook notebooks/1_EDA_Preprocessing.ipynb
Cleans and preprocesses data.

Handles missing values, encodes categorical features, scales numeric ones.

🤖 Step 2: Deep Learning Model
Run:

bash
Copy code
jupyter notebook notebooks/2_DL_Model.ipynb
Trains a Multi-Layer Perceptron (MLP) using PyTorch.

Evaluates performance with AUC and F1-score.

🎯 Step 3: Reinforcement Learning Agent
Run:

bash
Copy code
jupyter notebook notebooks/3_RL_Agent.ipynb
Frames loan approval as an offline RL problem.

Trains a DiscreteBC agent (d3rlpy).

Evaluates with Estimated Policy Value.

⚖️ Step 4: Comparison
Run:

bash
Copy code
jupyter notebook notebooks/4_Comparison.ipynb
Compares DL vs RL.

Shows cases where they agree/disagree.

Discusses business impact.

📊 Results
Deep Learning (MLP):

AUC ≈ 0.70

F1 ≈ 0.41

RL Agent (DiscreteBC):

Estimated Policy Value ≈ 0.105 (expected profit per loan)

👉 Insight:

DL is better for risk prediction.

RL directly optimizes profit (sometimes approving riskier but rewarding loans).

A hybrid system could give the best outcome.

🔮 Future Work
Include rejected loans for less biased training.

Explore stronger RL algorithms (CQL, CRR).

Deploy a hybrid DL+RL system in production.

Continuously monitor performance and retrain with new data.

📖 References
Dataset: LendingClub Loan Data (Kaggle)

RL Library: d3rlpy Documentation

👩‍💻 Author
Vaishnavi Reddy Gunapati
📧 Email: gunapativaishnavi348@gmail.com







