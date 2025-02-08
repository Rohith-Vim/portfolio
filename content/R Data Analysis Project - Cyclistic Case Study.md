---
title: R Data Analysis Project - Cyclistic Case Study
---

---
## Preface

> [!abstract] Summary
> Cyclistic is a bike-sharing company based out of Chicago. The company has two types of users:
> - Casual Users
> - Paying Members
> 
> Cyclistic is attempting to discern how to convert more casual users into paying members, as the company believes this will align with their long-term strategy for success. 
> 
> As part of this, one of the key pieces of information the marketing team needs is regarding the differences in Cyclistic usage by both groups. 
> 
> **My responsibility for this case study is to analyse the data, providing insights and recommendations for how casual users and paying members differ, and how we can create more paying customers of Cyclistic's service.**
> 
> The results of my analysis can be viewed by navigating to the [Findings](https://rohith-vim.github.io/portfolio/Data-Analysis--and--Report---Cyclistic-Case-Study#findings) section, and my recommended actions for Cyclistic can be viewed under the [Recommendations](https://rohith-vim.github.io/portfolio/Data-Analysis--and--Report---Cyclistic-Case-Study#recommendations) section.

---

I completed this case study with **R**, **Tableau**, and **Excel**. 

The completed report was made with **R Markdown**, as this allows for the representation of my code with its consequent output, enabling reproducibility of the problem-solving process I used.

To access the original report in R Markdown format, visit [this link](https://rohith-vim.github.io/cyclistic-case-study/).

**Companion Files:**

- For a changelog containing modifications I made to the data, visit [this link](https://rohith-vim.github.io/cyclistic-case-study-changelog/).
- To interact with the Tableau visualisations I made as part of this case study, visit the following links:
	- Mapping the Most Popular Start & End Stations for [Casual Users](https://public.tableau.com/views/CyclisticCaseStudy-CasualUsersBook/Dashboard1?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link).
	- Mapping the Most Popular Start & End Stations for [Annual Members](https://public.tableau.com/views/CyclisticCaseStudy-AnnualMembersBook/Dashboard1?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link).

---
## Scenario 

> [!info] Case Study Scenario 
> You are a junior data analyst working on the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.


From this, the business goal as I infer it is:

'**Design a marketing strategy, evidenced by the data, to convert Cyclistic’s casual riders into annual members.**'

As an analyst on this project, it is my responsibility to organise and gather insights from the data to support the creation of this marketing strategy. 

---
## Understanding the Problem

The marketing team outlines the following 3 questions to guide their effort toward the aforementioned business goal:

1.	How do annual members and casual riders use Cyclistic bikes differently?
2.	Why would casual riders buy Cyclistic annual memberships?
3.	How can Cyclistic use digital media to influence casual riders to become members?

The case study mentions that my manager and the Director of Marketing, Lily Moreno, has assigned me to specifically answer the first of the 3 questions. To bring clarity to the task at hand, I reformulated it following the SMART question approach:

'**How have Cyclistic’s casual and annual-membership users differed in their use of the service over the previous year?**'

My deliverable for this assignment is a report containing the following information:

1.	A clear statement of the business task 
2.	A description of all data sources used 
3.	Documentation of any cleaning or manipulation of data 
4.	A summary of the analysis 
5.	Supporting visualizations and key findings 
6.	Three key recommendations based on the analysis

These points will be addressed over the course of this report.

---
## Scope of Work (SoW)

#### Business Task:

'**How have Cyclistic’s casual and annual-membership users differed in their use of the service over the previous year?**'

#### Major Project Activities:

| **Activity**                                                                                       | **Description**                                                                                                                                                                                                                               |
| -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Data Collection                                                                                    | Collect relevant data from data source provided with the case study.                                                                                                                                                                          |
| Identify Attributes Featuring Noticeable Differences Between Casual & Annual Membership Users      | Work through data and identify trends where casual and annual membership users differ, taking note of the most prominent ones.                                                                                                                |
| Create Visualisations to Communicate Findings Where Differences Between User Types Are Significant | Decide upon and create effective diagrams/graphics to represent attributes where users differ.                                                                                                                                                |
| Deliver Final Report                                                                               | Deliver final report containing information on key areas in which user types differ, positing why those differences occur and how they can be worked with the increase memberships, supplemented by visualisations to better share this idea. |

#### This Project Does Not Include:

-	Implementation of solutions or recommendations.
-	Suggestion of digital media strategies to create more members.
-	Consideration of any data that is older than 1 year.

#### Deliverables:

-	**Final Report** (*Fulfilled By This Document*)
-	**Changelog** (*See Companion Files*)
-	**Visualisations of Attributes Where Casual and Annual-Membership Users Differ** (*Fulfilled By This Document*)
-	**Recommendations Based Upon the Findings** (*Fulfilled By This Document*)

#### Schedule & Milestones:

| **Activity**                                        | **Date of Activity (Estimated)** | **Description**                                                     |
| --------------------------------------------------- | -------------------------------- | ------------------------------------------------------------------- |
| Data Review                                         | _7/05/2024_                      | Complete review, clean up, and confirm understanding of data.       |
| Data Analysis                                       | _8/05/2024_                      | Conduct analysis on data.                                           |
| Identification of Key Attributes Where Users Differ | _8/05/2024_                      | Identify key areas where casual and annual-membership users differ. |
| Creation of Visuals                                 | _9/05/2024_                      | Produce visuals representing user differences.                      |
| Final Report                                        | _10/05/2024_                     | Produce report outlining my findings.                               |
|                                                     |                                  |                                                                     |

Estimated Date of Completion: **11th of May 2024**

---
## Data Sources Used

For this case study, data for the analysis was collected from [this link](https://divvy-tripdata.s3.amazonaws.com/index.html) (made available by Motivate International Inc. under [this license](https://divvybikes.com/data-license-agreement), as Cyclistic is a fictional company). The data we will be using is from 2021, categorized by the months of the year at the data source. 

To make this information easier to work with, we will be combining the 12 datasets from 2021 into a single dataset comprised of over 5 million records. This involves downloading and extracting each month’s dataset before uploading and combining them via RStudio, where we will also be conducting the cleaning, organisation, and analysis.

Files will also be renamed for ease of use. 

|  E.g. *‘202101-divvy-tripdata’ --> ’01-2021-tripdata’*

---
## Changelog

The changelog is available as a separate companion file to this report at [this link](https://rohith-vim.github.io/cyclistic-case-study-changelog/).

---

> [!info] Note
> To view the output of the following R code chunks, view the original R Markdown document at [this link](https://rohith-vim.github.io/cyclistic-case-study/).

---
## Environment Setup

Notes: To begin, we will set up the environment by installing and loading `tidyverse` (comes with `ggplot2`), `janitor`, `lubridate` and `circular`. Ensure these packages are installed before they are loaded.

```{r initialise, message=FALSE, warning=FALSE}
#load packages
library(tidyverse)
library(janitor)
library(lubridate)
library(ggplot2)
library(circular)
```

---
## Import Data Files

Notes: Next, we import the Cyclistic data files, which are formatted as CSVs. These files will also be renamed for ease of use during analysis.

*If you are attempting to follow this report's steps, it's important that you change the file address depending upon where you've stored the case study data.*

```{r import}
#import CSVs

jan21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/01-2021-tripdata.csv")
feb21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/02-2021-tripdata.csv")
mar21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/03-2021-tripdata.csv")
apr21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/04-2021-tripdata.csv")
may21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/05-2021-tripdata.csv")
jun21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/06-2021-tripdata.csv")
jul21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/07-2021-tripdata.csv")
aug21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/08-2021-tripdata.csv")
sep21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/09-2021-tripdata.csv")
oct21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/10-2021-tripdata.csv")
nov21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/11-2021-tripdata.csv")
dec21 <- read.csv("C:/Users/username/Documents/Cyclistic Case Study/2021_trip_data/12-2021-tripdata.csv")

```

---
## Check for Discrepancies

Notes: Before merging the CSVs into a single dataset, we will ensure all data files are identically formatted and that they can be brought together without issues. We will use the `str` function to output the variable names and data types, ensuring these are aligned across all datasets. This is also an opportunity to see if any field has been assigned the wrong data type and to correct this if necessary.

```{r check, message=FALSE, warning=FALSE}
#check datasets for discrepancies

str(jan21)
str(feb21)
str(mar21)
str(apr21)
str(may21)
str(jun21)
str(jul21)
str(aug21)
str(sep21)
str(oct21)
str(nov21)
str(dec21)

```

For reference, the following is the output if we run the first `str()` command:


> [!info] Case Study Scenario 
> ![visualisation 1](cyclistic_dem1.png)


We notice that the `started_at` and `ended_at` fields are wrongly formatted. These should be *POSIXct*, not *character* format. However, given that we will be merging the datasets shortly, instead of having to convert formats across 12 datasets, we will merge the data before converting these fields.

---
## Merge Data Files

Notes: Now we can merge the CSV files into a single, new dataset, known as a dataframe in R.

```{r merge}
#merges data files into dataframe

dataframe_2021 <- bind_rows(jan21, feb21, mar21, apr21, may21, jun21, jul21, aug21, sep21, oct21, nov21, dec21)

```

---
## Initial Cleaning of the New Dataset

Notes: With `dataframe_2021` created, it's time to clean the data and ensure it's ready for analysis. To start the cleaning process, we will clean field names for consistency using `clean_names()`, remove empty rows/columns using `remove_empty()`, and convert the `started_at` and `ended_at` fields to a `POSIXct` format, which represents calendar time.

```{r clean}
#clean and remove spaces and formatting inconsistences

dataframe_2021 <- clean_names(dataframe_2021)

#remove empty rows and columns

dataframe_2021 <- remove_empty(dataframe_2021, which = c())

#convert fields to correct format

dataframe_2021[['started_at']] <- as.POSIXct(dataframe_2021[['started_at']], 
                                   format = "%Y-%m-%d %H:%M:%S")

dataframe_2021[['ended_at']] <- as.POSIXct(dataframe_2021[['ended_at']], 
                                   format = "%Y-%m-%d %H:%M:%S")

```

---
## Processing the New Dataset

Notes: Continuing, based on what we can infer from the data, we realise we can extract more value from it if we create a few new columns. Currently, the data is primarily of use at the 'ride level'; that is, it's helpful for analysing rider patterns and popular routes. 

In order to align the data with the business task and make it more useful for extracting 'user level' insights, we can add the following fields.

```{r processing, warning=FALSE}
#add columns for 'start hour', 'day', 'month', 'trip duration' and 'trip distance'

dataframe_2021 <- dataframe_2021 %>%
  mutate(start_hr = hour(started_at)) %>%
  mutate(day = wday(started_at, label = TRUE, abbr = TRUE)) %>%
  mutate(month = month(started_at, label = TRUE, abbr = TRUE)) %>%
  mutate(trip_duration = difftime(ended_at, started_at)) %>%

#`trip_distance` requires the below formula as we're converting latitude and longitude to a distance value.

  mutate(trip_distance = acos(sin(rad(start_lat))*sin(rad(end_lat))+cos(rad(start_lat))
                              *cos(rad(end_lat))*cos(rad(end_lng)-rad(start_lng)))*6371)

```

---
## Final Cleaning of the New Dataset

Notes: With the data optimised for 'user level' analysis, the last step we'll complete is to remove any trips with a duration of less than 0 seconds. This way, no erroneous records will affect our analysis.

The easiest way to do this would be to create a final, new dataset, and to store the useful records here.

```{r erroneous_data}
#remove records with 'trip_duration < 0'

dataframe_2021_clean <- dataframe_2021[!(dataframe_2021$trip_duration<=0),]

```

---
## Visualisation 1 - Number of Rides by Cyclistic Member Type Charted Over A Week

Notes: Using `dataframe_2021_clean`, we can now begin to extract insights from our data. As a reminder, our business task is as follows:

**"How have Cyclistic’s casual and annual-membership users differed in their use of the service over the previous year?”**

With this task in mind, let's start with a chart comparing the total number of rides by casual users and members in 2021 charted over the course of a week.

```{r, fig.align='center', user_in_a_week}

#`scipen` used to output `Number of Rides` in a non-exponential format

options(scipen = 100, digits = 4)

#creates a bar chart showing number of rides by cyclistic member type charted over a week

ggplot(dataframe_2021_clean, aes(x=day, fill=member_casual)) + 
  geom_bar(position="dodge", alpha=0.7) +
  labs(title="Number of Rides by Member Type Across A Week (2021)",
       x="Day",
       y="Number of Rides",
       fill="Member Type") +
  scale_fill_manual(values=c("red", 
                             "blue"))

```


> [!ABSTRACT] Visual 1: Number of Rides by Member Type Across A Week
> ![visualisation 1](cyclistic_viz1.png)

Observations: 

**We find that members account for more rides on weekdays**, whereas, **on weekends, we see an uptick in casual user rides**. 

This might be due to members using Cyclistic as a primary method of transportation between residences and workplaces/schools, whereas casual users are more likely to engage with Cyclistic for entertainment/recreational use. For such users, a membership may seem excessive, as they would only make use of Cyclistic on weekends.

However, this isn't enough to make a concrete assumption on. To find out more, let's analyse more fields.

---
## Visualisation 2 - Number of Rides by Cyclistic Member Type Charted Across the Months of the Year

Notes: Next, lets compare the total number of rides by casual users and members in 2021 charted across the months of the year.

```{r, fig.align='center', users_p_month_in_year}

#`scipen` used to output `Number of Rides` in a non-exponential format

options(scipen = 100, digits = 4)

#creates a bar chart showing the number of rides by cyclistic member type charted across the months of the year

ggplot(dataframe_2021_clean, aes(x=month, fill=member_casual)) + 
  geom_bar(position="dodge", alpha=0.7) +
  labs(title="Number of Rides by Member Type Across the Months of the Year (2021)",
       x="Month",
       y="Number of Rides",
       fill="Member Type") +
  scale_fill_manual(values=c("red", 
                             "blue"))

```


> [!ABSTRACT] Visual 2: Number of Rides by Member Type Across the Months of the Year
> ![visualisation 2](cyclistic_viz2.png)


Observations:

It appears as though **members account for more trips in all months bar the summer ones of June, July and August, when casual users overtake them**. Following on with our theory of entertainment and recreational use, casual users seem more inclined to engage with Cyclistic when they have holidays. It's worth noting that June, July and August coincide with summer vacation time for many schools, and families may take holidays to enjoy the good weather and to cycle around the city. We will attempt to reinforce this notion in a later visualisation.

On the topic of seasons, we also see that more trips are taken in the summer months than in the winter ones. Given that Cyclistic is based in Chicago, this is likely explained by temperature differences, where summer months are milder and winter ones more extreme.

---
## Visualisation 3 - Hourly Use of Bikes by Member Type Across A Week

Notes: To learn more about the times at which Cyclistic bikes were used in 2021, the next visual will chart hourly bike usage by members and casual users over a week.

```{r, fig.width=16,fig.height=8, fig.align='center', hourly_bike_use}

#`scipen` used to output `Number of Rides` in a non-exponential format

options(scipen = 100, digits = 4)

#creates a bar chart showing the hourly use of bikes by member type across a week

ggplot(dataframe_2021_clean, aes(x=start_hr, fill=member_casual)) + 
  geom_bar(position="dodge", alpha=0.7) +
  scale_x_continuous(breaks=seq(00,23,1)) +
  facet_wrap(~day) +
  labs(title="Hourly Use of Bikes by Member Type Across A Week (2021)",
       x="Hour",
       y="Number of Rides",
       fill="Member Type") +
  scale_fill_manual(values=c("red", 
                             "blue"))

```


> [!ABSTRACT] Visual 3: Hourly Use of Bikes by Member Type Across A Week
> ![visualisation 3](cyclistic_viz3.png)


Observations:

Further providing evidence for the leisure/work difference we've uncovered, a breakdown of use by hour across a week shows that, **on weekdays, members account for more trips, whereas on weekends, casual users once again climb higher**. On Friday and Saturday, when most people have days off, casual use of Cyclistic's bikes increases. On weekdays, members make up for the majority, with spikes in trips between 7-9AM (morning commute to work/school hours) and 3-7PM (afternoon/evening commute to home hours).

Thus far, the data seems to suggest that casual users engage with Cyclistic in their free time and for leisure, whereas members use Cyclistic bikes as a primary method of transportation.

---
## Visualisation 4 - Average Trip Duration Between Casual and Annual Membership Users

Notes: Another useful visualisation would be to map the difference in average trip duration between Cyclistic user types. 

```{r avg_duration, message=FALSE, warning=FALSE, fig.align='center',}

#`scipen` used to output `Number of Rides` in a non-exponential format

options(scipen = 100, digits = 4)

#creates a bar chart showing the average trip duration for casual and annual membership users

ggplot(dataframe_2021_clean, aes(x = member_casual, y = trip_duration, fill=member_casual)) + 
  geom_bar(position="dodge", 
           alpha=0.7, 
           stat="summary", 
           fun="mean") +
  labs(title="Average Trip Duration by Member Type (2021)",
       x="Member Type",
       y="Trip Duration (s)",
       fill="Member Type") +
  scale_fill_manual(values=c("red", 
                             "blue"))

```


> [!ABSTRACT] Visual 4: Average Trip Duration by Member Type
> ![visualisation 4](cyclistic_viz4.png)


Observations:

In a rather surprising find, **casual users take trips almost double the length of members**. When we align this with our prevailing hypothesis, it appears to lend it credence. Casual users likely take lengthy bike rides as part of their entertainment, meaning they, on average, would spend longer on their trips than paying members, who have dedicated routes they take with their Cyclistic bikes.

It may also be a question of value. For casual users, who likely pay a one-time fee to take a single trip, they would want to maximise their use of the bike, whereas members, who may pay a flat fee for unlimited trips, are less likely to be concerned about maximising their trip duration.

---
## Visualisation 5 - Average Trip Distance Between Casual and Annual Membership Users

Notes: Following the previous graphic, lets also look compare the average trip distance between Cyclistic user types. 

```{r avg_distance, message=FALSE, warning=FALSE, fig.align='center'}

#`scipen` used to output `Number of Rides` in a non-exponential format

options(scipen = 100, digits = 4)

#creates a bar chart showing the average trip distance for casual and annual membership users

ggplot(dataframe_2021_clean, aes(x = member_casual, y = trip_distance, fill=member_casual)) + 
  geom_bar(position="dodge", 
           alpha=0.7, 
           stat="summary", 
           fun="mean") +
  labs(title="Average Trip Distance by Member Type (2021)",
       x="Member Type",
       y="Trip Distance (km)",
       fill="Member Type") +
  scale_fill_manual(values=c("red", 
                             "blue"))

```


> [!ABSTRACT] Visual 5: Average Trip Distance by Member Type
> ![visualisation 5](cyclistic_viz5.png)


Observations:

**Interestingly, casual users and members appear to take trips that cover close to the same distance**. Though, alone, this data doesn't offer much in the way of insight, we can combine our findings from the previous visualisation to reinforce our existing propositions.
Since it appears that members complete journeys of a similar length to casual users in less time, they may do so with the intent of reaching a destination by a deadline. Casual users, perhaps using Cyclistic bikes in their free time, are in no particular hurry to meet or follow a schedule. Hence, they complete their trips at a leisurely pace.

All in all, our graphed findings have lent a great deal of support to the theory of casual/member use of Cyclistic services which has been explored throughout these sections.

To continue, lets take another approach with the data.

---
## Visualisation 6 - Mapping the Most Popular Start & End Stations for Casual Users

Notes: The remaining visualisations will be mapped. To facilitate this, we will export data on the 10 most commonly used start and end stations by Cyclistic casual users, which we can combine into a single dataset via Excel before visualising with Tableau.

*If you would like to view the viz with additional information including specific trip count and ranking details, visit [this link](https://public.tableau.com/views/CyclisticCaseStudy-CasualUsersBook/Dashboard1?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link)*.

```{r casual_user_stations}

## Create Subset of Dataframe with A Count for Start Station Usage By Casual Users

top_start_stations_users <- dataframe_2021_clean %>% 
  filter(member_casual=="casual") %>%
  count(start_station_name, sort = TRUE)

## Remove Top Value (Which is Empty) and Keep Only the Top 10 Start Stations and Their Trip Count

top_start_stations_users <- head(top_start_stations_users, 11)
top_start_stations_users <- top_start_stations_users[-1,]
rownames(top_start_stations_users) <- NULL

## Declare Vectors for Start Station Latitude and Longitude, Which We Need for the Export

top_user_start_streets_lat <- c(41.89228, 41.88103, 41.90096, 41.86723, 41.92628,
                                41.91213, 41.88096, 41.91569, 41.90322, 41.86789)

top_user_start_streets_long <- c(-87.61204, -87.62408, -87.62378, -87.61536, -87.63083,
                                 -87.63466, -87.61674, -87.63460, -87.63432, -87.62304)

## Add Vectors for Start Station Latitude and Longitude to the Subset of Top 10 Start Stations

top_start_stations_users$start_lat <- top_user_start_streets_lat

top_start_stations_users$start_long <- top_user_start_streets_long

## Create CSV File to Export

write.csv(top_start_stations_users, "casual_start_stations.csv")

## Create Subset of Dataframe with A Count for End Station Usage By Casual Users

top_end_stations_users <- dataframe_2021_clean %>% 
  filter(member_casual=="casual") %>%
  count(end_station_name, sort = TRUE)

## Remove Top Value (Which is Empty) and Keep Only the Top 10 End Stations and Their Trip Count

top_end_stations_users <- head(top_end_stations_users, 11)
top_end_stations_users <- top_end_stations_users[-1,]
rownames(top_end_stations_users) <- NULL

## Declare Vectors for End Station Latitude and Longitude, Which We Need for the Export

top_user_end_streets_lat <- c(41.89228, 41.88103, 41.90096, 41.92628, 41.86723,
                                41.91213, 41.88096, 41.91172, 41.91569, 41.89147)

top_user_end_streets_long <- c(-87.61204, -87.62408, -87.62378, -87.63083, -87.61536,
                                 -87.63466, -87.61674, -87.62680, -87.63460, -87.62676)

## Add Vectors for End Station Latitude and Longitude to the Subset of Top 10 End Stations

top_end_stations_users$end_lat <- top_user_end_streets_lat

top_end_stations_users$end_long <- top_user_end_streets_long

## Create CSV File to Export

write.csv(top_end_stations_users, "casual_end_stations.csv")

```


> [!ABSTRACT] Visual 6: Casual Users - Most Popular Stations
> ![visualisation 6](cyclistic_viz6.png)
> This visual was made in Tableau. To interact with it, visit [this link](https://public.tableau.com/views/CyclisticCaseStudy-CasualUsersBook/Dashboard1?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link).


Observations:

**Casual users most commonly make use of Cyclistic's services in prominent tourist/leisure areas within Chicago**. Looking at the map, we see trips starting across the shorefront, and between destinations such as 'Shedd Aquarium', 'Theater on the Lake', and around 'Lincoln Park Zoo'. We see a reasonable variety between start and stop stations, indicating that users aren't bound to a particular path/destination in their trips.

---
## Visualisation 7 - Mapping the Most Popular Start & End Stations for Annual Members

Notes: Now we will export data on the 10 most commonly used start and end stations by Cyclistic annual members, which we will also combine via Excel represent with Tableau.

*If you would like to view the viz with additional information including specific trip count and ranking details, visit [this link](https://public.tableau.com/views/CyclisticCaseStudy-AnnualMembersBook/Dashboard1?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link)*.

```{r member_stations}

## Create Subset of Dataframe with A Count for Start Station Usage By Annual Members

top_start_stations_members <- dataframe_2021_clean %>% 
  filter(member_casual=="member") %>%
  count(start_station_name, sort = TRUE)

## Remove Top Value (Which is Empty) and Keep Only the Top 10 Start Stations and Their Trip Count

top_start_stations_members <- head(top_start_stations_members, 11)
top_start_stations_members <- top_start_stations_members[-1,]
rownames(top_start_stations_members) <- NULL

## Declare Vectors for Start Station Latitude and Longitude, Which We Need for the Export

top_member_start_streets_lat <- c(41.90297, 41.91213, 41.88918, 41.90322, 41.89399,
                               41.89472, 41.89435, 41.93758, 41.88224, 41.88872)

top_member_start_streets_long <- c(-87.63128, -87.63466, -87.63851, -87.63432, -87.62932,
                                -87.63436, -87.62280, -87.64410, -87.64107, -87.64445)

## Add Vectors for Start Station Latitude and Longitude to the Subset of Top 10 Start Stations

top_start_stations_members$start_lat <- top_member_start_streets_lat

top_start_stations_members$start_long <- top_member_start_streets_long

## Create CSV File to Export

write.csv(top_start_stations_members, "members_start_stations.csv")

## Create Subset of Dataframe with A Count for End Station Usage By Annual Members

top_end_stations_members <- dataframe_2021_clean %>% 
  filter(member_casual=="member") %>%
  count(end_station_name, sort = TRUE)

## Remove Top Value (Which is Empty) and Keep Only the Top 10 End Stations and Their Trip Count

top_end_stations_members <- head(top_end_stations_members, 11)
top_end_stations_members <- top_end_stations_members[-1,]
rownames(top_end_stations_members) <- NULL

## Declare Vectors for End Station Latitude and Longitude, Which We Need for the Export

top_member_end_streets_lat <- c(41.90297, 41.91213, 41.88918, 41.90322, 41.89399,
                               41.89435, 41.89472, 41.93758, 41.88224, 41.88189)

top_member_end_streets_long <- c(-87.63128, -87.63466, -87.63851, -87.63432, -87.62932,
                                -87.62280, -87.63436, -87.64410, -87.64107, -87.64879)

## Add Vectors for End Station Latitude and Longitude to the Subset of Top 10 End Stations

top_end_stations_members$end_lat <- top_member_end_streets_lat

top_end_stations_members$end_long <- top_member_end_streets_long

## Create CSV File to Export

write.csv(top_end_stations_members, "members_end_stations.csv")

```

> [!ABSTRACT] Visual 7: Annual Members - Most Popular Stations
> ![visualisation 7](cyclistic_viz7.png)
> This visual was made in Tableau. To view the original, visit [this link](https://public.tableau.com/views/CyclisticCaseStudy-AnnualMembersBook/Dashboard1?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link).

Observations:

**Member trips seem to start and stop at almost the exact same stations**. As a matter of fact, only one of the 10 most popular stations to start from varies from the 10 most popular stations to stop at. We also see that many stops occur in the downtown region, where businesses, schools, and universities likely operate. None of the prominent member stops exist in leisure areas either. All of this suggests that members follow defined, pre-considered paths from what are likely areas of residence/metro stations to areas of work/study. The consistency between start and stop stations suggests members have places to be at particular times; they aren't using Cyclistic with the same intent as casual users.

---
## Findings

Notes: With R, our data sources were combined, cleaned, analysed and modified, before being used for  visualisations generated with ggplot2 and Tableau. All in all, we've uncovered a great deal of insight with regard to the differences in casual and paying-member-use of Cyclistic bikes. The overview of these findings is as follows:

- **Casual users are more likely to make use of Cyclistic bikes on weekends and during holiday periods**; particularly in the summer months of June, July and August.
- **Members are more likely to make use of Cyclistic bikes on weekdays, particularly during commute hours**, and **have fairly stable engagement with the service throughout the year**.
- **Casual users spend double the amount of time members do on trips, despite casual user trips distance being only marginally lengthier than member trip distance**, suggesting **casual users are in less of a hurry and using Cyclistic bikes for recreational purposes**.
- **Members** on the other hand **complete their trips with duration in mind, likely commuting between home and a study or workplace**.
- **Casual users start and stop their trips from popular leisure areas**. Their start and stop stations aren't entirely aligned and are in close proximity to the shore-front/areas of activity such as parks or recreational facilities. Furthermore, there is a great difference between the most and least popular bike stations in the top 10, in particular between all other stations and 'Streeter Dr & Grand Ave', which is right by the Chicago Pier, a very popular tourist attraction.
- **Members start and stop their trips from almost entirely the same set of stations**. Their favourite stations are more concentrated in business areas, away from leisure hot-spots, and there is less variance in the trip count of the most and least popular stations in the top 10, suggesting they're all well used.

---
## Recommendations

Given these findings, there are a number of actions we can take to potentially increase the number of members using Cyclistic.

#### Advertising:

- **Increase advertisements shown around the most popular start/end stations for casual users**. To increase the effectiveness of these ads, run them over weekends, when more riders are likely to see them.

#### Membership Adjustments:

- **Provide more membership options**. For example, with an uptick in members over the summer months, a seasonal membership might be of interest to casual users during this time. This can also be offered over spring/autumn months to increase engagement with Cyclistic over these time periods.
- **Offer discounts for membership over the winter months to encourage more casual users to convert**. This may also encourage more use of Cyclistic bikes in the winter months.
- **Introduce a 'Recommend A Friend' programme, wherein a paying member can recommend a casual-user friend, who may receive a discount when they register for Cyclistic's membership**. The paying member may also be offered a discount if they recommend a friend, should they want to renew their membership.
- **Provide more value with the membership**. For example, if the Cyclistic app were to integrate a feature showing members the best route to take between stations, it might encourage more users to invest.

To conclude, by taking the right steps taken and executing the proper actions, Cyclistic can greatly increase the number of casual users it converts into members.
