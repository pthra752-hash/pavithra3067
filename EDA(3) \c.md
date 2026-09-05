PROGRAM 1
import pandas as pd
df = pd.read_csv("Messy_FoodSales.csv")
print(df)


OUT PUT 1
<img width="376" height="320" alt="Screenshot 2026-09-05 224911" src="https://github.com/user-attachments/assets/dc431b8b-f1c1-497f-9f53-a3e0b6b27d26" />

PROGRAM 2
import pandas as pd
df = pd.read_csv("Messy_Sales_Dataset.csv")
print(df.isnull().sum())

OUT PUT 2
<img width="87" height="113" alt="Screenshot 2026-09-05 230004" src="https://github.com/user-attachments/assets/bc458590-cbb6-4333-bbbd-a2242e60e0c8" />

PROGRAM 3
import pandas as pd
df = pd.read_csv("Messy_Sales_Dataset.csv")
df["Price"] = df["Price"].fillna(df["Price"].mean())
df["Rating"] = df["Rating"].fillna(df["Rating"].mean())
df["Quantity"] = df["Quantity"].fillna(df["Quantity"].mean())
 print(df)

OUT PUT 3
<img width="447" height="334" alt="Screenshot 2026-09-05 230029" src="https://github.com/user-attachments/assets/a3532e71-77ce-4020-a3fe-932933721f26" />


PROGRAM 4
import pandas as pd
df = pd.read_csv("Messy_Sales_Dataset.csv")
df["Category"] = df["Category"].fillna(df["Category"].mode()[0])
 print(df)

 OUT PUT 4
 <img width="386" height="319" alt="Screenshot 2026-09-05 230610" src="https://github.com/user-attachments/assets/0760846a-96c0-413f-94a8-563776b396b4" />

PROGRAM 5
import pandas as pd
df = pd.read_csv("Messy_Sales_Dataset.csv")
print(df[df.duplicated()])

OUT PUT 5
<img width="362" height="47" alt="Screenshot 2026-09-05 230633" src="https://github.com/user-attachments/assets/ac3a2cef-0bf3-4ba0-9d45-edaac175b89a" />


PROGRAM 6
import pandas as pd
df = pd.read_csv("Messy_Sales_Dataset.csv")
df = df.drop_duplicates()
print(df)

OUT PUT 6
<img width="379" height="301" alt="Screenshot 2026-09-05 231321" src="https://github.com/user-attachments/assets/61b233a5-e894-4b78-b808-ae9c81a0d923" />

PROGRAM 7
import pandas as pd
df = pd.read_csv("Messy_Sales_Dataset.csv")
df["Category"] = df["Category"].replace("furniture", "Furniture")
print(df)

OUT PUT 7
<img width="387" height="332" alt="Screenshot 2026-09-05 231339" src="https://github.com/user-attachments/assets/b8f80906-1915-42ef-b562-3a8991b5c914" />


PROGRAM 8
import pandas as pd
df = pd.read_csv("Messy_Sales_Dataset.csv")
df["Price"] = df["Price"].fillna(df["Price"].mean())
df["Rating"] = df["Rating"].fillna(df["Rating"].mean())
df["Quantity"] = df["Quantity"].fillna(df["Quantity"].mean())
df["Category"] = df["Category"].replace("furniture", "Furniture")
df = df.drop_duplicates()
print("Missing Values:")
print(df.isnull().sum())
print("\nDuplicate Records:")
print(df.duplicated().sum())
print("\nCleaned Dataset:")
print(df)

OUT PUT 8
<img width="442" height="480" alt="Screenshot 2026-09-05 231718" src="https://github.com/user-attachments/assets/fcc6fb6c-5af7-412e-a6f0-f51cbc36ded7" />

