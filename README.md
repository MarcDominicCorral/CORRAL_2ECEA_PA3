# CORRAL_2ECEA_PA3

# ECE2112

# Programming_Assignment_3
This Programming Assignment contains Python Code solution using Pandas (Python Data Analysis). This is made by Marc Dominic C. Corral from 2-ECE-A as a programming assignment for ECE 2112 - Adavance Computer Programming and Algorithms course.

# Problem 1
This problem loads a corresponding .csv file into a data frame named cars using pandas and displays the first five and last five rows of the resulting cars.

# Steps:
1.) Import Pandas Library into the Python Code.
```python
import pandas as pd #This imports pandas into the Python code.
```
2.) Use the code "pd.read" to load the said CSV file.
```python
cars = pd.read_csv('cars.csv') #pd.read is a python code that reads the file "cars.csv" into the code
cars
```
3.) Use the codes ".head()" and ".tail()" to get the first and last five rows of data frame.
```python
cars.head() #This gets the first 5 rows of the entire data frame from the loaded .csv file "cars.csv" 

cars.tail() #This gets the last 5 rows of the entire data frame from the loaded .csv file "cars.csv"
```
4.) Combine all the commands and construct the Python Code.
```python
import pandas as pd

cars = pd.read_csv('cars.csv')
cars

cars.head()

cars.tail()
```
5.) Run the Pyhthon Code. The output would be:

<img width="847" height="609" alt="image" src="https://github.com/user-attachments/assets/519029f7-d721-42be-93d5-4c0d84fc379e" />

# Problem 2
This problem uses the dataframe cars from the problem 1. Using subsetting, slicing and indexing operations, this problem will be able to solve the following informations:
1. Display the first five rows with odd-numbered columns of the cars in the .csv file.
2. Display the row that contains the "Model" of "Mazda RX4".
3. Determine the cylinder ("cyl") does the car model "Camaro Z28" have.
4. Determine how many cylindrs ("cyl") and what gear type ("gear") do the car models "Mazda RX4 Wag","Ford Pantera L" and "Honda Civic" have.

# Steps:
1.) Import Pandas Library into the Python Code.
```python
import pandas as pd #This imports pandas into the Python code
```
2.) Use the code "pd.read" to load the said CSV file.
```python
cars = pd.read_csv('cars.csv') #pd.read is a python code that reads the file "cars.csv" into the code
cars
```
3.) Get the first 5 rows of the data frame with odd-numbered columns.
```python
cars.loc[1:10:2,'Model':'hp'] #This particular code is used to get the first five rows with odd number columns. "loc[]" is the label- based indexing, "1:10:2" used to select the odd-numbered columns and the "'Model':'hp'" is used to get the first 5 rows
```
4.) We are asked to locate for a certain row with a specific model. We are tasked to locate for the model "Mazda RX4", to locate for the certain category for the specific variable, we use the code ".loc".
```python
cars.loc[cars['Model'] == 'Mazda RX4'] #This code locates "Mazda RX4" from the "Model" column and return/display all rows where "Model" column is equals to "Mazda RX4"
```
5.) Find for the car model "Camaro Z28" and output its cylinder. Use the code ".iloc" to locate for the model and "cyl" to output the cylinder.
```python
cars.loc[(cars['Model'] == 'Camaro Z28'), ['cyl']] #This code locates "Camaro Z28" from the "Model" column and returns only the cylinder count for the specific model
```
6.) We had to print out the cylinder and the gear type of the 3 specific models (Mazda RX4 Wag, Ford Pantera L, Honda Civic). To locate for the certain car models, use ".loc" and ".isin" codes to locate the car models.
```python
M = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic'] #This shows the list of the models
cars.loc[cars['Model'].isin(M),['Model', 'cyl', 'gear']] #This code locates the "Model" that can be found in the list (M) using the code "isin()", selects multiple column using the code "['Model', 'cyl', 'gear']" and returns the specified columns for matching models in the list (M)
```
7.) Combine all the commands and construct the Python Code.
```python
import pandas as pd

cars = pd.read_csv('cars.csv')
cars

cars.loc[1:10:2,'Model':'hp']

cars.loc[cars['Model'] == 'Mazda RX4']

cars.loc[(cars['Model'] == 'Camaro Z28'), ['cyl']]

M = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']
cars.loc[cars['Model'].isin(M),['Model', 'cyl', 'gear']]
```
8.) Run the Pyhthon Code. The outputs would be:

<img width="825" height="454" alt="image" src="https://github.com/user-attachments/assets/6e34cccf-3959-463e-ab57-e6799bb27d71" />
<img width="781" height="429" alt="image" src="https://github.com/user-attachments/assets/67d61436-e670-43a7-88fd-d6ee67daa0b8" />
