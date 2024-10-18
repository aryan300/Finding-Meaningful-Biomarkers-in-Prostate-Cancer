# Finding Meaningful Biomarkers in Prostate Cancer

This repository contains the **Finding Meaningful Biomarkers in Prostate Cancer** project, focused on identifying significant biomarkers that correlate with prostate cancer severity using gene expression data. The project applies various machine learning techniques to discover meaningful patterns and features, aiming to assist in better cancer prognosis and patient stratification.

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Technologies Used](#technologies-used)
- [Methodology](#methodology)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

Prostate cancer is one of the most common types of cancer among men. Accurately predicting its progression is critical for early diagnosis and treatment. This project aims to identify gene expression biomarkers related to prostate cancer severity (Gleason score) by analyzing high-dimensional gene expression data.

The dataset used contains:
- 60,483 gene expressions across multiple samples.
- Clinical data such as patient Gleason scores and cancer stages.

The project leverages feature selection and machine learning to detect relevant biomarkers and improve cancer prognosis accuracy.

## Objectives

- Identify gene biomarkers that correlate with prostate cancer severity (Gleason score).
- Handle high-dimensional data using appropriate feature selection techniques.
- Improve model performance by addressing class imbalance and outlier detection.
- Develop predictive models for cancer severity classification.

## Technologies Used

- **Python**: Main programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Scikit-learn**: Machine learning models and preprocessing
- **SMOTE**: Synthetic Minority Over-sampling for class imbalance
- **Isolation Forest**: Outlier detection
- **Information Gain**: Feature selection
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebook**: Development environment

## Methodology

1. **Data Preprocessing**: 
   - Cleaned the gene expression dataset, removed low-variance features, and normalized data.
   
2. **Class Imbalance Handling**: 
   - Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to address class imbalance between cancer severity classes.

3. **Outlier Detection**: 
   - Used **Isolation Forest** to detect and remove outliers from the dataset.

4. **Feature Selection**: 
   - Employed **Information Gain** to identify the most relevant gene expressions that contribute to prostate cancer progression.

5. **Machine Learning**:
   - Built classification models such as Logistic Regression, Random Forest, and XGBoost to predict prostate cancer severity based on the selected biomarkers.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/aryan300/Finding-Meaningful-Biomarkers-in-Prostate-Cancer.git
   cd Finding-Meaningful-Biomarkers-in-Prostate-Cancer
   ```

2. Create a virtual environment and install dependencies:

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

## Usage

1. Preprocess the dataset:

   - Run the `data_preprocessing.ipynb` notebook to clean the data and perform outlier detection.

2. Perform feature selection:

   - Use the `feature_selection.ipynb` notebook to apply Information Gain and select important biomarkers.

3. Train the models:

   - Use the `model_training.ipynb` notebook to train and evaluate machine learning models on the processed data.

4. Analyze results:

   - Run the `results_analysis.ipynb` notebook to visualize the performance of the models and analyze the selected biomarkers.

## Project Structure

```
.
├── data/                   # Raw and processed data files
├── notebooks/              # Jupyter notebooks for analysis and modeling
├── models/                 # Trained machine learning models
├── results/                # Model performance and feature analysis
├── README.md               # Project README file
├── requirements.txt        # Python dependencies
└── LICENSE                 # Project license
```

## Results

The project identified significant biomarkers correlating with prostate cancer severity. The models achieved the following performance metrics:

- **Accuracy**: 97.5%-99.5%
- **F1-Score**: 99.2%

These findings could potentially support personalized treatment plans for patients with prostate cancer.

## Contributing

Contributions are welcome! If you would like to improve the project, please submit a pull request or open an issue.

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Create a new Pull Request
