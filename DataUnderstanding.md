# DATA UNDERSTANDING

Firstly, we will use the dataframe found with the course material, data collision in Seattle City


```python
import pandas as pd 
df=pd.read_csv('Data-Collisions.csv',index_col=0)
df
```

    C:\Users\dell\anaconda3\lib\site-packages\IPython\core\interactiveshell.py:3063: DtypeWarning: Columns (33) have mixed types.Specify dtype option on import or set low_memory=False.
      interactivity=interactivity, compiler=compiler, result=result)
    




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
      <th>X</th>
      <th>Y</th>
      <th>OBJECTID</th>
      <th>INCKEY</th>
      <th>COLDETKEY</th>
      <th>REPORTNO</th>
      <th>STATUS</th>
      <th>ADDRTYPE</th>
      <th>INTKEY</th>
      <th>LOCATION</th>
      <th>...</th>
      <th>ROADCOND</th>
      <th>LIGHTCOND</th>
      <th>PEDROWNOTGRNT</th>
      <th>SDOTCOLNUM</th>
      <th>SPEEDING</th>
      <th>ST_COLCODE</th>
      <th>ST_COLDESC</th>
      <th>SEGLANEKEY</th>
      <th>CROSSWALKKEY</th>
      <th>HITPARKEDCAR</th>
    </tr>
    <tr>
      <th>SEVERITYCODE</th>
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
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>-122.323148</td>
      <td>47.703140</td>
      <td>1</td>
      <td>1307</td>
      <td>1307</td>
      <td>3502005</td>
      <td>Matched</td>
      <td>Intersection</td>
      <td>37475.0</td>
      <td>5TH AVE NE AND NE 103RD ST</td>
      <td>...</td>
      <td>Wet</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10</td>
      <td>Entering at angle</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-122.347294</td>
      <td>47.647172</td>
      <td>2</td>
      <td>52200</td>
      <td>52200</td>
      <td>2607959</td>
      <td>Matched</td>
      <td>Block</td>
      <td>NaN</td>
      <td>AURORA BR BETWEEN RAYE ST AND BRIDGE WAY N</td>
      <td>...</td>
      <td>Wet</td>
      <td>Dark - Street Lights On</td>
      <td>NaN</td>
      <td>6354039.0</td>
      <td>NaN</td>
      <td>11</td>
      <td>From same direction - both going straight - bo...</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-122.334540</td>
      <td>47.607871</td>
      <td>3</td>
      <td>26700</td>
      <td>26700</td>
      <td>1482393</td>
      <td>Matched</td>
      <td>Block</td>
      <td>NaN</td>
      <td>4TH AVE BETWEEN SENECA ST AND UNIVERSITY ST</td>
      <td>...</td>
      <td>Dry</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>4323031.0</td>
      <td>NaN</td>
      <td>32</td>
      <td>One parked--one moving</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-122.334803</td>
      <td>47.604803</td>
      <td>4</td>
      <td>1144</td>
      <td>1144</td>
      <td>3503937</td>
      <td>Matched</td>
      <td>Block</td>
      <td>NaN</td>
      <td>2ND AVE BETWEEN MARION ST AND MADISON ST</td>
      <td>...</td>
      <td>Dry</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>23</td>
      <td>From same direction - all others</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-122.306426</td>
      <td>47.545739</td>
      <td>5</td>
      <td>17700</td>
      <td>17700</td>
      <td>1807429</td>
      <td>Matched</td>
      <td>Intersection</td>
      <td>34387.0</td>
      <td>SWIFT AVE S AND SWIFT AV OFF RP</td>
      <td>...</td>
      <td>Wet</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>4028032.0</td>
      <td>NaN</td>
      <td>10</td>
      <td>Entering at angle</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
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
      <td>...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-122.290826</td>
      <td>47.565408</td>
      <td>219543</td>
      <td>309534</td>
      <td>310814</td>
      <td>E871089</td>
      <td>Matched</td>
      <td>Block</td>
      <td>NaN</td>
      <td>34TH AVE S BETWEEN S DAKOTA ST AND S GENESEE ST</td>
      <td>...</td>
      <td>Dry</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>24</td>
      <td>From opposite direction - both moving - head-on</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-122.344526</td>
      <td>47.690924</td>
      <td>219544</td>
      <td>309085</td>
      <td>310365</td>
      <td>E876731</td>
      <td>Matched</td>
      <td>Block</td>
      <td>NaN</td>
      <td>AURORA AVE N BETWEEN N 85TH ST AND N 86TH ST</td>
      <td>...</td>
      <td>Wet</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>13</td>
      <td>From same direction - both going straight - bo...</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-122.306689</td>
      <td>47.683047</td>
      <td>219545</td>
      <td>311280</td>
      <td>312640</td>
      <td>3809984</td>
      <td>Matched</td>
      <td>Intersection</td>
      <td>24760.0</td>
      <td>20TH AVE NE AND NE 75TH ST</td>
      <td>...</td>
      <td>Dry</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>28</td>
      <td>From opposite direction - one left turn - one ...</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-122.355317</td>
      <td>47.678734</td>
      <td>219546</td>
      <td>309514</td>
      <td>310794</td>
      <td>3810083</td>
      <td>Matched</td>
      <td>Intersection</td>
      <td>24349.0</td>
      <td>GREENWOOD AVE N AND N 68TH ST</td>
      <td>...</td>
      <td>Dry</td>
      <td>Dusk</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5</td>
      <td>Vehicle Strikes Pedalcyclist</td>
      <td>4308</td>
      <td>0</td>
      <td>N</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-122.289360</td>
      <td>47.611017</td>
      <td>219547</td>
      <td>308220</td>
      <td>309500</td>
      <td>E868008</td>
      <td>Matched</td>
      <td>Block</td>
      <td>NaN</td>
      <td>34TH AVE BETWEEN E MARION ST AND E SPRING ST</td>
      <td>...</td>
      <td>Wet</td>
      <td>Daylight</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>14</td>
      <td>From same direction - both going straight - on...</td>
      <td>0</td>
      <td>0</td>
      <td>N</td>
    </tr>
  </tbody>
