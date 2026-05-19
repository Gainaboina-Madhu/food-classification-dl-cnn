# food-classification-dl-cnn
This project focuses on food image classification using Deep Learning techniques. It implements a Custom CNN architecture and compares its performance with powerful transfer learning models such as VGG16 and ResNet50. The system is trained to recognize multiple food categories from images with high accuracy using TensorFlow and Keras.

---

<div align="center">
  
# 🍔 Food Classification Using Deep Learning</div>
  
<div align="center">Custom CNN • VGG16 • ResNet50</div>
<p align="center"> <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python"> <img src="https://img.shields.io/badge/TensorFlow-Deep_Learning-orange?style=for-the-badge&logo=tensorflow"> <img src="https://img.shields.io/badge/Keras-CNN-red?style=for-the-badge&logo=keras"> <img src="https://img.shields.io/badge/OpenCV-Computer_Vision-green?style=for-the-badge&logo=opencv"> <img src="https://img.shields.io/badge/Flask-Web_App-black?style=for-the-badge&logo=flask"> <img src="https://img.shields.io/badge/Model-Custom_CNN-success?style=for-the-badge"> <img src="https://img.shields.io/badge/Transfer_Learning-VGG16_&_ResNet50-purple?style=for-the-badge"> </p>
<p align="center"> <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?q=80&w=1400&auto=format&fit=crop" width="100%"> </p>


---

## 📖 Overview

Food image classification is a practical application of **Computer Vision** and **Deep Learning** that enables machines to automatically recognize and categorize food items from digital images. This capability has real-world value in domains like smart restaurants, nutrition tracking, food delivery apps, and healthcare.

This project presents a complete end-to-end **Food Classification System** that:

- Trains **three different deep learning models** — Custom CNN, VGG16, and ResNet50
- Applies **image preprocessing** and **data augmentation** to improve model robustness
- Evaluates and compares model performance using standard metrics
- Deploys the best model (**ResNet50 at 97% accuracy**) via a **Flask web application** for real-time food image prediction

---

## 🎯 Objectives

- ✅ Automatically classify food images into 34 distinct categories across Indian, Western, and Asian cuisines
- ✅ Build and train a Custom CNN model from scratch
- ✅ Leverage pretrained VGG16 and ResNet50 models via Transfer Learning
- ✅ Apply data augmentation to prevent overfitting and improve generalization
- ✅ Evaluate and compare all models using accuracy, precision, recall, and F1-score
- ✅ Deploy the best model as a real-world Flask web application

---

## 🍔 Food Categories

The model classifies images across **34 food categories** spanning Indian, Western, and Asian cuisines:

### 🇮🇳 Indian Foods
| # | Class | # | Class |
|---|---|---|---|
| 1 | Butter Naan | 2 | Pav Bhaji |
| 3 | Chicken Curry | 4 | Kadai Paneer |
| 5 | Chapati | 6 | Masala Dosa |
| 7 | Dal Makhani | 8 | Jalebi |
| 9 | Chole Bhature | 10 | Kulfi |
| 11 | Kaathi Rolls | 12 | Dhokla |
| 13 | Pakode | 14 | Paani Puri |
| 15 | Samosa | 16 | Idli |
| 17 | Chai | | |

### 🍔 Western / Fast Foods
| # | Class | # | Class |
|---|---|---|---|
| 18 | Burger | 19 | Pizza |
| 20 | Hot Dog | 21 | Sandwich |
| 22 | Fries | 23 | Baked Potato |
| 24 | Donut | 25 | Cheesecake |
| 26 | Apple Pie | 27 | Crispy Chicken |
| 28 | Taco | 29 | Taquito |

### 🌏 Asian / Other
| # | Class | # | Class |
|---|---|---|---|
| 30 | Sushi | 31 | Momos |
| 32 | Fried Rice | 33 | Ice Cream |
| 34 | Omelette | | |

---

## 🧠 Technologies Used

| Technology | Purpose |
|---|---|
| **Python 3.8+** | Core programming language |
| **TensorFlow 2.x** | Deep learning framework for model building and training |
| **Keras** | High-level API for CNN model development |
| **OpenCV** | Image reading, resizing, and preprocessing |
| **NumPy** | Numerical operations and array manipulation |
| **Pandas** | Dataset handling and tabular data analysis |
| **Matplotlib** | Plotting training curves and performance graphs |
| **Seaborn** | Statistical visualizations (confusion matrix heatmaps) |
| **Flask** | Backend web framework for model deployment |
| **HTML / CSS** | Frontend design for the web interface |

