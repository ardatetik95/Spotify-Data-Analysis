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

**Parts:
**

**Part 1: Getting the Data
**

In this part, I talk about how you can get your own Extended Streaming History data. This part has no coding or analysis in it. You can skip it if you already know how to get
the data.

**Part 2: Transforming and Uploading the Data
**

In the second part, I used Python, Excel to transform and SSIS to compile the data. I also used Microsoft SQL Server to create a data warehouse for my compiled data.

**Part 3: Cleaning the Data
**

In the third part, I cleaned the data in SQL and prepared it for analysis in Python.

**Part 4: Exploring and Analysing the Data
**

In the fourth and the last part, I took my data into Python and started analysing it according to my main purposes. I used Pandas library for general analysis
and Matplotlib library for simple visualization.

**Final Analysis:
**

**- T3: TTo find my top artists and tracks
**

![topsongs](https://github.com/user-attachments/assets/0fc3d7cc-519b-4034-b24a-761493e2adf8)


*T3.1: My top listened track in milliseconds is Sky Lab by Electronic Systems. This was unexpected. This song is 14:16 minutes long and I listened it a lot, so it came
out on top. Interestingly, some of my top 10 songs are not from my top 10 artists.

![topartist](https://github.com/user-attachments/assets/4e848403-5f9e-41f9-8676-ced4554e566a)

*T3.2: My top artist by playtime is Radiohead. I had a depressed era in 2023 and I blasted Radiohead too much (I'm glad im beyond that era, but i still love Radiohead).
Most of the bands in top 10 are the ones I have been listening since 2022 except Molchat Doma and Russian Circles. I met those bands in 2024 and they took their
places in the top.

**-T4: To find Date and Time trends in my listening habits**


**T4.1: Yearly Trends:
**

![year](https://github.com/user-attachments/assets/4cf1e640-2b23-4a14-9340-57a7e00cf1e1)

*T4.1.1: I started using Spotify regularly in 2021. Before that, I tried the platform several times between 2017-2020.

*T4.1.2: My listening time increased in 2022 and peaked in 2023. It decreased a bit in 2024.

*T4.1.3: This project is being done in February-March of 2025, so I only have data until the 18th of February. That's why the data is showing the 2025's listening time low.

![topinyears](https://github.com/user-attachments/assets/59c30fba-9ed2-4880-81eb-6c5c7bb96b84)

*T4.1.4: I discovered that every year, my top artist changes. Some of the previous years'top artists stay in the top 10 next year.

*T4.1.5: Even though I have some all time favorites in many years like All Them Witches and Opeth, I tend to add new names to top 10 artists every year.


**T4.2: Monthly Trends:
**

![months](https://github.com/user-attachments/assets/74cc6e5d-21b2-4e87-8f24-bc01c4faf64d)

*T4.2.1:When we check the monthly listening time data, we can see that my listening time peaks in Summer and Winter.

*T4.2.2:Especially the period between June-July and December-January I listen the most.

*T4.2.3:We can roughly say that I listen less in Autumn and Spring


**T4.3: Weekly Trends:
**

![weekdays](https://github.com/user-attachments/assets/cd3552b6-1ae3-454e-b6ad-55cb1796f78f)

*T4.3.1: The days that I listen the most is Monday, Wednesday and Sunday. Tuesday and Thursday are very close to each other and to Sunday.

*T4.3.2: I tend to listen less in Friday and Saturday.


**T4.4: Daily Trends:
**

*T4.4.1:My listening time peaked in the 11th of June 2022, the peak listening dates are mostly from the summer of 2022(focusing mostly on June with few exceptions).

![hours](https://github.com/user-attachments/assets/a3c79888-25c9-4087-9c7d-dd224f837f38)

*T4.4.2: My favorite listening hours are around 14:00-17:00 and 21:00-00:00

*T4.4.3: I start to listen around 14:00 and tend to keep up until 18:00 - 20:00, where it plummets down

*T4.4.4: Starting with 20:00, it starts to rise again, it peaks around 21:00 and 22:00, decreasing down by 01:00

*T4.4.5:We can say that my top listening times are in the late afternoon mid to late evening. You can find me with headsets around 14:00-17:00 and 20:00-23:00.


-To find the most skipped, picked and finished tracks


-To find correlations about why I skip a song

-To find if I am prone to listen some band repeatedly or do I explore new bands regularly

