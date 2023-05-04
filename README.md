# Citi Bike Analytics – Using Tableau

Link for tableau public
https://public.tableau.com/app/profile/fekadu.habteyohannes/viz/NYCCitiBikeAnalysis_16832194582680/TopTenStartingStations2?publish=yes

# 1. Background
# Source of Dataset
Since 2013, the Citi Bike program has implemented a robust infrastructure for collecting data on the program's utilization. Each month, bike data is collected, organized, and made public on the  (webpage).
However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have questions about the program, so your first task on the job is to build a set of data reports to provide the answers.
# Aims of the Assignment
The task is to aggregate the data found in the Citi Bike Trip History Logs and find two unexpected phenomena by taking/ working with a timespan of any chosen period.
Design different visualization for each phenomenon and prepare story as well as dashboard.
In addition, visualization dashboard and analytical report for answering City officials’ questions is expected from the assignment.
Basic requirements for the analysis (key performance indicators) are already defined but the analysis should not be limited on them. Basic questions that need to be answered in the analysis process are stated as follows
    •	How many trips have been recorded during the chosen period?
    •	By what percentage has total ridership grown
    •	How has the proportion of short-term customers and annual subscribers changed
    •	What is the gender breakdown of active participants (Male v. Female)
    •	How effective has gender outreach been in increasing female ridership over the timespan
    •	What are the peak hours in which bikes are used during summer months?
    •	What are the peak hours in which bikes are used during winter months?
    •	What are the top 10 stations in the city for starting a journey
    •	What are the top 10 stations in the city for ending a journey
    •	What are the bottom 10 stations in the city for starting a journey
    •	What are the bottom 10 stations in the city for ending a journey
    •	How does the average trip duration change by age
    •	What is the average distance in miles that a bike is ridden
    •	Which bikes (by ID) are most likely due for repair or inspection in the timespan
    •	How variable is the utilization by bike ID
# 2.Implementation
# Data used
Winter months of December 2019 & January & February 2020 and summer months of June, July and August 2020
The Citi Bike System Data provides csv files that include:
Trip Duration (seconds) | Start Time and Date | Stop Time and Date | Start Station Name | End Station Name | Station ID | Station Lat/Long | Bike ID | User Type (Customer Subscriber) | Gender (Zero=unknown; 1=male; 2=female) | Year of Birth
Six months csv files have been downloaded and pre-processed in jupyter notebook however only five months aggregated data able to be saved. Thus months of December 2019 and January & February 2020 as well as June and July 2020 data are used for analysis.
# Data Analysis Process
Different month’s data merging and data cleaning (dropping unnecessary column and incomplete data).
Main data cleaning and transformation being done in jupyter notebook are mentioned as follows:
    o	Merging csv files
    o	df1 = pd.read_csv("Resources/201912-citibike-tripdata.csv")
    o	df2 = pd.read_csv("Resources/202001-citibike-tripdata.csv")
    o	df3 = pd.read_csv("Resources/202002-citibike-tripdata.csv")
    o	df4 = pd.read_csv("Resources/202006-citibike-tripdata.csv")
    o	df5 = pd.read_csv("Resources/202007-citibike-tripdata.csv")
    o	df6 = pd.read_csv("Resources/202008-citibike-tripdata.csv")
    o	Drop rows where the trip duration is less than 60 seconds (found that it wasn't working properly) and Convert trip duration column from seconds to minutes
    o	 Rename values in gender column with strings gender = {0:"Unknown", 1:"Male", 2:"Female"}
    o	Calculate the distance of each ride
    o	Calculate age of riders and delete all rows where user age is over 90(out layers) and category of users in age bins
# Creating visualizations
Cleaned and transformed data were loaded in Tableau and some visualizations were made to address the key performance indicators.
All the visualization outputs of tableau (each indicators output worksheets, story and dashboard) are uploaded in Tableau public in the following link:
https://public.tableau.com/app/profile/fekadu.habteyohannes/viz/NYCCitiBikeAnalysis_16832194582680/TopTenStartingStations2?publish=yes
# 3. Drawing conclusions
Some basic conclusions are flagged in each visualization story and dashboard. Additional major conclusions are able to be drawn from the analysis as follows:
    1.	Vast majority of riders are male and most of them are in age category of 18-29 fallowed by age group of 53-68. Youth are the main users of ridership. youth takes longer trip duration(may be for entertainment)
    2.	In summer season the pick hours is from 6:30am to 8:30am and afternoon from 4:30pm to 6:30pm summer months. This seems job entry/exit or coming in/out time from work. During summer from 3pm to 6pm is the peak hours when bikes are used (exit/coming out from work)
    3.	New stations are established in the year 2020 the locations are seems to be aligned with the city expansion and populations of neighborhoods.
    4.	Within 24 hours of a day 2am to 4am is assumed to be ideal time for bike maintenance.
    5.	The bottom ten stations are having very few ridership records that shows they are not functioning properly. Due considerations is required to  make decision on these satiations after further assessment
