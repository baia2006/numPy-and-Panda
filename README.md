# numPy-and-Panda
#1. Data Types for Creating a Series in Pandas
A pandas.Series object can be created using:
Lists
Tuples
Dictionaries
NumPy arrays
Scalar values (single value repeated)
Other Pandas Series or DataFrame columns



#Q2
import pandas as pd

months_series = pd.Series([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12],
                          index=['January', 'February', 'March', 'April', 'May', 'June', 'July', 
                                 'August', 'September', 'October', 'November', 'December'])

print(months_series)



#Q3
students_dict = {'MatMIE': 30, 'Mat DAIS': 25, 'COMIE': 40, 'COMEC': 35}

students_series = pd.Series(students_dict)

print(students_series)



#Q4
import numpy as np

exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}

labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

df = pd.DataFrame(exam_data, index=labels)

print(df)


                
#Q5
filtered_df = df[df['attempts'] > 2]

print("Number of attempts in the examination is greater than 2:")
print(filtered_df)
