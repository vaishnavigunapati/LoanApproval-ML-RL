# LoanApproval-ML-RL


## 📌 Overview
This project explores how to make better loan approval decisions using both **Deep Learning (DL)** and **Offline Reinforcement Learning (RL)**.  

- **DL Model (MLP):** Predicts the probability of default for each applicant.  
- **RL Agent (DiscreteBC):** Learns an approval policy that balances profit vs risk.  

The business goal: **decide whether to approve or deny a loan to maximize financial returns**.

---

## 📂 Project Structure

Loan-Approval-Project/
├── notebooks/
│ ├── 1_EDA_Preprocessing.ipynb
│ ├── 2_DL_Model.ipynb
│ ├── 3_RL_Agent.ipynb
│ └── 4_Comparison.ipynb
├── d3rlpy_logs/ # RL training logs (auto-generated)
├── dataset.ipynb # raw dataset exploration
├── requirements.txt
└── README.md

yaml
Copy code

⚠️ **Note on Data:**  
The original dataset (`accepted_2007_to_2018.csv`) is **too large to upload to GitHub**.  
You can download it directly from Kaggle:  
👉 [LendingClub Loan Data on Kaggle](https://www.kaggle.com/datasets/wordsforthewise/lending-club)

---

## ⚙️ Setup Instructions

1. **Clone this repo**
```bash
git clone https://github.com/your-username/loan-approval-project.git
cd loan-approval-project
Create and activate environment

bash
Copy code
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/Mac
source venv/bin/activate
Install dependencies

bash
Copy code
pip install -r requirements.txt
Download dataset

Go to Kaggle and download accepted_2007_to_2018.csv.

Place it inside a folder named data/:

bash
Copy code
Loan-Approval-Project/data/accepted_2007_to_2018.csv
🚀 How to Run
1. Exploratory Data Analysis (EDA)
Run:

bash
Copy code
jupyter notebook notebooks/1_EDA_Preprocessing.ipynb
Cleans dataset, handles missing values, encodes categorical features, scales data.

Selects useful features for modeling.

2. Deep Learning Model
Run:

bash
Copy code
jupyter notebook notebooks/2_DL_Model.ipynb
Trains an MLP classifier in PyTorch.

Evaluates with AUC and F1-score.

3. Reinforcement Learning Agent
Run:

bash
Copy code
jupyter notebook notebooks/3_RL_Agent.ipynb
Frames loan approval as an offline RL problem.

Uses d3rlpy DiscreteBC algorithm.

Evaluates Estimated Policy Value (expected profit per loan).

4. Comparison & Analysis
Run:

bash
Copy code
jupyter notebook notebooks/4_Comparison.ipynb
Compares DL vs RL policies.

Shows where the models agree/disagree and their business impact.

📊 Key Results
Deep Learning Model (MLP):

AUC ≈ 0.70

F1 ≈ 0.41

RL Agent (DiscreteBC):

Estimated Policy Value ≈ 0.105 (profit per loan)

👉 Takeaway:

DL is good for predicting default risk.

RL directly optimizes profit, sometimes approving risky but profitable loans.

A hybrid DL + RL system could give the best outcome.

🔮 Future Improvements
Add rejected loans + more features (credit score history, repayment trends).

Explore stronger RL algorithms (CQL, CRR).

Deploy a hybrid DL–RL system for risk-aware profit optimization.

Monitor performance in production and retrain as market conditions change.

📖 References
Dataset: LendingClub Loan Data (Kaggle)

RL Framework: d3rlpy Documentation

👩‍💻 Author
Vaishnavi Reddy Gunapati
📧 Email: gunapativaishnavi348@gmail.com




