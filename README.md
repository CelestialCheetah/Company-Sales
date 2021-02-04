# Module_1
For Class

import pandas as pd
import numpy as np 
import matplotlib.pyplot as plt

sales = pd.read_csv("company_sales_data.csv")

sales = pd.read_csv("company_sales_data.csv")
df = pd.DataFrame(sales)

print(sales)

print(df)

x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
y = [211000, 183300, 224700, 222700, 209600, 201400, 295500, 361400, 234000, 266700, 412, 30200] 

plt.plot(x, y)
plt.title('Monthly Profits')
plt.xlabel('Month Number')
plt.ylabel('Total Profit')
plt.show()

plt.plot(x, y, color = 'red', marker = 'o', linestyle = 'dotted', linewidth = '3')
plt.title('Monthly Profits')
plt.xlabel('Month Number')
plt.ylabel('Sold Units number')
plt.show()

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
plt.plot(monthList, bathingsoapSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3)
plt.plot(monthList, shampooSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3)
plt.plot(monthList, moisturizerSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3)

plt.xlabel('Month Number')
plt.ylabel('Sales units in number')
plt.legend(loc='upper left')
plt.xticks(monthList)
plt.yticks([1000, 2000, 4000, 6000, 8000, 10000, 12000, 15000, 18000])
plt.title('Sales data')

toothpaste_sales = [5200, 5100, 4550, 5870, 4560, 4890, 4780, 5860, 6100, 8300, 7300, 7400]
plt.scatter(x, toothpaste_sales, color = 'green')
plt.title('Monthly Profits for Toothpaste')
plt.xlabel('Month Number')
plt.ylabel('Toothpaste Sales')
plt.grid(True)
plt.show()

monthList = df['month_number'].tolist()
facecreamdata = df['facecream'].tolist()
facewashdata = df['facewash'].tolist()

plt.bar([a-0.25 for a in monthList], facecreamdata, width = 0.25, label = 'Facecream data', align = 'edge' )
plt.bar([a+0.25 for a in monthList], facewashdata, width = 0.25, label = 'Facewash data', align = 'edge' )
plt.xlabel('Month Number')
plt.ylabel('Sales units in number')
plt.legend(loc='upper left')
plt.title(' Sales data')

plt.xticks(monthList)
plt.grid(True, linewidth= 1, linestyle="--")
plt.title('Facewash and facecream sales data')
plt.show()

