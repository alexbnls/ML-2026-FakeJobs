# 🕵️‍♂️ Fraud Job Postings Detection

Progetto di Machine Learning per il rilevamento di annunci di lavoro fraudolenti, sviluppato per il corso di Machine Learning (A.A. 2025/2026) presso l'**Università degli Studi di Salerno**.

## Descrizione
L'obiettivo del progetto è classificare annunci di lavoro come **Reali** o **Fraudolenti** utilizzando un dataset sbilanciato ( ~95% reali, ~5% frodi). La pipeline combina tecniche di NLP (TF-IDF) sui testi degli annunci con feature engineering avanzato sui metadati.

## Pipeline
1.  **Data Cleaning**: Gestione valori nulli, pulizia testo (rimozione HTML, stop words).
2.  **Feature Engineering**:
    * Estrazione metadati (lunghezza testo, presenza logo, range salariale).
    * Log-transformation per gestire gli outliers.
    * TF-IDF Vectorization (5000 features).
3.  **Modellazione**: Confronto tra Logistic Regression, Linear SVM e Random Forest.
4.  **Ottimizzazione**: Threshold Tuning per massimizzare l'F1-Score sulla classe minoritaria.

## Risultati
Il modello migliore è risultato essere il **Random Forest**.

| Metrica | Valore (Threshold 0.20) |
| :--- | :--- |
| **F1-Score** | **0.8023** |
| Recall | 80.92% |
| Precision | 79.55% |
| ROC-AUC | 0.9884 |

## Struttura della Repository
* `code/` - Notebook Python per l'analisi e il training.
* `report/` - Report finale in formato LaTeX/PDF.
* `images/` - Grafici generati (EDA, Confusion Matrix, Curve ROC/PR).
* `data/` - Dataset utilizzato (*fake_job_postings.csv*).

## Requisiti
Il progetto è sviluppato in Python. Le librerie principali utilizzate sono:
* `pandas`
* `numpy`
* `scikit-learn`
* `matplotlib` & `seaborn`
* `nltk`

## 👥 Autori
* **Alessandro D.**
* **Gaetano A.**