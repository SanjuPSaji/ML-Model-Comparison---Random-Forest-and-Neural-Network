# ML-Model-Comparison---Random-Forest-and-Neural-Network

This project uses machine learning models to diagnose breast cancer based on a dataset of features extracted from digitized images of fine needle aspirate (FNA) of breast masses. The models used are Random Forest and Neural Network classifiers.

## Dataset

The dataset contains the following columns:
- `id`: Identifier for each patient
- `diagnosis`: Diagnosis (M = malignant, B = benign)
- `radius_mean`, `texture_mean`, `perimeter_mean`, `area_mean`, `smoothness_mean`, `compactness_mean`, `concavity_mean`, `concave points_mean`, `symmetry_mean`, `fractal_dimension_mean`: Mean values of various features
- `radius_se`, `texture_se`, `perimeter_se`, `area_se`, `smoothness_se`, `compactness_se`, `concavity_se`, `concave points_se`, `symmetry_se`, `fractal_dimension_se`: Standard error values of various features
- `radius_worst`, `texture_worst`, `perimeter_worst`, `area_worst`, `smoothness_worst`, `compactness_worst`, `concavity_worst`, `concave points_worst`, `symmetry_worst`, `fractal_dimension_worst`: Worst values of various features

## Preprocessing

- Missing values in the dataset were identified and handled by dropping the column with missing values (`Unnamed: 32`).
- The `id` column was dropped as it is not relevant for the diagnosis.
- The `diagnosis` column was mapped to binary values (M = 1, B = 0).
- The data was split into training and testing sets with a 70-30 split.
- Feature scaling was applied using StandardScaler.

## Models

### Random Forest Classifier

- A Random Forest classifier was trained with a varying number of estimators.
- Learning curves were plotted for different numbers of estimators.
- The classifier achieved a training accuracy of 1.0000 and a test accuracy of 0.9708.

### Neural Network Classifier

- A Neural Network classifier was trained with different hidden layer sizes.
- Learning curves were plotted for different hidden layer sizes.
- The classifier achieved a training accuracy of 0.9950 and a test accuracy of 0.9766.

## Visualizations

- Learning curves for both models were plotted to compare training and testing errors.

## Results

- Random Forest Classifier:
  - Training Accuracy: 1.0000
  - Test Accuracy: 0.9708

- Neural Network Classifier:
  - Training Accuracy: 0.9950
  - Test Accuracy: 0.9766

## Requirements

- pandas
- scikit-learn
- matplotlib

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/SanjuPSaji/ML-Model-Comparison---Random-Forest-and-Neural-Network.git
   ```
2. Install the required packages:
   ```bash
   pip install pandas scikit-learn matplotlib
   ```
3. Run the Jupyter notebook or the Python script to preprocess the data, train the models, and visualize the results.

## Conclusion

The Neural Network classifier slightly outperformed the Random Forest classifier in terms of test accuracy, indicating its better generalization capability for this dataset.
