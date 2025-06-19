# Electric Field Signal Modeling with Polynomial Regression, Ridge & Lasso

This project demonstrates the modeling of electric field signals using polynomial regression techniques including Linear, Ridge, and Lasso regression. It focuses on analyzing time-domain electric signals and their power spectral densities using FFT, with a particular emphasis on **trimmed signal windows**.

## Project Structure

- `manual_load_data(...)`: Loads electric field data from `.txt` files.
- `train_model(...)`: Fits polynomial regression models on full signals.
- `train_model_no_scaling(...)`: Trains models without normalization on full signals.
- `trim_signal(...)`: Trims signal to focus on a pulse window.
- `calculate_power_spectrum(...)`: Computes linear-scale FFT.
- `calculate_power_spectrum_dB(...)`: Computes power spectral density in decibels.
- `train_model_on_trimmed(...)`: Trains Ridge or Lasso on trimmed signals.
- `train_and_plot_no_scaling_cut(...)`: Trains and visualizes models on pulse-only data.
- `plot_*`: Utility functions for plotting time-domain and frequency-domain comparisons.

##  Key Features

- Polynomial regression with degrees 2, 5, 10.
- Ridge & Lasso with customizable regularization strengths.
- Time-domain trimming: focuses on `[-363ps, -357ps]` window.
- Power Spectral Density (PSD) visualization using FFT.
- Coefficient interpretation for model introspection.
- Clear Armenian-language inline documentation and comments.

## Results Summary

- MSE comparison across model types and degrees.
- Visualization of predicted vs actual signals (trimmed).
- FFT-based analysis for frequency content comparison.
- Time-alignment check for input/output signal datasets.

## Data Requirements

You should include the following `.txt` files in the project root:
- `1.2.txt` — Input signal
- `3.2.0.txt` — Secondary input (not modeled)
- `3.2.2m20.txt` — Output 1
- `3.2.5m40.txt` — Output 2

Each file must contain two columns: `Time (ps)` and `Electric Field (a.u.)`.


