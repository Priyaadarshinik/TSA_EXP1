# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt

file_path = '/content/TSLA.csv'
data = pd.read_csv(file_path)

data['Date'] = pd.to_datetime(data['Date'])

data['MA30'] = data['Close'].rolling(window=30).mean()

plt.figure(figsize=(12, 6))
plt.plot(data['Date'], data['Close'], label='Close Price', color='blue')
plt.plot(data['Date'], data['MA30'], label='30-Day Moving Average', color='orange')
plt.title('Stock Price with 30-Day Moving Average')
plt.xlabel('Date')
plt.ylabel('Price')
plt.legend()
plt.grid(True)
plt.show()
```

# OUTPUT:

<img width="1013" height="541" alt="image" src="https://github.com/user-attachments/assets/0eed0a5d-5a6e-4036-b8c0-fba81ba61c23" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
