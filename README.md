# surfs_up
Climate analysis is needed for opening a new surf store that also sells ice-cream in Oahu, Hawaii. This project relates to advanced data storage and retrieval.
## Data Source
[hawaii.sqlite](https://github.com/rmat112/surfs_up/blob/main/hawaii.sqlite)
## Tools
Python, Flask, Jupyter Notebook, SQLite, SQLAlchemy
using Python, pandas, numpy, matplotlib, Jupyter notebook, VS Code
## Overview of Statistical Analysis
We need to write queries to filter the data from Measurements table in the hawaii.sqlite database to retrieve all the temperatures for the months of June and December. We will then convert those temperatures to a list, create a DataFrame from the list, and generate the summary statistics. We will write two additional queries to gather more weather data for these two months.<br/>
Click here for a link to the code: [SurfsUp_Challenge.ipynb](https://github.com/rmat112/surfs_up/blob/main/SurfsUp_Challenge.ipynb)

## Results
#### 1a. A query that filters the date column from the Measurement table to retrieve all the temperatures for the month of June:
![D1_1](https://github.com/rmat112/surfs_up/blob/main/Resources/D1_1.png)
#### 1b. The temperatures added to a list:![merge](https://user-images.githubusercontent.com/92052842/146614984-7164ed0e-d26b-4aa2-b60a-adabc4c4e8e3.png)

![D1_2](https://github.com/rmat112/surfs_up/blob/main/Resources/D1_2.png)
#### 1c. The list of temperatures converted to a Pandas DataFrame:
![D1_3](https://github.com/rmat112/surfs_up/blob/main/Resources/D1_3.png)
#### 1d. Summary statistics for the month of June:
![June_summary_stats](https://github.com/rmat112/surfs_up/blob/main/Resources/June_summary_stats.png)

#### 2a. A query that filters the date column from the Measurement table to retrieve all the temperatures for the month of December:
![D2_1](https://github.com/rmat112/surfs_up/blob/main/Resources/D2_1.png)
#### 2b. The temperatures added to a list:
![D2_2](https://github.com/rmat112/surfs_up/blob/main/Resources/D2_2.png)
#### 2c. The list of temperatures converted to a Pandas DataFrame:
![D2_3](https://github.com/rmat112/surfs_up/blob/main/Resources/D2_3.png)
#### 2d. Summary statistics for the month of December:
![Dec_summary_stats](https://github.com/rmat112/surfs_up/blob/main/Resources/Dec_summary_stats.png)

#### 3. Key Differences between data from June and December
#### 3a. <br/>
There are 1700 observations from the month of June as compared to 1517 observations from the month of December.<br/>
#### 3b. <br/>
Maximum temperatures in June and December vary by only a couple degrees (85 deg in June vs. 83 deg in Dec).<br/>
#### 3c. <br/>
Minimum temperatures in June and December vary by 8 degrees (64 deg in June vs. 56 deg in Dec).<br/>
#### 3d. <br/>
Mean temperatures in June and Dec vary only by 4 degrees (~75 deg in June vs. ~71 deg in Dec).<br/>

## Summary
After looking carefully at the analysis results it can be summarized that opening a surf store that also serves ice-cream, is totally safe in Oahu because sales will happen the same whether it is June or December. The high temperatures in June vs December are quite similar and are within the range of 83 to 85 deg. Also, the average temperatures are within the range of 71-75 deg. Some additional queries were made to assist in deciding the best location on the island.

### Additional Queries
#### A.  A query is written that filters the Measurement table to retrieve the Station IDs, number of observations, and temperatures for the month of June. It is then grouped by the Station ID and ordered by the number of observations, then put into a pandas dataframe:

![Query%231](https://github.com/rmat112/surfs_up/blob/main/Resources/Query%231.png)

#### B.  A query is written that filters the Measurement table to retrieve the Station IDs, number of observations, and temperatures for the month of December. It is then grouped by the Station ID and ordered by the number of observations, then put into a pandas dataframe:

![Query%232](https://github.com/rmat112/surfs_up/blob/main/Resources/Query%232.png)

#### C. The two dataframes created above are then merged in order to see a comparison:

![merge](https://github.com/rmat112/surfs_up/blob/main/Resources/merge.png)

#### D. A plot that shows comparison of no of Observations per station in June and December:

![Obs_comparison](https://github.com/rmat112/surfs_up/blob/main/Resources/Obs_comparison.png)

#### E. A plot that shows comparison of no of average temperatures per station in June and December:

![Temp_comparison](https://github.com/rmat112/surfs_up/blob/main/Resources/Temp_comparison.png)

#### F. Based on this additional analysis (Queries and plots) the following becomes evident: 
- There is no relation between the number of observations and average temperatures recorded at a certain station location.
- The location of following stations will be best suited for opening a new store:
  - USC00519397 (Most no. of observations and the highest average temp in the month of June)
  - USC00514830 (Highest Average temp in the month of December)
