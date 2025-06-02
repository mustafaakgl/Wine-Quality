# Wine-Quality-Regression

## Wine Quality Analysis

A comprehensive analysis of the physicochemical properties of red wines and their impact on quality and alcohol content.





### Table of Contents

1) Project Overview

2) Installation

3) Dataset

4) Analysis Pipeline

5) Exploratory Data Analysis (EDA)

6) Statistical Tests

7) Regression Modeling

8) Results

9) Future Work

10) Usage

11) License


### Project Overview

This project analyzes 1,599 samples of red wine to identify the key physicochemical variables affecting wine quality and alcohol content. Using a combination of data cleaning, statistical testing, and regression modeling, we:

Explored variable distributions and outliers

Handled outliers with Winsorization

Applied Yeo–Johnson transformations for normality

Checked multicollinearity via correlation and VIF

Built and evaluated OLS regression models for quality and alcohol prediction

### Installation

git clone <repository-url>
cd wine-quality-analysis
python3 -m venv venv
source venv/bin/activate  # on Windows use: venv\Scripts\activate
pip install -r requirements.txt

### Dataset

The data lives in data/winequality-red.csv and includes:

### Feature

Description

fixed acidity

Fixed acidity

volatile acidity

Volatile acidity

citric acid

Citric acid

residual sugar

Residual sugar

chlorides

Chloride content

free sulfur dioxide

Free SO₂

total sulfur dioxide

Total SO₂

density

Density (g/cm³)

pH

pH level

sulphates

Sulphate content

alcohol

Alcohol by volume (%)

quality

Quality score (0–10 integer)

Analysis Pipeline

## Exploratory Data Analysis (EDA)

#### Summary statistics: df.describe(), missing value checks

Distribution plots: histograms, boxplots

Outlier detection: IQR method

Correlation heatmap

Statistical Tests

Group comparisons (t-tests, ANOVA) between quality levels

Pearson correlation tests for key pairs

Post-hoc analysis (Tukey HSD)

#### Regression Modeling

Data preparation: Winsorizer for outliers, Yeo–Johnson for skewness

Multicollinearity checks: correlation matrix, VIF analysis

OLS regression using statsmodels for:

Quality prediction (R² ≈ 0.36)

Alcohol content prediction (R² ≈ 0.67)

Results

Quality Model: Explains ~36% of variance. Key drivers:

Positive: alcohol, sulphates

Negative: volatile acidity

Alcohol Model: Explains ~67% of variance. Strong predictors:

Chemical features broadly capture alcohol variability

Model diagnostics generally satisfy linear regression assumptions, with some multicollinearity and heavy-tail residuals noted.

#### Future Work

Implement regularized regression (Ridge, Lasso, Elastic Net)

Explore tree-based models (Random Forest, XGBoost)

Engineer features: polynomial, interaction, chemical ratios

Dimensionality reduction (PCA), clustering (K-Means)

Model interpretation with SHAP or LIME

Classification and ordinal regression on discretized quality

Deploy interactive dashboards (Streamlit, Dash)

## Usage

Notebooks for each analysis step are under notebooks/. To run:

## jupyter notebook  # or jupyter lab

Execute cells sequentially to reproduce findings, visualizations, and models.

## License

This project is released under the MIT License. See LICENSE for details.

