# Time Series Forecasting for Machine Learning Project

Welcome to the Machine Learning Project repository! This project explores various deep learning techniques and their applications.

## Table of Contents

- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Visualization](#visualization)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [Acknowledgments](#acknowledgments)

## Introduction
Accurately forecasting river and lake levels is essential for managing water resources and issuing flood alerts. Time series hydrological prediction models are commonly used for this purpose, as water level data from hydrological stations often have a time series structure. By leveraging historical data, these models can uncover hidden patterns and predict future water levels and behaviors. This information is crucial for resource management, flood impact mitigation, and natural disaster prevention.

There are two primary methods for constructing water level forecasting models: process-based and data-based numerical prediction. While process-based models like HEC-RAS (2017), MIKE-11 (2009, 2019), and MIKE-21 (2013, 2018) provide detailed physical event simulations, they require extensive hydrogeomorphic data and are computationally intensive. Additionally, the data requirements for these models can be challenging to meet, especially for water levels and flows.

In contrast, data-driven prediction models focus on identifying relationships and hidden information in the data using statistical and machine learning techniques. These models are generally faster and easier to implement, making them suitable for real-time river/lake flow forecasting. Data-driven models rely on available data and leverage statistical and machine learning methods to achieve accurate predictions.

Time series of hydrological data often include both linear and nonlinear components due to various external factors. Among linear statistical models, the autoregressive integrated moving average (ARIMA) model is widely used and effective for time series forecasting. For nonlinear time series, statistical machine learning techniques have been extensively employed.

Combining linear and nonlinear modeling approaches can enhance time series forecasting. This hybrid modeling strategy has shown promising results in various applications, as highlighted in studies by Pannakkong & Associates (2017), Zhong et al. (2017), Mohan and Reddy (2018), Yaseen et al. (2018), and others. Inspired by the success of hybrid models, we propose a two-part data-driven hybrid modeling process that uses statistical learning non-parametric and ARIMA models to capture the linear and nonlinear components of water level time series.

We hypothesize that using a hybrid approach can better expose hidden patterns in time series data than a single model. To test and validate our hypothesis, we will apply our method to three large datasets from hydrological stations along the Red River.

## Data Preprocessing
Datasets (Vu Quang, Hanoi, and Hung Yen).

Data preprocessing is a crucial step in preparing the dataset for model training. The following steps were undertaken:

- **Handling Missing Values**: Erroneous entries in the `Hour` column were replaced to ensure data consistency.
- **Date and Time Conversion**: The `Date` and `Hour` columns were converted into a unified `DateTime` index for easier manipulation and analysis.
- **Column Removal**: Unnecessary columns were dropped post-conversion to streamline the dataset.

## Model Training and Evaluation

We implemented several models to forecast water levels, including:

- **ARIMA**: For capturing linear components.
- **KNN, RF, SVM**: For capturing nonlinear components using machine learning techniques.
- **Hybrid models combining different architectures** : Description of the proposed hybrid modeling approach combining ARIMA with machine learning models.

Each model was trained and evaluated using historical data from various hydrological stations. We compared the models' performance using standard evaluation metrics such as Mean Absolute Error (MAE) and Root Mean Square Error (RMSE).

**Evaluation**
   - Data representation and pre-processing for the Red River hydrological stations.
   - Performance evaluation metrics including MAE, RMSE, R score, FSD, and NSE.
   - Comparative analysis of forecasting models on different datasets (Vu Quang, Hanoi, and Hung Yen).

## Visualization

Visualizations play a critical role in understanding the model's performance and data trends:

- **Data Visualization**: Initial data plots showcase water level trends over time, helping identify patterns and anomalies.
- **Prediction Visualization**: Comparative plots illustrate actual versus predicted water levels, as well as forecasts for various time horizons, demonstrating the model's predictive capability.

## Installation
To run this project locally, follow these steps:

- Clone the repository:
```bash
git clone https://github.com/Honpg/Deep-Learing.git
```
- Navigate to the project directory:
```bash
cd Machine-Learning
```

- Install the necessary dependencies
```bash
pip install -r requirements.txt
```
## Usage
To use the models, follow these instructions:

- Load the dataset:
```bash
Ensure your dataset is in the appropriate format as expected by the scripts.
```
- Run the Jupyter Notebooks:
Open the provided Jupyter notebooks to train and evaluate the models:
```bash
Arima_model.ipynb
KNN+ARIMA.ipynb
RF_KNN_SVM_ARIMA_single_model.ipynb
SVM(LINEAR)+ML(SVR_KNN_RF).ipynb
```

## Contributing

We welcome contributions to this project! Please fork the repository and create a pull request with your changes. For major changes, please open an issue to discuss what you would like to change:

**1.Fork the repository.**
**2.Create a new branch for your feature or bug fix.**
**3.Make your changes and commit them with clear messages.**
**4.Push your changes to your forked repository.**
**5.Submit a pull request with a description of your changes.**

## Acknowledgments
Special thanks to all contributors and the open-source community for their valuable resources and tools.

**Mentor** : [Prof.Hong Phan Thi Thu](https://scholar.google.com/citations?user=yXkziQIAAAAJ&hl=en&oi=ao)

**Member** : Khoi Nguyen Ta,Van Quoc Hoan Doan



