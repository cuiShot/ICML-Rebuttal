
### 1. Overview of Unseen Datasets

| Dataset | Description | Source | Date |
| :--- | :--- | :--- | :--- |
| **Neurofibromatosis Type 1** | Predicts disease type (sporadic vs. familial) using 331 patient clinical symptom records. | [🔗 UCI Link](https://archive.ics.uci.edu/dataset/1162/neurofibromatosis%2Btype%2B1%2Bclinical%2Bsymptoms%2Bof%2Bfamilial%2Band%2Bsporadic%2Bcases) | May 2025 |
| **Gallstone-1** | Predicts the presence of gallstones using 319 records of demographics and lab tests. | [🔗 UCI Link](https://archive.ics.uci.edu/dataset/1150/gallstone-1) | Apr 2025 |
| **Instagram Bot Detection** | Identifies automated bot accounts using user profile attributes and behavioral features. | [🔗 HuggingFace Link](https://huggingface.co/datasets/safhana2026/instagram_bot_detection) | 2026 |
| **Private Business Logs** | A private, anonymized tabular dataset of business and transaction logs designed for binary classification. It contains exactly 4,920 samples with a perfectly balanced class distribution (2,460 per class) and 24 mixed-type input features (numerical codes, categorical values, and ID-style strings). It has been rigorously processed to prevent data leakage, serving as a highly realistic evaluation benchmark. | - *(Private)* | - *(Private)* |



### 2. Experimental Results on New and Private Datasets

|           | gallstone(AUC)  | instagram_bot(AUC) | Neurofibromatosis(AUC) | private_dataset(AUC) |
| --------- |-----------------|--------------------|------------------------|----------------------|
| xgboost   | 88.10 ± 2.13    | 99.95 ± 0.01       | 95.77 ± 1.66           | 93.25 ± 1.00         |
| lightGBM  | 85.69 ± 2.40    | 99.96 ± 0.01       | 97.16 ± 1.17           | 93.96 ± 0.61         |
| autogluon | 86.62 ± 2.22    | 99.97 ± 0.01       | 96.30 ± 1.78           | 93.17 ± 0.87         |
| RNE       | 79.00 ± 3.36    | 99.97 ± 0.02       | 93.34 ± 4.46           | 92.52 ± 1.01         |
| DS_Agent  | 84.44 ± 3.70    | 99.95 ± 0.03       | 94.75 ± 2.15           | 92.64 ± 1.38         |
| OURS      | 88.61 ± 2.51    | 99.97 ± 0.01       | 97.57 ± 0.82           | 95.02 ± 0.39         |
