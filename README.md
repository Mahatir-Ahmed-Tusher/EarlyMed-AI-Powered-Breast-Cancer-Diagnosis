![logo](https://github.com/user-attachments/assets/eedf8d57-ee5b-47d4-acdb-72aa859fcde6)


# EarlyMed-AI-Powered-Breast-Cancer-Diagnosis

EarlyMed is a web-based AI-driven tool for breast cancer detection. It analyzes clinically significant cell features to predict whether a sample is **benign (non-cancerous) or malignant (cancerous)**. The model is trained on a well-structured dataset and deployed on **Render** for public access.

## 🌐 Live Web App

👉 [EarlyMed - Breast Cancer Prediction](https://earlymed-breast-cancer-diagnosis.onrender.com/)

---

## 📌 Project Overview
Early detection of breast cancer can significantly improve patient outcomes. EarlyMed uses **machine learning (ML) models** to assist in diagnosis by analyzing cytology reports and cell morphology data.

### ✨ Features:
- Predicts **benign** or **malignant** stages based on cell features.
- Uses **Fine Needle Aspiration (FNA) biopsy data**.
- Easy-to-use web interface with user-friendly input fields.
- Deployed on **Render**, making it accessible online.

---

## 📊 Dataset
We used a well-curated dataset containing **clinically significant features** of breast cancer cells obtained from FNA biopsies. Each sample includes:
- **Clump Thickness** (Cell group density)
- **Uniform Cell Size & Shape** (Consistency in cell sizes and shapes)
- **Marginal Adhesion** (How well cells stick together)
- **Single Epithelial Cell Size** (Size of normal epithelial cells)
- **Bare Nuclei** (Presence of bare nuclei in the sample)
- **Bland Chromatin** (Chromatin texture in nuclei)
- **Normal Nucleoli** (Size and shape of nucleoli in the nucleus)
- **Mitoses** (Rate of cell division)

These features are essential in determining whether the cells are cancerous.

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

---

## 🚀 Deployment
The web app is hosted on **Render**, making it accessible from anywhere. Simply visit:
👉 **[EarlyMed Web App](https://apx.render.app)**

### How to Use the Web App?
1. Open the web app.
2. Enter the required values obtained from a **cytology report** or **microscopic analysis**.
3. Click on the **Predict** button.
4. The AI will classify the sample as **benign** or **malignant** instantly.

✅ *Note: This tool is for informational purposes only. Always consult a medical professional for a confirmed diagnosis.*

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
git clone https://github.com/Mahatir-Ahmed-Tusher/EarlyMed-Breast-Cancer-Detection.git
cd EarlyMed-Breast-Cancer-Detection

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

## 📧 Contact
For queries, contact **Mahatir Ahmed Tusher**:
- **GitHub**: [Mahatir-Ahmed-Tusher](https://github.com/Mahatir-Ahmed-Tusher)
- **LinkedIn**: [Mahatir Ahmed Tusher](https://in.linkedin.com/in/mahatir-ahmed-tusher-5a5524257)

🚀 *Early detection saves lives—Let AI help you make informed decisions!*
