# 🥪 Canteen Shop Sales Analysis

A simple data analysis and visualization project that explores sales data from a canteen shop using **Python, Pandas, and Matplotlib**.

The project analyzes product sales, customer payment methods, weather conditions during purchases, and transaction amounts.

## 📌 Project Overview

The purpose of this project is to practice basic **data analysis and data visualization** using a canteen sales dataset.

The analysis includes:

* Loading and exploring sales data
* Analyzing the quantity of items sold
* Examining customer payment methods
* Analyzing weather conditions during purchases
* Visualizing total purchase amounts
* Creating bar charts, pie charts, and line graphs

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Matplotlib**
* **Google Colab / Jupyter Notebook**

## 📂 Project Structure

```text
Canteen-Shop-Analysis/
│
├── canteen_shop_analysis.py
├── sales.csv
└── README.md
```

## 📊 Analysis Performed

### 1. Load the Dataset

The sales dataset is loaded using Pandas:

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("sales.csv")
```

The first few records are displayed using:

```python
df.head()
```

### 2. Analyze Items Sold

The project extracts the **Item** and **Quantity** columns:

```python
items = df["Item"]
quantity = df["Quantity"]
```

A bar chart is created to visualize the quantity of each item sold:

```python
plt.bar(items, quantity)
plt.title("Items Sold")
plt.xlabel("Item")
plt.ylabel("Quantity")
plt.show()
```

This visualization helps show which products were purchased and their respective quantities.

### 3. Analyze Payment Methods

The number of purchases made using each payment method is calculated using:

```python
payment = df["Payment Method"].value_counts()
```

A bar chart displays how customers paid:

```python
plt.bar(payment.index, payment.values)
plt.title("How People Paid")
plt.xlabel("Payment Method")
plt.ylabel("Count")
plt.show()
```

This helps identify the most commonly used payment methods among customers.

### 4. Analyze Shopping Weather

The project analyzes the weather conditions during purchases:

```python
weather = df["Weather"].value_counts()
```

A pie chart is used to visualize the distribution:

```python
plt.pie(weather.values, labels=weather.index)
plt.title("Shopping Weather")
plt.show()
```

This provides a simple view of the weather conditions associated with customer purchases.

### 5. Analyze Purchase Amounts

A line graph is created using the **Total** column:

```python
plt.plot(df.index, df["Total"])
plt.title("Total Money")
plt.xlabel("Purchase Number")
plt.ylabel("Amount")
plt.show()
```

This chart shows how the total purchase amount changes across different transactions.

## 📈 Visualizations

The project generates four main visualizations:

* 📊 **Bar Chart — Items Sold**
* 📊 **Bar Chart — Payment Methods**
* 🥧 **Pie Chart — Shopping Weather**
* 📈 **Line Chart — Purchase Amounts**

These visualizations make the canteen sales data easier to understand and interpret.

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the Project Folder

```bash
cd Canteen-Shop-Analysis
```

### 3. Install the Required Libraries

```bash
pip install pandas matplotlib
```

### 4. Add the Dataset

Make sure the following file is located in the same directory as the Python script:

```text
sales.csv
```

The dataset should contain columns such as:

```text
Item
Quantity
Payment Method
Weather
Total
```

### 5. Run the Python File

```bash
python canteen_shop_analysis.py
```

The project can also be run using **Google Colab** or a **Jupyter Notebook**.

## 🎯 Skills Demonstrated

This project demonstrates basic skills in:

* Python programming
* Loading CSV datasets
* Data exploration
* Working with Pandas DataFrames
* Counting categorical values
* Extracting DataFrame columns
* Data visualization
* Bar charts
* Pie charts
* Line graphs
* Matplotlib

## 🔮 Future Improvements

The project could be expanded by adding:

* Identification of the best-selling item
* Total revenue calculation
* Average purchase amount
* Sales analysis by weather condition
* Payment method percentages
* Revenue by product
* Daily or weekly sales trends
* Most profitable products
* Improved chart formatting and labels
* Interactive dashboards

## 👤 Author

Created as a Python data analysis project using canteen shop sales data.

## 📄 License

This project is intended for educational and learning purposes.