</table>
<p>194673 rows × 37 columns</p>
</div>



Our target will be the severity code, it takes two values 1 or 2, it's the measure of the severity of an accident.


```python
df["SEVERITYCODE.1"].value_counts(dropna=False)
```




    1    136485
    2     58188
    Name: SEVERITYCODE.1, dtype: int64



Let's see what these values refers to


```python
df["SEVERITYDESC"].value_counts(dropna=False)
```




    Property Damage Only Collision    136485
    Injury Collision                   58188
    Name: SEVERITYDESC, dtype: int64



The data frame is an original one, so we have to extract our dataset. To doing so, there are many columns that we won't use. 
Besides the severity code we will keep WEATHER, which describes the weather at the time of crash, ROADCOND, which describes the condition of the road at the time of crash, LIGHTCOND, which describes the light conditions at the time of crash.


```python
df_new=df[["WEATHER","ROADCOND","LIGHTCOND"]]
df_new
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
      <th>WEATHER</th>
      <th>ROADCOND</th>
      <th>LIGHTCOND</th>
    </tr>
    <tr>
      <th>SEVERITYCODE</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>Overcast</td>
      <td>Wet</td>
      <td>Daylight</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Raining</td>
      <td>Wet</td>
      <td>Dark - Street Lights On</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Overcast</td>
      <td>Dry</td>
      <td>Daylight</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Clear</td>
      <td>Dry</td>
      <td>Daylight</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Raining</td>
      <td>Wet</td>
      <td>Daylight</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Clear</td>
      <td>Dry</td>
      <td>Daylight</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Raining</td>
      <td>Wet</td>
      <td>Daylight</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Clear</td>
      <td>Dry</td>
      <td>Daylight</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Clear</td>
      <td>Dry</td>
      <td>Dusk</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Clear</td>
      <td>Wet</td>
      <td>Daylight</td>
    </tr>
  </tbody>
</table>
<p>194673 rows × 3 columns</p>
</div>



Since the features ROADCOND and LIGHTOND are categorical variables, we have to transform them into values or numerical variables when we have to start building our model of ML.


```python

```
