# (Geo)Pandas Tutorial
A quick tutorial for the python libraries pandas and geopandas 🐼
Created by Sophie Spiliotopoulos for IDCE 30274, Nov 2020

### Data 
Data for this tutorial can be found in the `data` folder of the repo. This data includes mean sea ice concentration (SIC) data from the NSIDC and suspended particualte matter (SPM) data that was collected and created as a part of the Distributed Biological Observatory (DBO) project. You can learn more about the DBO [here](https://dbo.cbl.umces.edu) 

# Part 1: Getting Started 
Let's start by importing all the main libraries we'll need
```python
#install geopandas
!pip install geopandas 
#import libraries and give them aliases
import pandas as pd
import geopandas as gpd
```
I used Google Drive to store my data, so here I set up my drive. The data for this tutorial is in the `data`. 
```python 
from google.colab import drive 
drive.mount('/content/gdrive') 
# set root path
root_path = 'gdrive/My Drive/(geo)pandas_tutorial_final/' 
```
Now that Google Drive is set up, we'll bring in the first two datasets, a mean SIC for 1980-2010 and SPM data collected in the Pacific Arctic in 2019. 
```python 
#import .csv and call the data 
spm19 = pd.read_csv(root_path+"spm19_proc_blanks.csv")
mean_sic = pd.read_csv(root_path+"1981-2010_SIC_Daily.csv")
```

# Part 2: Reading Files with Pandas
The next few lines of code are testing out different way to read and your data files. 
