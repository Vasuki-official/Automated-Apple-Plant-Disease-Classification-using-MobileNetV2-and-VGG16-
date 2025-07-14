# Automated Apple Plant Disease Classification using MobileNetV2 and VGG16

This project focuses on accurately identifying apple leaf diseases using advanced deep learning techniques. By leveraging transfer learning with MobileNetV2 and VGG16 architectures, the model aims to assist farmers and agricultural professionals in early disease detection, promoting better yield and sustainable farming practices.

## Overview
Apple plants are highly susceptible to various diseases such as Black Rot, Scab, and Cedar Apple Rust, which significantly affect crop quality and productivity. Manual inspection is time-consuming and prone to errors. To overcome this challenge, we propose an automated image classification system that can detect and classify apple leaf diseases efficiently.

## Dataset
**Source:** PlantVillage dataset

#### Classes:

    Apple Healthy

    Apple Black Rot

    Apple Scab

    Apple Cedar Apple Rust

#### Data split:

    Training: ~4,000 images per class

    Validation: ~1,000 images per class

    Test set: Images not seen during training

## Methodology
### Data Preprocessing

- Images resized to 225×225 pixels

- Pixel normalization (0-1)

- Augmentation (flipping, rotation, shifting, zooming)

### Models Used:

- Sequential CNN (baseline)

- MobileNetV2 (lightweight, fast, and optimized for mobile applications)

- VGG16 (deeper architecture, strong feature extraction)

### Transfer Learning

- Pre-trained on ImageNet

- Custom classification layers added for four-class output

- Fine-tuning to adapt features for apple disease recognition

### Training Details

- **Optimizer:** Adam

- **Learning rate:** 0.0001 (with scheduling)

- **Loss function:** Categorical Cross-Entropy

- **Batch size:** 32

- Early stopping to prevent overfitting

# Results
    Metric	         Sequential CNN	        MobileNetV2   	VGG16
    Accuracy (%)	        98.63	           99.26	    99.13
    Validation Accuracy (%)	96.24	           99.18	    98.35
    Validation Loss	        14.10	           3.08	         5.34

**Best Performer**: MobileNetV2 showed the highest validation accuracy and lowest validation loss, making it a suitable choice for real-time field applications.

**Output Example**: The trained model successfully predicts unseen leaf images and outputs the correct disease class.

## Key Takeaways
MobileNetV2 offers an excellent balance between accuracy, speed, and resource efficiency.

VGG16, while accurate, is more resource-intensive and better suited for scenarios with higher computational power.

The approach supports precision agriculture by enabling farmers to monitor and address plant health issues quickly.

## How to Run
### Clone the repository:


    git clone https://github.com/your-username/apple-disease-classification.git
    cd apple-disease-classification
### Install required packages:


    pip install -r requirements.txt
### Prepare the dataset (follow folder structure in /data).

### Run training:


    python train.py
### Evaluate and make predictions on test images:


    python predict.py --image path_to_image.jpg
# Contributors

- **Vasuki P**, [SRM Institute of Science and Technology]

- **Suganthi N**, [SRM Institute of Science and Technology]

- **Jaya Sudha N D**, [SRM Institute of Science and Technology]

- **Raghuram S**, [SRM Institute of Science and Technology]

## Acknowledgments
We thank our project guide, faculty members, fellow students, and the open-source community for their valuable support and resources that made this research possible.

## License
This project is open-source and available under the **MIT License**.

### Future Work
Deploy as a mobile application for real-time field diagnosis

Extend to other fruit and vegetable crops

Integrate explainable AI techniques for better interpretability

### Feel free to fork, raise issues, or contribute to improve this project further!
