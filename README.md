Link for full access of Brain Tumor Classification project: https://drive.google.com/drive/folders/1icEKYDlAp1QTWArpOLY89usi-bntRkfI?usp=sharing

### Overview:

This study introduces three distinct models: RADNet, ViT, and a hybrid model that synthesizes features from both architectures. Comprehensive exploratory data analysis (EDA), preprocessing, and data augmentation strategies were employed to address class imbalance, optimize data quality and to observe how the models would deal given with minimal data information; only 4 classes of brain tumors MRI pictures. Through meticulous hyperparameter tuning using Keras Tuner's Hyperband, the models achieved remarkable accuracy and precision in distinguishing between glioma, meningioma, pituitary tumors, and healthy brain tissues. The RADNet model excelled, attaining a precision of 0.99 and an accuracy rate of 99% on augmented datasets, underscoring its superior performance and robustness. Conversely, the Vision Transformer (ViT) model achieved an accuracy of 89%, highlighting the necessity for extensive datasets to harness its full potential. The hybrid model demonstrated a balanced accuracy of 98% and an F1 score of 0.98, effectively combining the strengths of CNNs and transformers.

### Models implemented:

- RADNet
- ViT (Vision Transfomer)
- Hybrid (RADNet + ViT)

### Dataset Characteristics

Brain Tumor Classification (MRI) Dataset consists of images T-1 weighted MRI Scans with the same JPG type file varies in resolution, size and dimension (via manual inspection). Data is highly unbalanced in Training Dataset due to no_tumor pertaining only 395 files whilst the remnant subfolders procuring approximately 800 files each within Training Dataset. no_tumor should be modified to be converted into balance dataset afore venturing latter phase of employing classification models onto dataset.

### Data Pre-processing

Data Pre-processing of medical images, specifically T1-weighted MRI scans of brain tumors; glioma, meningioma, pituitary and no tumor aims to classify into four classes. The data collected from Kaggle for classification models are in image format JPG or JPEG Files (.jpg). This method is critical for enhancing the accuracy of deep learning models. This section illustrates the methods employed for preprocessing, including image augmentation, cropping, and resizing. These steps ensure that the images are standardized and augmented to improve the robustness of the classification models as the data is unclean. Notably, additional input of multiplying the no_tumor class within Training set by 28 instead of 14 as no_tumor class amount of data is relatively low.


	Large Dataset (With Augmentation) and Small Dataset (Without Augmentation)
Models will be trained on both “Larger Dataset” which augmentation is implemented (supplemental surge of data) and “Small Dataset” which augmentation is not implemented (data quantity remains identical), permits investigation on how models perform and operate with two diverse quantities of dataset.

	Image Dimensions:
IMG_SIZE is set to 224, this function ensures that image will be resized to 224 x 224 pixels due to ViT model as the size is consistent with traditional CNN-based models that are pre-trained on ImageNet. While ViT Model is inherently flexible and can process various image size and dimension, nonetheless, the key component of the ViT model is splitting of the images into patches which are then flattened and processed, hence if image is not 224 x 224, patching and subsequent process can be altered or modifying model architecture accordingly. The ViT model google/vit-base-patch16-224 has a particular implementation of the Vision Transformer from Google. ‘224’ signifies of model construction to accept input images of 224x224, and transformer architecture processes images via splitting into 16 x 16 patches, resulting in sequence of (224¦16)^2=196 patches.
