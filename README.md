# Artificial Neural Network - Customer Churn Prediction

A deep learning project implementing an Artificial Neural Network using TensorFlow/Keras to predict customer churn for a banking dataset.

## Project Overview

This project builds a binary classification model to predict whether a bank customer will leave (churn) based on various features such as credit score, geography, age, balance, and account activity. The implementation demonstrates core concepts of deep learning including data preprocessing, model architecture design, training, and evaluation.

## Dataset

**Churn Modelling Dataset**

The dataset contains customer information from a bank with the following features:

- **RowNumber**: Record index
- **CustomerId**: Unique customer identifier
- **Surname**: Customer surname
- **CreditScore**: Credit score of the customer
- **Geography**: Customer's country (France, Germany, Spain)
- **Gender**: Male or Female
- **Age**: Customer age
- **Tenure**: Number of years with the bank
- **Balance**: Account balance
- **NumOfProducts**: Number of bank products used
- **HasCrCard**: Whether customer has a credit card (0/1)
- **IsActiveMember**: Whether customer is an active member (0/1)
- **EstimatedSalary**: Estimated annual salary
- **Exited**: Target variable - whether customer left the bank (0/1)

## Technologies Used

- **Python 3.x**
- **TensorFlow 2.x** - Deep learning framework
- **Keras** - High-level neural networks API
- **Scikit-learn** - Data preprocessing and evaluation metrics
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib** - Data visualization

## Installation

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/SairajBhosale/Artifical_Neural_Network.git
cd Artifical_Neural_Network
```

2. Create a virtual environment:
```bash
python -m venv dl_env
```

3. Activate the virtual environment:

**Windows:**
```bash
.\dl_env\Scripts\activate
```

**Linux/Mac:**
```bash
source dl_env/bin/activate
```

4. Install required dependencies:
```bash
pip install -r requirements.txt
```

Or install manually:
```bash
pip install tensorflow scikit-learn pandas numpy matplotlib jupyter ipykernel
```

## Project Structure

```
Artifical_Neural_Network/
│
├── ann.ipynb                # Main Jupyter notebook with implementation
├── README.md               # Project documentation
├── requirements.txt        # Python dependencies
├── .gitignore             # Git ignore file
└── data/                  # Dataset directory (not included in repo)
    └── Churn_Modelling.csv
```

## Implementation Details

### Data Preprocessing

1. **Feature Selection**: Remove irrelevant columns (RowNumber, CustomerId, Surname)
2. **Encoding Categorical Variables**: Convert Geography and Gender to numerical format
3. **Train-Test Split**: Split data into training (80%) and testing (20%) sets
4. **Feature Scaling**: Normalize features using StandardScaler for optimal neural network performance

### Model Architecture

The Artificial Neural Network consists of:

- **Input Layer**: Accepts preprocessed features
- **Hidden Layers**: 
  - Dense layers with ReLU activation functions
  - Dropout layers for regularization to prevent overfitting
- **Output Layer**: Single neuron with sigmoid activation for binary classification

### Training Configuration

- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam
- **Metrics**: Accuracy
- **Epochs**: Configurable (typically 50-100)
- **Batch Size**: Configurable (typically 32)

## Model Architecture

```
Model: Sequential
_________________________________________________________________
Layer (type)                 Output Shape              Params   
=================================================================
Dense (hidden)               (None, units)             params    
Dropout                      (None, units)             0         
Dense (hidden)               (None, units)             params    
Dropout                      (None, units)             0         
Dense (output)               (None, 1)                 params    
=================================================================
```

## Results

The model achieves competitive performance in predicting customer churn:

- **Training Accuracy**: Reported in notebook
- **Test Accuracy**: Reported in notebook
- **Loss Metrics**: Training and validation loss tracked across epochs

Detailed performance metrics and visualizations are available in the Jupyter notebook.

## Usage

### Running the Project

1. Ensure you have the dataset (Churn_Modelling.csv) in the appropriate directory

2. Launch Jupyter Notebook:
```bash
jupyter notebook
```

3. Open `ann.ipynb`

4. Update the dataset path in the notebook:
```python
df = pd.read_csv("path/to/Churn_Modelling.csv")
```

5. Run all cells sequentially to:
   - Load and explore the data
   - Preprocess features
   - Build the neural network
   - Train the model
   - Evaluate performance
   - Make predictions

### Making Predictions

```python
# Example prediction for a new customer
new_customer = [[credit_score, geography, gender, age, tenure, 
                 balance, num_products, has_card, is_active, salary]]
prediction = model.predict(new_customer)
```

## Key Learnings

This project demonstrates:

- Building neural networks from scratch using TensorFlow/Keras
- Data preprocessing techniques for deep learning
- Handling categorical and numerical features
- Binary classification problem solving
- Regularization using dropout to prevent overfitting
- Model compilation and training workflows
- Evaluating model performance on test data
- Making predictions with trained models

## Future Improvements

Potential enhancements to the project:

- **Hyperparameter Tuning**: Optimize learning rate, number of layers, neurons per layer, dropout rate
- **Advanced Architectures**: Experiment with different network architectures
- **Cross-Validation**: Implement k-fold cross-validation for robust evaluation
- **Feature Engineering**: Create new features from existing data
- **Class Imbalance Handling**: Address potential imbalance in churn vs non-churn samples
- **Early Stopping**: Implement callbacks to prevent overfitting
- **Model Checkpointing**: Save best model weights during training
- **Visualization**: Add training history plots, confusion matrix, ROC curves
- **Ensemble Methods**: Combine multiple models for improved predictions
- **Deployment**: Create a web API for real-time predictions

## Performance Metrics to Add

- Confusion Matrix
- Precision, Recall, F1-Score
- ROC-AUC Curve
- Precision-Recall Curve
- Feature Importance Analysis

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add some improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

## License

This project is created for educational purposes.

## Acknowledgments

- Dataset: Churn Modelling Dataset
- TensorFlow and Keras documentation
- Scikit-learn documentation
- Deep Learning community

## Contact

**Sairaj Bhosale**
- GitHub: [@SairajBhosale](https://github.com/SairajBhosale)

---

**Note**: This project is part of a deep learning learning journey. Feedback and suggestions are always welcome!

**This README is AI generated**
