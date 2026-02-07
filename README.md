Advanced Time Series Forecasting using LSTM and Self-Attention

This repository contains a PyTorch-based implementation of an advanced time series forecasting model.
The project compares a baseline LSTM model with an LSTM model enhanced using a self-attention mechanism.
The task is to predict the next time step of a multivariate time series.

Project Overview

Time series forecasting involves learning temporal dependencies from sequential data.
LSTM networks are well suited for this purpose, and self-attention mechanisms can further improve interpretability by dynamically weighting important time steps.
This project demonstrates both approaches and compares their performance under identical training conditions.

The implementation is designed to run as a single executable script.

Key Features

Synthetic multivariate time series generation
Sliding window sequence preparation
Baseline LSTM model
LSTM with self-attention mechanism
Model training using PyTorch
Model evaluation using MAE and RMSE
Attention weight visualization

Dataset Description

The dataset is synthetically generated.
Total time steps: 1500
Number of features: 5
Sequence length: 30
Target variable: Next time step of the first feature

The dataset includes periodic signals, nonlinear transformations, and trend-based components.

Model Architecture

Baseline LSTM Model
Single-layer LSTM network
Final hidden state used for prediction
Fully connected output layer

LSTM with Self-Attention Model
Single-layer LSTM network
Self-attention applied across all time steps
Context vector computed using attention weights
Fully connected output layer

Training Configuration

Framework: PyTorch
Optimizer: Adam
Loss function: Mean Squared Error
Batch size: 32
Number of epochs: 10
Train-test split: 80 percent training, 20 percent testing

Evaluation Metrics

Mean Absolute Error
Root Mean Squared Error

Results

After training, the program prints MAE and RMSE values for both models.
In this experiment, the baseline LSTM achieved slightly better performance than the attention-based LSTM.
This outcome highlights that attention mechanisms do not always guarantee performance improvements, particularly on simpler or highly regular datasets.

Areas for Improvement

Model Performance

The attention-based LSTM performed slightly worse than the baseline LSTM in this experiment.
This result suggests that the synthetic dataset may not be complex enough to fully benefit from an attention mechanism.
Attention models typically demonstrate clearer advantages on longer sequences, noisier data, or tasks with irregular temporal dependencies.

Hyperparameter Tuning

Hyperparameter tuning was minimal, with fixed values for learning rate and number of epochs.
This choice was made to ensure simplicity and a fair comparison between models.
Future work can include systematic tuning using grid search or other optimization strategies.

Depth of Analysis

The analysis focuses primarily on implementation and architectural comparison.
A deeper investigation into hidden representations, learning dynamics, and architectural variations was outside the current scope but remains a potential extension.

Deliverables and Documentation

The project deliverables are intentionally lightweight, consisting of a clean README and executable script.
A detailed technical report was not included, as the goal of the repository is to demonstrate model implementation rather than serve as a full research study.

Attention Visualization

Attention visualization is limited to a single sample and is intended to demonstrate interpretability rather than provide a statistical comparison.
Future improvements may include averaging attention weights across multiple samples or comparing attention patterns across different prediction outcomes.

Requirements

Python 3.x
numpy
torch
matplotlib
scikit-learn

How to Run

Clone the repository
Open the Python script in a Python environment
Restart the runtime or kernel
Run the entire program in a single execution

Project Structure

time_series_lstm_attention.py
README.md

Use Cases

Educational demonstrations of LSTM and attention mechanisms
Time series forecasting experiments
Academic projects and coursework
Research prototyping

License

This project is intended for educational and experimental purposes.
