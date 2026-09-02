PROGRAM 1
import pandas as pd
df = pd.read_csv("fastfood_sales.csv")
print("Original Column Names:")
print(df.columns)
df.rename(columns={
    'orderid': 'Order_ID',
    'cust': 'Customer_Name',
    'age': 'Age',
    'prod': 'Product',
    'qty': 'Quantity',
    'price': 'Price',
    'city': 'City'
}, inplace=True)
print("\nRenamed Column Names:")
print(df.columns)

OUT PUT 1
<img width="566" height="105" alt="Screenshot 2026-09-02 233749" src="https://github.com/user-attachments/assets/0b84f071-f3a8-454f-ac1e-4c92d59f0340" />



Program 2
import pandas as pd
df = pd.read_csv("fastfood_sales.csv")
df.rename(columns={
    'orderid': 'Order_ID', 'cust': 'Customer_Name', 'age': 'Age',
    'prod': 'Product', 'qty': 'Quantity', 'price': 'Price', 'city': 'City'
}, inplace=True)
print("Before Conversion:")
print(df.dtypes)
df["Price"] = df["Price"].astype(float)
df["Quantity"] = df["Quantity"].astype(int)
print("\nAfter Conversion:")
print(df.dtypes)

out put 2
<img width="174" height="273" alt="Screenshot 2026-09-02 234108" src="https://github.com/user-attachments/assets/ce1b86c8-8014-4053-96eb-9dcedbf93350" />

Program 3
import pandas as pd
df = pd.read_csv("fastfood_sales.csv")
df.rename(columns={
    'orderid': 'Order_ID', 'cust': 'Customer_Name', 'age': 'Age',
    'prod': 'Product', 'qty': 'Quantity', 'price': 'Price', 'city': 'City'
}, inplace=True)
df["Age_EqualWidth"] = pd.cut(
    df["Age"], bins=4, labels=["Young", "Adult", "Middle Age", "Senior"]
)
df["Age_EqualFrequency"] = pd.qcut(
    df["Age"], q=4, labels=["Young", "Adult", "Middle Age", "Senior"]
)
print(df[["Age", "Age_EqualWidth", "Age_EqualFrequency"]])

out put 3
<img width="458" height="442" alt="Screenshot 2026-09-02 234347" src="https://github.com/user-attachments/assets/6787ee59-e826-49e4-9f3d-ff2ae7a785c2" />
