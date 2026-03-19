# Artificial Neural Network for Customer Churn Prediction

A deep learning project implementing an Artificial Neural Network (ANN) using TensorFlow/Keras to predict customer churn for a banking dataset.

## Project Overview

This project builds a binary classification model to predict whether a bank customer will leave (churn) based on various features such as credit score, geography, age, balance, and account activity. The model uses a multi-layer neural network architecture with dropout regularization to prevent overfitting.

## Dataset

**Churn Modelling Dataset** - Contains customer information from a bank with the following features:

- RowNumber
- CustomerId
- Surname
- CreditScore
- Geography
- Gender
- Age
- Tenure
- Balance
- NumOfProducts
- HasCrCard
- IsActiveMember
- EstimatedSalary
- Exited (Target Variable)

## Technologies Used

- **Python 3.x**
- **TensorFlow/Keras** - Deep learning framework
- **Scikit-learn** - Data preprocessing and model evaluation
- **Pandas** - Data manipulation
- **NumPy** - Numerical operations
- **Matplotlib** - Data visualization

## Project Structure

```
.
├── ann.ipynb           # Main Jupyter notebook with implementation
├── Churn_Modelling.csv # Dataset (not included in repo)
└── README.md           # Project documentation
```

## Setup Instructions

### 1. Create Virtual Environment

```bash
python -m venv dl_env
```

### 2. Activate Environment

**Windows:**
```bash
.\dl_env\Scripts\activate
```

**Linux/Mac:**
```bash
source dl_env/bin/activate
```

### 3. Install Dependencies

```bash
pip install ipykernel jupyter torch torchvision tensorflow scikit-learn pandas numpy matplotlib
```

## Model Architecture

The neural network consists of:

- **Input Layer**: Features from the dataset
- **Hidden Layers**: Dense layers with activation functions
- **Dropout Layers**: For regularization
- **Output Layer**: Single neuron with sigmoid activation for binary classification

## Implementation Steps

1. **Data Loading**: Import the Churn Modelling dataset
2. **Data Preprocessing**:
   - Remove unnecessary columns (RowNumber, CustomerId, Surname)
   - Handle categorical variables (Geography, Gender)
   - Split data into training and testing sets
   - Feature scaling using StandardScaler
3. **Model Building**:
   - Define Sequential model architecture
   - Add Dense and Dropout layers
   - Configure activation functions
4. **Model Compilation**:
   - Loss function: Binary crossentropy
   - Optimizer: Adam
   - Metrics: Accuracy
5. **Model Training**:
   - Train the model with specified epochs
   - Monitor validation performance
6. **Model Evaluation**:
   - Evaluate on test set
   - Generate predictions
   - Calculate accuracy metrics

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook ann.ipynb
```

2. Update the dataset path in the notebook:
```python
df = pd.read_csv("path/to/Churn_Modelling.csv")
```

3. Run all cells sequentially to:
   - Load and preprocess data
   - Build and train the model
   - Evaluate performance
   - Make predictions

## Key Features

- Binary classification for customer churn prediction
- Dropout regularization to prevent overfitting
- StandardScaler for feature normalization
- Train-test split for model validation
- Visualization of training history (if applicable)

## Results

The model achieves reasonable accuracy in predicting customer churn. Detailed metrics and performance analysis are available in the notebook.

## Future Improvements

- Hyperparameter tuning (learning rate, dropout rate, layer sizes)
- Experiment with different architectures
- Cross-validation for better generalization
- Feature engineering for improved predictions
- Early stopping callback for optimal training
- Model checkpointing to save best weights
- Confusion matrix and ROC curve analysis

## Learning Objectives

This project demonstrates:

- Building neural networks with TensorFlow/Keras
- Data preprocessing for deep learning
- Binary classification problem solving
- Regularization techniques
- Model evaluation and validation
- End-to-end deep learning workflow

## License

This project is for educational purposes.

## Acknowledgments

- Dataset source: Churn Modelling Dataset
- TensorFlow/Keras documentation
- Deep learning community resources
