# Subspace System Identification for Solar Power Prediction (on Solar Data of DAU)

## Overview
This project applies **subspace system identification** techniques to predict electricity output (Eac) from solar energy systems using temperature data. Unlike conventional machine learning approaches, subspace identification provides a structured methodology for modeling dynamic systems, particularly suited for time-series data in renewable energy applications.

## Why Subspace Identification?
Subspace identification offers several advantages over traditional machine learning models for this solar energy application:

- **Reduced Complexity**: Requires fewer data points while maintaining effective system modeling capabilities
- **Enhanced Interpretability**: Provides clear insights into system behavior, crucial for understanding energy system dynamics
- **Efficient Model Building**: Well-suited for systems where input-output relationships are governed by underlying physical dynamics
- **System-Theoretic Foundation**: Captures the underlying mathematical structure of the dynamic system

## Project Objectives
This research focuses on modeling the relationship between temperature (input) and electricity output (Eac, output) in solar energy systems. The primary goals are to:

  1. Demonstrate the effectiveness of subspace identification for solar energy prediction
  2. Compare performance against traditional machine learning approaches
  3. Provide interpretable models for system optimization and forecasting

## Libraries and Tools Used
- **Python**: Core language for scripting and analysis.
- **NumPy, Pandas**: For data manipulation and preprocessing.
- **Matplotlib, Plotly**: For data visualization.
- **scikit-learn**: For implementing baseline machine learning models.
- **matlab.engine**: Used to call MATLAB functions from Python. MATLAB was used for system identification due to the deprecation or limitations of Python alternatives.
- **Jupyter Notebook**: Interactive development environment for analysis and modeling.
- **MATLAB**: Primary tool for implementing the N4SID algorithm (`N4SID.m`).

## Project Structure and File Guide

### 1. March Data
- **File**: `March`  
- **Description**: Contains daily solar data for March 2025, including temperature and Eac values. This forms the basis for all downstream analysis.

### 2. Single Day Analysis
- **File**: `solar_panel_data_analysis_one_day.ipynb`  
- **Description**: Analyzes solar panel performance for a single day, showing the day-level effect of temperature on Eac.

### 3. Data Cleaning & Storage
- **File**: `Script.ipynb`  
- **Description**: Consolidates and cleans March 2025 data, handling missing values and outliers, and formats it for modeling.

### 4. Monthly Analysis
- **File**: `Analysis.ipynb`  
- **Description**: Explores trends, patterns, and anomalies in the full March dataset using visualizations and statistical summaries.

### 5. Data Extraction for Modeling
- **File**: `data.ipynb`  
- **Description**: Extracts and prepares model-ready features from the cleaned dataset.

### 6. Machine Learning Models
- **File**: `Machine_Learning.ipynb`  
- **Description**: Applies traditional ML models (e.g., regression, decision trees) to predict Eac and compares them with subspace methods.

### 7. N4SID System Identification
- **File**: `N4SID.m`  
- **Description**: This MATLAB script performs **N4SID** (Numerical Subspace State Space System Identification) on the solar data. It uses MATLAB’s system identification tools to create a stable and interpretable model capturing the temperature–output dynamics.

### 8. MISO Identification 
- **File**: `miso.ipynb`  
- **Description**: Applies a basic **MISO** (Multiple Input, Single Output) identification method using Python.

## Methodology
### Data Processing Pipeline
1. **Data Collection**: March 2025 solar panel measurements
2. **Data Cleaning**: Missing value imputation and outlier handling
3. **Feature Engineering**: Temperature-based feature extraction
4. **Model Development**: Both traditional ML and subspace identification approaches

## Additional Materials
For a broader understanding of the project’s objectives, methods, and outcomes:

- `Project_Report.pdf`: Full documentation of the methodology, results, and analysis.  
- `Presentation.pptx`: Slide deck summarizing the project for presentation or review purposes.

## License
This project is available under the MIT License. See the LICENSE file for more details.
