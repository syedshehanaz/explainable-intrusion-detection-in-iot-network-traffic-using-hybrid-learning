# explainable-intrusion-detection-in-iot-network-traffic-using-hybrid-learning


## Intrusion Detection System (IDS)

### Using MAE + DRL + SHAP and DAE + MARL + LIME

# 🔹 1. Introduction

This project is an Intrusion Detection System (IDS) designed to detect cyber-attacks in network traffic using Machine Learning and Reinforcement Learning.

It uses:

* Autoencoders (MAE / DAE) → Detect anomalies
* Reinforcement Learning (DRL / MARL) → Select threshold
* Explainable AI (SHAP / LIME) → Explain predictions

---

# 🔹 2. System Requirements

### Hardware:

* Minimum 4GB RAM (8GB recommended)

### Software:

* Python 3.8+
* Google Colab (Recommended)
* Browser (Chrome)

### Libraries:

* numpy
* pandas
* scikit-learn
* tensorflow / keras
* shap
* lime

---

# 🔹 3. Project Structure

```
IDS_Project/
│
├── dataset.csv
├── mae_drl_shap.ipynb
├── dae_marl_lime.ipynb
├── main.ipynb
└── README.md
```

---

# 🔹 4. How to Run the Project (Google Colab)

---

##  Step 1: Open Notebook

* Go to Google Colab
* Upload or open your `.ipynb` file

---

##  Step 2: Mount Google Drive

```python
from google.colab import drive
drive.mount('/content/drive')
```

---

##  Step 3: Load Dataset

```python
import pandas as pd

data = pd.read_csv('/content/drive/MyDrive/IDS_Project/dataset.csv')
```

---

##  Step 4: Install Dependencies

```python
!pip install shap lime stable-baselines3
```

---

##  Step 5: Preprocess Data

* Remove non-numeric columns
* Normalize data

```python
from sklearn.preprocessing import MinMaxScaler

data = data.select_dtypes(include=['number'])
scaler = MinMaxScaler()
data_scaled = scaler.fit_transform(data)
```

---

##  Step 6: Train Model

* Run all cells sequentially:

  * Autoencoder training
  * Error calculation
  * Threshold selection

---

##  Step 7: View Results

* Accuracy
* Predictions (Attack / Normal)
* Graphs (SHAP / LIME explanations)

---

# 🔹 5. Working of the System

```
Raw Data
   ↓
Preprocessing
   ↓
Autoencoder Training
   ↓
Reconstruction Error
   ↓
Threshold Selection (DRL / MARL)
   ↓
Prediction
   ↓
Explainability (SHAP / LIME)
```

---

# 🔹 6. Features

* Detects unknown cyber-attacks
* Works without labeled attack data (unsupervised learning)
* Uses AI to optimize detection
* Provides explanation for each prediction

---

# 🔹 7. Output Description

### ✔ Normal Traffic

* Low reconstruction error

### ✔ Attack Traffic

* High reconstruction error

### ✔ SHAP Output

* Shows feature importance globally

### ✔ LIME Output

* Explains individual predictions

---

# 🔹 8. Troubleshooting

| Issue                       | Solution          |
| --------------------------- | ----------------- |
| Dataset not loading         | Check file path   |
| SHAP slow                   | Use small sample  |
| Memory error                | Reduce batch size |
| Model not detecting attacks | Adjust threshold  |

---

# 🔹 9. Limitations

* Requires proper dataset preprocessing
* DRL/MARL may be simplified in implementation
* High computation for large datasets

---

# 🔹 10. Future Enhancements

* Real-time intrusion detection
* Deployment using Flask / Web App
* Integration with network monitoring tools
* Advanced RL tuning

---

# 🔹 11. Safety & Usage Notes

* This system is for educational and research purposes
* Not a replacement for enterprise security systems

---

# 🔹 12. Conclusion

This IDS project provides a smart, explainable, and adaptive approach to detecting cyber threats using modern AI techniques.
