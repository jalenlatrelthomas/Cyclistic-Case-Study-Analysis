# Cyclistic-Case-Study-Analysis

## Introduction & Overview
This case study gives an overview of the data analysis performed on trip data for Cyclistic, a rideshare company based in Chicago. Cyclistic features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day. 

The report will examine how annual members differ from casual riders across 6 months of data, 3 months from the winter and 3 from the summer. The data source used during the analysis is organized by distance using longitude and latitude. In addition, the data set includes Arrival and Departure Station Ids, delineated by membership types. The question asked by Cyclistic Stakeholders is: how do casual and membership riders differ from each other and how do we convert casual riders to annual memberships?

While cleaning data I found that certain ride IDs are missing start & end longitude, latitude, station name and IDs. I sorted the dataset based on the available start station names and tried to group them based on duration length, looking to associate missing station names & Ids with rides of the same duration that either started or ended in the same locations. However, due to the data being mock data, further analysis showed that not all stations were the same for ride lengths with the same start station name and similar ride length.

Though there were start station names and ids that were not present, I based the analysis around available start station names and ID’s and decided to focus my analysis on these metrics and how they impact membership differences on average. Therefore my numbers are as close to the averages as possible but will not be exact. I would need additional data around the missing start & end station names and IDs to determine exact trends around how they impact membership differences. 

For the purposes of this case study I used the 6 data sets below. I could not use all data from the same year due to the size of the file and the limitations of my space in google cloud. The data has been made available by Motivate International Inc. and can be found [[here](https://divvy-tripdata.s3.amazonaws.com/index.html)]. You can find the cleaned data sets and corresponding pivot tables at the links under the section titled Cleaned Data Sets & Ride Lengths and # of Rides by Day of Week.

December202012-divvy-tripdata

Jan202101-divvy-tripdata

February202102-divvy-tripdata

April202004-divvy-tripdata 

May202005-divvy-tripdata

June202006-divvy-tripdata

### Ride Length & Day of Week



The initial dataset does not include aggregated ride lengths and does not specify day of week in the time stamps for each ride. Additionally, ride length refers to the time frame the rideshare vehicle is checked out by any given user, it does not delineate between time parked and time used.  To calculate the ride lengths I used the tables below. The start and end times in columns C & D were used to aggregate ride lengths for each ride ID. The Day of Week was aggregated using a numeric key, 1=Sunday, 2=Monday etc. This allowed me to understand each ride on the basis of HHMMSS and the dates of each ride numerically.


