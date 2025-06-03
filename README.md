## **Model-Heterogeneous Semi-Supervised Federated Learning for ABIDE Images Classification**

This project implements a complete **Heterogeneous Semi-Supervised Federated Learning** approach on the **ABIDE** (Autism Brain Imaging Data Exchange) dataset, using MRI images in `.png` format along with annotations from a `.csv` file.

## 📌 Objective
To adapt with ABIDE dataset and implement the **HSSF** approach for :
- Learning from **clients with unlabeled or partially labeled data**
- Handling **heterogeneous models** across different clients (ResNet18, MobileNet, EfficientNet)
- Using a **central server (ResNet101)** for aggregation via prediction distillation


##  HSSF Architecture

1. **Public Supervised Learning (PSL)** – clients train locally on publicly labeled data  
2. **Regularity Condensation (RC)** – the server collects client predictions (logits) on public data  
3. **Regularity Fusion (RF)** – clients distill knowledge from the server via KL divergence  
4. **Semi-Supervised Learning (SSL)** – clients apply SA (Self-Assessment) and RPG (Reliable Pseudo-label Generation) on their own unlabeled data

## Dataset
- MRI images come from the ABIDE Preprocessed dataset converted to .png format.
- The file phenotypes_clean1.csv contains labels (autism or control) and subject IDs.

## License
- This project is for academic use only. 
- The original paper : “Ma, Yuxi, et al. "Model-heterogeneous semi-supervised federated learning for medical image segmentation." IEEE Transactions on Medical Imaging 43.5 (2024): 1804-1815.”

 ## Author
- Developed by Ameny Ihkaf as part of a Master’s thesis.


