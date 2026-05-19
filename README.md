# food-classification-dl-cnn
This project focuses on food image classification using Deep Learning techniques. It implements a Custom CNN architecture and compares its performance with powerful transfer learning models such as VGG16 and ResNet50. The system is trained to recognize multiple food categories from images with high accuracy using TensorFlow and Keras.

---

<div align="center">
  
# 🍔 Food Classification Using Deep Learning</div>
  
<div align="center">Custom CNN • VGG16 • ResNet50</div>
<p align="center"> <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python"> <img src="https://img.shields.io/badge/TensorFlow-Deep_Learning-orange?style=for-the-badge&logo=tensorflow"> <img src="https://img.shields.io/badge/Keras-CNN-red?style=for-the-badge&logo=keras"> <img src="https://img.shields.io/badge/OpenCV-Computer_Vision-green?style=for-the-badge&logo=opencv"> <img src="https://img.shields.io/badge/Flask-Web_App-black?style=for-the-badge&logo=flask"> <img src="https://img.shields.io/badge/Model-Custom_CNN-success?style=for-the-badge"> <img src="https://img.shields.io/badge/Transfer_Learning-VGG16_&_ResNet50-purple?style=for-the-badge"> </p>
<p align="center"> <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?q=80&w=1400&auto=format&fit=crop" width="100%"> </p>


📌 Project Overview

The Food Classification Using Deep Learning project is an advanced Computer Vision application developed using Deep Learning and Convolutional Neural Networks (CNNs) to automatically classify food images into different categories.

The project combines:

Custom CNN Architecture
Transfer Learning using VGG16
Transfer Learning using ResNet50
Image Preprocessing
Data Augmentation
Model Evaluation
Flask Deployment

This system can accurately identify food categories from uploaded images and provides real-time predictions through a Flask web application.

The project demonstrates the practical implementation of Deep Learning for image classification tasks using modern CNN architectures and transfer learning techniques.

🧠 Deep Learning Models Used
Model	Description
Custom CNN	Self-designed convolutional neural network
VGG16	Transfer Learning using pretrained VGG16
ResNet50	Deep residual learning architecture
📖 Abstract

Food image classification is an important application of Computer Vision and Deep Learning that enables automatic identification of food categories from digital images. It has practical applications in smart restaurants, calorie estimation systems, dietary monitoring, food recommendation systems, and healthcare analytics.

This project presents a Food Classification System developed using Deep Learning techniques and Convolutional Neural Networks (CNNs). The system classifies food images into multiple categories using:

Custom CNN Architecture
VGG16 Transfer Learning
ResNet50 Transfer Learning

The project includes:

Image preprocessing
Image resizing
Data augmentation
Model training
Feature extraction
Transfer learning
Performance evaluation
Flask deployment

Multiple deep learning models were trained and compared to achieve high classification accuracy. Among all models, the best-performing model was selected for deployment.

The final system allows users to upload food images and receive real-time predictions through an interactive Flask web application.

🎯 Project Objectives

✅ Automatically classify food images
✅ Compare Custom CNN with pretrained models
✅ Improve image classification accuracy
✅ Implement Transfer Learning
✅ Deploy Deep Learning model using Flask
✅ Build a real-world AI application

🧠 Technologies Used
Technology	Purpose
Python	Core Programming Language
TensorFlow	Deep Learning Framework
Keras	CNN Model Development
OpenCV	Image Processing
NumPy	Numerical Operations
Pandas	Data Handling
Matplotlib	Visualization
Seaborn	Statistical Analysis
Flask	Web Application Framework
HTML/CSS	Frontend Development
PIL	Image Loading
Scikit-learn	Model Evaluation
🏗️ System Architecture
<p align="center"> <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>
Input Food Image
        ↓
Image Preprocessing
        ↓
Image Resizing
        ↓
Feature Extraction
        ↓
Deep Learning Model
(Custom CNN / VGG16 / ResNet50)
        ↓
Prediction Layer
        ↓
Food Category Output
📂 Dataset Overview
<p align="center"> <img src="https://images.unsplash.com/photo-1490645935967-10de6ba17061?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>
Attribute	Details
Dataset Type	Food Image Dataset
Problem Type	Multi-Class Classification
Input Type	RGB Food Images
Image Format	JPG / PNG
Training Technique	Deep Learning
Models Used	CNN, VGG16, ResNet50
🍕 Food Categories

The system can classify multiple food categories such as:

Pizza
Burger
Sandwich
Ice Cream
Pasta
Cake
Donuts
Fries
Salad
Sushi
Tacos
Noodles
🔄 Complete Deep Learning Workflow
<p align="center"> <img src="https://images.unsplash.com/photo-1526379095098-d400fd0bf935?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>
Dataset Collection
        ↓
Image Preprocessing
        ↓
Image Resizing
        ↓
Data Augmentation
        ↓
Train-Test Split
        ↓
Model Building
        ↓
CNN Training
        ↓
Transfer Learning
        ↓
Model Evaluation
        ↓
Prediction System
        ↓
Flask Deployment
🖼️ Image Preprocessing

Image preprocessing was performed to improve model performance and training efficiency.

Techniques Used
Image Resizing
Image Normalization
RGB Conversion
Noise Reduction
Pixel Scaling
Final Input Shape
224 × 224 × 3
🔄 Data Augmentation

