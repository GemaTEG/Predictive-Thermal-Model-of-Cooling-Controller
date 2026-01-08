# Thermal Modeling for TEC-Based Cooling Controllers

This repository implements a comprehensive thermal modeling system for Thermoelectric Cooler (TEC) based cooling controllers using machine learning. The model is trained on data extracted and processed from server monitoring systems using Prometheus.

## Project Overview

A machine learning model built with XGBoost to predict and optimize thermal management in server environments using TEC-based cooling systems. The model achieves 81.88% explained variance with an RMSE of 0.817°C.

<h3>Main Implementation <a href="https://github.com/GemaTEG/Predictive-Thermal-Model-of-Cooling-Controller/blob/main/Thermal%20Model.ipynb">
   <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></h3>
## Table of Contents
- [Project Overview](#project-overview)
- [Model Performance](#model-performance)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Repository Structure](#repository-structure)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Model Performance

The XGBoost-based thermal model demonstrates excellent predictive capabilities:

### Training Metrics
- **Training Samples**: 1,270,501
- **Testing Samples**: 141,167

### Final Evaluation Results
| Metric | Value | Unit |
|--------|-------|------|
| **Test MSE** | 0.666960 | - |
| **Test RMSE** | 0.816676 | °C |
| **Test MAE** | 0.547755 | °C |
| **Test R²** | 0.818772 | - |
| **Variance Explained** | 81.88% | - |



Install dependencies via pip:
textpip install -r requirements.txt
requirements.txt contents:
textpandas==2.2.3
numpy==1.26.4
scikit-learn==1.5.2
xgboost==2.1.1
matplotlib==3.9.2
joblib==1.4.2
Setup

Clone the repo:textgit clone https://github.com/yourusername/tec-thermal-model.git
cd tec-thermal-model
Install dependencies (as above).
Place your data CSV in the appropriate path or update the notebook's file path.
Launch Jupyter:textjupyter notebook Thermal Model.ipynb

Usage

Run the Notebook:
Open Thermal Model.ipynb in Jupyter.
Execute cells sequentially to load data, train the model, and generate plots/metrics.

Inference with Saved Model:
Load the model:Pythonimport joblib
import pandas as pd
import numpy as np

model_cpu = joblib.load('model_cpu.pkl')
scaler_cpu = joblib.load('scaler_cpu.pkl')

# Prepare your input DataFrame with the same features
# Example: new_data = pd.DataFrame({...})  # Must match all_features list
new_data_scaled = scaler_cpu.transform(new_data)
predictions = model_cpu.predict(new_data_scaled)
print(predictions)

