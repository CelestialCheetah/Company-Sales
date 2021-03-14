# WORK IN PROGRESS
This is a coding project that was assigned to compare sales between multiple products, and to also visualized the caparisons using different styles of charts 
and features within the charts. 

```python:
import pandas as pd
import numpy as np 
import matplotlib.pyplot as plt
```
This is the crux of the project. Using ```python: Pandas Numpy Matplotlib.pyplot``` 
Afterwards I loaded in the data using ```python: Pandas``` shown below. The actaul CSV should be in the repository as well.

```python: sales = pd.read_csv("company_sales_data.csv")```

Here is a basic line chart showing the total profits of all items sold per month 

![Company sales montly_profits](https://user-images.githubusercontent.com/53583290/110728515-39166a00-81eb-11eb-9632-42a70b32d568.PNG)

This is the same chart with a slightly different line on the graph that uses points to specify each month to profits.

![Company sales montly_profits_2](https://user-images.githubusercontent.com/53583290/110728530-403d7800-81eb-11eb-87ba-ef2f0019e5aa.PNG)

This is the largest part of the project showing all the sales of the products in the data. Originally I would have prefered to use the data in a way to not use 
```python:.tolist(0)``` but the assigned called to use it. Along with the graph there is the codeblock I made to make the graph.

![Company sales all sales](https://user-images.githubusercontent.com/53583290/110728546-47648600-81eb-11eb-8206-5517df6aad31.PNG)

```python:
monthList = df['month_number'].tolist()
facecreamdata = df['facecream'].tolist()
facewashdata = df['facewash'].tolist()
toothPasteSalesData = df ['toothpaste'].tolist()
bathingsoapSalesData   = df ['bathingsoap'].tolist()
shampooSalesData   = df ['shampoo'].tolist()
moisturizerSalesData = df ['moisturizer'].tolist()

plt.plot(monthList, facecreamdata,   label = 'Face cream Sales Data', marker='o', linewidth=3)
plt.plot(monthList, facewashdata,   label = 'Face Wash Sales Data',  marker='o', linewidth=3)
plt.plot(monthList, toothPasteSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3)
plt.plot(monthList, bathingsoapSalesData, label = 'Bathing Soap Sales Data', marker='o', linewidth=3)
plt.plot(monthList, shampooSalesData, label = 'Shampoo Sales Data', marker='o', linewidth=3)
plt.plot(monthList, moisturizerSalesData, label = 'Moisturizer Sales Data', marker='o', linewidth=3)

plt.xlabel('Month Number')
plt.ylabel('Sales units in number')
plt.legend(loc='upper left')
plt.xticks(monthList)
plt.yticks([1000, 2000, 4000, 6000, 8000, 10000, 12000, 15000, 18000])
plt.title('Sales data') 
```
![Comapny sales bar graph](https://user-images.githubusercontent.com/53583290/110728562-4df2fd80-81eb-11eb-81b5-86ff15a9bbd8.PNG)

