Our data has 22 columns, holding 65,373 rows of data. This data is raw, so we have to reorganize and customize it for our need.

3.1) Unnecessary Columns

Some of these columns are not necessary for our analysis. Let’s talk about them

1) conn_country: This column holds country location data with two to three characters of abbreviation like “TR” and “USA”. Our analysis doesn’t need location data, so we will not use this column
2) ip_addr: This column holds the ip address of my devices. This information is irrelevant to our analysis and would not be safe to share, so will not use this column.
3) Offline: This column holds Boolean data to see if I’m listening music in offline mode. I don’t use the app in offline form much and this information is irrelevant to our analysis, so will not use this column.
4) incognito_mode: This column holds Boolean data to see if I’m using the app in private mode. I don’t use this attribute too often and This information is irrelevant to our analysis, so will not use this column.


![dw](https://github.com/user-attachments/assets/138e4434-8a9d-4b6a-aa4c-fb07d0696c37)

Solution:
We create a view without taking this columns into our table

![view1](https://github.com/user-attachments/assets/631115a5-195d-4f46-96b6-07c6740faa87)

The structure of our view:

![view1out](https://github.com/user-attachments/assets/9bea7ea5-4f30-44e4-81ed-e6e7c4e4319d)

3.2) Updating the Platform Column
Platform Column holds the data about in which platform I used the app. I use the app on web player, android and windows. 
While I was expecting to see 3 types of distinct data, I ran ınto some inconsistent data anomalies.

Web Player Distinct Platform Data:

![andr](https://github.com/user-attachments/assets/6c020eda-3ccc-4ccb-a1e2-dcf22dfbcc02)

![wind](https://github.com/user-attachments/assets/d82d92fc-25fa-4a93-8c4d-a624d4c196aa)

![web player](https://github.com/user-attachments/assets/ffffaf60-f3c4-4688-a5ce-49c9b2b71a3d)

WARNING!: The black parts hold personal and confidential information. If you plan to do this project and publish it, make sure to conceal them

Solution:

I decided to convert rows holding unorganized strings and organized them under their respective platform. Firstly, I copied my file under another view called “PLATFORMTEST” to be able to fix my mistakes and not to corrupt or disrupt our original data.

![plarc](https://github.com/user-attachments/assets/8b0a4f8d-c9f1-449f-82ff-1174e5f1977d)
![updt](https://github.com/user-attachments/assets/a660bfec-b2b2-4749-a47e-ae7b1a4609f5)

3.3) Renaming Columns

master_metadata_track_name,	
master_metadata_album_artist_name
master_metadata_album_album_name

These column names are too long and hold unnecessary data for our analysis. So on our view, I will be shortening their names and replacing them with proper ones.

![rename](https://github.com/user-attachments/assets/98e64a7a-df00-4eda-8e12-e7062bf676cf)

3.4) Cleaning Spotify_track_uri Data

This column holds a string part like “spotify:track:” before the track uri. We don’t need this part of the data.

![tr1](https://github.com/user-attachments/assets/64b58637-42d8-40e0-919f-6fa27427705d)

After Cleaning

![tr2](https://github.com/user-attachments/assets/44083b80-ab86-42c0-ac1e-9735374fc3b2)

3.5) Seperating Music and Podcast Data

As I tried to do simple exploratory analysis parts, I realized some difference between podcast and music data. 
Podcast data had its track_name, artist_name and album_name rows as null. Music data had its episode connected rows as null. 
I decided to create two more views holding relevant data for both tables so we can get correct results in our analysis.

Creating a View Table for Music Data

![mucis](https://github.com/user-attachments/assets/377e1f37-d52f-46c3-9ce3-6fc1c9d71e8d)

How our data looks after cleaning processes:

![music](https://github.com/user-attachments/assets/2df8a291-affd-45fc-b517-2dfdc39fb29b)


