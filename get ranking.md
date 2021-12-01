```python
import pandas as pd
```


```python
unirank= pd.read_csv(r'C:\Users\user\Downloads\unirank1.csv')
qsrank = pd.read_csv(r'C:\Users\user\Downloads\2020-QS-World-University-Rankings.csv')
```


```python
print(unirank.columns)
print(qsrank.columns)
len(qsrank["Institution Name"])
```

    Index(['Unnamed: 0', 'program', 'University', 'Master', 'Bacholer',
           'Graduate Certificate', 'Associate', 'LLM'],
          dtype='object')
    Index(['Rank in 2020', 'Rank in 2019', 'Institution Name', 'Country',
           'Classification', 'Unnamed: 5', 'Unnamed: 6', 'Unnamed: 7',
           'Unnamed: 8', 'Academic Reputation', 'Unnamed: 10',
           'Employer Reputation', 'Unnamed: 12', 'Faculty Student', 'Unnamed: 14',
           'Citations per Faculty', 'Unnamed: 16', 'International Faculty',
           'Unnamed: 18', 'International Students', 'Unnamed: 20', 'Overall Score',
           'Unnamed: 22', 'Unnamed: 23', 'Unnamed: 24', 'Unnamed: 25'],
          dtype='object')
    




    1025




```python
unirank["ranking"]=""    
```


```python
unirank["ranking"]=unirank
```


```python
a=list(qsrank["Rank in 2020"].fillna("-"))
for i in range(0,len(a)):
    try:
        a[i]=int(a[i].replace("=",""))
    except:
        pass

b=list(qsrank["Institution Name"].fillna("-"))
c=list(qsrank["Country"].fillna("-"))

```


```python
unirankdict= dict(zip(b,a))
unicountry=dict(zip(b,c))
```


```python
ranks=[]
country=[]
for i in unirank["University"]:
    try:
        ranks.append(unirankdict[i])
    except:
        ranks.append("")
unirank["ranking"]=ranks
for i in unirank["University"]:
    try:
        country.append(unicountry[i])
    except:
        country.append("")

```


```python
unirank["Country"]=country
```


```python
unirank
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>program</th>
      <th>University</th>
      <th>Master</th>
      <th>Bacholer</th>
      <th>Graduate Certificate</th>
      <th>Associate</th>
      <th>LLM</th>
      <th>ranking</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>MBA</td>
      <td>Harvard University</td>
      <td>master</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3</td>
      <td>United States</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>MS in Computational Science and Engineering</td>
      <td>Harvard University</td>
      <td>master</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3</td>
      <td>United States</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>Bachelors of Arts in Computer Science</td>
      <td>Harvard University</td>
      <td>NaN</td>
      <td>bacholer</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3</td>
      <td>United States</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>Master of Science in Data Science</td>
      <td>Harvard University</td>
      <td>master</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3</td>
      <td>United States</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>Bachelors in Economics</td>
      <td>Harvard University</td>
      <td>NaN</td>
      <td>bacholer</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3</td>
      <td>United States</td>
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
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>22935</th>
      <td>24</td>
      <td>Bachelor of Engineering with Honours in Electr...</td>
      <td>University of Waikato</td>
      <td>NaN</td>
      <td>bacholer</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>266</td>
      <td>New Zealand</td>
    </tr>
    <tr>
      <th>22936</th>
      <td>25</td>
      <td>Bachelor of Communication Studies</td>
      <td>University of Waikato</td>
      <td>NaN</td>
      <td>bacholer</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>266</td>
      <td>New Zealand</td>
    </tr>
    <tr>
      <th>22937</th>
      <td>26</td>
      <td>Master of Management</td>
      <td>University of Waikato</td>
      <td>master</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>266</td>
      <td>New Zealand</td>
    </tr>
    <tr>
      <th>22938</th>
      <td>27</td>
      <td>Master of Educational Management</td>
      <td>University of Waikato</td>
      <td>master</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>266</td>
      <td>New Zealand</td>
    </tr>
    <tr>
      <th>22939</th>
      <td>28</td>
      <td>LLM Master of Laws</td>
      <td>University of Waikato</td>
      <td>master</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>266</td>
      <td>New Zealand</td>
    </tr>
  </tbody>
</table>
<p>22940 rows × 10 columns</p>
</div>




```python
unirank.to_csv(r'C:\Users\user\Downloads\uniranksum1.csv')
```
