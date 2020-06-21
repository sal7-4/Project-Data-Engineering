# Data Modeling with Postgres
### Introduction
The purpose of this database is to analyze the data on songs for a startup called Sparkify and user activity on their new music streaming app.The analytics team can write queries on this Postgres database to understand what songs users are listening to.

### database schema design and ETL pipeline

#### Fact Table
 - songplays
     >(songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent)
#### Demension Table
 - users - users in the app
    >(user_id, first_name, last_name, gender, level)
 - songs - songs in music database
    >(song_id, title, artist_id, year, duration)
 - artists - artists in music database
    >(artist_id, name, location, latitude, longitude)
 - time - timestamps of records in songplays broken down into specific unit
    >(start_time, hour, day, week, month, year, weekday)

### Run Model

Run this model in terminal.


```sh
python create_tables.py
python etl.py
```

