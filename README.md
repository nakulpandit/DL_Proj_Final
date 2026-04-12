# Deep Learning Regression for Stellar Age Estimation

This project implements a Deep Learning regression model to estimate the stellar age of Red Giant stars using the APO-K2 stellar age catalog from VizieR.

## Dataset
The dataset is fetched from the VizieR catalog (`J/AJ/167/208/table3`). It includes various stellar parameters such as effective temperature (`teff`), surface gravity (`logg`), metallicity (`[Fe/H]`), stellar mass, radius, and asteroseismic parameters (`numax`, `deltanu`).

The target variable for prediction is `age_mode` (Stellar Age in Gyr).

## Methodology
1. **Data Preprocessing:**
   - Cleaning and filtering unphysical values.
   - Dropping missing data.
   - Standardizing the features using `StandardScaler`.
2. **Model Architecture:**
   - A multi-layer perceptron (MLP) built with TensorFlow/Keras.
   - Includes Dense and Dropout layers.
   - Optimized using Adam with Mean Squared Error (MSE) loss.
3. **Evaluation:**
   - The model is evaluated on a held-out test set generating metrics: MSE, RMSE, MAE, and $R^2$ score.
   - Extensive visualizations are provided for diagnostics, such as correlation heatmaps, pair plots, Q-Q plots, and feature importance.

## Visualisations
The `plots` directory contains generated visualisations capturing model performance and feature dependencies.

## Usage
1. Setup a virtual environment: `python3 -m venv venv`
2. Activate the environment: `source venv/bin/activate`
3. Install dependencies: `pip install numpy pandas matplotlib seaborn astroquery scikit-learn tensorflow jupyter`
4. Run the Jupyter Notebook: `jupyter notebook DL_project.ipynb`
