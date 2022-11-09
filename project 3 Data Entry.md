```python
import pandas as pd 

weather_data = {
    'day': ['1/1/2017','1/2/2017','1/3/2017','1/4/2017','1/5/2017','1/6/2017'],
    'temperature': [32,35,28,24,32,31],
    'windspeed': [6,7,2,7,4,2],
    'event': ['Rain', 'Sunny', 'Snow','Snow','Sunny', 'Sunny']
}
df = pd.DataFrame(weather_data)
df 
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
      <th>day</th>
      <th>temperature</th>
      <th>windspeed</th>
      <th>event</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1/1/2017</td>
      <td>32</td>
      <td>6</td>
      <td>Rain</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1/2/2017</td>
      <td>35</td>
      <td>7</td>
      <td>Sunny</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1/3/2017</td>
      <td>28</td>
      <td>2</td>
      <td>Snow</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1/4/2017</td>
      <td>24</td>
      <td>7</td>
      <td>Snow</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1/5/2017</td>
      <td>32</td>
      <td>4</td>
      <td>Sunny</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1/6/2017</td>
      <td>31</td>
      <td>2</td>
      <td>Sunny</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.describe()
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
      <th>temperature</th>
      <th>windspeed</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>6.000000</td>
      <td>6.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>30.333333</td>
      <td>4.666667</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.829708</td>
      <td>2.338090</td>
    </tr>
    <tr>
      <th>min</th>
      <td>24.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>28.750000</td>
      <td>2.500000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>31.500000</td>
      <td>5.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>32.000000</td>
      <td>6.750000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>35.000000</td>
      <td>7.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.shape
```




    (6, 4)




```python
newdf = df[2:5]
newdf
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
      <th>day</th>
      <th>temperature</th>
      <th>windspeed</th>
      <th>event</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>1/3/2017</td>
      <td>28</td>
      <td>2</td>
      <td>Snow</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1/4/2017</td>
      <td>24</td>
      <td>7</td>
      <td>Snow</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1/5/2017</td>
      <td>32</td>
      <td>4</td>
      <td>Sunny</td>
    </tr>
  </tbody>
</table>
</div>




```python
newdf = df.iloc[2:5 , :-1]
newdf
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
      <th>day</th>
      <th>temperature</th>
      <th>windspeed</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>1/3/2017</td>
      <td>28</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1/4/2017</td>
      <td>24</td>
      <td>7</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1/5/2017</td>
      <td>32</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.head(2)

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
      <th>day</th>
      <th>temperature</th>
      <th>windspeed</th>
      <th>event</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1/1/2017</td>
      <td>32</td>
      <td>6</td>
      <td>Rain</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1/2/2017</td>
      <td>35</td>
      <td>7</td>
      <td>Sunny</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.tail(2)
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
      <th>day</th>
      <th>temperature</th>
      <th>windspeed</th>
      <th>event</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>1/5/2017</td>
      <td>32</td>
      <td>4</td>
      <td>Sunny</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1/6/2017</td>
      <td>31</td>
      <td>2</td>
      <td>Sunny</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.event
```




    0     Rain
    1    Sunny
    2     Snow
    3     Snow
    4    Sunny
    5    Sunny
    Name: event, dtype: object




```python
df.day
```




    0    1/1/2017
    1    1/2/2017
    2    1/3/2017
    3    1/4/2017
    4    1/5/2017
    5    1/6/2017
    Name: day, dtype: object




```python
df.temperature
```




    0    32
    1    35
    2    28
    3    24
    4    32
    5    31
    Name: temperature, dtype: int64




```python
df.windspeed
```




    0    6
    1    7
    2    2
    3    7
    4    4
    5    2
    Name: windspeed, dtype: int64




```python
discipline = df[["day","event"]]
discipline
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
      <th>day</th>
      <th>event</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1/1/2017</td>
      <td>Rain</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1/2/2017</td>
      <td>Sunny</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1/3/2017</td>
      <td>Snow</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1/4/2017</td>
      <td>Snow</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1/5/2017</td>
      <td>Sunny</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1/6/2017</td>
      <td>Sunny</td>
    </tr>
  </tbody>
</table>
</div>




```python
print(df.temperature.mean())
print(df.temperature.median())
print(df.temperature.memory_usage())
print(df.temperature.std())
print(df.temperature.max())
print(df.temperature.min())
```

    30.333333333333332
    31.5
    176
    3.8297084310253524
    35
    24
    


```python
len(df["windspeed"])
```




    6




```python
len(df[ df['temperature'] < 30 ])
```




    2




```python
df.count()
```




    day            6
    temperature    6
    windspeed      6
    event          6
    dtype: int64




