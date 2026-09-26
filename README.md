# Cellula Technologies - RNN & LSTM Text Classification

This repository contains my Week 1 NLP task submission for Cellula Technologies.

The project implements and evaluates two deep learning models for multiclass text classification:

- Recurrent Neural Network (RNN)
- Long Short-Term Memory (LSTM)

## Project Structure

```text
Cellula_1week_AlaaBoghdady/
│
├── RNN/
│   ├── Cellula_RNN_Training.ipynb
│   └── RNN_Results.pdf
│
├── LSTM/
│   ├── Cellula_LSTM_Training.ipynb
│   └── LSTM_Results.pdf
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Dataset

The supplied dataset contains:

- `query`
- `image descriptions`
- `Toxic Category`

The target consists of 9 different classes.

## Project Workflow

1. Load and inspect the dataset.
2. Analyze class distribution and data quality.
3. Apply text preprocessing.
4. Combine query text with image-description text.
5. Create stratified training, validation, and test sets.
6. Tokenize and pad the text sequences.
7. Handle class imbalance using class weights.
8. Train and evaluate the RNN model.
9. Train and evaluate the LSTM model.
10. Generate classification reports, training curves, and confusion matrices.

## RNN Model

The RNN architecture includes:

- Embedding layer
- Spatial Dropout
- Bidirectional SimpleRNN
- Global Max Pooling
- Dense layer
- Dropout
- Softmax output layer

### RNN Results

| Metric | Result |
|---|---:|
| Accuracy | 93.33% |
| Macro F1 | 0.9344 |
| Weighted F1 | 0.9330 |

Required F1 score: **>= 0.75**

Result: **PASS**

## LSTM Model

The LSTM architecture includes:

- Embedding layer
- Spatial Dropout
- Bidirectional LSTM
- Global Max Pooling
- Dense layer
- Dropout
- Softmax output layer

### LSTM Results

| Metric | Result |
|---|---:|
| Accuracy | 95.33% |
| Macro F1 | 0.9504 |
| Weighted F1 | 0.9513 |

Required F1 score: **>= 0.85**

Result: **PASS**

## Data Quality Notes

During data analysis, several limitations were identified in the supplied dataset:

- 973 exact duplicate rows.
- 1,000 template-like rows.
- Class imbalance between categories.
- Repeated inputs were present across the dataset.

Because of these characteristics, the reported metrics should be interpreted as benchmark results on the supplied dataset.

For a production system, additional data cleaning, deduplication, label review, and a leakage-free external test set would be recommended.

## How to Run

1. Open either training notebook in Google Colab.
2. Upload the supplied dataset when requested.
3. Run all notebook cells.
4. The notebook will train and evaluate the selected model.
5. Review the generated classification report, confusion matrix, and F1 scores.

## Requirements

Install the required Python packages using:

```bash
pip install -r requirements.txt
```

Main libraries:

- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- scikit-learn

## License

This project is licensed under the **Apache License 2.0**.
