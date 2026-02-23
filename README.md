# 🧠 Neural Network for Pima Indians Diabetes Prediction

A binary classification neural network to predict diabetes in Pima Indian women based on clinical measurements.

## 📋 Project Overview

This project builds a **Sequential Neural Network** using TensorFlow/Keras to predict diabetes based on 8 clinical measurements from the Pima Indians Diabetes Database.

**Goal**: Binary classification (No Diabetes / Diabetes)

## 📊 Dataset

**Source**: UCI Machine Learning Repository via Kaggle  
**Total Samples**: 768 patients  
**Features**: 8 clinical measurements  
**Target**: Outcome (0 = No Diabetes, 1 = Diabetes)

### Features

| Feature | Description | Unit |
|---------|-------------|------|
| Pregnancies | Number of pregnancies | count |
| Glucose | Plasma glucose concentration | mg/dL |
| BloodPressure | Diastolic blood pressure | mmHg |
| SkinThickness | Triceps skinfold thickness | mm |
| Insulin | 2-hour serum insulin | μU/mL |
| BMI | Body mass index | kg/m² |
| DiabetesPedigreeFunction | Diabetes heredity score | score |
| Age | Age | years |

### Class Distribution
- No Diabetes (0): 500 samples (65.1%)
- Diabetes (1): 268 samples (34.9%)

## 🏗️ Model Architecture

```
Input Layer (8 features)
    ↓
Dense Layer (32 neurons, ReLU activation)
    ↓
Dense Layer (16 neurons, ReLU activation)
    ↓
Output Layer (1 neuron, Sigmoid activation)
```

**Total Parameters**: 784

## 🛠️ Data Preprocessing

1. **Missing Data**: Zero values replaced with median values for Glucose, BloodPressure, SkinThickness, Insulin, and BMI
2. **Train-Test Split**: 80-20 split with stratification
3. **Feature Scaling**: StandardScaler (mean=0, std=1)

## ⚙️ Training Configuration

- **Optimizer**: Adam (learning_rate=0.001)
- **Loss Function**: Binary Crossentropy
- **Metrics**: Binary Accuracy
- **Epochs**: 150 (with Early Stopping)
- **Batch Size**: 32
- **Validation Split**: 20%
- **Early Stopping**: Patience=10, monitoring validation loss

## 📈 Evaluation Metrics

The model is evaluated using:
- **Test Accuracy**: Overall correctness
- **Precision**: Of predicted diabetes, how many are correct
- **Recall**: Of actual diabetes cases, how many were detected
- **F1-Score**: Harmonic mean of precision and recall
- **Confusion Matrix**: Breakdown of predictions

### Medical Interpretation

🚨 **False Negatives (FN)** are critical - missing diabetes can lead to serious complications  
⚠️ **False Positives (FP)** are less critical - patients can be retested

## 📁 Project Structure

```
NeuralNetwork-Diabetes/
├── pima-diabetes-nn.ipynb    # Main Jupyter notebook
└── README.md                  # Project documentation
```

## 🚀 Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook pima-diabetes-nn.ipynb
```

2. Run the cells in order:
   - Part 1: Import Libraries and Load Dataset
   - Part 2: Exploratory Data Analysis
   - Part 3: Data Preprocessing
   - Part 4: Build Neural Network
   - Part 5: Compile and Train Model
   - Part 6: Visualize Training History
   - Part 7: Evaluate Model Performance
   - Part 8: Confusion Matrix & Detailed Metrics
   - Part 9: Classification Metrics

## 📦 Required Libraries

- numpy
- pandas
- scikit-learn
- tensorflow
- matplotlib
- seaborn
- kagglehub

## 📊 Visualizations

The notebook includes:
- Zero values distribution by feature
- Training/Validation accuracy curves
- Training/Validation loss curves
- Confusion matrix heatmap

## 🏥 Medical Significance

**Recall is critical** for medical screening - missing diabetes diagnosis has serious health consequences. The model aims to minimize false negatives (missed diabetes cases) while maintaining reasonable precision.

## 📧 Contact

**Nada Omar**  
GitHub: [@NadaOmar03](https://github.com/NadaOmar03)

---
