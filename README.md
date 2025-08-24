# Raisin Dataset PCA Analysis

A comprehensive Principal Component Analysis (PCA) implementation demonstrating dimensionality reduction techniques on a raisin classification dataset.

## 🎯 Project Overview

This project applies Principal Component Analysis to a raisin dataset to:
- Reduce data dimensionality while preserving classification performance
- Visualize high-dimensional data in lower dimensions
- Compare model performance between original features and PCA components
- Demonstrate various PCA visualization techniques

## 📊 Dataset

The analysis uses a raisin dataset containing morphological measurements of two raisin varieties:
- **Kecimen** raisins
- **Besni** raisins

### Features
- **Area**: Surface area of the raisin
- **MajorAxisLength**: Length of the major axis
- **MinorAxisLength**: Length of the minor axis
- **Eccentricity**: Measure of how elongated the raisin is
- **ConvexArea**: Area of the convex hull
- **Extent**: Ratio of the area to the bounding rectangle
- **Perimeter**: Perimeter of the raisin
- **Class**: Target variable (Kecimen/Besni)

## 🛠️ Technologies Used

### R Libraries
- `readxl` - Excel file reading
- `tidyverse` - Data manipulation and visualization
- `ggfortify` - Statistical model plotting
- `factoextra` - Multivariate analysis visualization
- `ggExtra` - Marginal plots
- `corrplot` - Correlation matrix visualization
- `gridExtra` - Multi-plot arrangements
- `caret` - Machine learning tools
- `VIM` - Missing value visualization

## 📁 Project Structure

```
raisin-pca-analysis/
├── README.md
├── Raisin_Dataset.csv
├── raisin-pca-analysis.Rmd
├── raisin-pca-analysis.html
└── plots/
    ├── correlation_matrix.png
    ├── scree_plot.png
    ├── pca_biplot.png
    └── combined_visualizations.png
```

## 🔍 Analysis Workflow

### 1. **Data Exploration**
- Load and examine dataset structure
- Generate summary statistics
- Create density plots for feature distribution
- Check for missing values

### 2. **Correlation Analysis**
- Compute correlation matrix
- Visualize feature relationships
- Identify highly correlated variables

### 3. **Data Preprocessing**
- Convert target variable to factor
- Separate features from target
- Standardize features (z-score normalization)

### 4. **Principal Component Analysis**
- Perform PCA on scaled features
- Analyze explained variance ratios
- Identify optimal number of components

### 5. **PCA Visualizations**
- **Scree Plot**: Variance explained by each component
- **Biplot**: Sample distribution with confidence ellipses
- **Variable Contribution**: Feature importance in PCs
- **Correlation Circle**: Variable relationships in PC space
- **Quality Representation**: Feature representation quality

### 6. **Predictive Modeling**
- Train logistic regression on original features
- Train logistic regression on PCA components
- Compare model performance

## 📈 Key Results

### PCA Findings
- **First 3 components** explain the majority of variance in the data
- Dimensionality reduced from 7 features to 3 principal components
- Clear separation between raisin classes in PCA space

### Model Performance Comparison
| Model Type | Accuracy | Features Used |
|------------|----------|---------------|
| Original Features | 0.8577778  | 7 features   |
| PCA Components    | 0.8655556  | 3 components |

> **Note**: The PCA model maintains comparable accuracy while using fewer features, demonstrating effective dimensionality reduction.

## 🚀 Getting Started

### Prerequisites
```r
# Install required packages
install.packages(c("readxl", "tidyverse", "ggfortify", "factoextra", 
                   "ggExtra", "corrplot", "gridExtra", "caret", "VIM"))
```

### Running the Analysis
1. Clone this repository
2. Ensure `Raisin_Dataset.csv` is in the project directory
3. Open `raisin-pca-analysis.Rmd` in RStudio
4. Knit the document or run chunks interactively

### Expected Output
- HTML report with all visualizations
- Correlation matrices and PCA plots
- Model performance metrics
- Comparative analysis results

## 📚 Educational Value

This project demonstrates:
- **PCA Theory**: Practical application of dimensionality reduction
- **Data Visualization**: Multiple techniques for exploring multivariate data
- **Model Comparison**: Evaluating trade-offs between complexity and performance
- **Statistical Analysis**: Correlation analysis and variance explanation

## 🎬 Tutorial Reference

Based on the YouTube tutorial: [PCA Analysis Tutorial](https://www.youtube.com/watch?v=gSnXIzhAQms&ab_channel=RajendraChoure)




