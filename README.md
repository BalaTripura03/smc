**Smart Waste Classification**
**Overview**
Smart Waste Classification is an innovative project aimed at automating the sorting of waste materials to enhance recycling efficiency and promote environmental sustainability. This project leverages deep learning and computer vision techniques to classify waste into categories such as biodegradable and non-biodegradable, with further granularity into multiple specific classes. The system is designed to reduce manual labor in waste sorting, improve recycling rates, and contribute to a cleaner environment.
**Features**
Automated Waste Classification: Utilizes a convolutional neural network (CNN) to classify waste items from images or real-time video feeds.
Multi-Stage Classification: 
Stage 1: Classifies waste into biodegradable and non-biodegradable.
Stage 2: Categorizes waste into nine distinct classes based on material characteristics.
Stage 3: Provides detailed classification into 36 specific waste types.


High Accuracy: Achieves up to 96% accuracy in two-class classification, 91% in nine-class, and 85.25% in 36-class classification.
Real-Time Processing: Supports real-time waste classification for integration into waste management systems.
IoT Integration: Incorporates IoT for real-time data monitoring and control, with potential for smart bin applications.
Explainable AI: Uses XAI techniques to enhance model interpretability and decision-making transparency.
Prototype Hardware: Includes a hardware architecture for autonomous waste sorting in industrial settings.

**Technologies Used**

Deep Learning Frameworks: TensorFlow, Keras
Computer Vision: OpenCV
IoT: Arduino, Bluetooth connectivity for real-time monitoring
Dataset: Custom TriCascade WasteImage dataset, combining multiple waste image datasets
Model Architecture: Lightweight Depth-wise Separable CNN (DP-CNN) with Ensemble Extreme Learning Machine (En-ELM) classifier

**Installation**

Clone the repository:git clone https://github.com/kishore7770407/Smart-Waste-Classification.git


Install required dependencies:pip install -r requirements.txt


Download the TriCascade WasteImage dataset and place it in the data/ directory.
Configure IoT hardware (e.g., Arduino) as per the setup guide in hardware/setup.md.

**Usage**

Train the model:python train.py --dataset data/TriCascade_WasteImage


Run real-time classification:python predict.py --model models/trained_model.h5


For IoT integration, upload the Arduino code from hardware/arduino_server.ino to your board and configure the Android app as described in docs/android_app.md.

Dataset
The project uses the TriCascade WasteImage dataset, a comprehensive collection of 35,264 images across 36 waste categories, combining four preexisting datasets for robust training and evaluation.
Performance

Two-Class Classification: 96% accuracy, 95% precision, 95% recall, 95% F1-score, 98.77% ROC-AUC
Nine-Class Classification: 91% accuracy, 90% precision, 89.44% recall, 89.66% F1-score, 98.57% ROC-AUC
Thirty-Six-Class Classification: 85.25% accuracy, 85.02% precision, 85.25% recall, 84.54% F1-score, 98.68% ROC-AUC
Inference Speed: Average testing time of 0.00001 seconds with the En-ELM classifier

Contributing
Contributions are welcome! Please fork the repository, create a new branch, and submit a pull request with your changes. Ensure your code follows the project's coding standards outlined in CONTRIBUTING.md.
License
This project is licensed under the MIT License. See LICENSE for details.
Acknowledgments

Inspired by advancements in deep learning and IoT for sustainable waste management.
Thanks to the open-source community for providing datasets and libraries like TensorFlow, Keras, and OpenCV.