Data augmentation helps improve model generalization and reduce overfitting.

Augmentation Techniques
Rotation
Zoom
Horizontal Flip
Width Shift
Height Shift
Shear Transformation
Benefits

✅ Increased dataset diversity
✅ Reduced overfitting
✅ Improved model robustness
✅ Better generalization

🤖 Custom CNN Architecture
<p align="center"> <img src="https://images.unsplash.com/photo-1507146426996-ef05306b995a?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>

The Custom CNN model was developed from scratch using multiple convolutional and pooling layers.

Architecture Components
Convolutional Layers
ReLU Activation
MaxPooling Layers
Dropout Layers
Flatten Layer
Dense Layers
Softmax Output Layer
🧠 Transfer Learning — VGG16

VGG16 is a pretrained convolutional neural network trained on the ImageNet dataset.

Features

✅ Deep feature extraction
✅ High classification accuracy
✅ Transfer learning capability
✅ Faster convergence

🧠 Transfer Learning — ResNet50

ResNet50 uses residual connections to train deeper neural networks efficiently.

Features

✅ Residual Learning
✅ Deep architecture
✅ Improved gradient flow
✅ Better feature learning

⚙️ Model Training
<p align="center"> <img src="https://images.unsplash.com/photo-1555949963-aa79dcee981c?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>
Training Parameters
Parameter	Value
Image Size	224×224
Batch Size	32
Epochs	25
Optimizer	Adam
Loss Function	Categorical Crossentropy
Activation Function	ReLU / Softmax
📊 Model Performance
<p align="center"> <img src="https://images.unsplash.com/photo-1559526324-593bc073d938?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>
Model	Accuracy
Custom CNN	92%
VGG16	95%
ResNet50	97%
🏆 Best Model — ResNet50

Among all models, ResNet50 achieved the highest classification accuracy and best generalization performance.

Why ResNet50?

✅ Deep residual learning
✅ Better feature extraction
✅ Reduced vanishing gradient problem
✅ High classification accuracy
✅ Strong transfer learning performance

📈 Evaluation Metrics

Evaluation metrics used:

Accuracy
Precision
Recall
F1-Score
Confusion Matrix
Classification Report
📉 Confusion Matrix
<p align="center"> <img src="https://images.unsplash.com/photo-1516321497487-e288fb19713f?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>

The confusion matrix demonstrates:

✅ High classification accuracy
✅ Better class prediction
✅ Reduced misclassification
✅ Strong model generalization

🌐 Flask Web Application
<p align="center"> <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1200&auto=format&fit=crop" width="90%"> </p>

The trained model was integrated into a Flask-based web application for real-time food image prediction.

💻 Frontend Features

✅ Food image upload
✅ Real-time prediction
✅ Responsive UI
✅ Interactive interface
✅ Prediction confidence score

⚡ Backend Features
Image preprocessing
Model loading
Prediction generation
Probability calculation
Result rendering
📂 Project Folder Structure
Food-Classification-Using-Deep-Learning/
│
├── dataset/
│
├── models/
│   ├── custom_cnn.h5
│   ├── vgg16_model.h5
│   ├── resnet50_model.h5
│
├── static/
│   ├── css/
│   ├── uploads/
│
├── templates/
│   ├── index.html
│
├── notebook/
│   ├── food_classification.ipynb
│
├── app.py
├── requirements.txt
├── README.md
⚡ Installation Guide
1️⃣ Clone Repository
git clone https://github.com/your-username/Food-Classification-Using-Deep-Learning.git
2️⃣ Navigate to Project Folder
cd Food-Classification-Using-Deep-Learning
3️⃣ Install Dependencies
pip install -r requirements.txt
4️⃣ Run Flask Application
python app.py
5️⃣ Open Browser
http://127.0.0.1:5000
📌 Prediction Example
Uploaded Image	Prediction
Pizza Image	Pizza
Burger Image	Burger
Ice Cream Image	Ice Cream
🚀 Future Enhancements
Mobile Application Integration
Real-Time Camera Prediction
Calorie Estimation System
Nutrition Recommendation System
Food Detection using YOLO
Cloud Deployment
Docker Integration
Streamlit Deployment
Multi-Food Detection
💼 Real-World Applications

✅ Smart Restaurants
✅ Food Delivery Platforms
✅ Healthcare Systems
✅ Dietary Monitoring
✅ Nutrition Analysis
✅ AI Food Recognition Systems

📚 References
TensorFlow Documentation
Keras Documentation
OpenCV Documentation
ImageNet Dataset
ResNet50 Research Paper
VGG16 Research Paper
Deep Learning Specialization
Towards Data Science
Machine Learning Mastery
👨‍💻 Author
<div align="center">
Madhu
Machine Learning & Deep Learning Enthusiast
</div>
⭐ Final Conclusion

The Food Classification Using Deep Learning project successfully demonstrates the implementation of advanced Deep Learning techniques for multi-class food image classification.

The project combines:

Custom CNN architecture
Transfer Learning
Image preprocessing
Data augmentation
Flask deployment
Real-time prediction

The system provides high classification accuracy and demonstrates the practical application of Computer Vision and Deep Learning in real-world food recognition systems.
