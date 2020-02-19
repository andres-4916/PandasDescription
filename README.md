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
  c = c.sum()
  c = c.sort_values(['quantity'], ascending=False)
  c.head(1)

***
+ c = chipo.groupby('choice_description').sum()
  c = c.sort_values(['quantity'], ascending=False)
  c.head(1)
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
https://github.com/guipsamora/pandas_exercises
