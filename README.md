# Multi-Disease Detection Using Retinal Fundus Scans (MDDRFS)

## Overview

This project focuses on multi-disease detection using retinal fundus scans and nerve segmentation through image processing and deep learning techniques. The main tasks include binary classification, multi-class classification, and nerve segmentation using different state-of-the-art deep learning architectures.

### Key Features

- **Binary Classification**: Classifying retinal fundus images into disease or no disease.
- **Multi-Class Classification**: Detecting multiple diseases from retinal fundus images.
- **Nerve Segmentation**: Segmenting nerve structures from fundus images for further analysis.
  
### Technologies Used

- **TensorFlow, Keras, PyTorch** for model building and experimentation.
- **Python** for scripting and data handling.
- **Deep Learning Models** like ResNet, EfficientNet, MobileNet, UNet, and more for classification and segmentation.

---

## Directory Structure

```bash
├── Augmentations                   # Augmentation scripts for data preprocessing
├── Data Segregation and Loading    # Scripts for segregating and loading data
├── Disease Detection               # Notebooks and scripts for binary and multi-class classification
├── Experiments                     # Notebooks for model experimentation
├── Frontend                        # Frontend code for the web interface
├── Nerve Segmentation              # Nerve segmentation training notebooks
├── backend                         # Backend code for the web interface
├── .gitignore                      # Git ignore file for ignoring unnecessary files
├── LICENSE                         # License file (Apache 2.0)
├── requirements.txt                # requirements file     
└── README.md                       # This readme file

```

---

## Data Reference

The reference public data has been uploaded to the Final Year drive. The Retinal Fundus Images Dataset contains images for [Multi Disease Classification](https://drive.google.com/drive/folders/1eMeRzGTF54cKfhUai8lg2bJwYsHUlP18?usp=sharing) and [Nerve Segementation](https://drive.google.com/drive/folders/1SyB0az9RY-j3BsRTdH0m-deUhHzAH2f9?usp=sharing) folder contains images, masks and lables for nerve segmentation. Additional proprietery data was used for training the model in addition to the publicly available datasets listed below.

Data Sources:
Segmentation:
1. [High-Resolution Fundus (HRF) Image Database](https://www5.cs.fau.de/research/data/fundus-images/)
2. [Drive Grand Challenege](https://drive.grand-challenge.org/Download/)
3. [PAPILA: Dataset with fundus images and clinical data of both eyes of the same patient for glaucoma assessment](https://pubmed.ncbi.nlm.nih.gov/35680965/)

Classification:
1. [Retinal Image Analysis for multi-Disease Detection Challenge](https://riadd.grand-challenge.org/Download/)
2. [FIVES: A Fundus Image Dataset for Artificial Intelligence based Vessel Segmentation](https://www.nature.com/articles/s41597-022-01564-3#Sec7)
3. [Retinal fundus images for glaucoma analysis: the RIGA dataset](https://deepblue.lib.umich.edu/data/concern/data_sets/3b591905z)

---

## Models Used

We use a variety of state-of-the-art deep learning models for the classification and segmentation tasks. These include:

### Pre-trained Models (Transfer Learning)

- **ResNet152V2**
- **EfficientNetB7**
- **MobileNetV2**
- **DenseNet201**
- **XceptionNet**
- **EfficientNetV2 (S, M, L)**

### Segmentation Models

- **UNet**

---

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yasho191/MDDRFS.git
   cd MDDRFS
   ```

2. Create a Python virtual environment and install the dependencies:
   ```bash
   python3 -m venv env
   source env/bin/activate
   pip install -r requirements.txt
   ```

3. Download and set up the datasets. Follow the instructions for dataset references mentioned above.

4. Train the models:
   - For **Binary Classification**, refer to the `Disease Detection` folder for training scripts.
   - For **Multi-Class Classification**, follow the same procedure in the `Disease Detection` folder.
   - For **Nerve Segmentation**, the training notebooks are in the `Nerve Segmentation` folder.

---

## How to Use

### Augmentation Tasks:
We have implemented a set of augmentations in the `Augmentations` folder. These include:
- Rotate
- Flip Horizontal/Vertical
- Center Crop
- Contrast/Brightness adjustments

### Classification Tasks

- **Binary Classification**: You can perform either **transfer learning** or **training from scratch** for disease detection.
- **Multi-Class Classification**: Similarly, multi-class disease detection supports **transfer learning** and **scratch training**.

### Nerve Segmentation

- **UNet** architectures has been employed for nerve segmentation tasks. The models can be trained using the notebooks provided in the `Nerve Segmentation` folder.

---

## Results

- The best-performing models from classification tasks will be **ensemble** for better accuracy.
- Segmentation results can be visualized using built-in functions from the notebooks.
- Model weights will not be made public. You can finetune your models using the provided training scripts.

---

## License

This project is licensed under the Apache 2.0 License. See the `LICENSE` file for details.
