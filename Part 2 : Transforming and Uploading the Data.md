2.1 Transforming the Data
	I took the streaming_history_audio files into a separate folder. The json type of data is tricky to work around so I had to transform it into a more workable and editable file format.
For this step, I used Python Pandas to transform them into excel files.

![converting files from json to excel file](https://github.com/user-attachments/assets/5793680f-dcb7-4c89-a1e3-269558d6c9c6)

2.2 Getting the Data Together
Turning json files into excel files, I stored them into a folder.

![exsel](https://github.com/user-attachments/assets/765c4c50-4c09-44f8-8e23-2f5b6106e339)

We have 5 files containing around 100.000 rows of data combined. We have to combine all of them in one table. But before that, we have to do some configurations in Excel.

2.2.1. Configurations in Excel
Step 1: Fixing the datetime data
Turned into an excel file, our datetime data came out in datetimezone format like this.

![t1](https://github.com/user-attachments/assets/48c7efb7-3db6-4606-9c0d-69769cc31f71)

This will create problems both in data conversion, data extraction and cleaning. So we turned that data into a datetime data using PowerQuery.

![t2](https://github.com/user-attachments/assets/86e56891-df64-4737-b29a-3894060e4f5e)

Step 2 : Figuring out what to do with offline_timestamp column
During my tests in SSIS, I ran into error after error because of this column. Errors occurred because of conversion problems. This column held data like NULLs, bigint numbers and mixed varchar data like 1.66266E+12. I evaluated if this column was needed for my analysis and decided to delete it.
2.2.2. Process in SSIS after Configuration
	To collect all the data in one place, firstly I created a database called “Spotify” in Microsoft SQL and added a table called SPOTIFY_DW_UNI

SPOTIFY_DW_UNI TABLE
![dw](https://github.com/user-attachments/assets/bec68bfa-25ff-42a0-bcdb-305f9687cb1e)

With my table ready to store data, I created an Integration Services Project in Microsoft Visual Studio. Constructing a Data Flow Task to take excel data, union them all into an OLE DB Destination, I managed to merge data from five files in one database for further processes.

SSIS Structure
![SSIS](https://github.com/user-attachments/assets/85604e11-3d60-4761-964a-43155870d557)
