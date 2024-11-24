# DePTH2-Analysis

## Overview
DePTH is a predictive model designed to assess the interaction between Human leukocyte antigens(HLA) and T-cell receptor(TCR). By inputting an HLA and a TCR, the model generates a score representing their association. For details on the model structure and usage, please refer to [https://liusi2019.github.io/DePTH-tutorial/](#).

## Features
This repository focuses on the further development and analysis of the DePTH model, including:
1. **Confounding Factors Analysis**  
   - Analysis of factors such as:
     - TCR generation probability
     - CDR3 length  

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
```

### Confounding Variable Analysis

#### TCR generation probability




