# Multivariate Time Series Forecasting Using Transformers
## Authors:
- Łukasz Wajda
- Michał Orlewski
- Przemysław Rewiś

## Project Description:
This project focuses on developing a Transformers-based neural network for modeling and forecasting multivariate time series data using a dataset related to COVID-19 in Poland. The entire project was implemented in Python using the Keras library for defining and training the neural network, as well as numpy, pandas, matplotlib, and sklearn for data analysis and model evaluation. 

## Data Preparation:
After an initial review of the dataset, specific parameters such as new cases, total tests conducted, new recoveries, and active cases were chosen as the data for modeling. Data preprocessing was performed, including removing unnecessary columns, handling missing data, and scaling the data using Min-Max Scaler.

## Model Architecture:
The model utilizes the Transformers architecture and consists of several key components, including the Time2Vector layer for encoding time information, self-attention mechanisms (SingleAttention and MultiAttention) for capturing dependencies between data points, and a TransformerEncoder for integrating all these elements.

## Data Splitting Methods:
Three different data splitting methods were employed in the project:

- K-Fold Cross Validation: Splitting data into folds and training the model on different data subsets.
- Time Series Split: Accounting for the temporal order of data when splitting into training and test sets.
- Blocking Time Series Split: Considering data blocks with similar patterns.

## Model Evaluation:
For each data splitting method, the model was evaluated using various metrics such as Mean Squared Error (MSE), Mean Absolute Error (MAE), Coefficient of Determination (R^2), Index of Agreement, and Mean Absolute Percentage Error (MAPE). These metric results aided in assessing the model's quality and selecting the appropriate data splitting method.

## Model Training:
The final version of the model was trained using properly prepared training, validation, and test data. The model was trained for 50 epochs, saving the best version based on validation data performance.

## Summary and Conclusions:
The project focused on comparing the performance of Transformers and LSTM networks in forecasting multivariate time series data. The results indicate that Transformers are more flexible in modeling complex time patterns, such as long-term dependencies and nonlinear trends, while LSTM networks are more efficient in capturing local dependencies and sequential time patterns.

## Sources:
- Article on Transformers in Time Series Forecasting
- [Keras Documentation](https://keras.io/api/)
- [scikit-learn Documentation](https://scikit-learn.org/stable/modules/classes.html)

*This README.md file provides a brief summary of the project, offering information about its authors, description, methodology, and results. Detailed documentation contains complete information regarding project implementation and analysis.*
