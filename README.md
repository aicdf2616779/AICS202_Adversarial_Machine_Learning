# AICS202 – Adversarial Machine Learning

## 1. Project Overview

This project explores adversarial machine learning through four practical laboratory exercises. The experiments investigate baseline model performance, adversarial evasion, data poisoning, and robustness defences using the handwritten digits dataset and a Logistic Regression classifier.

The practical exercises were conducted in a Kali Linux environment using Python and machine learning libraries.

## 2. Project Objectives

- Establish baseline machine learning performance.
- Investigate the impact of adversarial input perturbations.
- Examine the effects of training-data label corruption.
- Evaluate adversarial robustness and defence approaches.
- Identify security limitations and recommend appropriate safeguards.

## 3. Laboratory Exercises

### Lab 01 – Baseline and Threat Modelling

Established the baseline performance of the classifier and identified potential adversarial threats.

- Dataset: Handwritten digits
- Total samples: 1,797
- Training samples: 1,347
- Test samples: 450
- Clean test accuracy: 96.22%

### Lab 02 – FGSM Evasion

Evaluated the effect of Fast Gradient Sign Method (FGSM) perturbations on classification accuracy.

| Epsilon | Accuracy |
|---:|---:|
| 0.00 | 96.2% |
| 0.03 | 90.7% |
| 0.07 | 79.1% |
| 0.12 | 51.6% |
| 0.18 | 20.4% |

The results show that classification accuracy decreased as perturbation strength increased.

### Lab 03 – Poisoning and Data Integrity

Investigated the effect of random training-label corruption on model performance.

| Label Corruption | Labels Changed | Clean Test Accuracy |
|---:|---:|---:|
| 0% | 0 | 96.2% |
| 5% | 67 | 96.0% |
| 10% | 135 | 95.8% |
| 20% | 269 | 93.3% |

The results indicate that increasing label corruption reduced the model's clean test accuracy.

### Lab 04 – Robustness Defences

Compared baseline and adversarially augmented training under clean and adversarial evaluation.

| Evaluation Metric | Baseline | Augmented Training |
|---|---:|---:|
| Clean accuracy | 96.2% | 94.0% |
| FGSM accuracy | 51.6% | 28.4% |
| PGD accuracy | 48.9% | 26.0% |

In this experimental run, adversarially augmented training did not improve the measured FGSM or PGD accuracy. Further investigation is required.

## 4. Project Structure

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
```

## 5. Installation and Setup

Clone the repository:

```bash
git clone https://github.com/aicdf2616779/AICS202_Adversarial_Machine_Learning.git
cd AICS202_Adversarial_Machine_Learning
```

Create and activate a Python virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

## 6. Limitations

- The experiments use a relatively small handwritten digits dataset.
- The evaluation focuses on Logistic Regression.
- The attack methods and configurations are limited to those implemented in the practical notebooks.
- The results come from controlled laboratory experiments and should not be treated as proof of production-level security.

## 7. Ethical Considerations

The experiments were conducted in a controlled educational environment for academic learning and responsible security research.

## 8. Author Information

- **Student Name:** [Shamsu Wada]
- **Student ID:** [2026/AICDF/16779]
- **Course:** AICS202 – Adversarial Machine Learning
- **Institution:** ICDFA

---

*This repository contains practical laboratory notebooks, experimental findings, supporting evidence, and assessment documentation for the AICS202 Adversarial Machine Learning project.*
