# Crab-age-prediction

## Data Preprocessing

1. **Loading Data**: The dataset is loaded from CSV files.
2. **Checking Data Types**: Ensured all columns have appropriate data types.
3. **Handling Missing Values**: Verified that there are no empty values.
4. **Encoding Categorical Variables**: The `Sex` column is converted into numerical form using one-hot encoding.
5. **Handling Outliers**: Outliers were removed based on the interquartile range (IQR) method.
6. **Feature Scaling**: Standardization was applied using `StandardScaler`.

## Feature Selection and Extraction

- A correlation matrix was generated to analyze relationships between features.
- Principal Component Analysis (PCA) was performed to reduce dimensionality and handle multicollinearity.
- Ridge Regression was explored as an alternative approach.

## Model Training

### Ridge Regression

- Grid search with cross-validation was performed to find the best alpha parameter.
- The model was evaluated using Mean Absolute Error (MAE).
- Results indicated that the best alpha value was `0`, meaning a plain linear regression model performed best.

### Linear Regression

- A basic linear regression model was trained on the standardized data.
- Predictions were made for the test dataset.

## Final Predictions

- The trained linear regression model was applied to the competition test dataset.
- The predicted crab ages were saved in `Final_submission_BA.csv` for submission.

## Results and Observations

- The independent variables did not exhibit strict linear relationships with the target variable, indicating that a plain linear model might not be the best predictor.
- Outlier removal improved data distribution slightly.
- PCA did not improve model performance.
- Ridge regression suggested that a simple linear regression model was optimal.
- Final predictions were generated using a standard linear regression model.

## Contributing

If you'd like to contribute to this project, feel free to submit a pull request with improvements or enhancements.

## License

This project is open-source and available for educational and research purposes.
