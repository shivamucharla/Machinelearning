# Stock Price Prediction and Forecasting

This project aims to predict and forecast the stock prices of Apple Inc. (AAPL) using a Long Short-Term Memory (LSTM) neural network. The workflow includes data collection, preprocessing, model creation, training, and prediction.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Collection](#data-collection)
3. [Data Preprocessing](#data-preprocessing)
4. [Model Creation](#model-creation)
5. [Prediction and Plotting](#prediction-and-plotting)
6. [Forecasting for Next 30 Days](#forecasting-for-next-30-days)
7. [Installation](#installation)
8. [Usage](#usage)
9. [License](#license)

## Project Overview
This project utilizes historical stock price data to train an LSTM model, which is then used to predict future stock prices based on past trends. The model is evaluated using the Root Mean Square Error (RMSE) metric.

## Data Collection
Data is collected from Tiingo using the following code:

```python
!pip install pandas-datareader

import pandas_datareader as pdr

# Replace with your actual API key
df = pdr.get_data_tiingo('AAPL', api_key='YOUR_API_KEY')
df.to_csv('AAPL.csv')



## Data Preprocessing
- **The collected data is preprocessed by:

- **Loading the data into a DataFrame.
- **Extracting the 'close' prices.
- **Normalizing the data using MinMaxScaler.
- **Splitting the data into training and testing sets (65% training, 35% testing).

import pandas as pd
from sklearn.preprocessing import MinMaxScaler

df = pd.read_csv('AAPL.csv')
df1 = df.reset_index()['close']
scaler = MinMaxScaler(feature_range=(0, 1))
df1 = scaler.fit_transform(np.array(df1).reshape(-1, 1))


## Prediction and Plotting
- **The model is trained on the training dataset and validated using the testing dataset. Predictions for both training and testing datasets are made and visualized.

## Prediction and Plotting
- **The model is trained on the training dataset and validated using the testing dataset. Predictions for both training and testing datasets are made and visualized.

## Forecasting for Next 30 Days
- **The model is used to forecast stock prices for the next 30 days based on the last 100 days of data from the test dataset. The results are visualized alongside the historical prices.

from numpy import array
lst_output = []
n_steps = 100
i = 0
while (i<30):
    if (len(temp_input)>100):
        x_input = np.array(temp_input[1:])
        print("{} day_input {}".format(i,x_input))
        x_input = x_input.reshape(1,-1)
        x_input = x_input.reshape((1,n_steps,1))
        
        yhat = model.predict(x_input, verbose=0)

        print("{} day_input {}".format(i,yhat))
        temp_input.extend(yhat[0].tolist())
        temp_input = temp_input[1:]
        lst_output.extend(yhat[0].tolist()) 
        i = i+1
    else:
        x_input = x_input.reshape((1,n_steps,1))
        yhat = model.predict(x_input, verbose=0)

        print(yhat[0])
        temp_input.extend(yhat[0].tolist())
        print(len(temp_input))
        lst_output.extend(yhat[0].tolist())
        i = i+1
print(lst_output)

7. Installation
- **To run this project, you need to install the following Python packages:

- **Tpip install pandas-datareader
- **Tpip install numpy
- **Tpip install matplotlib
- **Tpip install scikit-learn
- **Tpip install tensorflow

8. Usage
### Clone the repository:

git clone https://github.com/yourusername/stock-price-prediction.git
cd stock-price-prediction

9. License
- **This project is licensed under the MIT License. See the LICENSE file for more details.


### Instructions for Usage
- Make sure to replace `'YOUR_API_KEY'` in the Data Collection section with your actual Tiingo API key.
- Adjust the repository URL in the Installation section according to your GitHub repository's name.

- **You can use this template to create a comprehensive README file for your project on GitHub!

