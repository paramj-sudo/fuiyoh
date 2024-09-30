# NEXUS Kaggle Contest
Team Fuiyoh

# MLP Model for Drug Target Classification

## Overview
This repository contains an implementation of a Multi-Layer Perceptron (MLP) model for classifying drug target statuses based on various features. The model preprocesses text data using TF-IDF vectorization and applies one-hot encoding for categorical variables. It achieves a validation accuracy of **95%**.

## Table of Contents
- [Installation](#installation)
- [Data](#data)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

To run this project, you need Python 3.x and the following libraries:

- pandas
- numpy
- scikit-learn
- tensorflow

You can install the required libraries using pip:

```bash
pip install pandas numpy scikit-learn tensorflow
```

## Data

The dataset used for training and validation is in CSV format and contains various features, including:

- **DRUGTYPE**
- **Drug_high_status**
- **Drug_Status**
- **Disease_of_highest_status**
- **BIOCLASS**
- **SYNONYMS**
- **FUNCTION**
- **Disease**
- **Target_Status** (the target variable)

Place the dataset in the same directory as the script, naming the training file `train.csv`.



## Model Architecture

The model is built using the following layers:

- **Input Layer:** Accepts the preprocessed input features.
- **Two Branches:** 
  - Branch 1 with a larger number of neurons and Leaky ReLU activation.
  - Branch 2 with fewer neurons to capture different feature interactions.
- **Concatenation Layer:** Merges the outputs from both branches.
- **Hidden Layers:** Multiple Dense layers with Leaky ReLU activation, Batch Normalization, and Dropout for regularization.
- **Output Layer:** A softmax layer for multi-class classification.

### Hyperparameters

- **Layer Sizes:** [256, 512, 1024, 512, 256]
- **Dropout Rate:** 0.4
- **Learning Rate:** 0.001
- **Batch Size:** 256
- **Epochs:** 150
- **L2 Regularization Factor:** 0.0001

## Results

The model achieves a validation accuracy of **95%**. This high accuracy indicates that the model effectively captures the relationships in the data and generalizes well to unseen samples.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License

