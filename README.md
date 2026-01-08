# Thermal Modeling of Cooling Controllers

This repository implements a comprehensive thermal modeling system for Thermoelectric Cooler (TEC) based cooling controllers using machine learning. The model is trained on data extracted and processed from server monitoring systems using Prometheus.

## Project Overview

A machine learning model built with XGBoost to predict and optimize thermal management in server environments using TEC-based cooling systems. The model achieves 81.88% explained variance with an RMSE of 0.817°C.

<h3>Main Implementation <a href="https://github.com/GemaTEG/Predictive-Thermal-Model-of-Cooling-Controller/blob/main/Thermal%20Model.ipynb">
   <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></h3>

## Table of Contents
- [Project Overview](#project-overview)
- [Model Performance](#model-performance)
- [Training Metrics](#Training-Metrics)
- [Final Evaluation Results](#Final-Evaluation-Results)
- [Performance Visualization](#Performance-Visualization)
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



### Performance Visualization
<div align="center"> <img src="https://github.com/GemaTEG/Predictive-Thermal-Model-of-Cooling-Controller/blob/main/residual%20destribution.png" width="700" alt="Model Performance Visualization"/> </div>


