# CORRAL_2ECEA_PA3

# ECE2112

# Programming_Assignment_3
This Programming Assignment contains Python Code solution using Pandas (Python Data Analysis). This is made by Marc Dominic C. Corral from 2-ECE-A as a programming assignment for ECE 2112 - Adavance Computer Programming and Algorithms course.

# Problem 1
This problem loads a corresponding .csv file into a data frame named cars using pandas and displays the first five and last five rows of the resulting cars.

# Python Code:
```python
import pandas as pd

cars = pd.read_csv('cars.csv')
cars

cars.head()

cars.tail()
```

# Outputs:
<img width="847" height="609" alt="image" src="https://github.com/user-attachments/assets/519029f7-d721-42be-93d5-4c0d84fc379e" />

# Code Explanation:
```python

import pandas as pd #This imports pandas into the Python code

cars = pd.read_csv('cars.csv') #pd.read is a python code that reads the file "cars.csv" into the code
cars

cars.head() #This gets the first 5 rows of the entire data frame from the loaded .csv file "cars.csv" 

cars.tail() #This gets the last 5 rows of the entire data frame from the loaded .csv file "cars.csv"
```

# Problem 2
This problem uses the dataframe cars from the problem 1. Using subsetting, slicing and indexing operations, this problem will be able to solve the following informations:
1. Display the first five rows with odd-numbered columns of the cars in the .csv file.
2. Display the row that contains the "Model" of "Mazda RX4".
3. Determine the cylinder ("cyl") does the car model "Camaro Z28" have.
4. Determine how many cylindrs ("cyl") and what gear type ("gear") do the car models "Mazda RX4 Wag","Ford Pantera L" and "Honda Civic" have.

# Python Code:
```python
import pandas as pd

cars = pd.read_csv('cars.csv')
cars

cars.loc[1:10:2,'Model':'hp']

cars.loc[cars['Model'] == 'Mazda RX4']

cars.loc[(cars['Model'] == 'Camaro Z28'), ['cyl']]

M = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']
cars.loc[cars['Model'].isim(M),['Model', 'cyl', 'gear']]
```

# Outputs:
<img width="766" height="446" alt="image" src="https://github.com/user-attachments/assets/07247019-0da6-4241-a12e-6dbecfb63d73" />
<img width="781" height="429" alt="image" src="https://github.com/user-attachments/assets/67d61436-e670-43a7-88fd-d6ee67daa0b8" />

# Code Explanation:
```python
import pandas as pd #This imports pandas into the Python code

cars = pd.read_csv('cars.csv') #pd.read is a python code that reads the file "cars.csv" into the code
cars

cars.loc[1:10:2,'Model':'hp'] #This particular code is used to get the first five rows with odd number columns. "loc[]" is the label- based indexing, "1:10:2" used to select the odd-numbered columns and the "'Model':'hp'" is used to get the first 5 rows

cars.loc[cars['Model'] == 'Mazda RX4'] #This code locates "Mazda RX4" from the "Model" column and return/display all rows where "Model" column is equals to "Mazda RX4" 

cars.loc[(cars['Model'] == 'Camaro Z28'), ['cyl']] #This code locates "Camaro Z28" from the "Model" column and returns only the cylinder count for the specific model

M = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic'] #This shows the list of the models
cars.loc[cars['Model'].isim(M),['Model', 'cyl', 'gear']] #This code locates the "Model" that can be found in the list (M) using the code "isin()", selects multiple column using the code "['Model', 'cyl', 'gear']" and returns the specified columns for matching models in the list (M)
```
