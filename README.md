# 🩺 Liver Cirrhosis Stage Detection

## 📌 Objective
Build a machine learning system that predicts the **stage of liver damage** (liver cirrhosis) given patient medical data.

---

## 📊 Dataset
The dataset comes from a **Mayo Clinic study on primary biliary cirrhosis (PBC)** of the liver, carried out between **1974–1984**.  
It contains patient demographics, clinical observations, and laboratory measurements.

### **Source**
- **Study Period:** 1974–1984  
- **Location:** Mayo Clinic  
- **Target Variable:** `Stage` (histologic stage of disease: 1, 2, or 3)

---

## 📄 Column Descriptions

| Column         | Description |
|----------------|-------------|
| **N_Days**     | Days between registration and death, transplantation, or study end in 1986 |
| **Status**     | Patient status: `C` (censored), `CL` (censored due to liver transplantation), `D` (death) |
| **Drug**       | Type of drug administered: `D-penicillamine` or `placebo` |
| **Age**        | Age in days |
| **Sex**        | `M` (male) or `F` (female) |
| **Ascites**    | Presence of ascites: `N` (No) or `Y` (Yes) |
| **Hepatomegaly** | Presence of hepatomegaly: `N` (No) or `Y` (Yes) |
| **Spiders**    | Presence of spider angiomas: `N` (No) or `Y` (Yes) |
| **Edema**      | `N` (no edema and no diuretics), `S` (edema resolved with diuretics), `Y` (edema despite diuretics) |
| **Bilirubin**  | Serum bilirubin in mg/dl |
| **Cholesterol**| Serum cholesterol in mg/dl |
| **Albumin**    | Albumin in gm/dl |
| **Copper**     | Urine copper in µg/day |
| **Alk_Phos**   | Alkaline phosphatase in U/liter |
| **SGOT**       | SGOT (a liver enzyme) in U/ml |
| **Triglycerides** | Triglycerides in mg/dl |
| **Platelets**  | Platelets per cubic ml/1000 |
| **Prothrombin**| Prothrombin time in seconds |
| **Stage**      | Histologic stage of disease (1, 2, or 3) |

---

## 🛠 Approach

1. **Data Preprocessing**
   - Handled missing values
   - Encoded categorical variables (`Sex`, `Ascites`, etc.)
   - Standardized numerical features

2. **Exploratory Data Analysis (EDA)**
   - Visualized feature distributions
   - Checked correlations with target variable
   - Identified important clinical patterns

3. **Modeling**
   - Used **Random Forest Classifier**
   - Hyperparameter tuning with Grid Search
   - 5-fold cross-validation for robust evaluation

4. **Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1-score
   - Feature importance analysis to identify key medical indicators

---

## 📈 Results
- **Model:** Random Forest Classifier  
- **Accuracy:** ~87%   
- **Top Features:** Bilirubin, Albumin, Prothrombin, Platelets, Age

---

## 🧰 Tech Stack
- **Python**: Data processing & modeling
- **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/liver-cirrhosis-stage-detection.git
cd liver-cirrhosis-stage-detection

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the notebook
jupyter notebook Liver_Cirrhosis_Stage_Detection.ipynb
