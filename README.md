# PAMAP2 Preprocessed Dataset for Human Activity Recognition (HAR)

This repository provides a clean and reproducible preprocessed version of the PAMAP2 Physical Activity Monitoring dataset for Human Activity Recognition (HAR) research.

---

## Dataset Overview

The PAMAP2 dataset is a widely used benchmark for HAR containing data from 9 subjects (8 male, 1 female; age 27.2 ± 3.1 years) performing 18 physical activities. Data is collected using three IMU sensors (hand, chest, ankle) and a heart rate monitor at 100 Hz sampling rate.

In this work, the raw `.dat` files were obtained directly from the official source in their original format. No previously published preprocessed versions were used, ensuring full control over the preprocessing pipeline.

---

## Preprocessing Pipeline

All preprocessing was performed independently to ensure consistency and experimental validity:

- Removal of missing/invalid values (NaN filtering)  
- Selection of 15 valid activity classes  
- Sliding window segmentation  
  - Window size: 128  
  - Stride: 64  
- Leave-One-Subject-Out (LOSO) cross-validation setup  
- Optional data augmentation for training balance  

---

## Dataset Statistics

- Total segments: ~32,000  
- Subjects: 9 (LOSO evaluation protocol)  
- Sampling rate: 100 Hz  
- Input features: Multi-channel IMU sensor signals  
- Task: Multi-class Human Activity Recognition  

---

## Usage

This dataset can be directly used for:

- Federated Learning experiments  
- Deep learning models (LSTM, GRU, CNN, Transformer-based HAR)  
- Personalized HAR systems  
- Benchmark evaluation under LOSO protocol  

The same processed dataset is used for both the proposed method (PrivFedHAR) and all baseline models to ensure fair and consistent comparison.

---

## Dataset Access

Due to size limitations, the dataset is hosted externally.

You can access it here:

🔗 Google Drive: https://drive.google.com/file/d/1P_7neoQg9JIubZ4gfRGzhjgbrusctuTJ/view?usp=drive_link

Please ensure the link access is set to **"Anyone with the link can view"**.

---

## Original Dataset

The PAMAP2 Physical Activity Monitoring dataset is publicly available at:

https://archive.ics.uci.edu/ml/datasets/pamap2+physical+activity+monitoring

This dataset is widely used in wearable sensing and Human Activity Recognition research.

---

## License

This repository is released under the MIT License, allowing free use, modification, and distribution with proper attribution.

---

## Citation

If you use this dataset, please cite the original PAMAP2 dataset:
