# California-Housing-Analysis

Dataset:  
Use the California Housing dataset available in the sklearn library. This dataset contains
information about various features of houses in California and their respective median prices.

## 1. Loading and Preprocessing
* Loaded the California Housing dataset using the fetch_california_housing function from sklearn.  
* Converted the dataset into a pandas DataFrame for easier handling.
* Handled missing values and duplicates
* Performed feature scaling using StandardScaler method. This standardizes dataset's independent variables within a certain range.

#2. Regression Algorithm Implementation

Implemented the following regression algorithms:
* Linear Regression
  Linear Regression is a statistical model that assumes a linear relationship between the input features (independent variables) and the target variable (dependent variable). It tries to find the best-fitting straight line that minimizes the sum of squared differences between the predicted values and the actual values.

**Suitability for this dataset:** Linear Regression can be suitable for the California Housing dataset if there's an assumption that the median house value (target) changes proportionally with the input features like median income, house age, etc. It's a good starting point for regression tasks and can identify which features have a statistically significant linear relationship with the target.

* Decision Tree Regressor
  A Decision Tree Regressor builds a tree-like model of decisions, where each internal node represents a 'test' on an attribute, each branch represents the outcome of the test, and each leaf node represents the prediction value. The tree is built by recursively partitioning the data into subsets based on the features that best reduce impurity in the target variable.

**Suitability for this dataset:** Decision Tree Regressors are well-suited for the California Housing dataset because they can capture non-linear relationships and interactions between features without requiring explicit feature engineering for such relationships. They are robust to outliers and can handle both numerical and categorical data implicitly. This allows them to model complex decision rules that might dictate house prices, such as different pricing structures based on specific ranges of median income, number of rooms, or location (latitude/longitude).

#3. Model Evaluation and Comparison

Evaluated the performance of each algorithm using the following metrics:  
* Mean Squared Error (MSE)
* Mean Absolute Error (MAE)
* R-squared Score (R²)

###Based on the evaluation metrics calculated:

####Decision Tree Regressor is the best-performing algorithm.

* It has a lower Mean Absolute Error (MAE) of 0.4582 compared to Linear Regression's 0.5322. A lower MAE indicates better accuracy.
* It also has a lower Mean Squared Error (MSE) of 0.5160 compared to Linear Regression's 0.5518. A lower MSE indicates better performance.
* Furthermore, its R-squared Score (R²) of 0.6062 is higher than Linear Regression's 0.5789. A higher R² indicates a better fit of the model to the data.

The Decision Tree Regressor is likely performing better because it can capture non-linear relationships and interactions between features that a linear model cannot.


####Linear Regression is the worst-performing algorithm between the two.

* It consistently shows higher MAE and MSE, and a lower R² score compared to the Decision Tree Regressor.
* This suggests that the linear model might not be complex enough to capture the underlying patterns in the California Housing dataset, which often exhibit non-linear relationships between features and housing prices. 
