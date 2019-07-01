# Traffic Congestion Prediction - Didi Dataset

The repository is to predict traffic congestion with Didi dataset.


## Requirements

- `pyspark`
- `numpy`
- `pandas`


## Steps

1.  Run `data_processing.ipynb` to pre process the data;
2.  Run `model.ipynb` to train the model.



## Solutiin and Results

It's diffcult to process massive data using traditional approaches, so we chose to use PySpark to process the data.

The idea is inspired by HMM algorithm, where the traffic status of one place is influenced by the surrounding place. Based on the stats of surrounding places in the past, we can predict the central plae status using HMM. In order to fit data into HMM model, we divided the traditioanl map place into different grids and then predict the status of each grid in the time zone.

The final model achived 79.4% accuracy.
