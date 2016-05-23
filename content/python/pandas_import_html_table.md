Title: Importing an HTML table into pandas
Slug: pandas_import_html_table
Summary: Importing an HTML table into pandas
Date: 2016-05-01 12:00
Category: Data Wrangling
Tags: Basics
Authors: Chris Albon




```python
# Import the required module
import pandas as pd
```


```python
# Create a variable with the url to the website contain the html table
url = "http://floodobservatory.colorado.edu/Archives/MasterListrev.htm"
```


```python
# Read the html table into pandas
data = pd.read_html(url, header=0)
```

The resulting data will be a list of dataframe objects


```python
# View the data
data
```




    [    Register  #  Annual DFO #  (discontinued)             Glide #  \
     0          4163                           NaN                   0   
     1          4162                           NaN                   0   
     2          4161                           NaN                   0   
     3          4160                           NaN                   0   
     4          4159                           NaN                   0   
     5          4158                           NaN                   0   
     6          4157                           NaN                   0   
     7          4156                           NaN                   0   
     8          4155                           NaN                   0   
     9          4154                           NaN                   0   
     10         4153                           NaN                   0   
     11         4152                           NaN                   0   
     12         4151                           NaN                   0   
     13         4150                           NaN                   0   
     14         4149                           NaN                   0   
     15         4148                           NaN  TC-2014-000071-MEX   
     16         4147                           NaN                   0   
     17         4146                           NaN                   0   
     18         4145                           NaN  FL-2014-000070-LKA   
     19         4144                           NaN                   0   
     20         4143                           NaN  FL-2014-000062-CHN   
     21         4142                           NaN  FL-2014-000063-TJK   
     22         4141                           NaN                   0   
     23         4140                           NaN                   0   
     24         4139                           NaN                   0   
     25         4138                           NaN  FF-2014-000059-SRB   
     26         4137                           NaN                   0   
     27         4136                           NaN  FF-2014-000060-AFG   
     28         4135                           NaN                   0   
     29         4134                           NaN                   0   
     30         4133                           NaN                   0   
     31         4132                           NaN  FL-2014-000045-SLB   
     32         4131                           NaN  FL-2014-000038-ZAF   
     33         4130                           NaN                   0   
     34         4129                           NaN                   0   
     35         4128                           NaN                   0   
     36         4127                           NaN  FL-2014-000030-PRY   
     37         4126                           NaN                   0   
     38         4125                           NaN                   0   
     39         4124                           NaN  SS-2014-000032-MHL   
     40         4123                           NaN                   0   
     41         4122                           NaN                   0   
     42         4121                           NaN                   0   
     43         4120                           NaN                   0   
     44         4119                           NaN                   0   
     45         4118                           NaN                   0   
     46         4117                           NaN  FL-2014-000008-BOL   
     47         4116                           NaN                   0   
     48         4115                           NaN                   0   
     49         4114                           NaN  FL-2013-000159-LCA   
     50         4113                           NaN  FL-2013-000157-BRA   
     51         4112                           NaN                   0   
     52         4111                           NaN                   0   
     53         4110                           NaN  FL-2013-000149-THA   
     54         4109                           NaN                   0   
     55         4108                           NaN                   0   
     56         4107                           NaN  FL-2013-000148-MYS   
     57         4106                           NaN                   0   
     58         4105                           NaN  FL-2013-000141-SOM   
     59         4104                           NaN                   0   
                 ...                           ...                 ...   
     
                 Country      Other  Nations  Affected  \
     0            Brazil    Uruguay      NaN       NaN   
     1             Nepal          0      NaN       NaN   
     2        Bangladesh          0      NaN       NaN   
     3               USA          0      NaN       NaN   
     4            Brazil          0      NaN       NaN   
     5             Sudan          0      NaN       NaN   
     6       New Zealand          0      NaN       NaN   
     7          Thailand          0      NaN       NaN   
     8             China          0      NaN       NaN   
     9             India          0      NaN       NaN   
     10      Philippines          0      NaN       NaN   
     11              USA          0      NaN       NaN   
     12         Bulgaria          0      NaN       NaN   
     13         Paraguay     Brazil      NaN       NaN   
     14           Russia          0      NaN       NaN   
     15           Mexico  Guatamala      NaN       NaN   
     16             Iran          0      NaN       NaN   
     17            China          0      NaN       NaN   
     18        Sri Lanka          0      NaN       NaN   
     19      Afghanistan          0      NaN       NaN   
     20            China          0      NaN       NaN   
     21       Tajikistan          0      NaN       NaN   
     22            Italy          0      NaN       NaN   
     23         Tanzania          0      NaN       NaN   
     24           Serbia     Bosnia      NaN       NaN   
     25          Romania   Bulgaria      NaN       NaN   
     26         Tanzania          0      NaN       NaN   
     27      Afghanistan          0      NaN       NaN   
     28              USA          0      NaN       NaN   
     29              USA          0      NaN       NaN   
     30        Argentina          0      NaN       NaN   
     31  Solomon Islands          0      NaN       NaN   
     32     South Africa    Namibia      NaN       NaN   
     33        Australia          0      NaN       NaN   
     34              USA          0      NaN       NaN   
     35          Zimbawe          0      NaN       NaN   
     36         Paraguay          0      NaN       NaN   
     37          Burundi          0      NaN       NaN   
     38      New Zealand          0      NaN       NaN   
     39              USA          0      NaN       NaN   
     40       Mozambique          0      NaN       NaN   
     41           France      Italy      NaN       NaN   
     42        Indonesia          0      NaN       NaN   
     43        Australia          0      NaN       NaN   
     44          Zimbawe          0      NaN       NaN   
     45          Zimbawe          0      NaN       NaN   
     46          Bolivia          0      NaN       NaN   
     47             Peru          0      NaN       NaN   
     48              USA          0      NaN       NaN   
     49    Saint Vincent  St. Lucia      NaN       NaN   
     50           Brazil          0      NaN       NaN   
     51        Indonesia          0      NaN       NaN   
     52   United Kingdom    Ireland      NaN       NaN   
     53         Thailand          0      NaN       NaN   
     54             Cuba          0      NaN       NaN   
     55            Niger          0      NaN       NaN   
     56         Malaysia          0      NaN       NaN   
     57   United Kingdom    Germany      NaN       NaN   
     58          Somalia          0      NaN       NaN   
     59     Saudi Arabia          0      NaN       NaN   
                     ...        ...      ...       ...   
     
        Detailed  Locations (click on active links to access inundation extents)  \
     0           State of Rio Grande do Sul; Uruguay River                         
     1   Sindhupalchok, Lalitpur and Chitwan districts ...                         
     2   Bhola District in the Division of Barisal, Ban...                         
     3          Mendenhall Lake and  River, Juneau, Alaska                         
     4   Amazonas State; Northwestern Brazil; Careiro d...                         
     5   Sinja locality in the eastern Sudan state of S...                         
     6   North Island, Hikurangi Swamp area, north of W...                         
     7                      Rayong, Chiang Rai, and  Trang                         
     8   Southern China; Hunan,  Jiangxi provinces; Gua...                         
     9                                               Assam                         
     10        Southern Philippine province of Maguindanao                         
     11  South Dakota, Iowa, Illinois, Missouri, Minnesota                         
     12  Eastern Bulgaria; Varna district of Asparuhov;...                         
     13  Southern Brazil, Parana State; Paraguay River ...                         
     14  Altai region, Khakassia  Republic, and Altai R...                         
     15                     Chiapas, SE Mexico.W Guatamala                         
     16          Khorasan, Mazandaran and Semnan provinces                         
     17                 Southern China, Guangdong Province                         
     18                     Western districts of Sri Lanka                         
     19                                    Baghlan provinc                         
     20  Hunan Province, including Guiyang, Shenzhen ci...                         
     21  Khatlon Province, Rudaki and Vahdat districts,...                         
     22                     Marche region of central Italy                         
     23                    Rufiji District in Coast Region                         
     24                             Bosnia,Serbia, Croatia                         
     25                 Bulgaria, Serbia, southern Romania                         
     26                               Dar es Salaam region                         
     27  Northwestern Afghanistan; Jowzjan Province, pr...                         
     28               Gulf Coast; Northeast Atlantic Coast                         
     29             Southern Alabama, southern Mississippi                         
     30                       Western province of Neuquenr                         
     31                                            Honiara                         
     32                         SADC region, Zambezi River                         
     33  Southeast and Central Queensland; Yeppoon area...                         
     34             Southern Mississippi, Wilkinson County                         
     35                                       Tokwe-Mukosi                         
     36   Luque, Mariano Roque Alonso, Lambaré, and Limpio                         
     37                                          Bujumbura                         
     38                 Christchurch, including Avon River                         
     39                                             Majuro                         
     40  Johannesburg , Kliptown, Soweto; eastern South...                         
     41  Southeastern France, western France, Pisa, Lig...                         
     42                                 Jakarta, Tangerang                         
     43                        Top End, Northern Territory                         
     44  Communities downstream of the Tokwe-Mukrosi Da...                         
     45                                         Muzarabani                         
     46  La Paz, Beni, Santa Cruz  and Cochabamba; Beni...                         
     47                       Southern Andean Cusco region                         
     48              Nelson and Carroll Counties, Kentucky                         
     49        Saint Vincent and the Grenadines, St. Lucia                         
     50  Southeast states of Minas Gerais and Espirito ...                         
     51                    North Sumatras Langkat district                         
     52  Central and southern Scotland, Wales, Ireland,...                         
     53  Southeast provinces; Nakhon Si Thammarat, Song...                         
     54                                             Havana                         
     55                 South-east Niger, Komadougou River                         
     56  Kuala Lumpur, east coast states of Pahang and ...                         
     57     Eastern England coast, northern European coast                         
     58                                 Northeast Puntland                         
     59  Riyadh, other parts of the Kingdom including n...                         
                                                       ...                         
     
        Validation  (post event #3503)      Began      Ended  Duration in  Days  \
     0                            News 2014-07-03 2014-07-14                 12   
     1                            News 2014-07-01 2014-07-14                 14   
     2                            News 2014-07-13 2014-07-14                  2   
     3                            News 2014-07-11 2014-07-14                  4   
     4                            News 2014-05-22 2014-07-14                 54   
     5                            News 2014-07-07 2014-07-14                  8   
     6                            News 2014-07-05 2014-07-14                 10   
     7                            News 2014-07-11 2014-07-14                  4   
     8                            News 2014-06-05 2014-06-25                 21   
     9                            News 2014-06-23 2014-06-25                  3   
     10                           News 2014-06-17 2014-06-25                  9   
     11                           News 2014-06-10 2014-07-14                 35   
     12                           News 2014-06-19 2014-06-25                  7   
     13                           News 2014-06-03 2014-07-14                 42   
     14                           News 2014-06-04 2014-06-10                  7   
     15                           News 2014-06-01 2014-06-10                 10   
     16                           News 2014-06-01 2014-06-10                 10   
     17                           News 2014-05-30 2014-06-10                 12   
     18                           News 2014-06-04 2014-06-10                  7   
     19                           News 2014-06-03 2014-06-10                  8   
     20                           News 2014-05-12 2014-05-16                  5   
     21                           News 2014-05-10 2014-05-16                  7   
     22                           News 2014-05-02 2014-05-10                  9   
     23                           News 2014-05-10 2014-05-16                  7   
     24                           News 2014-05-12 2014-05-16                  5   
     25                           News 2014-04-17 2014-05-01                 15   
     26                           News 2014-04-18 2014-05-01                 14   
     27                           News 2014-04-20 2014-05-16                 27   
     28                           News 2014-04-30 2014-05-01                  2   
     29                           News 2014-04-01 2014-04-08                  8   
     30                           News 2014-04-01 2014-04-08                  8   
     31                           News 2014-04-01 2014-04-08                  8   
     32                           News 2014-03-01 2014-03-30                 30   
     33                           News 2014-03-24 2014-03-30                  7   
     34                           News 2014-03-25 2014-03-30                  6   
     35                           News 2014-02-01 2014-03-30                 58   
     36                           News 2014-02-25 2014-03-10                 14   
     37                           News 2014-02-19 2014-03-10                 20   
     38                           News 2014-03-03 2014-03-10                  8   
     39                           News 2014-03-03 2014-03-10                  8   
     40                           News 2014-02-24 2014-03-10                 15   
     41                           News 2014-01-20 2014-02-07                 19   
     42                           News 2014-01-08 2014-02-07                 31   
     43                           News 2014-02-02 2014-02-07                  6   
     44                           News 2014-01-15 2014-02-07                 24   
     45                           News 2014-01-15 2014-02-07                 24   
     46                           News 2014-01-10 2014-05-01                112   
     47                           News 2014-01-01 2014-01-04                  4   
     48                           News 2013-12-22 2014-01-04                 14   
     49                           News 2013-12-26 2014-01-04                 10   
     50                           News 2013-12-23 2014-01-04                 13   
     51                           News 2013-12-29 2014-01-04                  7   
     52                           News 2013-12-27 2014-02-07                 43   
     53                           News 2013-11-20 2013-12-08                 19   
     54                           News 2013-12-01 2013-12-08                  8   
     55                           News 2013-11-03 2013-12-08                 36   
     56                           News 2013-12-01 2013-12-08                  8   
     57                           News 2013-12-05 2013-12-08                  4   
     58                           News 2013-11-08 2013-11-19                 12   
     59                           News 2013-11-18 2013-11-19                  2   
                                   ...        ...        ...                ...   
     
         Dead  Displaced  Damage (USD)                 Main cause  Severity *  \
     0     10      50000           NaN                 Heavy Rain         2.0   
     1     16       2400           NaN            Torrential Rain         1.5   
     2      0      30000           NaN  Heavy Rain and  High Tide         1.5   
     3      0          0           NaN                 Jökulhlaup         1.0   
     4      0          0           NaN                 Heavy Rain         2.0   
     5      0      42400           NaN                 Heavy Rain         1.5   
     6      0          0           NaN                 Heavy Rain         1.0   
     7      0        500           NaN                 Heavy Rain         1.0   
     8     14     337000           NaN             Monsoonal Rain         1.0   
     9      0      10000           NaN              Monsoonal Ran         1.0   
     10     0      35000           NaN                 Heavy Rain         1.0   
     11     0        600           NaN                 Heavy Rain         2.0   
     12    12       2000           NaN            Torrential Rain         2.0   
     13     9     265000           NaN                  Heay Rain         2.0   
     14    70       3000           NaN            Torrential Rain         1.5   
     15    22      25000           NaN             Monsoonal Rain         1.5   
     16    37     440000           NaN             Monsoonal Rain         1.5   
     17     6        500           NaN                 Heavy Rain         1.0   
     18     5      16000           NaN      Tropical Storm  Boris         1.5   
     19     0        300           NaN                 Heavy Rain         1.5   
     20     1      10000           NaN                 Heavy Rain         2.0   
     21     0        425           NaN                 Heavy Rain         1.5   
     22     2        250           NaN            Torrential Rain         1.5   
     23     0      22000           NaN                 Heavy Rain         1.0   
     24     3       4000           NaN                 Heavy Rain         2.0   
     25     0        640           NaN            Torrential Rain         1.5   
     26    41          0           NaN            Torrential Rain         1.5   
     27   123       6000           NaN            Torrential Rain         1.5   
     28     1        200           NaN            Torrential Rain         2.0   
     29     2        300           NaN                 heavy Rain         1.5   
     30     0       2000           NaN                 Heavy Rain         1.5   
     31    23      10000           NaN                 Heavy Rain         2.0   
     32    37       3528           NaN                 Heavy Rain         1.5   
     33     1          0           NaN            Torrential Rain         1.5   
     34     0        200           NaN                 Heavy Rain         1.5   
     35     0       4000           NaN                  Dam Break         1.0   
     36     0       2000           NaN                 Heavy Rain         1.0   
     37    69      20000           NaN            Torrential Rain         2.0   
     38     0         80           NaN                 Heavy Rain         2.0   
     39     0        900           NaN                Storm Surge         1.5   
     40     4      20000           NaN                 Heavy Rain         1.0   
     41     4       1000           NaN                 Heavy Rain         1.5   
     42    23      20000           NaN                 Heavy Rain         1.5   
     43     0          0           NaN   Tropical Storm  Fletcher         1.0   
     44     0       4000           NaN                 Heavy Rain         1.5   
     45     0          0           NaN                 Heavy Rain         1.5   
     46    60      84000           NaN                 Heavy Rain         2.0   
     47     0        300           NaN                 Heavy Rain         1.0   
     48     5          0           NaN                 Heavy Rain         1.0   
     49    11          0           NaN                 Heavy Rain         1.0   
     50    45      60000           NaN                 Heavy Rain         2.0   
     51     0       4500           NaN                 Heavy Rain         1.0   
     52     0        200           NaN                 Heavy Rain         1.5   
     53    23      15254           NaN             Monsoonal Rain         1.5   
     54     2        227           NaN            Torrential Rain         1.0   
     55     0       1000           NaN                 Heavy Rain         1.0   
     56     1      19000           NaN             Monsoonal Rain         1.5   
     57     8       4000           NaN                Storm Surge         2.0   
     58   100          0           NaN             Tropical Storm         1.5   
     59    15        121           NaN            Torrential Rain         1.5   
          ...        ...           ...                        ...         ...   
     
         Affected sq  km  Magnitude  (M)**  Centroid X      
     0        44866.4600               6.0   -58.02560 ...  
     1        11578.7700               5.4    84.62070 ...  
     2          217.5290               2.8    90.54980 ...  
     3         2950.8200               4.1  -134.44600 ...  
     4       256564.5700               7.4   -59.55970 ...  
     5       137141.2800               6.2    33.08000 ...  
     6         8581.2400               4.9   174.06800 ...  
     7        15921.6300               4.8    99.73900 ...  
     8       377101.6300               6.9   112.35800 ...  
     9        49220.5300               5.2    94.71600 ...  
     10       15356.3100               5.1   124.73000 ...  
     11      418317.1300               7.5   -94.79440 ...  
     12       24415.4200               5.5    27.04260 ...  
     13      554605.2500               7.7   -53.54700 ...  
     14     1829701.4000               7.3    94.36960 ...  
     15      113685.4300               6.2   -94.02740 ...  
     16      305525.2500               6.7    57.25440 ...  
     17       45994.3000               5.7   113.34200 ...  
     18       10337.4700               5.0    80.16680 ...  
     19       44203.9300               5.7    68.01780 ...  
     20      205001.2700               6.3   111.46700 ...  
     21       41719.4600               5.6    69.37870 ...  
     22       11256.3300               5.2    13.01300 ...  
     23       22249.3400               5.2    38.94420 ...  
     24      115747.6900               6.1    19.22360 ...  
     25       87430.6900               6.3    24.49400 ...  
     26       18498.3900               5.6    38.96890 ...  
     27       83722.3400               6.5    66.43420 ...  
     28      260469.8100               6.0   -84.94650 ...  
     29       82418.5600               6.0   -87.61880 ...  
     30       69876.7800               5.9   -70.29840 ...  
     31        5480.7500               4.9   160.34200 ...  
     32     1037639.2000               7.7    25.60740 ...  
     33      250162.1200               6.4   150.11700 ...  
     34       53220.7900               5.7   -89.12820 ...  
     35       17205.6400               6.0    31.34790 ...  
     36        6829.5700               5.0   -57.58330 ...  
     37        3237.4200               5.1    29.64990 ...  
     38        1015.8400               4.2   172.61300 ...  
     39          34.8366               2.6   168.72900 ...  
     40      481907.8800               6.9    31.54590 ...  
     41       82989.4500               6.4     7.09930 ...  
     42       35769.2200               6.2   107.70600 ...  
     43      426979.8400               6.4   131.73200 ...  
     44       72462.2300               6.4    28.92310 ...  
     45      142586.1000               6.7    30.85310 ...  
     46      381576.6500               7.9   -64.01350 ...  
     47       74144.6600               5.5   -71.52320 ...  
     48       16069.9100               5.4   -86.78990 ...  
     49         830.2320               3.9   -60.98860 ...  
     50      314284.9100               6.9   -41.94230 ...  
     51       22524.6300               5.2    97.28930 ...  
     52      126149.7900               6.9    -1.51144 ...  
     53       38676.7100               6.0   100.39500 ...  
     54        7627.3000               4.8   -81.39580 ...  
     55       65791.1400               6.4    13.20170 ...  
     56      106697.5300               6.1   102.36200 ...  
     57       51279.6000               5.6     7.53306 ...  
     58      181848.0200               6.5    57.42760 ...  
     59      361386.8400               6.0    44.80840 ...  
                     ...               ...         ...      
     
     [276 rows x 29 columns]]




```python
# Select the first (and in this case only) dataframe object
data[0]
```




<div style="max-height:1000px;max-width:1500px;overflow:auto;">
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Register  #</th>
      <th>Annual DFO #  (discontinued)</th>
      <th>Glide #</th>
      <th>Country</th>
      <th>Other</th>
      <th>Nations</th>
      <th>Affected</th>
      <th>Detailed  Locations (click on active links to access inundation extents)</th>
      <th>Validation  (post event #3503)</th>
      <th>Began</th>
      <th>Ended</th>
      <th>Duration in  Days</th>
      <th>Dead</th>
      <th>Displaced</th>
      <th>Damage (USD)</th>
      <th>Main cause</th>
      <th>Severity *</th>
      <th>Affected sq  km</th>
      <th>Magnitude  (M)**</th>
      <th>Centroid X</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0 </th>
      <td> 4163</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>          Brazil</td>
      <td>   Uruguay</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>         State of Rio Grande do Sul; Uruguay River</td>
      <td> News</td>
      <td>2014-07-03</td>
      <td>2014-07-14</td>
      <td>  12</td>
      <td>  10</td>
      <td>  50000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>   44866.4600</td>
      <td> 6.0</td>
      <td> -58.02560</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1 </th>
      <td> 4162</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>           Nepal</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Sindhupalchok, Lalitpur and Chitwan districts ...</td>
      <td> News</td>
      <td>2014-07-01</td>
      <td>2014-07-14</td>
      <td>  14</td>
      <td>  16</td>
      <td>   2400</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td>   11578.7700</td>
      <td> 5.4</td>
      <td>  84.62070</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2 </th>
      <td> 4161</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>      Bangladesh</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Bhola District in the Division of Barisal, Ban...</td>
      <td> News</td>
      <td>2014-07-13</td>
      <td>2014-07-14</td>
      <td>   2</td>
      <td>   0</td>
      <td>  30000</td>
      <td>NaN</td>
      <td> Heavy Rain and  High Tide</td>
      <td> 1.5</td>
      <td>     217.5290</td>
      <td> 2.8</td>
      <td>  90.54980</td>
      <td>...</td>
    </tr>
    <tr>
      <th>3 </th>
      <td> 4160</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>             USA</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>        Mendenhall Lake and  River, Juneau, Alaska</td>
      <td> News</td>
      <td>2014-07-11</td>
      <td>2014-07-14</td>
      <td>   4</td>
      <td>   0</td>
      <td>      0</td>
      <td>NaN</td>
      <td>                Jökulhlaup</td>
      <td> 1.0</td>
      <td>    2950.8200</td>
      <td> 4.1</td>
      <td>-134.44600</td>
      <td>...</td>
    </tr>
    <tr>
      <th>4 </th>
      <td> 4159</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>          Brazil</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Amazonas State; Northwestern Brazil; Careiro d...</td>
      <td> News</td>
      <td>2014-05-22</td>
      <td>2014-07-14</td>
      <td>  54</td>
      <td>   0</td>
      <td>      0</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>  256564.5700</td>
      <td> 7.4</td>
      <td> -59.55970</td>
      <td>...</td>
    </tr>
    <tr>
      <th>5 </th>
      <td> 4158</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>           Sudan</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Sinja locality in the eastern Sudan state of S...</td>
      <td> News</td>
      <td>2014-07-07</td>
      <td>2014-07-14</td>
      <td>   8</td>
      <td>   0</td>
      <td>  42400</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>  137141.2800</td>
      <td> 6.2</td>
      <td>  33.08000</td>
      <td>...</td>
    </tr>
    <tr>
      <th>6 </th>
      <td> 4157</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>     New Zealand</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> North Island, Hikurangi Swamp area, north of W...</td>
      <td> News</td>
      <td>2014-07-05</td>
      <td>2014-07-14</td>
      <td>  10</td>
      <td>   0</td>
      <td>      0</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>    8581.2400</td>
      <td> 4.9</td>
      <td> 174.06800</td>
      <td>...</td>
    </tr>
    <tr>
      <th>7 </th>
      <td> 4156</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>        Thailand</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                    Rayong, Chiang Rai, and  Trang</td>
      <td> News</td>
      <td>2014-07-11</td>
      <td>2014-07-14</td>
      <td>   4</td>
      <td>   0</td>
      <td>    500</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   15921.6300</td>
      <td> 4.8</td>
      <td>  99.73900</td>
      <td>...</td>
    </tr>
    <tr>
      <th>8 </th>
      <td> 4155</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>           China</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Southern China; Hunan,  Jiangxi provinces; Gua...</td>
      <td> News</td>
      <td>2014-06-05</td>
      <td>2014-06-25</td>
      <td>  21</td>
      <td>  14</td>
      <td> 337000</td>
      <td>NaN</td>
      <td>            Monsoonal Rain</td>
      <td> 1.0</td>
      <td>  377101.6300</td>
      <td> 6.9</td>
      <td> 112.35800</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9 </th>
      <td> 4154</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>           India</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                             Assam</td>
      <td> News</td>
      <td>2014-06-23</td>
      <td>2014-06-25</td>
      <td>   3</td>
      <td>   0</td>
      <td>  10000</td>
      <td>NaN</td>
      <td>             Monsoonal Ran</td>
      <td> 1.0</td>
      <td>   49220.5300</td>
      <td> 5.2</td>
      <td>  94.71600</td>
      <td>...</td>
    </tr>
    <tr>
      <th>10</th>
      <td> 4153</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>     Philippines</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>       Southern Philippine province of Maguindanao</td>
      <td> News</td>
      <td>2014-06-17</td>
      <td>2014-06-25</td>
      <td>   9</td>
      <td>   0</td>
      <td>  35000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   15356.3100</td>
      <td> 5.1</td>
      <td> 124.73000</td>
      <td>...</td>
    </tr>
    <tr>
      <th>11</th>
      <td> 4152</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>             USA</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> South Dakota, Iowa, Illinois, Missouri, Minnesota</td>
      <td> News</td>
      <td>2014-06-10</td>
      <td>2014-07-14</td>
      <td>  35</td>
      <td>   0</td>
      <td>    600</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>  418317.1300</td>
      <td> 7.5</td>
      <td> -94.79440</td>
      <td>...</td>
    </tr>
    <tr>
      <th>12</th>
      <td> 4151</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>        Bulgaria</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Eastern Bulgaria; Varna district of Asparuhov;...</td>
      <td> News</td>
      <td>2014-06-19</td>
      <td>2014-06-25</td>
      <td>   7</td>
      <td>  12</td>
      <td>   2000</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 2.0</td>
      <td>   24415.4200</td>
      <td> 5.5</td>
      <td>  27.04260</td>
      <td>...</td>
    </tr>
    <tr>
      <th>13</th>
      <td> 4150</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>        Paraguay</td>
      <td>    Brazil</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Southern Brazil, Parana State; Paraguay River ...</td>
      <td> News</td>
      <td>2014-06-03</td>
      <td>2014-07-14</td>
      <td>  42</td>
      <td>   9</td>
      <td> 265000</td>
      <td>NaN</td>
      <td>                 Heay Rain</td>
      <td> 2.0</td>
      <td>  554605.2500</td>
      <td> 7.7</td>
      <td> -53.54700</td>
      <td>...</td>
    </tr>
    <tr>
      <th>14</th>
      <td> 4149</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>          Russia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Altai region, Khakassia  Republic, and Altai R...</td>
      <td> News</td>
      <td>2014-06-04</td>
      <td>2014-06-10</td>
      <td>   7</td>
      <td>  70</td>
      <td>   3000</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td> 1829701.4000</td>
      <td> 7.3</td>
      <td>  94.36960</td>
      <td>...</td>
    </tr>
    <tr>
      <th>15</th>
      <td> 4148</td>
      <td>NaN</td>
      <td> TC-2014-000071-MEX</td>
      <td>          Mexico</td>
      <td> Guatamala</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                    Chiapas, SE Mexico.W Guatamala</td>
      <td> News</td>
      <td>2014-06-01</td>
      <td>2014-06-10</td>
      <td>  10</td>
      <td>  22</td>
      <td>  25000</td>
      <td>NaN</td>
      <td>            Monsoonal Rain</td>
      <td> 1.5</td>
      <td>  113685.4300</td>
      <td> 6.2</td>
      <td> -94.02740</td>
      <td>...</td>
    </tr>
    <tr>
      <th>16</th>
      <td> 4147</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>            Iran</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>         Khorasan, Mazandaran and Semnan provinces</td>
      <td> News</td>
      <td>2014-06-01</td>
      <td>2014-06-10</td>
      <td>  10</td>
      <td>  37</td>
      <td> 440000</td>
      <td>NaN</td>
      <td>            Monsoonal Rain</td>
      <td> 1.5</td>
      <td>  305525.2500</td>
      <td> 6.7</td>
      <td>  57.25440</td>
      <td>...</td>
    </tr>
    <tr>
      <th>17</th>
      <td> 4146</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>           China</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                Southern China, Guangdong Province</td>
      <td> News</td>
      <td>2014-05-30</td>
      <td>2014-06-10</td>
      <td>  12</td>
      <td>   6</td>
      <td>    500</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   45994.3000</td>
      <td> 5.7</td>
      <td> 113.34200</td>
      <td>...</td>
    </tr>
    <tr>
      <th>18</th>
      <td> 4145</td>
      <td>NaN</td>
      <td> FL-2014-000070-LKA</td>
      <td>       Sri Lanka</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                    Western districts of Sri Lanka</td>
      <td> News</td>
      <td>2014-06-04</td>
      <td>2014-06-10</td>
      <td>   7</td>
      <td>   5</td>
      <td>  16000</td>
      <td>NaN</td>
      <td>     Tropical Storm  Boris</td>
      <td> 1.5</td>
      <td>   10337.4700</td>
      <td> 5.0</td>
      <td>  80.16680</td>
      <td>...</td>
    </tr>
    <tr>
      <th>19</th>
      <td> 4144</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>     Afghanistan</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                   Baghlan provinc</td>
      <td> News</td>
      <td>2014-06-03</td>
      <td>2014-06-10</td>
      <td>   8</td>
      <td>   0</td>
      <td>    300</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>   44203.9300</td>
      <td> 5.7</td>
      <td>  68.01780</td>
      <td>...</td>
    </tr>
    <tr>
      <th>20</th>
      <td> 4143</td>
      <td>NaN</td>
      <td> FL-2014-000062-CHN</td>
      <td>           China</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Hunan Province, including Guiyang, Shenzhen ci...</td>
      <td> News</td>
      <td>2014-05-12</td>
      <td>2014-05-16</td>
      <td>   5</td>
      <td>   1</td>
      <td>  10000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>  205001.2700</td>
      <td> 6.3</td>
      <td> 111.46700</td>
      <td>...</td>
    </tr>
    <tr>
      <th>21</th>
      <td> 4142</td>
      <td>NaN</td>
      <td> FL-2014-000063-TJK</td>
      <td>      Tajikistan</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Khatlon Province, Rudaki and Vahdat districts,...</td>
      <td> News</td>
      <td>2014-05-10</td>
      <td>2014-05-16</td>
      <td>   7</td>
      <td>   0</td>
      <td>    425</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>   41719.4600</td>
      <td> 5.6</td>
      <td>  69.37870</td>
      <td>...</td>
    </tr>
    <tr>
      <th>22</th>
      <td> 4141</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>           Italy</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                    Marche region of central Italy</td>
      <td> News</td>
      <td>2014-05-02</td>
      <td>2014-05-10</td>
      <td>   9</td>
      <td>   2</td>
      <td>    250</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td>   11256.3300</td>
      <td> 5.2</td>
      <td>  13.01300</td>
      <td>...</td>
    </tr>
    <tr>
      <th>23</th>
      <td> 4140</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>        Tanzania</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                   Rufiji District in Coast Region</td>
      <td> News</td>
      <td>2014-05-10</td>
      <td>2014-05-16</td>
      <td>   7</td>
      <td>   0</td>
      <td>  22000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   22249.3400</td>
      <td> 5.2</td>
      <td>  38.94420</td>
      <td>...</td>
    </tr>
    <tr>
      <th>24</th>
      <td> 4139</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>          Serbia</td>
      <td>    Bosnia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                            Bosnia,Serbia, Croatia</td>
      <td> News</td>
      <td>2014-05-12</td>
      <td>2014-05-16</td>
      <td>   5</td>
      <td>   3</td>
      <td>   4000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>  115747.6900</td>
      <td> 6.1</td>
      <td>  19.22360</td>
      <td>...</td>
    </tr>
    <tr>
      <th>25</th>
      <td> 4138</td>
      <td>NaN</td>
      <td> FF-2014-000059-SRB</td>
      <td>         Romania</td>
      <td>  Bulgaria</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                Bulgaria, Serbia, southern Romania</td>
      <td> News</td>
      <td>2014-04-17</td>
      <td>2014-05-01</td>
      <td>  15</td>
      <td>   0</td>
      <td>    640</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td>   87430.6900</td>
      <td> 6.3</td>
      <td>  24.49400</td>
      <td>...</td>
    </tr>
    <tr>
      <th>26</th>
      <td> 4137</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>        Tanzania</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                              Dar es Salaam region</td>
      <td> News</td>
      <td>2014-04-18</td>
      <td>2014-05-01</td>
      <td>  14</td>
      <td>  41</td>
      <td>      0</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td>   18498.3900</td>
      <td> 5.6</td>
      <td>  38.96890</td>
      <td>...</td>
    </tr>
    <tr>
      <th>27</th>
      <td> 4136</td>
      <td>NaN</td>
      <td> FF-2014-000060-AFG</td>
      <td>     Afghanistan</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Northwestern Afghanistan; Jowzjan Province, pr...</td>
      <td> News</td>
      <td>2014-04-20</td>
      <td>2014-05-16</td>
      <td>  27</td>
      <td> 123</td>
      <td>   6000</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td>   83722.3400</td>
      <td> 6.5</td>
      <td>  66.43420</td>
      <td>...</td>
    </tr>
    <tr>
      <th>28</th>
      <td> 4135</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>             USA</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>              Gulf Coast; Northeast Atlantic Coast</td>
      <td> News</td>
      <td>2014-04-30</td>
      <td>2014-05-01</td>
      <td>   2</td>
      <td>   1</td>
      <td>    200</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 2.0</td>
      <td>  260469.8100</td>
      <td> 6.0</td>
      <td> -84.94650</td>
      <td>...</td>
    </tr>
    <tr>
      <th>29</th>
      <td> 4134</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>             USA</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>            Southern Alabama, southern Mississippi</td>
      <td> News</td>
      <td>2014-04-01</td>
      <td>2014-04-08</td>
      <td>   8</td>
      <td>   2</td>
      <td>    300</td>
      <td>NaN</td>
      <td>                heavy Rain</td>
      <td> 1.5</td>
      <td>   82418.5600</td>
      <td> 6.0</td>
      <td> -87.61880</td>
      <td>...</td>
    </tr>
    <tr>
      <th>30</th>
      <td> 4133</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>       Argentina</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                      Western province of Neuquenr</td>
      <td> News</td>
      <td>2014-04-01</td>
      <td>2014-04-08</td>
      <td>   8</td>
      <td>   0</td>
      <td>   2000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>   69876.7800</td>
      <td> 5.9</td>
      <td> -70.29840</td>
      <td>...</td>
    </tr>
    <tr>
      <th>31</th>
      <td> 4132</td>
      <td>NaN</td>
      <td> FL-2014-000045-SLB</td>
      <td> Solomon Islands</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                           Honiara</td>
      <td> News</td>
      <td>2014-04-01</td>
      <td>2014-04-08</td>
      <td>   8</td>
      <td>  23</td>
      <td>  10000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>    5480.7500</td>
      <td> 4.9</td>
      <td> 160.34200</td>
      <td>...</td>
    </tr>
    <tr>
      <th>32</th>
      <td> 4131</td>
      <td>NaN</td>
      <td> FL-2014-000038-ZAF</td>
      <td>    South Africa</td>
      <td>   Namibia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                        SADC region, Zambezi River</td>
      <td> News</td>
      <td>2014-03-01</td>
      <td>2014-03-30</td>
      <td>  30</td>
      <td>  37</td>
      <td>   3528</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td> 1037639.2000</td>
      <td> 7.7</td>
      <td>  25.60740</td>
      <td>...</td>
    </tr>
    <tr>
      <th>33</th>
      <td> 4130</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>       Australia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Southeast and Central Queensland; Yeppoon area...</td>
      <td> News</td>
      <td>2014-03-24</td>
      <td>2014-03-30</td>
      <td>   7</td>
      <td>   1</td>
      <td>      0</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td>  250162.1200</td>
      <td> 6.4</td>
      <td> 150.11700</td>
      <td>...</td>
    </tr>
    <tr>
      <th>34</th>
      <td> 4129</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>             USA</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>            Southern Mississippi, Wilkinson County</td>
      <td> News</td>
      <td>2014-03-25</td>
      <td>2014-03-30</td>
      <td>   6</td>
      <td>   0</td>
      <td>    200</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>   53220.7900</td>
      <td> 5.7</td>
      <td> -89.12820</td>
      <td>...</td>
    </tr>
    <tr>
      <th>35</th>
      <td> 4128</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>         Zimbawe</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                      Tokwe-Mukosi</td>
      <td> News</td>
      <td>2014-02-01</td>
      <td>2014-03-30</td>
      <td>  58</td>
      <td>   0</td>
      <td>   4000</td>
      <td>NaN</td>
      <td>                 Dam Break</td>
      <td> 1.0</td>
      <td>   17205.6400</td>
      <td> 6.0</td>
      <td>  31.34790</td>
      <td>...</td>
    </tr>
    <tr>
      <th>36</th>
      <td> 4127</td>
      <td>NaN</td>
      <td> FL-2014-000030-PRY</td>
      <td>        Paraguay</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>  Luque, Mariano Roque Alonso, Lambaré, and Limpio</td>
      <td> News</td>
      <td>2014-02-25</td>
      <td>2014-03-10</td>
      <td>  14</td>
      <td>   0</td>
      <td>   2000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>    6829.5700</td>
      <td> 5.0</td>
      <td> -57.58330</td>
      <td>...</td>
    </tr>
    <tr>
      <th>37</th>
      <td> 4126</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>         Burundi</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                         Bujumbura</td>
      <td> News</td>
      <td>2014-02-19</td>
      <td>2014-03-10</td>
      <td>  20</td>
      <td>  69</td>
      <td>  20000</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 2.0</td>
      <td>    3237.4200</td>
      <td> 5.1</td>
      <td>  29.64990</td>
      <td>...</td>
    </tr>
    <tr>
      <th>38</th>
      <td> 4125</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>     New Zealand</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                Christchurch, including Avon River</td>
      <td> News</td>
      <td>2014-03-03</td>
      <td>2014-03-10</td>
      <td>   8</td>
      <td>   0</td>
      <td>     80</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>    1015.8400</td>
      <td> 4.2</td>
      <td> 172.61300</td>
      <td>...</td>
    </tr>
    <tr>
      <th>39</th>
      <td> 4124</td>
      <td>NaN</td>
      <td> SS-2014-000032-MHL</td>
      <td>             USA</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                            Majuro</td>
      <td> News</td>
      <td>2014-03-03</td>
      <td>2014-03-10</td>
      <td>   8</td>
      <td>   0</td>
      <td>    900</td>
      <td>NaN</td>
      <td>               Storm Surge</td>
      <td> 1.5</td>
      <td>      34.8366</td>
      <td> 2.6</td>
      <td> 168.72900</td>
      <td>...</td>
    </tr>
    <tr>
      <th>40</th>
      <td> 4123</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>      Mozambique</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Johannesburg , Kliptown, Soweto; eastern South...</td>
      <td> News</td>
      <td>2014-02-24</td>
      <td>2014-03-10</td>
      <td>  15</td>
      <td>   4</td>
      <td>  20000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>  481907.8800</td>
      <td> 6.9</td>
      <td>  31.54590</td>
      <td>...</td>
    </tr>
    <tr>
      <th>41</th>
      <td> 4122</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>          France</td>
      <td>     Italy</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Southeastern France, western France, Pisa, Lig...</td>
      <td> News</td>
      <td>2014-01-20</td>
      <td>2014-02-07</td>
      <td>  19</td>
      <td>   4</td>
      <td>   1000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>   82989.4500</td>
      <td> 6.4</td>
      <td>   7.09930</td>
      <td>...</td>
    </tr>
    <tr>
      <th>42</th>
      <td> 4121</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>       Indonesia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                Jakarta, Tangerang</td>
      <td> News</td>
      <td>2014-01-08</td>
      <td>2014-02-07</td>
      <td>  31</td>
      <td>  23</td>
      <td>  20000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>   35769.2200</td>
      <td> 6.2</td>
      <td> 107.70600</td>
      <td>...</td>
    </tr>
    <tr>
      <th>43</th>
      <td> 4120</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>       Australia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                       Top End, Northern Territory</td>
      <td> News</td>
      <td>2014-02-02</td>
      <td>2014-02-07</td>
      <td>   6</td>
      <td>   0</td>
      <td>      0</td>
      <td>NaN</td>
      <td>  Tropical Storm  Fletcher</td>
      <td> 1.0</td>
      <td>  426979.8400</td>
      <td> 6.4</td>
      <td> 131.73200</td>
      <td>...</td>
    </tr>
    <tr>
      <th>44</th>
      <td> 4119</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>         Zimbawe</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Communities downstream of the Tokwe-Mukrosi Da...</td>
      <td> News</td>
      <td>2014-01-15</td>
      <td>2014-02-07</td>
      <td>  24</td>
      <td>   0</td>
      <td>   4000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>   72462.2300</td>
      <td> 6.4</td>
      <td>  28.92310</td>
      <td>...</td>
    </tr>
    <tr>
      <th>45</th>
      <td> 4118</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>         Zimbawe</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                        Muzarabani</td>
      <td> News</td>
      <td>2014-01-15</td>
      <td>2014-02-07</td>
      <td>  24</td>
      <td>   0</td>
      <td>      0</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>  142586.1000</td>
      <td> 6.7</td>
      <td>  30.85310</td>
      <td>...</td>
    </tr>
    <tr>
      <th>46</th>
      <td> 4117</td>
      <td>NaN</td>
      <td> FL-2014-000008-BOL</td>
      <td>         Bolivia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> La Paz, Beni, Santa Cruz  and Cochabamba; Beni...</td>
      <td> News</td>
      <td>2014-01-10</td>
      <td>2014-05-01</td>
      <td> 112</td>
      <td>  60</td>
      <td>  84000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>  381576.6500</td>
      <td> 7.9</td>
      <td> -64.01350</td>
      <td>...</td>
    </tr>
    <tr>
      <th>47</th>
      <td> 4116</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>            Peru</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                      Southern Andean Cusco region</td>
      <td> News</td>
      <td>2014-01-01</td>
      <td>2014-01-04</td>
      <td>   4</td>
      <td>   0</td>
      <td>    300</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   74144.6600</td>
      <td> 5.5</td>
      <td> -71.52320</td>
      <td>...</td>
    </tr>
    <tr>
      <th>48</th>
      <td> 4115</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>             USA</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>             Nelson and Carroll Counties, Kentucky</td>
      <td> News</td>
      <td>2013-12-22</td>
      <td>2014-01-04</td>
      <td>  14</td>
      <td>   5</td>
      <td>      0</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   16069.9100</td>
      <td> 5.4</td>
      <td> -86.78990</td>
      <td>...</td>
    </tr>
    <tr>
      <th>49</th>
      <td> 4114</td>
      <td>NaN</td>
      <td> FL-2013-000159-LCA</td>
      <td>   Saint Vincent</td>
      <td> St. Lucia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>       Saint Vincent and the Grenadines, St. Lucia</td>
      <td> News</td>
      <td>2013-12-26</td>
      <td>2014-01-04</td>
      <td>  10</td>
      <td>  11</td>
      <td>      0</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>     830.2320</td>
      <td> 3.9</td>
      <td> -60.98860</td>
      <td>...</td>
    </tr>
    <tr>
      <th>50</th>
      <td> 4113</td>
      <td>NaN</td>
      <td> FL-2013-000157-BRA</td>
      <td>          Brazil</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Southeast states of Minas Gerais and Espirito ...</td>
      <td> News</td>
      <td>2013-12-23</td>
      <td>2014-01-04</td>
      <td>  13</td>
      <td>  45</td>
      <td>  60000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 2.0</td>
      <td>  314284.9100</td>
      <td> 6.9</td>
      <td> -41.94230</td>
      <td>...</td>
    </tr>
    <tr>
      <th>51</th>
      <td> 4112</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>       Indonesia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                   North Sumatras Langkat district</td>
      <td> News</td>
      <td>2013-12-29</td>
      <td>2014-01-04</td>
      <td>   7</td>
      <td>   0</td>
      <td>   4500</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   22524.6300</td>
      <td> 5.2</td>
      <td>  97.28930</td>
      <td>...</td>
    </tr>
    <tr>
      <th>52</th>
      <td> 4111</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>  United Kingdom</td>
      <td>   Ireland</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Central and southern Scotland, Wales, Ireland,...</td>
      <td> News</td>
      <td>2013-12-27</td>
      <td>2014-02-07</td>
      <td>  43</td>
      <td>   0</td>
      <td>    200</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.5</td>
      <td>  126149.7900</td>
      <td> 6.9</td>
      <td>  -1.51144</td>
      <td>...</td>
    </tr>
    <tr>
      <th>53</th>
      <td> 4110</td>
      <td>NaN</td>
      <td> FL-2013-000149-THA</td>
      <td>        Thailand</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Southeast provinces; Nakhon Si Thammarat, Song...</td>
      <td> News</td>
      <td>2013-11-20</td>
      <td>2013-12-08</td>
      <td>  19</td>
      <td>  23</td>
      <td>  15254</td>
      <td>NaN</td>
      <td>            Monsoonal Rain</td>
      <td> 1.5</td>
      <td>   38676.7100</td>
      <td> 6.0</td>
      <td> 100.39500</td>
      <td>...</td>
    </tr>
    <tr>
      <th>54</th>
      <td> 4109</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>            Cuba</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                            Havana</td>
      <td> News</td>
      <td>2013-12-01</td>
      <td>2013-12-08</td>
      <td>   8</td>
      <td>   2</td>
      <td>    227</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.0</td>
      <td>    7627.3000</td>
      <td> 4.8</td>
      <td> -81.39580</td>
      <td>...</td>
    </tr>
    <tr>
      <th>55</th>
      <td> 4108</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>           Niger</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                South-east Niger, Komadougou River</td>
      <td> News</td>
      <td>2013-11-03</td>
      <td>2013-12-08</td>
      <td>  36</td>
      <td>   0</td>
      <td>   1000</td>
      <td>NaN</td>
      <td>                Heavy Rain</td>
      <td> 1.0</td>
      <td>   65791.1400</td>
      <td> 6.4</td>
      <td>  13.20170</td>
      <td>...</td>
    </tr>
    <tr>
      <th>56</th>
      <td> 4107</td>
      <td>NaN</td>
      <td> FL-2013-000148-MYS</td>
      <td>        Malaysia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Kuala Lumpur, east coast states of Pahang and ...</td>
      <td> News</td>
      <td>2013-12-01</td>
      <td>2013-12-08</td>
      <td>   8</td>
      <td>   1</td>
      <td>  19000</td>
      <td>NaN</td>
      <td>            Monsoonal Rain</td>
      <td> 1.5</td>
      <td>  106697.5300</td>
      <td> 6.1</td>
      <td> 102.36200</td>
      <td>...</td>
    </tr>
    <tr>
      <th>57</th>
      <td> 4106</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>  United Kingdom</td>
      <td>   Germany</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>    Eastern England coast, northern European coast</td>
      <td> News</td>
      <td>2013-12-05</td>
      <td>2013-12-08</td>
      <td>   4</td>
      <td>   8</td>
      <td>   4000</td>
      <td>NaN</td>
      <td>               Storm Surge</td>
      <td> 2.0</td>
      <td>   51279.6000</td>
      <td> 5.6</td>
      <td>   7.53306</td>
      <td>...</td>
    </tr>
    <tr>
      <th>58</th>
      <td> 4105</td>
      <td>NaN</td>
      <td> FL-2013-000141-SOM</td>
      <td>         Somalia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>                                Northeast Puntland</td>
      <td> News</td>
      <td>2013-11-08</td>
      <td>2013-11-19</td>
      <td>  12</td>
      <td> 100</td>
      <td>      0</td>
      <td>NaN</td>
      <td>            Tropical Storm</td>
      <td> 1.5</td>
      <td>  181848.0200</td>
      <td> 6.5</td>
      <td>  57.42760</td>
      <td>...</td>
    </tr>
    <tr>
      <th>59</th>
      <td> 4104</td>
      <td>NaN</td>
      <td>                  0</td>
      <td>    Saudi Arabia</td>
      <td>         0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td> Riyadh, other parts of the Kingdom including n...</td>
      <td> News</td>
      <td>2013-11-18</td>
      <td>2013-11-19</td>
      <td>   2</td>
      <td>  15</td>
      <td>    121</td>
      <td>NaN</td>
      <td>           Torrential Rain</td>
      <td> 1.5</td>
      <td>  361386.8400</td>
      <td> 6.0</td>
      <td>  44.80840</td>
      <td>...</td>
    </tr>
    <tr>
      <th></th>
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
  </tbody>
</table>
<p>276 rows × 29 columns</p>
</div>

