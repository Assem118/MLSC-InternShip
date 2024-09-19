# Near-Earth Objects (NEOs) Predictions

## Project Overview

This project focuses on the analysis of Near-Earth Objects (NEOs) to predict whether an NEO is hazardous or non-hazardous using machine learning models. The dataset contains information about various NEOs and their physical and orbital characteristics, and the task is to build a predictive model for identifying hazardous NEOs.

## Dataset

The dataset contains **338,199 records** with **9 columns**:

- **neo_id**: Unique identifier for each NEO.
- **name**: The name of the NEO.
- **absolute_magnitude**: The intrinsic brightness of the NEO (with some missing values).
- **estimated_diameter_min**: Minimum estimated diameter of the NEO (with some missing values).
- **estimated_diameter_max**: Maximum estimated diameter of the NEO (with some missing values).
- **orbiting_body**: The celestial body that the NEO orbits (mostly Earth).
- **relative_velocity**: The speed of the NEO relative to Earth.
- **miss_distance**: The closest distance the NEO will approach Earth.
- **is_hazardous**: A boolean indicator of whether the NEO is classified as hazardous.

## Key Steps and Work Done

### 1. Data Importing and Cleaning

The data was imported and thoroughly explored to understand its structure, and missing values were handled appropriately:
- **Missing values handling**: Columns with missing values, such as `absolute_magnitude`, `estimated_diameter_min`, and `estimated_diameter_max`, were filled using the median of each respective column due to their small percentage of missing data (0.008%).
  
### 2. Exploratory Data Analysis (EDA)

Several statistical summaries and visualizations were created to explore the dataset:

- **Descriptive statistics**: Summary statistics such as the range, median, and distribution for key variables (e.g., `absolute_magnitude`, `estimated_diameter_min`, `relative_velocity`, etc.).
- **Visualizations**:
  - **Distribution of hazardous vs. non-hazardous NEOs** (Pie chart, Count plot).
  - **Histograms** of key numeric features.
  - **Scatter plots** showing relationships between `estimated_diameter_min` vs `estimated_diameter_max`, and `miss_distance` vs `relative_velocity`.
  - **Correlation heatmap**: Illustrated the correlations between numeric features.

### 3. Data Preprocessing

To prepare the data for model training, several steps were taken:

- **Feature selection**: Dropped irrelevant features such as `neo_id`, `name`, and `orbiting_body`.
- **Train-test split**: The data was split into training (80%) and testing (20%) sets, maintaining the class distribution using stratified sampling.
- **Standardization**: The numeric features were scaled using `StandardScaler` to ensure they had similar ranges.
- **Handling class imbalance**: The dataset was imbalanced with more non-hazardous than hazardous NEOs. To address this, **SMOTE** (Synthetic Minority Oversampling Technique) was applied to oversample the minority class (hazardous NEOs) in the training set.

### 4. Model Training and Evaluation

Multiple machine learning models were trained and evaluated using various metrics, including **precision**, **recall**, **F1-score**, **AUC-ROC**, and **cross-validation scores**. The models included:

- **Logistic Regression**
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **K-Nearest Neighbors**
- **XGBoost Classifier**
- **Neural Networks**

#### Model Results:

Each model's performance was compared based on:
- Precision, Recall, and F1-score to measure how well the models classified hazardous NEOs.
- AUC-ROC to evaluate the model's ability to distinguish between hazardous and non-hazardous NEOs.
- Cross-validation scores to check for model stability and generalization performance.

### 5. Model Selection

After evaluating all models, the **best-performing model** was selected based on the highest **AUC-ROC score**.

## Visualizations and Plots

The notebook contains various visualizations that provide insight into the data and model performance:
- Pie charts and count plots showing class distribution.
- Histograms and scatter plots for numeric features.
- Correlation heatmaps to explore relationships between variables.
- Model performance metrics comparison, including precision, recall, F1-score, and AUC-ROC.

## Conclusion

The project successfully explored and cleaned the dataset, handled class imbalance, and trained several machine learning models. The best model was selected based on AUC-ROC, and future work could involve further tuning of the selected model or trying advanced ensemble techniques.

---

