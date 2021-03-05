# wiki_k12_shooting

Scrapping on [k12 shooting table in wikipedia](https://en.wikipedia.org/wiki/List_of_school_shootings_in_the_United_States)
 
 - Adding geographical info Longitude and Latittude
 
 - Data clean
 
 - Saved in prosessed_data.csv 
 
 ![img](resource/visualization.png)

# Data Mining 

1. Use Roberta model to do Q/A task on "Descripton column", I asked "Which school?" to extracted School name, and also did Spacy NER looking for "ORG", and Roberta outperform a lot.
2. Using GCP Place API to find school's information on google map, it inludes detailed address, location, useer reviews. I extracted county data and save in 'County" column in school_county.csv
3. school's detail information is saved in school_detail.pkl, it is a dictionary, key is the index of school_county.csv.
