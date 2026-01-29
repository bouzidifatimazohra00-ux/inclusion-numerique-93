```python
import pandas as pd

village = pd.read_csv("ecoStat-jeux-données-village-Tung-Lam.csv")
village
```





  <div id="df-911e1163-55ba-46c2-8a9d-4f9a0abccb2b" class="colab-df-container">
    <div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id</th>
      <th>sex</th>
      <th>age</th>
      <th>pre_income</th>
      <th>program</th>
      <th>post_income</th>
      <th>sex_num</th>
      <th>program_num</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Male</td>
      <td>45</td>
      <td>979.407453</td>
      <td>No program</td>
      <td>1281.490982</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Female</td>
      <td>23</td>
      <td>663.545110</td>
      <td>No program</td>
      <td>1041.346836</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Female</td>
      <td>42</td>
      <td>729.256002</td>
      <td>No program</td>
      <td>1247.336819</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Female</td>
      <td>34</td>
      <td>744.371565</td>
      <td>Program</td>
      <td>1248.704147</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Female</td>
      <td>53</td>
      <td>768.991891</td>
      <td>No program</td>
      <td>1342.932254</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>995</th>
      <td>996</td>
      <td>Male</td>
      <td>35</td>
      <td>637.734280</td>
      <td>No program</td>
      <td>1195.449627</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>996</th>
      <td>997</td>
      <td>Female</td>
      <td>50</td>
      <td>845.625777</td>
      <td>Program</td>
      <td>1426.746177</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>997</th>
      <td>998</td>
      <td>Male</td>
      <td>41</td>
      <td>818.407329</td>
      <td>No program</td>
      <td>1246.869065</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>998</th>
      <td>999</td>
      <td>Female</td>
      <td>53</td>
      <td>805.797636</td>
      <td>No program</td>
      <td>1349.237168</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>999</th>
      <td>1000</td>
      <td>Male</td>
      <td>46</td>
      <td>869.211571</td>
      <td>No program</td>
      <td>1301.508129</td>
      <td>1</td>
      <td>0</td>
    </tr>
  </tbody>
</table>

</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-911e1163-55ba-46c2-8a9d-4f9a0abccb2b')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

 

   
  </div>


   



     



