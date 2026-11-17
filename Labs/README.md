cat > README.md <<'EOF'
# AICS202 – Adversarial Machine Learning

## Project Overview

This project investigates adversarial machine learning through four practical laboratory exercises. It examines baseline model performance, adversarial evasion, data poisoning, and robustness defences using the handwritten digits dataset and a Logistic Regression classifier.

The practical work was conducted in a Kali Linux environment using Python, NumPy, scikit-learn, Matplotlib, and Jupyter Notebook.

## Laboratory Exercises

| Lab | Topic | Description |
|---|---|---|
| Lab 01 | Baseline and Threat Modelling | Establishes clean model performance and identifies potential adversarial threats. |
| Lab 02 | FGSM Evasion | Evaluates the effect of Fast Gradient Sign Method perturbations on classification accuracy. |
| Lab 03 | Poisoning and Data Integrity | Examines the effect of random training-label corruption on model performance. |
| Lab 04 | Robustness Defences | Compares baseline and adversarially augmented training under clean and adversarial evaluation. |

## Experimental Results

### Lab 01 – Baseline Performance

- Dataset: Handwritten digits dataset
- Total samples: 1,797
- Training samples: 1,347
- Test samples: 450
- Clean test accuracy: 96.22%

### Lab 02 – FGSM Evasion

| Epsilon | Accuracy |
|---:|---:|
| 0.00 | 96.2% |
| 0.03 | 90.7% |
| 0.07 | 79.1% |
| 0.12 | 51.6% |
| 0.18 | 20.4% |

The results show a decline in classification accuracy as perturbation strength increases.

### Lab 03 – Data Poisoning

| Label Corruption | Labels Changed | Clean Test Accuracy |
|---:|---:|---:|
| 0% | 0 | 96.2% |
| 5% | 67 | 96.0% |
| 10% | 135 | 95.8% |
| 20% | 269 | 93.3% |

The experiment demonstrates that random label corruption can reduce model performance, with a larger reduction observed at 20% corruption.

### Lab 04 – Robustness Comparison

| Evaluation Metric | Baseline Model | Augmented Model |
|---|---:|---:|
| Clean accuracy | 96.2% | 94.0% |
| FGSM accuracy | 51.6% | 28.4% |
| PGD accuracy | 48.9% | 26.0% |

In this experiment, adversarially augmented training did not improve the measured FGSM or PGD accuracy. Further investigation and improved defence evaluation are therefore required.

## Project Structure

```text
AICS202_Adversarial_Machine_Learning/
├── Labs/
│   ├── AICS202_Lab01_Baseline_Threat_Model.ipynb
│   ├── AICS202_Lab02_FGSM_Evasion.ipynb
│   ├── AICS202_Lab03_Poisoning_Data_Integrity.ipynb
│   ├── AICS202_Lab04_Robustness_Defences.ipynb
│   └── README.md
├── evidence/
│   ├── Lab01/
│   ├── Lab02/
│   ├── Lab03/
│   └── Lab04/
├── results/
├── report/
├── .gitignore
├── README.md
└── requirements.txt
