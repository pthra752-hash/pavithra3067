PROGRAM 1
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Sales_Dataset.csv")
category_sales = df.groupby('Category')['Total Sales'].sum()
plt.figure(figsize=(8,5))
category_sales.plot(kind='bar', color='#4C72B0')
plt.title("Total Sales by Category")
plt.xlabel("Category")
plt.ylabel("Total Sales")
plt.tight_layout()
plt.savefig("output_program1.png", dpi=120)
plt.show()

OUT PUT 1<img width="594" height="444" alt="Screenshot 2026-09-02 201300" src="https://github.com/user-attachments/assets/9585f030-b0b9-46c6-99af-bebf5bddfa85" />


PROGRAM 2
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("/content/Rolling_Dataset (1).csv")

category_count = df["Category"].value_counts()

category_count.plot(
    kind="pie",
    autopct="%1.1f%%",
    figsize=(7,7)
)

plt.title("Product Category Distribution")
plt.ylabel("")
plt.show()



OUT PUT 2
<img width="545" height="525" alt="Screenshot 2026-09-02 222841" src="https://github.com/user-attachments/assets/b3efd4a6-e51a-4286-bc11-d365588f7e8e" />


PROGARM 3
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("/content/Sales_Dataset.csv")
df.columns = df.columns.str.strip()
plt.figure(figsize=(8,5))
plt.hist(df["Unit Price"], bins=10, edgecolor="black")
plt.title("Distribution of Unit Price")
plt.xlabel("Unit Price")
plt.ylabel("Frequency")
plt.grid(True)
plt.show()

OUT PUT 3<img width="686" height="348" alt="Screenshot 2026-09-02 230326" src="https://github.com/user-attachments/assets/d1df18ff-7394-4ade-9b89-e02fbaa8e9b2" />
PROGRAM 4


import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("/content/Sales_Dataset.csv")
df.columns = df.columns.str.strip()
plt.figure(figsize=(8,5))
plt.hist(df["Unit Price"], bins=10, edgecolor="black")
plt.title("Distribution of Unit Price")
plt.xlabel("Unit Price")
plt.ylabel("Frequency")
plt.grid(True)

plt.show()


OUT PUT 4
<img width="704" height="331" alt="Screenshot 2026-09-02 230741" src="https://github.com/user-attachments/assets/00322765-fad8-4d36-a6ab-a79570840163" />

Program 5

import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("/content/Sales_Dataset.csv")
df.columns = df.columns.str.strip()
plt.figure(figsize=(8,5))
plt.scatter(df["Unit Price"], df["Total Sales"])
plt.title("Unit Price vs Total Sales")
plt.xlabel("Unit Price")
plt.ylabel("Total Sales")
plt.grid(True)
plt.show()

OUT PUT 5
<img width="708" height="369" alt="Screenshot 2026-09-02 230957" src="https://github.com/user-attachments/assets/9776ba8c-b82e-4275-9067-843b34adddb8" />
