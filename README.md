# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

**NAME : THARUN SRIDHAR**

**REGISTER NO : 212223230230**

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/b88ad490-ee37-4510-b137-f3d9b30897d2)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image](https://github.com/user-attachments/assets/b3c14236-3dfe-496f-a034-534cb4d39164)

```
import seaborn as sns
import matplotlib.pyplot as plt
# Load the tips dataset
tips = sns.load_dataset('tips')
#Calculate the average total bill and tip for each day of the week
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip =tips.groupby('day') ['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
#Set the labels and title
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/474a2942-7fcd-415d-95a8-e9a044260964)

```
avg_total_bill = tips.groupby('time') ['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom = avg_total_bill, label='Tip', width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/209691c0-2da6-4e9b-8249-db4f3dd7f836)

```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
#Set labels and title
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/2ea7bca2-a875-49a6-87cb-d21cc444a150)

```
tips = sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
# Set labels and title
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/a0eeff60-961d-4ad6-a92b-301a0de8f3e5)

```
import seaborn as sns
import matplotlib.pyplot as plt
sns.histplot(data=tips,x="total_bill", hue="smoker", kde=True, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```
![image](https://github.com/user-attachments/assets/68fdf05a-f034-424c-9783-ddeeb6c91d47)

```
import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/9eabb59d-fe6b-4e70-bdcd-7b32e0ba8342)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "red", "edgecolor": "darkblue"},
whiskerprops={"color": "red", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 2})
```
![image](https://github.com/user-attachments/assets/fc0a4327-5e4c-403b-91fa-66256f18f50e)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
#Add labels and title
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/38a8587a-7f09-4dd3-a3d7-004ef5e9f61c)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![image](https://github.com/user-attachments/assets/2dac3ca5-72b1-4f88-a6bd-b8368dd2b6ad)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip,palette='Set1')
```
![image](https://github.com/user-attachments/assets/9890468f-f538-41f6-bb04-f477375a3cf6)

```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/user-attachments/assets/4b2049af-7d2a-4bb3-ad7c-64cc66379556)

```
import seaborn as sns
# use to set style of background of plot
sns.set(style="whitegrid")
# loading data-set
tips = sns.load_dataset("tips")
sns.violinplot(x="tip", y="day", data=tip,palette="Set1")
```
![image](https://github.com/user-attachments/assets/7822a68c-30cd-4ab2-8e16-26113db350d4)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/b9b1fb5f-0cd9-4f35-8aa7-1c79d6910213)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set1',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/c03cd357-7b23-4aca-9615-2264850ad52b)

```
import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt
tips = sns.load_dataset("tips")
numeric_cols = tips.select_dtypes (include=np.number).columns
corr = tips [numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap='plasma',linewidth=0.5)
```
![image](https://github.com/user-attachments/assets/f16eb96c-c879-4494-95f6-c4fcdd8dee1d)


# Result:
 Hence, Data Visualization using seaborn library is performed successfully.
