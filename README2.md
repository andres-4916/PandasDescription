# PandasDescription:pencil2::computer:
+ import pandas as pd: what it does is important the necessary libraries
***
+ users = pd.read_csv ('https://raw.githubusercontent.com/justmarkham/DAT8/master/data/u.user',
                      sep = '|', index_col = 'user_id'): What it does is search the link database and use it as user_id as the primary one.
   ***                   
+ users.head (26): what it does is show the number of data that is written inside the parenthesis
***
+ users.tail (11) unlike the head this sample but since the last one, the head starts from the beginning it starts from the end the data numbers
***
+ users.shape [0] what it does is show vertically and horizontally, with 0 shows vertically how much data is in that row and if we use 1 it shows horizontally the columns above that divide the data.
***
+ users.columns: this command shows the columns, the difference of the shape is that it shows number and this shows with names and type.
***
+ users.index: this shows the total data in the form of numbers.
***
+ users.dtypes: shows the type of data that is if it is int64 or object
***
+ users ['occupation'] shows, along with the id, the order in which the row we selected is shown and winged, shows corresponding id along with what we want to see.
***
+ users.occupation.nunique (): shows the different data you have, if there is repeated data find all and show as only 1.
***
+ users.occupation.value_counts (). head (1) .index [0]: of all the data it shows which is the most used or the most repeated of all and is searched by writing the row of which we want to know what is repeated.
***
+ users.describe (include = "all"): this describes everything from the database, quantity, type, percentage, etc.
***
+ users.occupation.describe () summarizes only the specific column showing the most used data, the type of data, how much data an the frequency used round (users.age.mean ()) shows the average age of the database that users are.
***
+ users.age.value_counts (). tail (): shows the age that is least used, the least used of all, as can be shown in the other tables.

# description folder two:pencil2:

+ import pandas as pd: we import the necessary libraries.
***
+ drinks = pd.read_csv ('https://raw.githubusercontent.com/justmarkham/DAT8/master/data/drinks.csv')
drinks.head (): let's get the address where the database is a name and show the table.
***
+ drinks.groupby ('country'). beer_servings.mean (): What it does is search as a link, showing country with beer_servings data.
***
+ drinks.groupby ('continent'). wine_servings.describe (): this function shows in addition to the average it also shows part of the median along with its other filters such as those that are most requested, the total percentage, average percentage, etc. Difference of the mean is that this shows everything besides the mean (mean) making a type link between tables.
***
+ drinks.groupby ('continent'). mean (): print the average of what you select but of each column in general.
***
+ drinks.groupby ('continent'). median (): shows the median of the selected column.
***

+ drinks.groupby ('continent'). spirit_servings.agg (['mean', 'min', 'max']): shows the average, minimum and maximum values.

