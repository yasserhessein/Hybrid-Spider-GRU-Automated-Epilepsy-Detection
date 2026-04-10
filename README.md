# Automated Epilepsy Detection Hybrid Spider-GRU and ANN Ensemble with Optimized EEG


---

## 📌 Overview

Epilepsy is a chronic neurological disorder affecting ~50 million people worldwide.  
This project proposes a **novel Spider-GRU architecture** (multi-branch GRU with spider-inspired fusion) combined with an **ANN ensemble** for automated epilepsy detection using EEG signals.  

The system also integrates **Particle Swarm Optimization (PSO)** for hyperparameter tuning and a **hard voting ensemble** to improve classification robustness.  

A **PyQt5-based GUI** is provided for real-world clinical deployment (manual or batch CSV input).

✅ Achieves **>99% accuracy** on the BEED dataset.

---

## 🧠 Key Contributions

- End-to-end automated epilepsy detection pipeline (ML + DL + hybrid models)
- Novel **Spider-GRU** architecture for enhanced temporal feature learning
- **Hybrid CNN-LSTM & CNN-BiLSTM** for spatiotemporal feature extraction
- **PSO-optimized Extra Trees (ET+PSO)** for feature selection & hyperparameter tuning
- **Hard Voting Ensemble (ANN + Spider-GRU)** → 99.18% accuracy
- **User-friendly GUI** (PyQt5) for manual or batch EEG classification
- Publicly available code & models

---

## 📊 Dataset

**Bangalore EEG Epilepsy Dataset (BEED)**  
- 16,000 EEG segments (20 sec each)  
- 256 Hz sampling rate, 16 channels (X1–X16)  
- 4 balanced classes:  
  - Healthy (0)  
  - Generalized Seizure (1)  
  - Focal Seizure (2)  
  - Seizure Event (3)  
- 80 subjects (21–55 years, equal gender representation)

---

## 🧪 Models Evaluated

### Machine Learning
- Logistic Regression, AdaBoost, Decision Tree, Random Forest, SVM, SGD, MLP, Extra Trees  
- **ET + PSO** (optimized)

### Deep Learning
- ANN, CNN, LSTM, GRU, BiLSTM  
- Hybrid: CNN-LSTM, CNN-BiLSTM  
- **Spider-GRU** (proposed)

### Ensemble
- **Hard Voting (ANN + Spider-GRU)** → best performance

---

## 📈 Results (Top Performers)

| Model               | Accuracy | Precision | Recall | F1-Score | MCC    |
|---------------------|----------|-----------|--------|----------|--------|
| ET + PSO            | 98.31%   | 98.32%    | 98.26% | 98.28%   | 97.75% |
| Spider-GRU          | 98.81%   | 98.82%    | 98.81% | 98.81%   | 98.41% |
| **Hard Voting Ensemble** | **99.18%** | **99.18%** | **99.18%** | **99.18%** | **98.91%** |

- Misclassifications mostly between Focal and Generalized seizure types (clinically expected)
- Zero false positives for Healthy class in top models

---

## 🖥️ Graphical User Interface (GUI)

Built with **PyQt5** – supports:

- **Manual input** of 16 EEG channel values
- **CSV batch upload** for multiple patient records
- Real-time prediction + confidence score
- Dynamic EEG signal plot (16 channels)

<img width="853" height="421" alt="image" src="https://github.com/user-attachments/assets/434e3004-1d12-412a-85ce-34f2741df8f4" />


---

## 🚀 Deployment & Latency

- Real-time inference: **~67 ms per sample** (dual T4 GPU setup)
- Ready for clinical decision support systems
- Not yet a certified medical device (research prototype)

---

├── models/ # Trained models (ANN, Spider-GRU, ensemble)

├── gui/ # PyQt5 GUI files

├── preprocessing/ # Label encoding, train/test split

├── optimization/ # PSO for Extra Trees

├── evaluation/ # Metrics, confusion matrices, reports

├── data/ # BEED dataset

## 📂 Repository Structure


---

## 🔗 Data & Code Availability

**Full implementation code** (preprocessing, training, evaluation, GUI):  
👉 [https://github.com/yasserhessein/Hybrid-Spider-GRU-Automated-Epilepsy-Detection](https://github.com/yasserhessein/Hybrid-Spider-GRU-Automated-Epilepsy-Detection)

**Dataset:**  
Bangalore EEG Epilepsy Dataset (BEED) – [UCI Link](https://doi.org/10.24432/C5K33B)

---

## 📄 Citation

If you use this work, please cite:

```bibtex
@article{shakir2025automated,
  title={Automated Epilepsy Detection Using a Hybrid Spider-GRU and ANN Ensemble with Optimized EEG Classification},
  author={Shakir, Yasir Hussein and AL Mandhari, Eshaq Aziz Awadh and Abdulnabi, Mohamed and Mutlag, Reem Ali and Al Mamari, Wadha Humaid Said and Forcado, Marvin Rick Gadon},
  journal={Bulletin of Electrical Engineering and Informatics},
  year={2025}
}