---

## 🏗️ System Architecture

The system follows a clean pipeline from raw image input to predicted food category output:

```
┌─────────────────┐
│  Input Food     │  ← User uploads a food image (JPG/PNG)
│     Image       │
└────────┬────────┘
         ↓
┌─────────────────┐
│    Image        │  ← Resize to 224×224, normalize pixels, convert to RGB
│  Preprocessing  │
└────────┬────────┘
         ↓
┌─────────────────┐
│    Feature      │  ← CNN layers extract low-level and high-level visual features
│   Extraction    │
└────────┬────────┘
         ↓
┌─────────────────────────────┐
│     Deep Learning Model     │  ← Custom CNN / VGG16 / ResNet50
└────────────┬────────────────┘
             ↓
┌─────────────────┐
│   Prediction    │  ← Softmax outputs probability scores for all 12 classes
│     Layer       │
└────────┬────────┘
         ↓
┌─────────────────┐
│  Food Category  │  ← Final predicted label + confidence score
│     Output      │
└─────────────────┘
```

---

## 📂 Dataset Overview

| Attribute | Details |
|---|---|
| Problem Type | Multi-Class Image Classification |
| Number of Classes | 34 food categories (Indian, Western, Asian) |
| Input Type | RGB food images |
| Image Format | JPG / PNG |
| Input Shape | 224 × 224 × 3 |
| Models Used | Custom CNN, VGG16, ResNet50 |

---

## 🔄 Deep Learning Workflow

### Step 1 — Dataset Collection
Food images were collected for all 12 categories. Each category contains multiple images to ensure adequate training data for the model.

### Step 2 — Image Preprocessing
Raw images are prepared for model input through:
- **Resizing** all images to a uniform **224 × 224 pixels**
- **Normalization** — pixel values scaled from [0, 255] to [0, 1] for stable training
- **RGB Conversion** — ensuring all images are in 3-channel RGB format
- **Noise Reduction** — smoothing out irregularities in raw images

### Step 3 — Data Augmentation
To artificially expand the dataset and prevent overfitting, the following augmentation techniques are applied during training:

| Technique | Effect |
|---|---|
| Rotation | Randomly rotates image by a degree range |
| Zoom | Randomly zooms in/out of the image |
| Horizontal Flip | Mirrors the image left-to-right |
| Width Shift | Shifts image horizontally |
| Height Shift | Shifts image vertically |
| Shear Transformation | Distorts image along an axis |

### Step 4 — Train / Test Split
The dataset is split into training and validation sets to measure real-world generalization performance.

### Step 5 — Model Training
Three models are trained independently on the same dataset for fair comparison:
- Custom CNN (built from scratch)
- VGG16 (pretrained + fine-tuned)
- ResNet50 (pretrained + fine-tuned)

### Step 6 — Evaluation
Each model is evaluated on the validation set using multiple metrics.

### Step 7 — Flask Deployment
The best-performing model (ResNet50) is integrated into a Flask web application for real-time predictions.

---

## 🤖 Model Details

### 1️⃣ Custom CNN

A Convolutional Neural Network designed and trained entirely from scratch on the food dataset.

**Architecture:**

```
Input (224×224×3)
       ↓
Conv2D → ReLU → MaxPooling
       ↓
Conv2D → ReLU → MaxPooling
       ↓
Conv2D → ReLU → MaxPooling
       ↓
Flatten
       ↓
Dense → ReLU → Dropout
       ↓
Dense → Softmax (12 classes)
```

**Layer explanations:**
- **Convolutional Layers** — learn spatial features like edges, textures, colors, and shapes directly from image pixels
- **ReLU Activation** — introduces non-linearity, allowing the model to learn complex patterns
- **MaxPooling** — reduces spatial dimensions by keeping dominant features, reducing computation
- **Dropout** — randomly disables neurons during training to prevent overfitting
- **Flatten** — converts 2D feature maps into a 1D vector for the fully connected layers
- **Softmax Output** — produces a probability distribution across all 12 food classes

**Result: 92% accuracy**

---

### 2️⃣ VGG16 — Transfer Learning

