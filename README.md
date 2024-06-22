# Startup Success Prediction
Note: As of June 20, this repository is a work in progress.

## Project Overview
This project aims to predict the success of startups using machine learning. The prediction model is designed to help venture capital firms evaluate potential investments by classifying startups as successful or not based on various features.

## Project Objectives
- Develop a machine learning model to predict startup success.
- Define success as a startup that has been 'acquired'.
- Use sectoral clustering to identify thematic sectors among startups.
- Evaluate the model's performance and visualize the training process.

## Datasets
- **Primary Dataset:** Contains information about startups including categories, funding amounts, status, and other relevant features.
- **Features Used:** `category_code`, `country_code`, `founded_at`, `funding_total_usd`, `status`, and other categorical identifiers.

## Method
1. **Data Cleaning and Preprocessing:**
   - Convert dates to datetime format.
   - Fill missing values.
   - Log transform of funding amounts.
   - Create a binary target variable `successful` based on the `status` column.

2. **Sectoral Clustering:**
   - Use Latent Dirichlet Allocation (LDA) for clustering startups into sectors based on `category_code` and `country_code`.

3. **Label Encoding:**
   - Encode categorical features using LabelEncoder.

4. **Neural Network Model:**
   - Build and train a neural network to predict startup success.
   - Implement early stopping to prevent overfitting.
   - Evaluate the model using accuracy and mean absolute error.
   - Visualize training and validation accuracy and loss.

## Model Architecture
- **Input Layer:** Features from the dataset after preprocessing.
- **Hidden Layers:** 
  - Dense layer with 64 units and ReLU activation.
  - Dropout layer with 50% dropout rate.
  - Dense layer with 32 units and ReLU activation.
  - Dropout layer with 50% dropout rate.
- **Output Layer:** 
  - Dense layer with 1 unit and sigmoid activation for binary classification.
- **Optimizer:** Adam
- **Loss Function:** Binary Crossentropy
- **Metrics:** Accuracy

## Results
- **Model Accuracy:** 98.367%
- **Mean Absolute Error:** 0.01536
- **Visualizations:**
  - Training and validation accuracy and loss plots to analyze the model's performance and detect potential overfitting.

![Unknown-1](https://github.com/indiatoryy/startup-valuation-analysis/assets/105636722/254a1734-0bb9-46a5-866d-cce05b7866d9)

## Next Steps
- **Hyperparameter Tuning:** Experiment with different hyperparameters to further improve the model's performance.
- **Feature Expansion:** Explore additional features that might contribute to better predictions.
- **Advanced Models:** Experiment with other machine learning models such as Random Forest, Gradient Boosting, or more complex deep learning architectures.
- **Deployment:** Develop a pipeline for deploying the model into a production environment for real-time predictions.
