# AI-ML Assignment 1: Medical Insurance Cost Prediction

## Objective
The primary goal of this assignment is to train and evaluate a Multiple Linear Regression model capable of predicting medical insurance costs for individuals based on a given set of personal and demographic features.

## Dataset Link
[Kaggle: Medical Cost Personal Insurance Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)

*(Please note: To run this code locally, you must download the `insurance.csv` file from Kaggle and place it in the same directory as the notebook, as it is excluded from this repository.)*

## Libraries Used
- **Pandas**: Data manipulation and reading CSV files.
- **NumPy**: Mathematical operations and array handling.
- **Matplotlib & Seaborn**: Creating data visualizations, specifically the scatter plot.
- **Scikit-Learn**: Splitting the data, training the Linear Regression model, and computing evaluation metrics.

## Methodology
1. **Data Understanding**: Imported the CSV file, analyzed the initial rows, and classified variables into numerical and categorical types.
2. **Data Preprocessing**: Verified that there were no missing values in the data. Converted categorical columns (`sex`, `smoker`, `region`) into dummy variables. The dataset was then divided into 80% training data and 20% testing data.
3. **Model Development**: Constructed and trained a Multiple Linear Regression model using the training subset.
4. **Model Evaluation**: Tested the model's accuracy on the test subset. Performance was tracked using Mean Absolute Error (MAE), Mean Squared Error (MSE), and the R-squared (R²) metric. A scatter plot of true versus predicted charges was also generated.

## Results
*(Note: Metrics based on an 80/20 split with `random_state=101`)*
- **Mean Absolute Error (MAE)**: ~3994.46
- **Mean Squared Error (MSE)**: ~33311355.28
- **R-squared (R²) Score**: ~0.7606

## Conclusion
**Key findings:** The Multiple Linear Regression algorithm serves as a good preliminary model for estimating health insurance costs. It achieves an R² score of about 0.76, indicating a decent overall fit. However, its accuracy drops noticeably when predicting cases with exceptionally high medical charges.

**Factors affecting insurance charges:** Analysis suggests that a person's smoking habits, their BMI, and their age are the strongest contributors to higher insurance premiums.

**One limitation of Linear Regression for this problem:** Linear regression strictly assumes that all features affect the target variable in an additive, linear fashion. It fails to automatically account for complex interactions between variables, such as the multiplied health risk associated with an older patient who both smokes and has a high BMI.
