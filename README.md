This is a coding project that was assigned to compare sales between multiple products, and to also visualized the caparisons using different styles of charts.
```python:
import pandas as pd
import numpy as np 
import matplotlib.pyplot as plt```

```python:
sales = pd.read_csv("company_sales_data.csv")```

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
plt.title('Sales data')```
