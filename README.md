# Wine Quality Analysis 🍷

## Overview
This project combines chemical analysis with wine quality assessment. We collected wine samples (both red and white) from various wineries, each rated on a scale from 0 to 10.

## What's Inside?
- **DataFrames:** Two main datasets – one with labels and one without.
- **Visualizations:** Images that show the distributions of wine types and quality ratings.

## Labeling the Wine Samples 🍇
We employed a semi-supervised approach to assign red or white labels to the unlabeled samples:
- **Exploratory Data Analysis (EDA):** Cleaned and scaled the data.
- **Model Training:** Built a Random Forest model on the labeled data using balanced weights to handle class imbalances.
- **Semi-Supervised Labeling:** Predicted probabilities for unlabeled samples and set a threshold to assign labels confidently. This process successfully labeled **3823** new samples, with iterative retraining to cover most unknowns.

## Evaluating Wine Quality 🍾
Next, we shifted focus to assessing wine quality:
- **Distribution Check:** Analyzed the quality score distribution, noting an imbalance in the ratings.
- **Regression Trees:** Trained decision regression trees with wine quality as the target. We experimented with various parameter combinations and measured performance using Mean Absolute Error (MAE).
- **Optimization:** Employed grid search with cross-validation to fine-tune the model.
- **Insights:** Key factors influencing quality turned out to be chlorides, alcohol, density, sulphates, and free sulfur dioxide, rather than sugars or acidity.

## Project Structure 📂
