# Housing Price Prediction Model

## Project Overview
This project utilizes **Linear Regression** to predict house prices based on features such as area, proximity to main roads, air conditioning, parking spaces, and more. Through rigorous feature engineering, data scaling, and cross-validation, the model achieves a cross-validated R² score of **67%**, explaining 67% of the variance in housing prices.

The goal of this project was to develop a reliable and interpretable regression model for housing price prediction, focusing on simplicity and performance.

---

## Dataset Description
The dataset includes the following key features:
- **Numerical Features**:
  - `area`: Total area of the house in square feet.
  - `parking`: Number of parking spaces.
- **Categorical Features** (encoded as binary):
  - `mainroad`: Whether the house is near a main road.
  - `prefarea`: Whether the house is in a preferred area.
  - `airconditioning`: Whether the house has air conditioning.
- **Engineered Features**:
  - `area_bathrooms`: Interaction between area and number of bathrooms.
  - `stories_airconditioning`: Interaction between stories and air conditioning.
  - `parking_guestroom`: Combined effect of parking and guestroom availability.

After preprocessing, unnecessary or low-impact features like `bathrooms`, `bedrooms`, and redundant interaction terms were dropped to optimize the model.

---

## Feature Engineering
To enhance model performance, several new interaction features were added:
1. `area_bathrooms`: Captures the influence of house size and number of bathrooms.
2. `stories_airconditioning`: Highlights multi-story houses with air conditioning.
3. `parking_guestroom`: Reflects premium properties with parking and guestrooms.
4. `area_basement`: Explores synergy between house size and having a basement.
5. Additional interactions aimed at uncovering complex relationships.

---

## Model and Methods
### Algorithms Used
- **Linear Regression**: Chosen for its interpretability and efficiency in capturing linear relationships.
- **StandardScaler**: Applied to normalize numerical features, ensuring consistency across varied scales.

### Preprocessing Steps
1. **Scaling**: Used Scikit-learn’s `StandardScaler` to standardize all numerical features.
2. **Feature Refinement**: Low-impact features and redundant interaction terms were removed to reduce noise.
3. **Cross-Validation**: Stratified K-Folds were used to validate performance across different data splits.

### Key Metric
- **Cross-Validated R² Score**: **67%**, indicating the model explains a substantial portion of housing price variability.

---

## How to Use
1. **Installation**:
   Install Python 3.8+ and the following dependencies:
   ```bash
   pip install pandas scikit-learn numpy matplotlib