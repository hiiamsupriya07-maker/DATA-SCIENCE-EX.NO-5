# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 ```
# STEP 1: Include the necessary Library
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
# STEP 2: Create sample dataset
data = {
 "Month": ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
 "Sales": [200, 250, 300, 280, 350, 400],
 "Expenses": [150, 180, 200, 190, 220, 260],
 "Customers": [30, 45, 50, 40, 60, 75]
}
df = pd.DataFrame(data)
# Convert Month to numeric index for some plots
x = np.arange(len(df["Month"]))
# STEP 3: Apply data visualization techniques to identify patterns
# Line Plot - Shows trend over time
print("Line plot")
plt.figure(figsize=(8,5))
plt.plot(df["Month"], df["Sales"], color="blue", marker="o", linestyle="-", linewid
plt.plot(df["Month"], df["Expenses"], color="red", marker="s", linestyle="--", line
plt.title("Monthly Sales vs Expenses")
plt.xlabel("Month")
plt.ylabel("Amount")
plt.legend(loc="best")
plt.grid(True)
plt.show()
# STEP 4: Apply various data visualization tools
# Bar Chart - Compare categories
print("Bar Chart")
months = ['Jan','Feb','Mar','Apr','May','Jun']
customers = [30,45,50,40,60,75]
plt.bar(months, customers,
 color=['red','blue','green','orange','purple','cyan'],
 edgecolor='black',
 linewidth=2)
plt.title("Number of Customers per Month")
plt.xlabel("Month")
plt.ylabel("Customers")
plt.show()
# Scatter Plot - Relationship between Sales and Customers
print("Scatter Plot")
plt.figure(figsize=(7,5))
plt.scatter(df["Customers"], df["Sales"], color="purple", s=100, marker="o")
In [18]:
plt.title("Customers vs Sales Relationship")
plt.xlabel("Customers")
plt.ylabel("Sales")
plt.grid(True)
plt.show()
# Histogram - Distribution of Sales values
print("Hisogram")
plt.figure(figsize=(7,5))
plt.hist(df["Sales"], bins=5, color="orange", edgecolor="black", alpha=0.8)
plt.title("Distribution of Sales")
plt.xlabel("Sales Value")
plt.ylabel("Frequency")
plt.grid(axis="y")
plt.show()
# Pie Chart - Proportion of expenses
print("Pie Chart")
plt.figure(figsize=(6,6))
plt.pie(df["Expenses"],
 labels=df["Month"],
 autopct="%1.1f%%",
 startangle=90,
 colors=["red","blue","green","yellow","purple","cyan"])
plt.title("Monthly Expense Distribution")
plt.show()
# STEP 5: Using necessary parameters in functions
# (Parameters used: figsize, color, marker, linestyle, linewidth, labels, title, grid)
```
# Output
![Output]Screenshot 2026-03-15 143228.png
![Output]Screenshot 2026-03-15 143237.png
![Output]Screenshot 2026-03-15 143257.png
## Result:
 Thus ,data visualization using maplot library for the given data was implemented successfully.
