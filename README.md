 # Nowcasting E-commerce Transaction value using Google trends: Deep Learning Approach 

 This project focuses on nowcasting e-commerce transaction value and volume using advanced time series forecasting models. 
 The study integrates Google Trends data with transaction metrics to understand consumer behavior patterns and predict short-term e-commerce activity.
The research compares traditional statistical models ( SARIMAX) with deep learning architectures such as LSTM, Bi-LSTM, GRU, Bi-GRU, and a Hybrid BiLSTM–BiGRU model using walk-forward validation

# Objectives
1.	To investigate how Google Trends search terms can be formulated to represent e-commerce transaction behaviour.
2.	To implement deep learning models for nowcasting the value of e-commerce transactions in South Africa.
3.	To evaluate and compare the performance of these models with traditional forecasting methods in predicting e-commerce transaction value

# Methodology
## 1. Data Extraction

The data used for this study was extracted from official e-commerce transaction records available on Statistics South Africa (Stats SA) and Google Trends.

E-commerce Data: Monthly transaction value and volume from 2018–2025.

Google Trends Data: Search trend indices for keywords related to online shopping behavior.

Merging Process: Both datasets were merged on the date field (daily frequency), aligning temporal indices for correlation and forecasting analysis.

## 2. Data Preprocessing

Converted the date column to datetime format and set as index.

Resampled data to a daily frequency to ensure temporal consistency.

Missing values were handled through linear interpolation.

Normalization using Min–Max scaling was applied to all continuous features.

## 3. Feature Selection

Two main techniques were used:

Mutual Information (MI): To measure dependency between features and target variables.

Correlation Filtering: To remove redundant features with correlation coefficients above 0.9.

## 4. Data Denoising and Outlier Detection

Denoising: A moving average filter was applied to smooth temporal fluctuations and remove noise.

Outlier Detection: The IQR (Interquartile Range) method was used to detect and remove extreme values that could distort model learning.

## 4.  Modeling

Implemented and compared multiple forecasting models:

Model	Description
SARIMAX :	Classical time series model with external regressors
LSTM	: Long Short-Term Memory network for sequential dependencies
Bi-LSTM	: Bidirectional LSTM for forward and backward temporal patterns
GRU: 	Gated Recurrent Unit for efficient long-term modeling
Bi-GRU: 	Bidirectional GRU to enhance context learning
Hybrid (BiLSTM + BiGRU)	: Combined model capturing complex nonlinearities

## 5. Evaluation Metrics

Models were assessed using:

RMSE – Root Mean Squared Error

MAE – Mean Absolute Error

R² – Coefficient of Determination