```python
import pandas as pd 

columns = []
data = dict()

num = int(input("please enter the number of columns"))
while(num > 0):
    columns.append(input("please enter the column name: "))
    num -=1

for i in columns:
    data[i] = []

rows = int(input("please enter the number of rows: "))
while(rows > 0):
    for i in data:
        value = input(f"please enter the value of {i}: ")
        data[i].append(value)

    rows-=1
dataframe = pd.DataFrame(data)
dataframe
```

    please enter the number of columns10
    please enter the column name: A
    please enter the column name: B
    please enter the column name: C
    please enter the column name: D
    please enter the column name: E
    please enter the column name: F
    please enter the column name: G
    please enter the column name: H
    please enter the column name: I
    please enter the column name: J
    please enter the number of rows: 10
    please enter the value of A: 1
    please enter the value of B: 2
    please enter the value of C: 3
    please enter the value of D: 4
    please enter the value of E: 5
    please enter the value of F: 6
    please enter the value of G: 7
    please enter the value of H: 8
    please enter the value of I: 9
    please enter the value of J: 10
    please enter the value of A: A1
    please enter the value of B: B2
    please enter the value of C: C3
    please enter the value of D: D4
    please enter the value of E: E5
    please enter the value of F: F6
    please enter the value of G: G7
    please enter the value of H: H8
    please enter the value of I: I9
    please enter the value of J: J10
    please enter the value of A: 10
    please enter the value of B: 20
    please enter the value of C: 30
    please enter the value of D: 40
    please enter the value of E: 50
    please enter the value of F: 60
    please enter the value of G: 70
    please enter the value of H: 80
    please enter the value of I: 90
    please enter the value of J: 100
    please enter the value of A: -10
    please enter the value of B: -20
    please enter the value of C: -30
    please enter the value of D: -40
    please enter the value of E: -50
    please enter the value of F: -60
    please enter the value of G: -70
    please enter the value of H: -80
    please enter the value of I: -90
    please enter the value of J: -100
    please enter the value of A: AA
    please enter the value of B: AB
    please enter the value of C: AC
    please enter the value of D: AD
    please enter the value of E: AE
    please enter the value of F: AF
    please enter the value of G: AG
    please enter the value of H: AH
    please enter the value of I: AI
    please enter the value of J: AJ
    please enter the value of A: BB
    please enter the value of B: BA
    please enter the value of C: BC
    please enter the value of D: BD
    please enter the value of E: BE
    please enter the value of F: BF
    please enter the value of G: BG
    please enter the value of H: BI
    please enter the value of I: BH
    please enter the value of J: BJ
    please enter the value of A: CA
    please enter the value of B: CB
    please enter the value of C: CC
    please enter the value of D: CD
    please enter the value of E: CE
    please enter the value of F: CF
    please enter the value of G: CG
    please enter the value of H: CH
    please enter the value of I: CI
    please enter the value of J: CJ
    please enter the value of A: DA
    please enter the value of B: DB
    please enter the value of C: DC
    please enter the value of D: DD
    please enter the value of E: DE
    please enter the value of F: DF
    please enter the value of G: DG
    please enter the value of H: DH
    please enter the value of I: DI
    please enter the value of J: DJ
    please enter the value of A: EA
    please enter the value of B: EB
    please enter the value of C: EC
    please enter the value of D: ED
    please enter the value of E: EF
    please enter the value of F: EE
    please enter the value of G: EG
    please enter the value of H: EH
    please enter the value of I: EI
    please enter the value of J: EJ
    please enter the value of A: FA
    please enter the value of B: FB
    please enter the value of C: FC
    please enter the value of D: FD
    please enter the value of E: FE
    please enter the value of F: FF
    please enter the value of G: FG
    please enter the value of H: FH
    please enter the value of I: FI
    please enter the value of J: FJ
    




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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
      <th>F</th>
      <th>G</th>
      <th>H</th>
      <th>I</th>
      <th>J</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>8</td>
      <td>9</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B2</td>
      <td>C3</td>
      <td>D4</td>
      <td>E5</td>
      <td>F6</td>
      <td>G7</td>
      <td>H8</td>
      <td>I9</td>
      <td>J10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>10</td>
      <td>20</td>
      <td>30</td>
      <td>40</td>
      <td>50</td>
      <td>60</td>
      <td>70</td>
      <td>80</td>
      <td>90</td>
      <td>100</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-10</td>
      <td>-20</td>
      <td>-30</td>
      <td>-40</td>
      <td>-50</td>
      <td>-60</td>
      <td>-70</td>
      <td>-80</td>
      <td>-90</td>
      <td>-100</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AA</td>
      <td>AB</td>
      <td>AC</td>
      <td>AD</td>
      <td>AE</td>
      <td>AF</td>
      <td>AG</td>
      <td>AH</td>
      <td>AI</td>
      <td>AJ</td>
    </tr>
    <tr>
      <th>5</th>
      <td>BB</td>
      <td>BA</td>
      <td>BC</td>
      <td>BD</td>
      <td>BE</td>
      <td>BF</td>
      <td>BG</td>
      <td>BI</td>
      <td>BH</td>
      <td>BJ</td>
    </tr>
    <tr>
      <th>6</th>
      <td>CA</td>
      <td>CB</td>
      <td>CC</td>
      <td>CD</td>
      <td>CE</td>
      <td>CF</td>
      <td>CG</td>
      <td>CH</td>
      <td>CI</td>
      <td>CJ</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DA</td>
      <td>DB</td>
      <td>DC</td>
      <td>DD</td>
      <td>DE</td>
      <td>DF</td>
      <td>DG</td>
      <td>DH</td>
      <td>DI</td>
      <td>DJ</td>
    </tr>
    <tr>
      <th>8</th>
      <td>EA</td>
      <td>EB</td>
      <td>EC</td>
      <td>ED</td>
      <td>EF</td>
      <td>EE</td>
      <td>EG</td>
      <td>EH</td>
      <td>EI</td>
      <td>EJ</td>
    </tr>
    <tr>
      <th>9</th>
      <td>FA</td>
      <td>FB</td>
      <td>FC</td>
      <td>FD</td>
      <td>FE</td>
      <td>FF</td>
      <td>FG</td>
      <td>FH</td>
      <td>FI</td>
      <td>FJ</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
