| Date       | Product  | Sales |
| ---------- | -------- | ----: |
| 01/01/2024 | Kurta    |   120 |
| 02/01/2024 | Saree    |   135 |
| 03/01/2024 | Shoes    |   128 |
| 04/01/2024 | Watch    |   142 |
| 05/01/2024 | Handbag  |   150 |
| 06/01/2024 | T-Shirt  |   155 |
| 07/01/2024 | Jeans    |   160 |
| 08/01/2024 | Sneakers |   165 |
| ...        | ...      |   ... |
| 25/01/2024 | Jeans    |   225 |




PROGRAM 1

import pandas as pd
df = pd.read_csv("Rolling_Dataset.csv")
df["Date"] = pd.to_datetime(df["Date"], dayfirst=True)
df.set_index("Date", inplace=True)
df["Rolling_Mean"] = df["Sales"].rolling(window=7).mean()
df["Rolling_SD"] = df["Sales"].rolling(window=7).std()
print(df[["Sales", "Rolling_Mean", "Rolling_SD"]]

OUT PUT 1

<img width="254" height="270" alt="Screenshot 2026-09-01 203830" src="https://github.com/user-attachments/assets/e81bdc4c-549e-4dce-a302-cff9cd9e51d6" />



PROGRAM 2

Program 2: Plot Original Sales and Rolling Mean
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Rolling_Dataset.csv")
df["Date"] = pd.to_datetime(df["Date"], dayfirst=True)
df.set_index("Date", inplace=True)
df["Rolling_Mean"] = df["Sales"].rolling(window=7).mean()
plt.figure(figsize=(10,5))
plt.plot(df.index, df["Sales"], label="Original Sales")
plt.plot(df.index, df["Rolling_Mean"], linewidth=3, label="7-Day Rolling Mean")
plt.title("Sales vs 7-Day Rolling Mean")
plt.xlabel("Date")
plt.ylabel("Sales")
plt.legend()
plt.show()


OUT PUT 2

<img width="390" height="202" alt="Screenshot 2026-09-01 204156" src="https://github.com/user-attachments/assets/a67a9af3-6e1e-4aca-82f2-eba19e63d2b8" />


PROGRAM 3

import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Rolling_Dataset.csv")
df["Date"] = pd.to_datetime(df["Date"], dayfirst=True)
df.set_index("Date", inplace=True
df["Rolling_SD"] = df["Sales"].rolling(window=7).std()
plt.figure(figsize=(10,5))
plt.plot(df.index, df["Rolling_SD"], linewidth=3)
plt.title("7-Day Rolling Standard Deviation")
plt.xlabel("Date")
plt.ylabel("Standard Deviation")
plt.show()


OUT PUT 3<img width="389" height="211" alt="Screenshot 2026-09-01 204353" src="https://github.com/user-attachments/assets/d0e2ef85-b877-41a0-b828-5eaa24c0bbd6" />

