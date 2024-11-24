# DePTH2-Analysis

## Overview
DePTH is a predictive model designed to assess the interaction between Human leukocyte antigens(HLA) and T-cell receptor(TCR). By inputting an HLA and a TCR, the model generates a score representing their association. For details on the model structure and usage, please refer to [https://liusi2019.github.io/DePTH-tutorial/](#).

## Features
This repository focuses on the further development and analysis of the DePTH model, including:
1. **Confounding Factors Analysis**  
   - Analysis of factors such as:
     - CDR3 length  
     - TCR generation probability  

2. **DePTH 2.0 Enhancements**  
   - Updates and improvements to the original DePTH model for better performance and usability.


## Getting Started

### Prerequisites
All the analyses conducted in this project are implemented in **R**. Depending on the type of analysis, different R packages are required. For convenience, we list all the required packages below. Please ensure they are installed before running the scripts.

### Required R Packages
To run the analyses, you will need the following R packages:

- `tidyr`
- `dplyr`
- `lmtest`
- `stringr`
- `ggplot2`
- `gridExtra`
- `plotly`
- `Matrix`
- `uwot`
- `irlba`
- `pROC`
- `ggpointdensity`
- `viridis`
- `purrr`
- `igraph`
- `pbapply`
- `data.table`
- `Rtsne`
- `leidenbase`
- `reshape2`

### Installing Required Packages
You can install the required packages in R using the following command:

```R
required_packages <- c(
  "tidyr", "dplyr", "lmtest", "stringr", "ggplot2", "gridExtra", "plotly",
  "Matrix", "uwot", "irlba", "pROC", "ggpointdensity", "viridis", "purrr",
  "igraph", "pbapply", "data.table", "Rtsne", "leidenbase", "reshape2"
)

install.packages(setdiff(required_packages, installed.packages()[, "Package"]))

## Confounding Variable Analysis

### Overview
This section focuses on analyzing potential confounding variables that may influence the performance or interpretation of the DePTH model. Confounding variables such as **CDR3 length** and **TCR generation probability** are evaluated to better understand their impact on model predictions.

### Steps for Analysis
1. **Data Preparation**:  
   - Ensure that the dataset includes relevant features such as CDR3 length and generation probability.  
   - Clean and preprocess the data as needed.

2. **Exploratory Data Analysis (EDA)**:  
   - Use visualizations and statistical summaries to assess the distribution of confounding variables.  
   - Examples include histograms for CDR3 length or scatter plots for TCR generation probability vs. predicted scores.

3. **Statistical Testing**:  
   - Perform statistical tests to evaluate the relationship between confounding variables and model outputs (e.g., correlation analysis or regression models).

4. **Visualization of Results**:  
   - Generate plots to illustrate the effects of confounding variables:
     - CDR3 length distributions.
     - Predicted scores stratified by TCR generation probabilities.
   - Use packages like `ggplot2`, `ggpointdensity`, and `viridis` for detailed visualizations.

### Example Code
```R
# Example: Analyze the effect of CDR3 length
library(ggplot2)
library(ggpointdensity)

# Scatter plot of predicted score vs. CDR3 length
ggplot(data, aes(x = CDR3_length, y = predicted_score)) +
  geom_pointdensity() +
  scale_color_viridis() +
  labs(
    title = "Effect of CDR3 Length on Predicted Scores",
    x = "CDR3 Length",
    y = "Predicted Score"
  ) +
  theme_minimal()





