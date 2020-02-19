# PandasDescription:pencil2::computer:
## Chipotle:
+ import pandas as pd
***
+ import numpy as np //necessity as pandas is built on np///
***
+ chipo = pd.read_csv(url, sep = '\t') //read csv file//
***
+ chipo.head(10) //see top 5 rows of data//
***
+ chipo.shape[0] 
***
+ chipo.info() //not null part is very useful to see how many nulls are there in data//
***
+ chipo.shape 
***
+ chipo.columns //column names//
***
+ chipo.index //
***
+ c = chipo.groupby('item_name')
+ c = c.sum()
+ c = c.sort_values(['quantity'], ascending=False)
+ c.head(1)

***
 + c = chipo.groupby('choice_description').sum()
 + c = c.sort_values(['quantity'], ascending=False)
 + c.head(1)
***
+ total_items_orders = chipo.quantity.sum()
  total_items_orders
***
+ chipo.item_price.dtype
***

+ dollarizer = lambda x: float(x[1:-1])
  chipo.item_price = chipo.item_price.apply(dollarizer)
***

+ chipo.item_price.dtype
***

+ revenue = (chipo['quantity']* chipo['item_price']).sum()
  print('Revenue was: $' + str(np.round(revenue,2)))
***
+ orders = chipo.order_id.value_counts().count()
  orders
***

+ chipo['revenue'] = chipo['quantity'] * chipo['item_price']
  order_grouped = chipo.groupby(by=['order_id']).sum()
  order_grouped.mean()['revenue']
***
+ chipo.groupby(by=['order_id']).sum().mean()['revenue']
***

+ chipo.item_name.value_counts().count() 
***
## Occupation:

+ import pandas as pd 
***
+ users = pd.read_csv('https://raw.githubusercontent.com/justmarkham/DAT8/master/data/u.user', 
                      sep='|', index_col='user_id')
 ***
 + users.head(25)
 ***
 
 + users.tail(10
***
+ users.shape[0]
***
+ users.shape[1]
***
+ users.columns
***
+ users.index
***
+ users.dtypes
***
+ users.occupation
***
+ users.occupation.nunique()
***
+ users.occupation.value_counts().head(1).index[0]
***
+ users.describe()
***
+ 
users.describe(include = "all")
***
+ users.occupation.describe()
***
+ round(users.age.mean())
***
+ users.age.value_counts().tail()
***

## World Food Facts
REFERENCE: https://github.com/guipsamora/pandas_exercises
