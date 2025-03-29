# Spotify-Data-Analysis
In this project, I took my Spotify Streaming History data. I used certain methods and programs to compile, clean and analyze this data to find out about my listening habits.

My main purposes in this project are: (I used T to shorten the tasks)

- T1: To practice ms SSIS and Python Pandas Data Analysis skills

- T2: To work with a raw data and cleaning it myself

- T3: To find my top artists and tracks

- T4: To find Date and Time trends in my listening habits

- T5: To find the most skipped, picked and finished tracks

- T6: To find correlations about why I skip a song

- T7: To find if I am prone to listen some band repeatedly or do I explore new bands regularly

This project is seperated into four parts. Each and every part has a different program in use to practice certain skills and to do certain jobs.

Parts:
 

Part 1: Getting the Data
 

In this part, I talk about how you can get your own Extended Streaming History data. This part has no coding or analysis in it. You can skip it if you already know how to get
the data.

Part 2: Transforming and Uploading the Data
 

In the second part, I used Python, Excel to transform and SSIS to compile the data. I also used Microsoft SQL Server to create a data warehouse for my compiled data.

Part 3: Cleaning the Data
 

In the third part, I cleaned the data in SQL and prepared it for analysis in Python.

Part 4: Exploring and Analysing the Data
 

In the fourth and the last part, I took my data into Python and started analysing it according to my main purposes. I used Pandas library for general analysis
and Matplotlib library for simple visualization.


Final Analysis:
 

- T3: To find my top artists and tracks
 

![topsongs](https://github.com/user-attachments/assets/0fc3d7cc-519b-4034-b24a-761493e2adf8)


My top listened track in milliseconds is Sky Lab by Electronic Systems. This was unexpected. This song is 14:16 minutes long and I listened it a lot, so it came
out on top. Interestingly, some of my top 10 songs are not from my top 10 artists.

![topartist](https://github.com/user-attachments/assets/4e848403-5f9e-41f9-8676-ced4554e566a)

My top artist by playtime is Radiohead. I had a depressed era in 2023 and I blasted Radiohead too much (I'm glad im beyond that era, but i still love Radiohead).
Most of the bands in top 10 are the ones I have been listening since 2022 except Molchat Doma and Russian Circles. I met those bands in 2024 and they took their
places in the top.

- T4: To find Date and Time trends in my listening habits 


T4.1: Yearly Trends:
 

![year](https://github.com/user-attachments/assets/4cf1e640-2b23-4a14-9340-57a7e00cf1e1)

I started using Spotify regularly in 2021. Before that, I tried the platform several times between 2017-2020.

My listening time increased in 2022 and peaked in 2023. It decreased a bit in 2024.

This project is being done in February-March of 2025, so I only have data until the 18th of February. That's why the data is showing the 2025's listening time low.

![topinyears](https://github.com/user-attachments/assets/59c30fba-9ed2-4880-81eb-6c5c7bb96b84)

I discovered that every year, my top artist changes. Some of the previous years'top artists stay in the top 10 next year.

Even though I have some all time favorites in many years like All Them Witches and Opeth, I tend to add new names to top 10 artists every year.


T4.2: Monthly Trends:
 

![months](https://github.com/user-attachments/assets/74cc6e5d-21b2-4e87-8f24-bc01c4faf64d)

When we check the monthly listening time data, we can see that my listening time peaks in Summer and Winter.

Especially the period between June-July and December-January I listen the most.

We can roughly say that I listen less in Autumn and Spring.


T4.3: Weekly Trends:
 

![weekdays](https://github.com/user-attachments/assets/cd3552b6-1ae3-454e-b6ad-55cb1796f78f)

The days that I listen the most is Monday, Wednesday and Sunday. Tuesday and Thursday are very close to each other and to Sunday.

I tend to listen less in Friday and Saturday.


T4.4: Daily Trends:
 

My listening time peaked in the 11th of June 2022, the peak listening dates are mostly from the summer of 2022(focusing mostly on June with few exceptions).

![hours](https://github.com/user-attachments/assets/a3c79888-25c9-4087-9c7d-dd224f837f38)

My favorite listening hours are around 14:00-17:00 and 21:00-00:00

I start to listen around 14:00 and tend to keep up until 18:00 - 20:00, where it plummets down

Starting with 20:00, it starts to rise again, it peaks around 21:00 and 22:00, decreasing down by 01:00

We can say that my top listening times are in the late afternoon mid to late evening. You can find me with headsets around 14:00-17:00 and 20:00-23:00.


- T5: To find the most skipped, picked and finished tracks

** Most Finished Tracks ** 

We can start by the finished tracks. I used reason_end column's "trackdone" value to filter the finished tracks.

![finish](https://github.com/user-attachments/assets/4bb96fad-ba91-471a-958e-73759a0502e1)

9 of the top 15 most finished songs belong to the artists who are not in my Top 15 List

** Most Picked Tracks **

We can continue with the most picked tracks. I evaluated the values in reason_start column. I thought that "clickrow" and "backbtn" values can be filtered picked as a filter.

To compare if there are any differences between the values when I take "backbtn" or leave it out, I compared the values.

![backbtn](https://github.com/user-attachments/assets/86c073cd-d3bc-4593-acd6-6351ff1812d1)

There are some small differences between two tables. For both of them we can say, I tend to pick tracks from Molchat Doma and Radiohead regularly.

** Most Skipped Tracks **

Lastly, we can check the most skipped tracks. We used reason_end's (endplay, backbtn, fwdbtn, clickrow) values for filtering the skipped tracks.

During this process, I checked the data and realized I tend to skip the song near the end and Spotify counts them as skipped tracks.

To balance this out, I found the average ms_played in the overall playtime and added a second filter, counting the ms_played below average as skipped tracks.

![skips](https://github.com/user-attachments/assets/9fc233dc-5a69-471c-adc8-bfd540e282ba)

My average filtering can be debatable, but when we check the data, we can see that Boa by Duvet and Ingenue by Atoms for Peace are the most skipped tracks

- T6: To find correlations about why I skip a song

I wondered about why I skip the tracks. I thought there may be a connection between shuffle and skip reason. I compared most skipped(with avg filter) and most shuffled tracks.

![shuffles](https://github.com/user-attachments/assets/59aea3dd-fc0d-492b-b72b-d96dd9943594)

I found out that 6 of the top 15 skipped songs are in the most shuffled tracks list.

- T7: To find if I am prone to listen some band repeatedly or do I explore new bands regularly

I compared my top 15 artists and last played 15 artists to have a slight opinion about this question.

![latest](https://github.com/user-attachments/assets/edfeaf37-e0b0-4bad-83b1-5ce528bb9cc9)

My listening trends seem to be a bit more leaning to discovery. I try new artists regularly. If I like the song, I check the band. Some of these new band stick around for a while. New ones stay with me and become a new all-time favorite. I occasionally return back to some of my top artists like Molchat Doma and Radiohead.
