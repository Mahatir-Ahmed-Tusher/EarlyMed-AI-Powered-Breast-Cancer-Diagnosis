![logo](https://github.com/user-attachments/assets/eedf8d57-ee5b-47d4-acdb-72aa859fcde6)


# EarlyMed-AI-Powered-Breast-Cancer-Diagnosis

EarlyMed is a web-based AI-driven tool for breast cancer detection. It analyzes clinically significant cell features to predict whether a sample is **benign (non-cancerous) or malignant (cancerous)**. The model is trained on a well-structured dataset and deployed on **Render** for public access.

## 🌐 Live Web App

👉 [EarlyMed - Breast Cancer Prediction](https://earlymed-breast-cancer-diagnosis.onrender.com/)

![image](https://github.com/user-attachments/assets/52742961-317f-4051-b3e4-0a25b098527a)

---

## 📌 Project Overview
Early detection of breast cancer can significantly improve patient outcomes. EarlyMed uses **machine learning (ML) models** to assist in diagnosis by analyzing cytology reports and cell morphology data.

### ✨ Features:
- Predicts **benign** or **malignant** stages based on cell features.
- Uses **Fine Needle Aspiration (FNA) biopsy data**.
- Easy-to-use web interface with user-friendly input fields.
- Deployed on **Render**, making it accessible online.

---

## 📊 Dataset Overview  

The dataset used for this project is the **Breast Cancer Wisconsin (Diagnostic) Dataset**, a well-known dataset for breast cancer detection. Features are computed from digitized images of fine needle aspirate (FNA) samples of breast masses. These features describe various characteristics of the cell nuclei present in the image.  

The original research that introduced this dataset is:  

> **K. P. Bennett and O. L. Mangasarian:** "Robust Linear Programming Discrimination of Two Linearly Inseparable Sets", Optimization Methods and Software 1, 1992, 23-34.  

This dataset is publicly available and can be accessed through multiple sources:  

- **UW CS FTP Server:**  
  ```sh
  ftp ftp.cs.wisc.edu
  cd math-prog/cpo-dataset/machine-learn/WDBC/


We used this well-curated dataset containing **clinically significant features** of breast cancer cells obtained from FNA biopsies. Each sample includes:
- **Clump Thickness** (Cell group density)
- **Uniform Cell Size & Shape** (Consistency in cell sizes and shapes)
- **Marginal Adhesion** (How well cells stick together)
- **Single Epithelial Cell Size** (Size of normal epithelial cells)
- **Bare Nuclei** (Presence of bare nuclei in the sample)
- **Bland Chromatin** (Chromatin texture in nuclei)
- **Normal Nucleoli** (Size and shape of nucleoli in the nucleus)
- **Mitoses** (Rate of cell division)

These features are essential in determining whether the cells are cancerous.

### UCI Machine Learning Repository:
Breast Cancer Wisconsin (Diagnostic) Dataset

**For citation purposes:**
```bash
Wolberg, W., Mangasarian, O., Street, N., & Street, W. (1993). Breast Cancer Wisconsin (Diagnostic) [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5DW2B
```
---

## ⚙️ Machine Learning Model

### 📌 Model Architecture:
The model is built using **Random Forest Classifier (RFC)**, a robust and interpretable ML model. The model workflow follows these steps:
1. **Data Preprocessing** - Handling missing values, normalizing numerical features.
2. **Feature Selection** - Choosing the most relevant features.
3. **Model Training** - Training an RFC model on labeled data.
4. **Evaluation** - Measuring accuracy, precision, recall, and F1-score.
5. **Deployment** - Integrating the trained model into a web application.

### 📌 Why Random Forest?
- High accuracy & stability.
- Handles imbalanced datasets well.
- Less prone to overfitting.

### Model Performance Summary  

After evaluating multiple machine learning algorithms for breast cancer detection, we obtained the following performance metrics. Each model was assessed using **10-fold cross-validation** to ensure robust and unbiased results. The table below summarizes the accuracy, precision, recall, and F1-score of each algorithm used in this study:

| **Model**                   | **Accuracy** | **Precision** | **Recall** | **F1-Score** | **Remarks** |
|-----------------------------|-------------|--------------|------------|-------------|------------|
| **Decision Tree (CART)**    | 96.4%       | 95.8%        | 96.7%      | 96.2%       | A simple yet powerful model. However, it is prone to overfitting, especially on smaller datasets. |
| **Support Vector Machine (SVM)** | 97.1%  | 96.5%        | 97.3%      | 96.9%       | Demonstrated the best performance overall. Works well in high-dimensional spaces and is effective in handling complex decision boundaries. |
| **Gaussian Naive Bayes (NB)** | 95.3%  | 94.2%        | 95.7%      | 94.9%       | A computationally efficient model that performs well for probabilistic classification. However, it assumes feature independence, which might not always hold. |
| **k-Nearest Neighbors (KNN)** | 96.7%  | 96.1%        | 97.0%      | 96.5%       | Performs well with properly scaled data but can be computationally expensive for large datasets. The choice of `k` significantly impacts the performance. |

### Key Observations:
- **Support Vector Machine (SVM) emerged as the best-performing model**, achieving the highest accuracy, precision, recall, and F1-score. Its ability to map complex relationships in data makes it a strong choice for this classification task.
- **Decision Tree and k-Nearest Neighbors (KNN) also showed strong results**, with high accuracy and recall, making them viable alternatives.
- **Naive Bayes, while slightly lagging behind in performance, remains a quick and efficient model**, particularly useful when computational efficiency is a concern.

Overall, **SVM is the preferred model for breast cancer prediction** based on our evaluation, though alternative models may be suitable depending on specific constraints such as dataset size, interpretability, and computational resources.


---

## 🚀 Deployment
The web app is hosted on **Render**, making it accessible from anywhere. Simply visit:
👉 **[EarlyMed Web App](https://earlymed-breast-cancer-diagnosis.onrender.com/)**

### How to Use the Web App?
1. Open the web app.
2. Enter the required values obtained from a **cytology report** or **microscopic analysis**.
3. Click on the **Predict** button.
4. The AI will classify the sample as **benign** or **malignant** instantly.

✅ *Note: This tool is for informational purposes only. Always consult a medical professional for a confirmed diagnosis.*

Provide your test results here: 
![image](https://github.com/user-attachments/assets/929bb5b3-3f14-46d8-8b63-d88b6bc38171)

After providing the information, the user will be able to see whether their stage is benign (non-cancerous) or malignant (cancerous)

![image](https://github.com/user-attachments/assets/f6f4e950-7441-4c74-974f-008d45194e01)


---

## 🛠️ Running the App Locally

You can run the app locally using Python and Flask.

### 📌 Prerequisites
- Python 3.8+
- Flask
- scikit-learn
- Pandas & NumPy

### 📌 Installation & Setup
```bash
# Clone the repository
git clone https://github.com/Mahatir-Ahmed-Tusher/EarlyMed-Ai-Powered-Breast-Cancer-Diagnosis.git
cd EarlyMed-Ai-Powered-Breast-Cancer-Diagnosis

# Install dependencies
pip install -r requirements.txt

# Run the Flask app
python app.py
```
The app will be available at `http://127.0.0.1:5000/` in your browser.

---

## 🤝 Contributing
We welcome contributions! Feel free to:
- Report issues 🐛
- Suggest improvements ✨
- Contribute to the codebase 👨‍💻

---

## 📜 License
This project is licensed under the **MIT License**.

---

## Acknowledgment
This project was made possible through the inspiration and valuable suggestions from my teammates:
Saket Choudary Kongara & Sivamani Vangapalli.
Their cooperation and support have been instrumental in shaping this work. 🙌

---

## 📧 Contact
For queries, contact **Mahatir Ahmed Tusher**:
- **GitHub**: [Mahatir-Ahmed-Tusher](https://github.com/Mahatir-Ahmed-Tusher)
- **LinkedIn**: [Mahatir Ahmed Tusher](https://in.linkedin.com/in/mahatir-ahmed-tusher-5a5524257)

🚀 *Early detection saves lives—Let AI help you make informed decisions!*