VGG16 is a deep CNN pretrained on the **ImageNet** dataset (1.2 million images, 1000 classes), developed by the Visual Geometry Group at Oxford University.

**How Transfer Learning works here:**
- The **pretrained VGG16 base** (13 convolutional layers) is loaded with ImageNet weights and used as a fixed feature extractor
- A **custom classification head** (Dense → Dropout → Softmax for 12 classes) is added on top
- Only the top layers are trained; the base layers retain their pretrained knowledge

**Architecture overview:**
```
VGG16 Base (frozen weights)
  → Block1: Conv → Conv → MaxPool
  → Block2: Conv → Conv → MaxPool
  → Block3: Conv × 3 → MaxPool
  → Block4: Conv × 3 → MaxPool
  → Block5: Conv × 3 → MaxPool
       ↓
Custom Head (trainable)
  → Flatten → Dense(256) → Dropout → Dense(12) → Softmax
```

**Why VGG16?**
- Deep 16-layer architecture proven on large-scale image classification
- Rich feature extraction — early layers detect edges and textures; deeper layers detect complex shapes
- Faster convergence compared to training from scratch
- Strong baseline model widely used in transfer learning research

**Result: 95% accuracy**

---

### 3️⃣ ResNet50 — Transfer Learning ⭐ Best Model

ResNet50 is a 50-layer deep CNN pretrained on **ImageNet**, introduced by Microsoft Research in 2015. It solved the **vanishing gradient problem** in very deep networks through **residual (skip) connections**.

**The key innovation — Residual Block:**

```
Input (x)
   │
   ├──→ Conv → BatchNorm → ReLU → Conv → BatchNorm ──→ + ──→ ReLU → Output
   │                                                    ↑
   └────────────────────────────────────────────────────┘
                    (Skip / Shortcut Connection)
```

Instead of learning a full mapping F(x), each block learns the **residual** F(x) - x (the difference). This makes it much easier for gradients to flow backward through many layers during training.

**Architecture overview:**
```
ResNet50 Base (pretrained, frozen)
  → Conv1 + BatchNorm + ReLU + MaxPool
  → Layer1: 3× Residual Blocks (64 filters)
  → Layer2: 4× Residual Blocks (128 filters)
  → Layer3: 6× Residual Blocks (256 filters)
  → Layer4: 3× Residual Blocks (512 filters)
  → GlobalAveragePooling
       ↓
Custom Head (trainable)
  → Dense(256) → Dropout → Dense(12) → Softmax
```

**Why ResNet50 performs best:**
- **Residual connections** prevent vanishing gradients even at 50 layers deep
- **Batch Normalization** stabilizes training and allows higher learning rates
- **GlobalAveragePooling** reduces overfitting compared to large Flatten + Dense layers
- **50 layers of feature learning** captures far richer representations than shallower models
- Strong generalization from ImageNet pretraining on diverse, large-scale data

**Result: 97% accuracy** ✅

---

## ⚙️ Training Configuration

| Parameter | Value | Reason |
|---|---|---|
| Image Input Size | 224 × 224 × 3 | Standard size for VGG16 and ResNet50 pretrained weights |
| Batch Size | 32 | Balance between memory usage and gradient stability |
| Epochs | 25 | Sufficient for convergence with augmented data |
| Optimizer | Adam | Adaptive learning rate — fast and stable convergence |
| Loss Function | Categorical Crossentropy | Standard for multi-class classification |
| Hidden Activation | ReLU | Prevents vanishing gradients, fast computation |
| Output Activation | Softmax | Outputs probability distribution over 12 classes |

---

## 📊 Model Performance

| Model | Accuracy | Training Approach |
|---|---|---|
| Custom CNN | 92% | Trained from scratch |
| VGG16 | 95% | Transfer learning from ImageNet |
| **ResNet50** | **97%** ✅ | Transfer learning — residual architecture |

### Evaluation Metrics Explained

| Metric | What it measures |
|---|---|
| **Accuracy** | Overall percentage of correctly classified images |
| **Precision** | Of all images predicted as class X, how many truly are X |
| **Recall** | Of all true class X images, how many were correctly predicted |
| **F1-Score** | Harmonic mean of precision and recall — balanced metric |
| **Confusion Matrix** | Table showing predicted vs. actual class counts visually |
| **Classification Report** | Per-class breakdown of precision, recall, and F1-score |

