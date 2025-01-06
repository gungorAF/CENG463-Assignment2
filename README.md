# CENG463 - Assignment 2

This repository contains the implementation and results for Assignment 2 of the CENG463 (Introduction to NLP) course at METU. The assignment focuses on analyzing parliamentary speeches to determine:
1. The political ideology of the speaker's party (left-wing or right-wing).
2. Whether the speaker's party is in government or opposition.

## Dataset
The datasets used in this assignment are:
- orientation-pr-dataset: Used for identifying political ideology.
- power-pr-dataset: Used for identifying government/opposition status.

Both datasets are provided in tab-separated text file format (.tsv).

## Tasks and Methodology
### Task 1: Identify Political Ideology
- A masked language model was fine-tuned on the orientation-pr-dataset for classification.
- Class imbalance was addressed through oversampling.
- Data was split into:
  - 78% for training
  - 12% for validation
  - 10% for testing

### Task 2: Identify Government/Opposition Status
- Similar to Task 1, the model was fine-tuned on the power-pr-dataset.

### Inference
- A causal language model was used in a zero-shot manner for inference. 
- Predictions were generated using a prompt-based setup.

## Results
The fine-tuned masked language model outperformed the zero-shot causal model in all performance metrics (accuracy, precision, recall, and F1 score). Details of the results can be found in the report.

## Requirements
- Python 3.8+
- transformers library
- pandas
- scikit-learn
