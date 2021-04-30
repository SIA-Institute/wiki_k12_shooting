# wiki_k12_shooting

Scrapping on [k12 shooting table in wikipedia](https://en.wikipedia.org/wiki/List_of_school_shootings_in_the_United_States)
 
 - Adding geographical info Longitude and Latittude
 
 - Data clean
 
 - Saved in prosessed_data.csv (Reloacte to old_dataframe)
 
 ![img](resource/visualization.png)

# Data Mining 

1. Using __Roberta__ model to do Q/A task on "Descripton" column, I asked __"Which school?"__ to extracted School name, and also did Spacy NER for specific "ORG" tag for benchmarking, the result shows Roberta extracted data more effectively.
2. Using GCP Place API to find school's information on google map, the queried data including address, administrative info, useer reviews etc. I extracted county data only and saved in 'County" column with _school_county.csv_
3. The rest of school's google map detail information is saved in _school_detail.pkl_, it is a dictionary, key is the index of school_county.csv.

# Connect with Census data

1. Claened data is called _school_county_v2.csv_

<<<<<<< Updated upstream
2. Using code like this to merge with census dataframe.
```Python
df_county.merge(df_census,left_on=['States','County'],right_on=['States','County'],how='left')

```
=======
2. Using code like this to merge dataframe.
```python
df_county.merge(df_census,left_on=['States','County'],right_on=['States','County'],how='left')
```
>>>>>>> Stashed changes