```python
display(village.info())
display(village.describe())
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 1000 entries, 0 to 999
    Data columns (total 8 columns):
     #   Column       Non-Null Count  Dtype  
    ---  ------       --------------  -----  
     0   id           1000 non-null   int64  
     1   sex          1000 non-null   object 
     2   age          1000 non-null   int64  
     3   pre_income   1000 non-null   float64
     4   program      1000 non-null   object 
     5   post_income  1000 non-null   float64
     6   sex_num      1000 non-null   int64  
     7   program_num  1000 non-null   int64  
    dtypes: float64(2), int64(4), object(2)
    memory usage: 62.6+ KB



    




  <div id="df-12866989-8bae-4b37-85c4-8602cf6292e7" class="colab-df-container">
    <div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id</th>
      <th>age</th>
      <th>pre_income</th>
      <th>post_income</th>
      <th>sex_num</th>
      <th>program_num</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>1000.000000</td>
      <td>1000.0000</td>
      <td>1000.000000</td>
      <td>1000.000000</td>
      <td>1000.00000</td>
      <td>1000.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>500.500000</td>
      <td>34.8900</td>
      <td>802.410383</td>
      <td>1229.303490</td>
      <td>0.59400</td>
      <td>0.497000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>288.819436</td>
      <td>9.4863</td>
      <td>103.289190</td>
      <td>107.816412</td>
      <td>0.49133</td>
      <td>0.500241</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>6.0000</td>
      <td>487.841044</td>
      <td>880.158269</td>
      <td>0.00000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>250.750000</td>
      <td>29.0000</td>
      <td>733.248698</td>
      <td>1158.582090</td>
      <td>0.00000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>500.500000</td>
      <td>35.0000</td>
      <td>803.975180</td>
      <td>1231.949935</td>
      <td>1.00000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>750.250000</td>
      <td>41.0000</td>
      <td>870.159361</td>
      <td>1302.697146</td>
      <td>1.00000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1000.000000</td>
      <td>62.0000</td>
      <td>1116.793765</td>
      <td>1560.954199</td>
      <td>1.00000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>





```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(10, 6))
sns.histplot(data=village, x='pre_income', kde=True, color='blue', alpha=0.5, label='Pre-Income')
sns.histplot(data=village, x='post_income', kde=True, color='orange', alpha=0.5, label='Post-Income')
plt.title('Overlay of Pre-Income and Post-Income Distributions')
plt.xlabel('Income')
plt.ylabel('Frequency')
plt.grid(True)
plt.legend()
plt.show()
```


    
![png](./ecoStatTung_Lam_files/ecoStatTung_Lam_3_0.png)
    



```python
display(village.groupby('program')[['pre_income', 'post_income']].describe())
```



  <div id="df-7cba93e7-9c79-4e63-ae3f-f0e665cd27f5" class="colab-df-container">
    <div>

<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="8" halign="left">pre_income</th>
      <th colspan="8" halign="left">post_income</th>
    </tr>
    <tr>
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
    <tr>
      <th>program</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>No program</th>
      <td>503.0</td>
      <td>803.329778</td>
      <td>101.506667</td>
      <td>544.998552</td>
      <td>733.652041</td>
      <td>805.665067</td>
      <td>871.631933</td>
      <td>1116.793765</td>
      <td>503.0</td>
      <td>1179.977293</td>
      <td>94.598373</td>
      <td>880.158269</td>
      <td>1117.320179</td>
      <td>1181.743386</td>
      <td>1242.057069</td>
      <td>1441.986926</td>
    </tr>
    <tr>
      <th>Program</th>
      <td>497.0</td>
      <td>801.479890</td>
      <td>105.156600</td>
      <td>487.841044</td>
      <td>732.592979</td>
      <td>801.801591</td>
      <td>868.507391</td>
      <td>1102.247561</td>
      <td>497.0</td>
      <td>1279.225173</td>
      <td>96.907668</td>
      <td>978.941979</td>
      <td>1218.631974</td>
      <td>1285.887273</td>
      <td>1346.743730</td>
      <td>1560.954199</td>
    </tr>
  </tbody>
</table>





```python
plt.figure(figsize=(12, 6))
sns.histplot(data=village, x='pre_income', hue='program', kde=True)
plt.title('Distribution of Pre-Income by Program')
plt.xlabel('Pre-Income')
plt.ylabel('Frequency')
plt.grid(True)
plt.show()
```


    
![png](./ecoStatTung_Lam_files/ecoStatTung_Lam_5_0.png)
    



```python
plt.figure(figsize=(10, 6))
sns.histplot(data=village[village['program'] == 'No program'], x='pre_income', kde=True, color='blue', alpha=0.5, label='Pre-Income')
sns.histplot(data=village[village['program'] == 'No program'], x='post_income', kde=True, color='orange', alpha=0.5, label='Post-Income')
plt.title('Overlay of Pre-Income and Post-Income Distributions')
plt.xlabel('Income')
plt.ylabel('Frequency')
plt.grid(True)
plt.legend()
plt.show()
```


    
![png](ecoStatTung_Lam_files/ecoStatTung_Lam_6_0.png)
    



```python
plt.figure(figsize=(12, 6))
sns.histplot(data=village, x='post_income', hue='program', kde=True)
plt.title('Distribution of Post-Income by Program')
plt.xlabel('Post-Income')
plt.ylabel('Frequency')
plt.grid(True)
plt.show()
```


    
![png](ecoStatTung_Lam_files/ecoStatTung_Lam_7_0.png)
    



```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(10, 6))
sns.scatterplot(data=village, x='pre_income', y='post_income', hue='program')
plt.title('Pre-Income vs Post-Income by Program')
plt.xlabel('Pre-Income')
plt.ylabel('Post-Income')
plt.grid(True)
plt.show()
```


    
![png](ecoStatTung_Lam_files/ecoStatTung_Lam_8_0.png)
    



```python
village['income_increase'] = village['post_income'] - village['pre_income']
display(village.head())
```



  <div id="df-52c772a9-69c7-476b-9996-cb80bf7e1ec7" class="colab-df-container">
    <div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id</th>
      <th>sex</th>
      <th>age</th>
      <th>pre_income</th>
      <th>program</th>
      <th>post_income</th>
      <th>sex_num</th>
      <th>program_num</th>
      <th>income_increase</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Male</td>
      <td>45</td>
      <td>979.407453</td>
      <td>No program</td>
      <td>1281.490982</td>
      <td>1</td>
      <td>0</td>
      <td>302.083530</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Female</td>
      <td>23</td>
      <td>663.545110</td>
      <td>No program</td>
      <td>1041.346836</td>
      <td>0</td>
      <td>0</td>
      <td>377.801726</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Female</td>
      <td>42</td>
      <td>729.256002</td>
      <td>No program</td>
      <td>1247.336819</td>
      <td>0</td>
      <td>0</td>
      <td>518.080817</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Female</td>
      <td>34</td>
      <td>744.371565</td>
      <td>Program</td>
      <td>1248.704147</td>
      <td>0</td>
      <td>1</td>
      <td>504.332581</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Female</td>
      <td>53</td>
      <td>768.991891</td>
      <td>No program</td>
      <td>1342.932254</td>
      <td>0</td>
      <td>0</td>
      <td>573.940364</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-52c772a9-69c7-476b-9996-cb80bf7e1ec7')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  

  
  </div>


   




```python
from scipy import stats

program_group = village[village['program'] == 'Program']['income_increase']
no_program_group = village[village['program'] == 'No program']['income_increase']

ttest_result = stats.ttest_ind(program_group, no_program_group)

print(f"T-test statistic: {ttest_result.statistic}")
print(f"P-value: {ttest_result.pvalue}")

if ttest_result.pvalue < 0.05:
    print("The difference in income increase between the two groups is statistically significant.")
else:
    print("There is no statistically significant difference in income increase between the two groups.")
```

    T-test statistic: 11.511317490733365
    P-value: 7.025779640137422e-29
    The difference in income increase between the two groups is statistically significant.

