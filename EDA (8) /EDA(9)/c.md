INPUT DATA SET
S.No Product   Category   Sales   Orders   Revenue   Rating    Disc.(%)
1    Kurta     Clothing   120     8        12000     4.5       10
2    Saree     Clothing   135     9        13500     4.6       12
3    T-Shirt   Clothing   140     10       14000     4.4       15
4    Jeans     Clothing   150     11       15000     4.7       10
5    Shirt     Clothing   145     10       14500     4.5       8
6    Hoodie    Clothing   155     12       15500     4.8       15
7    Jacket    Clothing   160     12       16000     4.6       20
8    Kurta     Clothing   165     13       16500     4.7       12
9    Saree     Clothing   170     14       17000     4.8       10
10   T-Shirt   Clothing   175     14       17500     4.5       18
11   Shoes     Footwear   95      6        9500      4.2       5
12   Sneakers  Footwear   100     7        10000     4.3       8
13   Sandals   Footwear   105     7        10500     4.4       10
14   Boots     Footwear   110     8        11000     4.5       12
15   Loafers   Footwear   115     8        11500     4.3       15
16   Slippers  Footwear   120     9        12000     4.4       10
17   SportShoes Footwear  125     9        12500     4.6       18
18   Sneakers  Footwear   130     10       13000     4.5       12
19   Sandals   Footwear   135     10       13500     4.6       8
20   Boots     Footwear   140     11       14000     4.7       10
21   Kurta     Clothing   180     15       18000     4.9       15
22   Jeans     Clothing   185     15       18500     4.8       20
23   SportShoes Footwear  145     11       14500     4.7       15
24   Loafers   Footwear   150     12       15000     4.8       18
25   Jacket    Clothing   190     16       19000     4.9       10




PROGARM 1

Python Program
Program 1: Perform Independent Sample t-test
import pandas as pd
from scipy.stats import ttest_ind
# Load the dataset
df = pd.read_csv("TTest_Dataset.csv")
# Create two groups
clothing = df[df["Category"] == "Clothing"]["Sales"]
footwear = df[df["Category"] == "Footwear"]["Sales"]
# Perform Independent Sample t-test
t_value, p_value = ttest_ind(clothing, footwear)
# Display results
print("t-value :", t_value)
print("p-value :", p_value)

OUT PUT 1<img width="472" height="165" alt="Screenshot 2026-09-01 211315" src="https://github.com/user-attachments/assets/7b443df0-70a9-4f36-96dd-f9fd3fedbe7e" />


PROGRAM 2

import pandas as pd
from scipy.stats import ttest_ind
# Load the dataset
df = pd.read_csv("TTest_Dataset.csv")
# Create two groups
clothing = df[df["Category"] == "Clothing"]["Sales"]
footwear = df[df["Category"] == "Footwear"]["Sales"]
# Perform Independent Sample t-test
t_value, p_value = ttest_ind(clothing, footwear)
# Significance level
alpha = 0.05
print("t-value :", t_value)
print("p-value :", p_value)
# Conclusion
if p_value < alpha:
    print("\nConclusion:")
    print("Reject the Null Hypothesis (H0)")
    print("There is a significant difference between the Sales of "
          "Clothing and Footwear products.")
else:
    print("\nConclusion:")
    print("Fail to Reject the Null Hypothesis (H0)")
    print("There is no significant difference between the Sales of "
          "Clothing and Footwear products.")



OUT PUT 2
<img width="551" height="162" alt="Screenshot 2026-09-01 211727" src="https://github.com/user-attachments/assets/f387454d-eee9-4b53-8423-48dd7b3cd19d" />

PROGRAM 3

import pandas as pd
# Load the dataset
df = pd.read_csv("TTest_Dataset.csv")
# Group statistics
stats = df.groupby("Category")["Sales"].agg(["count", "mean", "std", "min", "max"])
print("Sales Statistics by Category")
print(stats)

OUT PUT 3
<img width="394" height="145" alt="Screenshot 2026-09-01 211832" src="https://github.com/user-attachments/assets/60aae1a6-a2ba-4a62-b6a8-d3110115f838" />

