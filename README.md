# 🎓 Students Performance Regression

A lightweight notebook project that predicts students’ **Math, Reading, and Writing** scores using simple linear‑regression models built with Keras/TensorFlow.

---

## 📁 Project structure
StudentsPerformance.ipynb   # Main notebook (EDA → models → predictions)
StudentsPerformance.csv     # Raw dataset (1 000 rows × 8 columns)
requirements.txt            # Python dependencies
LICENSE                     # MIT License text
README.md                   # You’re reading it

🔍 What’s inside?
| Section                              | Key points                                                                                                                                                             |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Exploratory Data Analysis**     | Unique category counts, descriptive statistics, correlation matrix                                                                                                     |
| **2. Feature Engineering**           | One‑hot encoding of categorical features; clean numeric column names (`reading_score`, `math_score`, …)                                                                |
| **3. Modelling**                     | Three independent linear models *(Dense (1))*: <br> • `math_score ⇐ reading + writing` <br> • `reading_score ⇐ math + writing` <br> • `writing_score ⇐ reading + math` |
| **4. Evaluation & Helper Functions** | Custom prediction tables, L1 loss, RMSE plots, scatter “predicted vs. actual” diagnostics                                                                              |

Typical training RMSE after 30 epochs (train‑set):
| Target  | RMSE  |
| ------- | ----- |
| Math    | ≈ 8.7 |
| Reading | ≈ 8.5 |
| Writing | ≈ 8.9 |

🚀 Quick start
# 1. Install dependencies
python -m venv .venv
source .venv/bin/activate            # Windows ➜ .venv\Scripts\activate
pip install -r requirements.txt

# 2. Launch notebook
jupyter notebook StudentsPerformance.ipynb
