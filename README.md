# Klasifikasi-Gamber

## Dataset

The dataset used for this project is the [Vegetable Image Dataset](https://www.kaggle.com/datasets/misrakahmed/vegetable-image-dataset). 

- **Number of classes**: 15
- **Number of images per class**: ~1400
- **Total data** : 21.000

## Model Architecture

The CNN model follows a Sequential architecture:

1. `Conv2D (32, 3x3)` + ReLU + MaxPooling2D
2. `Conv2D (64, 3x3)` + ReLU + MaxPooling2D
3. `Conv2D (128, 3x3)` + ReLU + MaxPooling2D
4. Flatten
5. `Dense (256)` + ReLU
6. Output layer: `Dense (15)` + Softmax

## Training

- **Optimizer**: Adam
- **Loss Function**: `categorical_crossentropy`
- **Data Augmentation**: `ImageDataGenerator`
- **Callbacks**: `EarlyStopping` and `ModelCheckpoint` used during training

### Performance

- **Training Accuracy**: 97.89%
- **Validation Accuracy**: 98.52%
- **Testing Accuracy**: 98.62%

## Model Deployment

The model is exported into the following formats:
- **SavedModel** for TensorFlow Serving
- **TFLite** for mobile devices
- **TensorFlow.js** for web applications

## Author
Ester Tri Wahyuningsih
ID Dicoding: MC002D5X0841
