Input Dataset
Dataset preview (sales_dataset_2025.csv, first 15 rows)
Date	Region	Category	Product	Units_Sold	Unit_Price	Discount_Percent	Total_Sales	Customer_Rating
2025-01-01	East	Furniture	Chair	43	390.95	20	16810.85	1.6
2025-01-02	East	Groceries	Cooking Oil	11	433.76	15	4771.36	1.6
2025-01-03	North	Groceries	Wheat Flour	2	362.39	5	724.78	1.7
2025-01-04	West	Toys	Action Figure	22	8.5	0	187.00	2.2
2025-01-05	South	Groceries	Cooking Oil	28	487.01	10	13636.28	2.5
2025-01-06	North	Furniture	Bookshelf	3	430.67	20	1292.01	2.8
2025-01-07	North	Clothing	Shoes	14	405.16	0	5672.24	1.1
2025-01-08	West	Clothing	Shoes	47	343.22	15	16131.34	3.0
2025-01-09	North	Groceries	Wheat Flour	36	95.21	15	3427.56	2.2
2025-01-10	South	Clothing	Shoes	29	484.94	5	14063.26	2.8
2025-01-11	West	Clothing	Jeans	14	365.00	15	5110.00	1.2
2025-01-12	North	Toys	Doll	18	272.15	5	4898.70	4.9
2025-01-13	North	Furniture	Bookshelf	41	151.66	20	6218.06	1.3
2025-01-14	North	Electronics	Smartwatch	44	150.28	10	6612.32	1.8
2025-01-15	North	Groceries	Cooking Oil	5	463.52


program 1
# Import Pandas library
import pandas as pd

# Load the dataset
df_sales = pd.read_csv('/content/sample_data/sales_dataset_2025.csv')

# Display the dataset
display(df_sales)

OUTPUT 1
<img width="593" height="470" alt="Screenshot 2026-09-02 152634" src="https://github.com/user-attachments/assets/1dd1fc6e-04b6-414b-8883-21e0c1c3cead" />


PROGRAM 2
df_sales = pd.read_csv('/content/sample_data/sales_dataset_2025.csv')
display(df_sales.head()

OUT PUT2

<img width="595" height="387" alt="Screenshot 2026-09-02 152657" src="https://github.com/user-attachments/assets/cd2c7d76-860f-48fe-8fc2-7f10dc84ef90" />


PROGRAM 3
df_sales = pd.read_csv('/content/sample_data/sales_dataset_2025.csv')
display(df_sales.tail())

OUT PUT
<img width="424" height="395" alt="Screenshot 2026-09-02 152709" src="https://github.com/user-attachments/assets/80cea4a1-b111-4b77-9b44-9da3f4af9d36" />


PROGRAM 4
df_sales = pd.read_csv('/content/sample_data/sales_dataset_2025.csv')
display(df_sales.info())

OUY PUT 4
<img width="530" height="374" alt="Screenshot 2026-09-02 152730" src="https://github.com/user-attachments/assets/ebab320c-3fa0-4f00-9a58-73412f4d84a5" />

PROGRAM 5
df_sales = pd.read_csv('/content/sample_data/sales_dataset_2025.csv')
display(df_sales.shape)

OUT PUT 5<img width="107" height="73" alt="Screenshot 2026-09-02 152715" src="https://github.com/user-attachments/assets/fc8dfe5d-5ee4-43af-bc89-364895eb322a" />

PROGRAM 6

df_sales = pd.read_csv('/content/sample_data/sales_dataset_2025.csv')
display(df_sales.describe())


OUT PUT 6
<img width="568" height="407" alt="Screenshot 2026-09-02 153816" src="https://github.com/user-attachments/assets/892c1110-1978-4a0e-a329-f2cd37a3f58a" />

