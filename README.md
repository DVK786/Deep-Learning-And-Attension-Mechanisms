Advanced Time Series Forecasting using LSTM and Self-Attention

This repository contains a PyTorch-based implementation of an advanced time series forecasting model.
The project compares a baseline LSTM model with an LSTM model enhanced using a self-attention mechanism.
The task is to predict the next time step of a multivariate time series.

Project Overview

Time series forecasting requires learning temporal dependencies from sequential data.
LSTM networks are effective for this purpose, and self-attention further improves performance by allowing the model to focus on the most relevant time steps.
This project demonstrates both approaches and compares their results.

The entire implementation is designed to run in a single execution cell.

Key Features

Synthetic multivariate time series generation
Sliding window sequence creation
Baseline LSTM model
LSTM with self-attention mechanism
Model training using PyTorch
Model evaluation using MAE and RMSE
Attention weight analysis

Dataset Description

The dataset is synthetically generated.
Total time steps: 1500
Number of features: 5
Sequence length: 30
Target variable: Next time step of the first feature

The dataset includes periodic signals, nonlinear components, and trend-based features.

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
The LSTM with self-attention generally achieves better performance by emphasizing important time steps in the input sequence.

Attention Analysis

Attention weights are generated for a sample test sequence.
These weights indicate how much importance the model assigns to each time step during prediction.

Requirements

Python 3.x
numpy
torch
matplotlib
scikit-learn

Dependencies can be installed using pip.

How to Run

Clone the repository
Open the Python script in a Jupyter Notebook, Google Colab, or local Python environment
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
