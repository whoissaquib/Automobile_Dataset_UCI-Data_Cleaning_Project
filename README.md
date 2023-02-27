# Automobile_Dataset_UCI-Repo
This dataset consist of data From 1985 Ward's Automotive Yearbook.

Source:

Creator/Donor:

Jeffrey C. Schlimmer (Jeffrey.Schlimmer '@' a.gp.cs.cmu.edu)

Sources:

1) 1985 Model Import Car and Truck Specifications, 1985 Ward's Automotive Yearbook.
2) Personal Auto Manuals, Insurance Services Office, 160 Water Street, New York, NY 10038
3) Insurance Collision Report, Insurance Institute for Highway Safety, Watergate 600, Washington, DC 20037

Data Cleaning Operation was done and shown in the above python notebook

1 - So, how do we identify all those missing values and deal with them?
How to work with missing data?

Steps for working with missing data:

Identify missing data
deal with missing data
correct data format

2 - Identify & Handle Missing Values
Convert "?" to NaN

In the car dataset, missing data comes with the question mark "?". We replace "?" with NaN (Not a Number), which is Python's default missing value marker, for reasons of computational speed and convenience.

3 - Evaluating for Missing Data

The missing values are converted to Python's default. We use Python's built-in functions to identify these missing values. There are two methods to detect missing data:

.isnull()
.notnull()
The output is a boolean value indicating whether the value that is passed into the argument is in fact missing data.
Count missing values in each column

Using a for loop in Python, we can quickly figure out the number of missing values in each column. In the body of the for loop the method ".value_counts()" counts the number of "True" values.

4 - How to deal with missing data?

drop data
a. drop the whole row
b. drop the whole column
replace data
a. replace it by mean
b. replace it by frequency
c. replace it based on other functions
Whole columns should be dropped only if most entries in the column are empty. In our dataset, none of the columns are empty enough to drop entirely. We have some freedom in choosing which method to replace data; however, some methods may seem more reasonable than others. We will apply each method to many different columns:

Replace by mean:

"normalized-losses": 41 missing data, replace them with mean
"stroke": 4 missing data, replace them with mean
"bore": 4 missing data, replace them with mean
"horsepower": 2 missing data, replace them with mean
"peak-rpm": 2 missing data, replace them with mean

Replace by frequency:

"num-of-doors": 2 missing data, replace them with "four".
Reason: 84% sedans is four doors. Since four doors is most frequent, it is most likely to occur
Drop the whole row:

"price": 4 missing data, simply delete the whole row
Reason: price is what we want to predict. Any data entry without price data cannot be used for prediction; therefore any row now without price data is not useful to us



5 - Replace "NaN" by mean value in columns

6 - Correct data format
The last step in data cleaning is checking and making sure that all data is in the correct format (int, float, text or other).

In Pandas, we use

.dtype() to check the data type

.astype() to change the data type


HENCE VARIOUS DATA CLEANING AND MANIPULATION OPERATION WERE PERFORMED USING PANDAS LIBRARY



