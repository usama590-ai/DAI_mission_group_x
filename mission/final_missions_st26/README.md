# DAI Mission — Predicting Corporate Financial Distress

**Course:** Data and AI in Economics | TU Dortmund  
**Group:** X  
**Group Members:** Usama Saleem, Zi Zhang, Ekin Yuecesan

---

## Research Question

Can machine learning models trained on Compustat financial statement ratios predict corporate financial distress more accurately than the classical Altman Z-Score, and to what extent does leverage *causally* increase distress probability rather than merely correlating with it?

---

## Repository Structure

```
├── DAI_Mission_Final_Submission_group_x.ipynb   # Main notebook (fully executed)
├── requirements.txt                     # All dependencies
├── slides.pdf                           # Presentation slides (PDF)
├── README.md                            # This file
└── data/
    └── compustat_raw.csv                # Raw Compustat data (33 MB)
```

---

## How to Run

**1. Clone the repository**
```bash
git clone https://github.com/usama590-ai/DAI_mission_group_x.git
cd DAI_mission_group_x
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the notebook**

Open `DAI_Mission_Final_Submission_group_x.ipynb` in Jupyter and run all cells top to bottom (Kernel → Restart & Run All).

The notebook loads data automatically from `data/compustat_raw.csv` — no manual setup required.

---

## Methods Used

| Block | Method |
|---|---|
| Causal Inference | Backdoor adjustment via DoWhy DAG, firm fixed effects, placebo refuter, sensitivity analysis |
| Supervised Learning | Lasso, Logistic Regression, SVM, Random Forest, Neural Network |
| Unsupervised Learning | PCA + KMeans clustering (k=3) |

---

## Data

Source: Compustat North America (Fundamentals Annual) via WRDS, TU Dortmund institutional access.  
The dataset is included directly in the `data/` folder (33 MB, within GitHub's 100 MB limit).  
Data is governed by the WRDS/Compustat licence and is not for redistribution.
