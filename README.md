# Blockchain_Healthcare
Machine Learning methods on blockchain healthcare dataset
===== FIRST 5 ROWS =====
   blockchain  trust_score  data_integrity  transaction_time  fraud_incidents  \
0           0    44.030257       69.273253          4.092353                5   
1           1    56.096956       91.736987          3.953791                1   
2           1    75.877793       85.059986          3.266859                4   
3           1    89.134737       89.264036          5.698025                2   
4           0    55.376299       69.004687         16.571447                6   

   patient_satisfaction  stakeholders  
0              4.321855            69  
1              5.769232            90  
2              7.639082            37  
3              6.875269            62  
4              4.115032            22  

===== DATA INFO =====
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 5000 entries, 0 to 4999
Data columns (total 7 columns):
 #   Column                Non-Null Count  Dtype  
---  ------                --------------  -----  
 0   blockchain            5000 non-null   int64  
 1   trust_score           5000 non-null   float64
 2   data_integrity        5000 non-null   float64
 3   transaction_time      5000 non-null   float64
 4   fraud_incidents       5000 non-null   int64  
 5   patient_satisfaction  5000 non-null   float64
 6   stakeholders          5000 non-null   int64  
dtypes: float64(4), int64(3)
memory usage: 273.6 KB
None

===== DATA SHAPE =====
(5000, 7)

===== MISSING VALUES =====
blockchain              0
trust_score             0
data_integrity          0
transaction_time        0
fraud_incidents         0
patient_satisfaction    0
stakeholders            0
dtype: int64

===== STATISTICAL SUMMARY =====
       blockchain  trust_score  data_integrity  transaction_time  \
count  5000.00000  5000.000000     5000.000000       5000.000000   
mean      0.50000    64.815667       80.011753          7.535548   
std       0.50005    17.978197       11.105132          3.211853   
min       0.00000    11.633445       53.122104         -2.270400   
25%       0.00000    49.797858       70.031380          5.009847   
50%       0.50000    64.704095       79.926670          7.535405   
75%       1.00000    79.835179       90.035382         10.034386   
max       1.00000   115.290552      106.420591         18.958169   

       fraud_incidents  patient_satisfaction  stakeholders  
count      5000.000000           5000.000000   5000.000000  
mean          3.977200              6.483218     52.131200  
std           2.237606              1.822377     27.713838  
min           1.000000              1.546646      5.000000  
25%           2.000000              4.954289     28.000000  
50%           5.000000              6.468061     52.000000  
75%           6.000000              8.003390     76.000000  
max          11.000000             11.354573     99.000000  

