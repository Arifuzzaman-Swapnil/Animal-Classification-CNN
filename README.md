# 🐾 Animal Classification using CNNs | Capstone Project

---

## 📘 Project Description

This capstone project applies deep learning techniques to classify 30 different animal species from images using Convolutional Neural Networks (CNNs). The entire pipeline—from data collection and preprocessing to model training and web deployment—was built from scratch.

---

## 🎯 Project Goal

- Build an accurate and efficient AI system that can classify 30 animal species.
- Train, evaluate, and compare various deep learning models.
- Deploy the best-performing ensemble model in a user-friendly web application.

---

## 🔬 Methodology

![Methodology Diagram](./methodology-preview.pdf)

---

## 📂 Dataset

- **Collection Source**: Captured from zoos, online databases, and open datasets.
- **Image Count**: 3,000 images (100 images per class)
- **Image Size**: Resized to 512x512 pixels
- **Format**: JPG
- **Split**: 70% training, 15% validation, 15% test

---

## 🐾 Animal Classes

| ID | Animal Name       | ID | Animal Name        |
|----|-------------------|----|--------------------|
| 1  | Lion              | 16 | Gorilla            |
| 2  | Tiger             | 17 | Cheetah            |
| 3  | Elephant          | 18 | Giraffe            |
| 4  | Zebra             | 19 | Flamingo           |
| 5  | Monkey            | 20 | Camel              |
| 6  | Deer              | 21 | Tortoise           |
| 7  | Cow               | 22 | Buffalo            |
| 8  | Goat              | 23 | Dog                |
| 9  | Cat               | 24 | Leopard            |
| 10 | Horse             | 25 | Rhinoceros         |
| 11 | Bear              | 26 | Red Panda          |
| 12 | Kangaroo          | 27 | Peacock            |
| 13 | Sheep             | 28 | Fox                |
| 14 | Wolf              | 29 | Hyena              |
| 15 | Crocodile         | 30 | Ostrich            |

---

## 🏷️ Annotation

- Tool: **ImageJ (ImageFiji)**
- Process: Manually labeled and organized into folders by class
- Exported metadata for reference and audit

---

## 🧹 Preprocessing

- Resized all images to `512x512`
- Removed duplicate and corrupted files
- Auto-oriented and renamed all files
- Ensured `.jpg` format consistency
- Used `PIL`, `OpenCV`, and `os` libraries

---

## 🔁 Augmentation Techniques

- **Random Rotation**: Up to ±40 degrees  
- **Horizontal and Vertical Shifts**: Up to 20%  
- **Shear Transformation**: Applied shearing along axes  
- **Zoom In/Out**: Random zoom up to 20%  
- **Horizontal Flipping**: Enabled  
- **Brightness Adjustment**: Ranged between 0.8 to 1.2  
- **Fill Mode**: Nearest neighbor filling after transformation  

---

## 🧠 Models & Performance

| Model Variant                   | Accuracy (%) | Precision | Recall | F1-Score |
|--------------------------------|--------------|-----------|--------|----------|
| EfficientNetV2B0               | 98.50        | 98.92     | 98.29  | 98.60    |
| EfficientNetV2B0 (CV)          | 83.86        | 92.29     | 78.90  | -        |
| EfficientNetV2B3               | 83.33        | 84.45     | 83.33  | 83.31    |
| EfficientNetV2B3 (Fine-Tuned)  | 83.48        | 84.69     | 83.48  | 83.26    |
| MobileNet                      | 98.00        | 98.00     | 98.00  | 98.00    |
| MobileNet (CV)                 | 97.69        | 97.60     | 97.40  | 97.40    |
| MobileNetV3Small               | 95.94        | 96.17     | 95.94  | 95.85    |
| DenseNet121                    | 98.08        | 98.20     | 98.08  | 98.09    |
| DenseNet121 (CV)               | 96.79        | 96.96     | 96.75  | 96.77    |
| InceptionV3                    | 98.08        | 98.17     | 98.08  | 98.08    |
| InceptionV3 (CV)               | 97.22        | 97.32     | 97.22  | 97.17    |
| VGG19                          | 82.69        | 83.16     | 82.69  | 82.25    |
| **Ensemble Model**             | **98.44**    | **99.00** | **98.00** | **98.00** |

---

## 🤖 Ensemble Model (Final)

- Combined outputs of:
  - ✅ EfficientNetV2B0  
  - ✅ MobileNetV3Small  
  - ✅ DenseNet121  
- Strategy: Averaged softmax probabilities
- ✅ Achieved **98.44% Accuracy**
- ✅ Excellent generalization in both test and cross-validation sets

---

## 📊 Result Analysis

- High precision and recall for most models
- MobileNet and EfficientNet variants performed best
- Ensemble improved robustness across difficult classes
- Plotted:
  - Confusion matrices
  - Accuracy/loss curves
  - 5-fold cross-validation plots

---

## 🌐 Web Deployment

- **Backend**: Flask (Python)
- **Frontend**: HTML/CSS/Bootstrap
- **Functionality**:
  - User Login / Register
  - Upload animal image
  - Get prediction + class-wise confidence
- **Model Integrated**: Final Ensemble Model
- **Platform**: Deployed locally & on [Deta Space / Render / Railway] *(replace as needed)*

🔗 **Live Demo Link**: [[https://your-app-link.com](https://your-app-link.com)](https://github.com/Arifuzzaman-Swapnil/Animal-Classification-WebSite)

---

## 👨‍💻 Contributors

- Md Arifuzzaman Swapnil  
- Email: md.arifuzzamanswapnil@gmail.com
- Phone number: 01722569839

---

## 📄 License

This project is open-source and available under the MIT License.

