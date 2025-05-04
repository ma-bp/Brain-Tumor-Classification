Link for full access of Brain Tumor Classification project: https://drive.google.com/drive/folders/1icEKYDlAp1QTWArpOLY89usi-bntRkfI?usp=sharing

This study introduces three distinct models: RADNet, ViT, and a hybrid model that synthesizes features from both architectures. Comprehensive exploratory data analysis (EDA), preprocessing, and data augmentation strategies were employed to address class imbalance and optimize data quality. Through meticulous hyperparameter tuning using Keras Tuner's Hyperband, the models achieved remarkable accuracy and precision in distinguishing between glioma, meningioma, pituitary tumors, and healthy brain tissues. The RADNet model excelled, attaining a precision of 0.99 and an accuracy rate of 99% on augmented datasets, underscoring its superior performance and robustness. Conversely, the Vision Transformer (ViT) model achieved an accuracy of 89%, highlighting the necessity for extensive datasets to harness its full potential. The hybrid model demonstrated a balanced accuracy of 98% and an F1 score of 0.98, effectively combining the strengths of CNNs and transformers.

Models implemented:

- RADNet
- ViT (Vision Transfomer)
- Hybrid (RADNet + ViT)

