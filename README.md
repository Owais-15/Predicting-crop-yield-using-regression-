# Predicting-crop-yield-using-regression
# Crop Yield Prediction

## Project Goal

The primary objective of this project is to develop and train a predictive model for crop yield. The model utilizes various factors, including environmental conditions (temperature, precipitation), soil characteristics (though not explicitly used in the final model), and pesticide application. By accurately predicting crop yield, this project aims to contribute to more sustainable farming practices, potentially reducing the land area required for cultivation and mitigating associated environmental impacts.

## Data Sources

The project uses four datasets:

- **`pesticides.csv`**: Contains information on pesticide usage.
- **`rainfall.csv`**: Provides data on average annual precipitation.
- **`temp.csv`**: Includes average temperature data.
- **`yield.csv`**: Contains crop yield data.

These datasets were merged and cleaned to create a unified dataset (`df_yield`) for analysis and modeling.

## Data Exploration (EDA)

The data exploration phase involved:

- Examining the structure and content of each dataset.
- Cleaning the data by selecting relevant columns and renaming them for consistency.
- Merging the datasets based on 'Year' and 'Area'.
- Analyzing numerical and categorical data statistics.
- Visualizing data distributions and relationships using histograms, scatter plots, and box plots to understand the impact of temperature, pesticides, and precipitation on crop yield across different crop types and regions.

## Modeling

Several regression models were implemented and evaluated to predict crop yield:

- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Decision Tree Regressor
- K-Nearest Neighbors Regressor
- Neural Network Regressor

The data was split into training and testing sets (80/20 split) and categorical features were one-hot encoded.

## Results

The models were evaluated using the following metrics:

- R-squared ($R^2$)
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

A comparison of the model performances is summarized in the table below:

| Model             | Set      | MAE          | RMSE         | MSE            | R^2   |
|-------------------|----------|--------------|--------------|----------------|-------|
| Random Forest     | Training | 1847.07      | 4804.71      | 23085255.50    | 0.996 |
|                   | Test     | 4617.85      | 12087.54     | 146108829.92   | 0.978 |
| Gradient Boosting | Training | 940.24       | 2098.54      | 4403874.27     | 0.999 |
|                   | Test     | 19008.43     | 11892.89     | 141440936.93   | 0.978 |
| Decision Tree     | Training | 1510.57      | 5174.75      | 26778126.02    | 0.996 |
|                   | Test     | 4869.18      | 13837.34     | 191472181.04   | 0.971 |
| K-Nearest         | Training | 144.19       | 1614.77      | 2607486.06     | 0.999 |
|                   | Test     | 28741.47     | 54523.71     | 2972835842.96  | 0.555 |
| Neural Network    | Training | 25961.33     | 39646.89     | 1571876351.55  | 0.771 |
|                   | Test     | 26146.88     | 39810.19     | 1584851962.55  | 0.762 |
| Linear Regression | Training | 27565.79     | 45027.95     | 2027516959.43  | .705  |
|                   | Test     | 27570.11     | 44948.42     | 2020360951.03  | 0.697 |

The Gradient Boosting model demonstrated the best performance, with high R-squared values and lower error metrics compared to other models, indicating a strong ability to generalize to unseen data.

Feature importance analysis using the Gradient Boosting model highlighted the significance of 'Item' (crop type), 'Area' (region), and environmental factors in predicting crop yield.

Cross-validation and learning curve analysis further supported the Gradient Boosting model's performance and indicated that more data could potentially improve its predictive power.

## Conclusions

Based on the evaluation metrics and analysis, the Gradient Boosting model is the most suitable for predicting crop yield in this project. Its high accuracy on both training and testing datasets, coupled with its ability to generalize well, makes it a reliable tool for providing yield predictions given the input features. The project successfully demonstrates the potential of using machine learning to aid in crop yield prediction for more sustainable agricultural practices.

## References

The project utilized data and information from the following sources:

1. Databank, T.W.: Climate change overview: Country summary (2023), accessed on October 20, 2023
2. Food, of the United Nations, A.O.: Faostat (2023), accessed on October 20, 2023
3. Geopard: Predicting crop yield with remote sensing data (2023), accessed: 2023-11-21
4. Jupyter, P.: Project Jupyter: Open source software for interactive computing (2023), accessed: 2023-11-02
5. OECD: Crop Production (2023), accessed on October 25, 2023
6. Ritchie, H., Rosado, P., Roser, M.: Crop yields. Our World in Data (2022), accessed on October 20, 2023
7. pandas development team, T.: pandas: Powerful data structures for data analysis (2023), accessed: 2023-11-02
8. USDA: Food security status of U.S. households in 2022 (2023), accessed on October 2 2023
9.