---

## 🌐 Flask Web Application

The trained ResNet50 model is integrated into a **Flask-based web application** for real-time food image prediction without writing any code.

### How it works:
1. User opens the web app in a browser
2. Clicks **Upload Image** and selects a food photo (JPG/PNG)
3. The image is sent to the Flask backend
4. Flask preprocesses the image (resize to 224×224, normalize)
5. The ResNet50 model runs inference and returns predictions
6. The predicted **food category** and **confidence score (%)** are displayed on screen

### Features:
- ✅ Food image upload via browser
- ✅ Real-time prediction with confidence percentage
- ✅ Clean, responsive, interactive UI
- ✅ Handles JPG and PNG image formats
- ✅ No coding knowledge required to use

---

## 📂 Project Structure

```
Food-Classification-Using-Deep-Learning/
│
├── dataset/                        # Food image dataset (12 categories)
│
├── models/
│   ├── custom_cnn.h5               # Trained Custom CNN model weights
│   ├── vgg16_model.h5              # Trained VGG16 model weights
│   └── resnet50_model.h5           # Trained ResNet50 model weights (best)
│
├── static/
│   ├── css/                        # Stylesheet for web application
│   └── uploads/                    # Temporarily stores uploaded images
│
├── templates/
│   └── index.html                  # Web app frontend (HTML + UI)
│
├── notebook/
│   └── food_classification.ipynb   # Full model training and evaluation notebook
│
├── app.py                          # Flask backend — handles routing and prediction
├── requirements.txt                # All Python dependencies
└── README.md                       # Project documentation
```

---

## ⚡ Getting Started

### Prerequisites
- Python 3.8 or higher
- pip package manager
- (Recommended) A virtual environment

### Installation & Setup

```bash
# 1. Clone the repository
git clone https://github.com/your-username/Food-Classification-Using-Deep-Learning.git
 
# 2. Navigate into the project folder
cd Food-Classification-Using-Deep-Learning
 
# 3. (Optional but recommended) Create a virtual environment
python -m venv venv
source venv/bin/activate          # On Windows: venv\Scripts\activate
 
# 4. Install all required dependencies
pip install -r requirements.txt
 
# 5. Run the Flask web application
python app.py
```



### Usage
1. Open your browser and navigate to `http://127.0.0.1:5000`
2. Click **Upload Image** and choose a food photo from your device
3. Click **Predict** — the app will display the predicted food category and confidence score

---

## 🚀 Future Enhancements

| Enhancement | Description |
|---|---|
| 📷 Real-Time Camera | Live food detection and classification via webcam |
| 🔢 Calorie Estimation | Estimate calorie count based on predicted food type |
| 🥗 Nutrition Info | Display full nutritional values per food item |
| 🎯 YOLO Detection | Detect and localize multiple food items in a single image |
| ☁️ Cloud Deployment | Host on AWS / GCP / Heroku for public access |
| 🐳 Docker | Containerize the full application for easy portability |
| 📊 Streamlit | Build an alternative interactive data science UI |
| 📱 Mobile App | Android / iOS food recognition app |

---

## 💼 Real-World Applications

- 🍽️ **Smart Restaurants** — Automatically identify dishes from customer-uploaded photos
- 🚚 **Food Delivery Apps** — Verify food orders and assist menu categorization
- 🏥 **Healthcare Analytics** — Monitor and analyze patient dietary habits
- 📋 **Dietary Monitoring** — Track food consumption in wellness and fitness apps
- 🧬 **Nutrition Analysis** — Automate nutritional data extraction from food images
- 🤖 **AI Food Recognition** — Core intelligence engine for any food-aware AI system

---

## 👨‍💻 Author

# Gainaboina Madhu


---

## ⭐ Conclusion

This project successfully demonstrates how **Deep Learning** and **Computer Vision** can be combined to build an accurate, end-to-end food classification system. By training and comparing a Custom CNN with two powerful transfer learning models (VGG16 and ResNet50), the project clearly shows the advantage of pretrained models for image classification tasks.

**ResNet50** emerged as the best model with **97% classification accuracy**, thanks to its innovative residual connections that allow effective training of very deep networks. The system is fully deployed as a Flask web application, making it practical and accessible for real-world use.

---

> 💡 Found this project useful? Please give it a ⭐ on GitHub — it helps others discover it too!
