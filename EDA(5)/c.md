PROGRAM 1

import pandas as pd
df = pd.read_csv(&quot;FastFood_Sales_Dataset.csv&quot;)
num_data = df.select_dtypes(include=[&#39;number&#39;])
corr_matrix = num_data.corr()
print(&quot;Correlation Matrix&quot;)
print(corr_matrix)

OUT PUT 1
<img width="643" height="117" alt="Screenshot 2026-09-02 235455" src="https://github.com/user-attachments/assets/1d792fa0-94d6-4dea-b0e4-11855de90c98" />


PROGRAM 2
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv(&quot;FastFood_Sales_Dataset.csv&quot;)
num_data = df.select_dtypes(include=[&#39;number&#39;])
corr_matrix = num_data.corr()
plt.figure(figsize=(8,6))
sns.heatmap(corr_matrix,
annot=True,
cmap=&quot;coolwarm&quot;,
fmt=&quot;.2f&quot;)
plt.title(&quot;Correlation Matrix Heatmap&quot;)
plt.show()

OUT PUT 2
<img width="512" height="358" alt="Screenshot 2026-09-02 235535" src="https://github.com/user-attachments/assets/e7d65be0-32ce-40e4-9308-5b6c4372ce44" />



PROGRAM 3
import pandas as pd
df = pd.read_csv(&quot;FastFood_Sales_Dataset.csv&quot;)
num_data = df.select_dtypes(include=[&#39;number&#39;])
corr_matrix = num_data.corr()
print(&quot;Highly Correlated Variable Pairs\n&quot;)
for i in range(len(corr_matrix.columns)):
for j in range(i+1, len(corr_matrix.columns)):
value = corr_matrix.iloc[i, j]
if value &gt; 0.8 or value &lt; -0.8:
print(corr_matrix.columns[i])
corr_matrix.columns[j],
&quot;=&quot;, round(value,2))

OUT PUT 3
<img width="366" height="230" alt="Screenshot 2026-09-02 235559" src="https://github.com/user-attachments/assets/705be382-325d-4f91-b46f-8120890b4da3" />
