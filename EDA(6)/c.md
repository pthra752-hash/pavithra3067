PROGRAM 1
import pandas as pd
df = pd.read_csv("Pairplot_Dataset.csv")
print("E-Commerce Sales Dataset")
print(df.head())
print("\nDataset Information")
print(df.info())

OUT PUT 1
<img width="390" height="353" alt="Screenshot 2026-09-05 233239" src="https://github.com/user-attachments/assets/64acd538-3227-4b97-9e05-88482a54360d" />


PROGRAM 2
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df = pd.read_csv("Pairplot_Dataset.csv")
sns.pairplot(
    df,
    vars=["Price", "Rating", "Sales", "Discount", "Stock"],
    hue="Category",
    diag_kind="hist"
)
plt.show()

OUT PUT 2
<img width="581" height="508" alt="Screenshot 2026-09-05 233305" src="https://github.com/user-attachments/assets/ea144394-7c14-400c-86a7-42a673af7fd1" />

