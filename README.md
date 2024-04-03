# Cyclistic-Case-Study-Analysis

## Introduction & Overview
This case study gives an overview of the data analysis performed on trip data for Cyclistic, a rideshare company based in Chicago. Cyclistic features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day. 

The report will examine how annual members differ from casual riders across 6 months of data, 3 months from the winter and 3 from the summer. The data source used during the analysis is organized by distance using longitude and latitude. In addition, the data set includes Arrival and Departure Station Ids, delineated by membership types. The question asked by Cyclistic Stakeholders is: how do casual and membership riders differ from each other and how do we convert casual riders to annual memberships?

While cleaning data I found that certain ride IDs are missing start & end longitude, latitude, station name and IDs. I sorted the dataset based on the available start station names and tried to group them based on duration length, looking to associate missing station names & Ids with rides of the same duration that either started or ended in the same locations. However, due to the data being mock data, further analysis showed that not all stations were the same for ride lengths with the same start station name and similar ride length.

Though there were start station names and ids that were not present, I based the analysis around available start station names and ID’s and decided to focus my analysis on these metrics and how they impact membership differences on average. Therefore my numbers are as close to the averages as possible but will not be exact. I would need additional data around the missing start & end station names and IDs to determine exact trends around how they impact membership differences. 

For the purposes of this case study I used the 6 data sets below. I could not use all data from the same year due to the size of the file and the limitations of my space in google cloud. The data has been made available by Motivate International Inc. and can be found [here](https://divvy-tripdata.s3.amazonaws.com/index.html). You can find the cleaned data sets and corresponding pivot tables at the links under the section titled Cleaned Data Sets & Ride Lengths and # of Rides by Day of Week.

December202012-divvy-tripdata

Jan202101-divvy-tripdata

February202102-divvy-tripdata

April202004-divvy-tripdata 

May202005-divvy-tripdata

June202006-divvy-tripdata

### Ride Length & Day of Week



The initial dataset does not include aggregated ride lengths and does not specify day of week in the time stamps for each ride. Additionally, ride length refers to the time frame the rideshare vehicle is checked out by any given user, it does not delineate between time parked and time used.  To calculate the ride lengths I used the tables below. The start and end times in columns C & D were used to aggregate ride lengths for each ride ID. The Day of Week was aggregated using a numeric key, 1=Sunday, 2=Monday etc. This allowed me to understand each ride on the basis of HHMMSS and the dates of each ride numerically.

<img width="318" alt="Screen Shot 2024-03-25 at 12 56 25 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/4c9e4e01-29cb-4290-b562-62a24d2a838b">

<img width="310" alt="Screen Shot 2024-03-25 at 12 56 09 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/c736b493-4126-4bad-afa4-d1c1f332f308">

## Average Ride Length & Per Day of Week
I used the aggregated ride lengths to compile the pivot table below. The table shows the average ride per day of week by membership type. This helps to identify what days of the week experience the highest number of rides, organizing them by membership type on average.

<img width="296" alt="Screen Shot 2024-03-25 at 1 02 49 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/efc0bb84-ac67-43b4-8184-ee5540a7c808">
<img width="359" alt="Screen Shot 2024-03-25 at 1 03 00 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/90e0f6d2-4b51-4d14-9437-88369fe4b6e7">

## Count of rides per Day of Week
I added the count of rides to the pivot table above, to provide further insight into the number of rides per day of week, and grouped them by membership type. 

<img width="689" alt="Screen Shot 2024-03-25 at 1 05 20 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/b2bf4a71-6eba-4897-81ee-65a88336ec1e">

## Mode of Ride Length, Day of Week & # of Mode Rides
Mode of ride length & day of week was calculated for each dataset to aggregate the ride length most frequented per month and the days that experienced the highest number of rides on average. 

<img width="418" alt="Screen Shot 2024-03-25 at 1 08 24 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/7903b362-da5d-4e73-81fe-650f3e74a90f">

## Cleaned Data Sets, Ride Lengths and # of Rides by Day of Week:

[Ride Length & # of Rides By Day of Week February](https://docs.google.com/spreadsheets/d/1LEwkYq1PjTjEe4oLYj-9U9xrLK3gX3j287tq6oa3Bio/edit#gid=2142493916)

[Ride Length & # of Rides By Day of Week January](https://docs.google.com/spreadsheets/d/1eEE-p4uyeG3fEuHpyc9kpGu9nIp6dDi7c1oX6SRcIjc/edit#gid=916359140)

[Ride Length & # of Rides By Day of Week December](https://docs.google.com/spreadsheets/d/10NVAol5Tmh2Yqg1ESbApo6AiFb4fyu5zdpsHbyc6NFo/edit#gid=1439903572)

[Ride Length & # of Rides By Day of Week April](https://docs.google.com/spreadsheets/d/1sVyhf9NU7fOG02B3N02IEl4FB4nam7fgzNtORperVgE/edit#gid=749954461)

[Ride Length & # of Rides By Day of Week May](https://docs.google.com/spreadsheets/d/170CiR4kz0bMbfsRtHoOGmk1ap11ggD2nuZzrjdV2iQc/edit#gid=1974284798)

[Ride Length & # of Rides By Day of Week June](https://docs.google.com/spreadsheets/d/1Bk-Yo5xGh8Ty_VeSdJHMA3gPu1nNo_MCnRFmMiUtudQ/edit#gid=96394589)

<img width="765" alt="Screen Shot 2024-03-25 at 1 14 09 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/e32a34ef-dc54-425a-8d10-7961c4a97bdb">

# ANALYSIS:

## Number of Rides

The tables below highlight the highest number of rides by day of week for each month and the day of the week that averaged the highest number of rides for each membership type. 

<img width="1006" alt="April   May" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/91892f27-7667-4197-9d0c-11f6175c3693">
<img width="945" alt="Dec" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/61f5d327-78a3-44c3-b8bc-1c9ef78fc8ae">
<img width="943" alt="Feb" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/912d20c1-c0e5-4ee7-ab67-2863d14df3d6">
<img width="955" alt="Jan" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/15e045fa-77be-44db-9896-6cf3aa68ce31">
<img width="952" alt="June" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/7d78e46b-7646-40c6-be86-8a5fdd867616">


**MEMBERSHIP RIDERS** (29.2% Difference)
Avg. Highest # of Rides by Day of Week: Saturday 16276
Avg. Lowest # of Rides by Day of Week: Monday 12134


**CASUAL RIDERS** (58.7% Difference)
Avg. Highest # of Rides by Day of Week: Sunday 10320
Avg. Lowest # of Rides by Day of Week: Monday 5636

Membership Riders ride at 44.8% higher rates on average, than Casual Riders.

## Number of Rides per Day of Week (Member)
<img width="606" alt="Screen Shot 2024-03-25 at 1 16 14 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/8d7f182c-d427-4f29-a8cf-c40a958eddb8">

## Number of Rides per Day of Week (Casual)
<img width="604" alt="Screen Shot 2024-03-25 at 1 16 59 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/caa913d8-1f00-4bca-b092-c994519205c6">

## Ride Length 
The tables below highlight the longest ride lengths for each day of the week grouped by month. The tables also show the longest average ride length and are grouped by membership type. 

**MEMBERSHIP RIDERS**

Longest Ride Length on Average: Sunday 0:19:30 

Shortest Ride Length on Average: Tuesday -1:05:14 

**CASUAL RIDERS**

Longest Ride Length on Average: Friday 0:53:05

Shortest Ride Length on Average: Tuesday -0:47:04

Casual riders average 92.83% longer ride lengths than membership riders. 

**AVG Ride Length per Day of Week (Member)**

<img width="607" alt="Screen Shot 2024-03-25 at 1 21 21 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/144be507-fded-4e72-9b5f-9e0f525b9777">

**AVG Ride Length per Day of Week (Casual)**

<img width="609" alt="Screen Shot 2024-03-25 at 1 22 06 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/6f938b57-7d1d-4775-ad65-0cc1553fa13e">

## **MOST FREQ. RIDE ID & CORRESPONDING START STATION:**

**December**: Clark St & Elm St (TA1307000039) 

[Query 1](https://console.cloud.google.com/bigquery?sq=589920680070:9a1cfd8c00f0471d948c00eeef16e484)

[Query 2](https://console.cloud.google.com/bigquery?sq=589920680070:23070268e2dc459891cab1cd651329c9)

**Jan**: Clark St & Elm St (TA1307000039)

[Query 1](https://console.cloud.google.com/bigquery?sq=589920680070:6865a27c63db4e64811d5bcac7e8e558)

[Query 2](https://console.cloud.google.com/bigquery?sq=589920680070:446b488a96d54c33bb0668bf96821e70)

**Feb**: Dearborn St & Erie St (13045)

[Query 1]

[Query 2]

**April**: Clark St & Elm St (176)

[Query 1](https://console.cloud.google.com/bigquery?sq=589920680070:0b0d26d56c4d4d79a0fc687dc4b6338a)

[Query 2](https://console.cloud.google.com/bigquery?sq=589920680070:a0299ee0a7744b72b95a8267c039aeb7)

**May**: Clark St & Elm St (176)

[Query 1](https://console.cloud.google.com/bigquery?sq=589920680070:f7cf08b37974477fbb33c8b35d9a1ea4)

[Query 2](https://console.cloud.google.com/bigquery?sq=589920680070:facd8aae6c724f4784e064af218a4762)

**June**: Streeter Dr & Grand Ave (35)

[Query 1](https://console.cloud.google.com/bigquery?sq=589920680070:9703730501b0472abeba3214a401f767)

[Query 2](https://console.cloud.google.com/bigquery?sq=589920680070:facd8aae6c724f4784e064af218a4762)

<img width="707" alt="Screen Shot 2024-03-25 at 1 29 35 PM" src="https://github.com/jalenlatrelthomas/Cyclistic-Case-Study-Analysis/assets/162640411/0a90e825-cf2b-4dc7-b619-368ca7370aca">

# **SOLUTION PROPOSAL:**

To answer Cyclistic’s question: how do casual and membership riders differ from each other, we see that on average Membership Riders ride at 44.8% higher rates than Casual Riders. We see that Casual riders average 92.83% longer ride lengths than membership riders. Additionally, the start station at Clark St & Elm St. experiences the highest number of rides on average across data sets for both membership types, and we see the average highest number of rides on Saturday and Sunday throughout the year. 

Cyclistic can increase its membership conversion rate by providing 3 incentives to its consumer base. The first would be a referral program that gives membership riders X amount of rides for free upon a referred member's first ride. The second would be to provide the first 5 rides at a discounted rate when casual members convert to membership status. Both of these measures incentivize not only membership conversion but actual use of the membership. The 3rd incentive would be discounted rides on weekends for all membership riders. Given that these are days that both membership types experience high ride rates, it could incentivize casual riders to convert to membership status on the basis of convenience as these are days that already experience high ride rates. 















