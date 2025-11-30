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

# Load the CSV file
file_path = 'AI_Resume_Screening.csv'  
data = pd.read_csv(file_path)
data.set_index('Salary Expectation ($)', inplace=True)

plt.figure(figsize=(15, 6))
plt.title('Salary growth over time')
plt.xlabel('Experience (Years)')
plt.ylabel('Salary Expectation ($)')
plt.plot(data.index, data['Salary Expectation ($)'], label='Salary Expectation', color='violet')
```

# OUTPUT:

<img width="1211" height="520" alt="image" src="https://github.com/user-attachments/assets/0545c616-8d0b-43f7-97a1-98da5d288079" />


# RESULT:
Thus we have created the python code for plotting the time series of given data.
