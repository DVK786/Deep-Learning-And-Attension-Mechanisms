Advanced Time Series Forecasting using LSTM and Self Attention

Overview
This project implements a time series forecasting system using deep learning. Two neural network models are developed and compared to study the impact of attention mechanisms on forecasting performance.

The models implemented are:

A baseline LSTM model

An LSTM model with a self attention mechanism

The objective is to predict the next time step value in a multivariate time series and analyze whether attention improves performance over a standard LSTM.

The entire implementation is provided as a single executable Python script for simplicity and reproducibility.

Dataset Description
A synthetic multivariate time series dataset is generated to simulate realistic temporal behavior.

Total time steps: 1500
Number of input features: 5
Sequence length: 30

The features include sinusoidal, cosine, logarithmic, and nonlinear transformations with added noise.
The target variable is the next time step value of the first feature.

Model Architectures

Baseline LSTM Model
The baseline model consists of a single LSTM layer followed by a fully connected output layer. The final hidden state of the LSTM is used to generate the prediction. This model serves as a reference for comparison.

LSTM with Self Attention Model
This model uses an LSTM encoder to process the input sequence. A self attention mechanism is applied over all LSTM outputs to compute a weighted context vector. The context vector is then passed through a fully connected layer to generate the final prediction. The attention mechanism allows the model to focus on important time steps in the sequence.

Training Configuration

Optimizer: Adam
Learning rate: 0.001
Loss function: Mean Squared Error
Epochs: 10
Batch size: 32
Train test split: 80 percent training and 20 percent testing

Hyperparameters were kept fixed to focus on architectural comparison rather than optimization.

Evaluation Metrics

The models are evaluated using the following metrics on the test dataset:

Mean Absolute Error
Root Mean Squared Error

These metrics provide complementary measures of forecasting accuracy.

Results Summary

In the current experiment, the baseline LSTM slightly outperformed the LSTM with attention. This indicates that the attention mechanism did not provide a measurable performance gain for this specific dataset and configuration.

Analysis of Attention Performance

The underperformance of the attention based model can be explained by several factors:

The synthetic dataset contains smooth and regular temporal patterns that a standard LSTM can already model effectively.
The sequence length is relatively short, limiting the benefit of modeling long range dependencies.
The attention mechanism introduces additional parameters, which may increase model complexity without sufficient data complexity.
Hyperparameter tuning was minimal, which may prevent the attention model from reaching its full potential.

These results do not imply that attention mechanisms are ineffective in general, but rather that their benefits are dependent on the nature of the data and the task.

Attention Visualization

Attention weights are visualized for a single test sample to demonstrate interpretability. The visualization shows how the model distributes importance across different time steps when making a prediction.

A deeper statistical analysis across multiple samples is not included and is considered future work.

Limitations

Hyperparameter tuning was minimal.
Only synthetic data was used for evaluation.
Attention analysis was limited to a single sample visualization.
The project structure is minimal and focused on demonstration rather than large scale benchmarking.

Future Work

Perform systematic hyperparameter tuning including learning rate and hidden size.
Evaluate the models on real world time series datasets.
Analyze attention weights across multiple samples and time windows.
Include additional evaluation metrics such as Mean Absolute Percentage Error.
Expand the project into a modular multi file structure with a detailed technical report.

How to Run

Install the required libraries using pip.
Run the Python script containing the implementation.

Conclusion

This project provides a clear and reproducible comparison between a baseline LSTM and an attention enhanced LSTM for time series forecasting. Although attention did not outperform the baseline in this setup, the implementation and analysis provide a strong foundation for further experimentation and improvement.
