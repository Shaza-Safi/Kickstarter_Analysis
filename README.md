# Kickstarter_Analysis

## Overview of Project:

### Background:
Lousie wants to start a campaign to fund her play “Fever” with an estimated of USD 10,000. Considering this is her first campaign she has doubts related to her campaign and requires insight from previous related campaigns. 

### Purpose:
In order to help Louise better run her campaign and identify various factors that could help her reach her funding goal and succeed in her Project, a detailed analysis needs to be done on large sample of crowdfunding projects campaigned on Kickstarter. 


## Analysis and Challenges: 

### Analysis of Outcomes Based on Launch Date
I created a pivot table Keeping the Parent Category and Year in the filers. This can help refocus my analysis on only Theater Category which is more relevant to Louise’s Project. I organized the Pivot table to show the outcomes in columns and the Dates Launch (I only kept the months here) in rows. Representing months would show a clearer trend of when is the best time to Launch Theater related projects that are successful. 
![] (https://github.com/Shaza-Safi/Kickstarter_Analysis/blob/main/Supporting_Pics/Theater%20Outcomes%20by%20Launch%20Date%20Pivot%20table.PNG)

Next, I created a pivot chart and found the line chart to be best when demonstrating fluctuation during a a period of time. 

### Analysis of Outcomes Based on Goals
When comparing outcomes to goals, its important to categorize goals in ranges in order to identify which projects are more successful and which are failing in comparison to the goal of the campaign. I have used an “countifs” formula to tell excel to grab the value from the kickstarter worksheet that has a specific range of goal value, has an outcome of “successful” & has a subcatergory of “play”. I did this formula across different outcome categories and different goal ranges. After that I divided the number of successful outcomes for each goal range by the total number of projects to come up with the percentage of successful campaign for that given range and duplicated the same process to the other columns and rows respectively while doing some adjustment to the formulas as shown in the image below: 
Using the Percentage of outcomes based on goals I have prepared the below line chart:

### Challenges and Difficulties Encountered
1-	The UNIX Timestamps were challenging to use as they were unreadable, therefore I Used a formula to convert “launch date” & “End date” from UNIX Timestamps to readable dates in order to identify trends related to the period of the campaign. The formula takes the timestamp value and converts it from seconds to a readable date as shown below. 
2-	The Category column has both Parent Category & Subcategory clubbed together which is a drawback as you cannot analyze outcomes based on a more relevant category (Theater), now can you drill down to (Plays) as a Subcategory. To resolve this challenge, I used “convert text to column” tool to Extract “Parent Category” & “Subcategory” in two separate columns.

## Results

### What are two conclusions you can draw about the Outcomes based on Launch Date?
1-	You can notice a spike in successful Theater Campaigns in Q2 of the calendar year (April, May & June). This is demonstrated in the chart where the count of successful theater campaigns reached the highest level of 111 & 100 in the months of May & June.
2-	You also can notice that by the end of the calendar year (more specifically December) the successful campaigns for Theater go down reaching to almost same level as the failed number of campaigns. This could be explained by backers closing up ties with pledged campaigns committed to throughout the year. 


### What can you conclude about the Outcomes based on Goals?
1-	You can notice the percentage of successful campaigned plays is highest when the goal ranges between less than USD 10,000 and up to less than USD5,000 and constantly drops down after that. Vice versa, the percentage of failed campaigned plays constantly increases from above USD 5,000. Therefore, you can assume the higher the funded goal is for a play that campaign meets it funded goals. 
2-	You can also notice that number of plays reduces when the funded goal increases. This leads to having an exaggerated increases and decreases in percentage of successful plays anywhere above a the goal of USD 25,000 as the number of plays is very low having a huge impact on the percentages and vice versa for percentage of failed.


### What are some limitations of this dataset?
1-	The dataset is very broad and requires to be refocused to more related areas to Louise campaign. For instance, her project to be funded is a play, however the number of plays in the theater category are very little compared to the total number of campaigns in the sample making our analysis less tackling that specific Niche. 
2-	When looking at the year which Theater Campaigns were launch you can notice that anywhere before 2014 there was only a few campaigns. When doing an outcome based on launch date the analysis takes into account those years when trying to find trends to outcomes based on launch date.


### What are some other possible tables and/or graphs that we could create?
1-	We could calculate the mean, median & standard deviation of goals that are successful and are in Theater Category. This can be presented through a histogram
2-	Calculate the Integrates Quartile Range IQR for goals that are successful and are in Theater Category and identify Outliers using a Box plot.
