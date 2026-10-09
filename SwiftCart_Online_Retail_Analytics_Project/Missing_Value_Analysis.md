# SwiftCart Missing Value Analysis

## Raw Missing Values
Age                 1085
index               1080
Order ID            1080
Cust ID             1079
Gender              1075
Age Group           1068
Date                 465
Month                465
Status                 0
Channel                0
SKU                    0
Category               0
Size                   0
Qty                    0
currency               0
Amount                 0
ship-city              0
ship-state             0
ship-postal-code       0
ship-country           0
B2B                    0

## Approach
Missing IDs and demographic values were retained because the source does not support reliable imputation. Missing exact dates were not reconstructed from month labels.

Where a valid date existed and Month was missing, Month was derived from Date. Month missingness therefore fell from **465** to **8**.

## Limitation
Analyses using customer ID, demographics, or exact date should acknowledge the remaining missing records.
