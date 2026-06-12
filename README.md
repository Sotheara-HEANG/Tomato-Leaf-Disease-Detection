# Tomato and Potato Leaf Disease Detection (LDD) using CNN

This repository contains the implementation of a Convolutional Neural Network (CNN) designed to classify and detect diseases in tomato and potato leaves. This project is part of the final assignment for the Artificial Intelligence course.

## Project Structure

```text
├── Train/
│   ├── CNN-Tomato LDD.ipynb       # Jupyter notebook for Tomato disease classification model
│   ├── Tomato_LDD.ipynb          # Jupyter notebook for Tomato disease classification model (v2)
│   ├── Train.ipynb               # Model training notebook
│   └── cnn_train.py              # Python script training the CNN classifier using Keras
├── .gitignore                    # Git ignore configuration
└── README.md                     # Project documentation
```

> [!NOTE]
> The datasets used for training and validation are excluded from this repository due to size constraints. The files `Dataset/` and `Dataset.zip` should be placed locally in the root directory before running the models.

## Model Architecture

The CNN classifier built in `cnn_train.py` consists of:
- **3 Convolutional Layers**:
  - Convolution2D (32 filters, 3x3 kernel, ReLU activation) -> MaxPooling2D (2x2 pool)
  - Convolution2D (16 filters, 3x3 kernel, ReLU activation) -> MaxPooling2D (2x2 pool)
  - Convolution2D (8 filters, 3x3 kernel, ReLU activation) -> MaxPooling2D (2x2 pool)
- **Flatten Layer**
- **Fully Connected (Dense) Layer**:
  - Dense (128 units, ReLU activation) with a Dropout rate of 0.5 to prevent overfitting
- **Output Layer**:
  - Dense (10 units representing the classes, Softmax activation)

## Installation & Setup

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd "AI Project"
   ```

2. **Install Dependencies**:
   Ensure you have Python installed. Install the required libraries using pip:
   ```bash
   pip install tensorflow keras numpy jupyter
   ```

3. **Prepare the Dataset**:
   Extract your dataset zip (`Dataset.zip`) into the project root. Ensure the folders are organized as:
   - `train/`: Training images grouped by class folder.
   - `val/`: Validation images grouped by class folder.

## Training the Model

To train the model using the Python script:
```bash
python Train/cnn_train.py
```

To run and experiment interactively via Jupyter Notebook:
```bash
jupyter notebook Train/Train.ipynb
```
