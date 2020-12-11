# Assignment-5_Data

Here, I would like to expain the whole code of python: 

# Imported the libraries

import pandas as pd
import numpy as np

# Read the csv file of youtube_dataset
df = pd.read_csv("youtube_dataset.csv", encoding="windows-1252")

# you can see the data by calling head fucntion
df.head()

# see the information about the data
df.info()

# Save the 1000 rows from the youtube_dataset into new variable 
new_df = df.iloc[:1000]

# Now you can see the 1000 rows from the main dataset
new_df

# Distributions of Channel Type from the 1000 row which I have stored in new variable
new_df['channeltype'].value_counts()

# Created a dataframe for 1000 records which I have taken in new variable, so from this code, you will get the CSV file in spcecific folder.
trans_df = pd.DataFrame(new_df)
trans_df.to_csv ("youtube.csv", index=False)
