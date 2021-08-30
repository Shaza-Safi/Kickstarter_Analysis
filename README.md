# Kickstarter_Analysis

## Overview of Project:

### Background:
Lousie wants to start a campaign to fund her play “Fever” with an estimate of $10,000. Considering this is her first campaign she has doubts related to her campaign and requires insight from previous related campaigns. 

### Purpose:
In order to help Louise better run her campaign, identify various factors that could help her reach her funding goal and succeed in her Project, a detailed analysis needs to be done on large sample of crowdfunding projects campaigned on Kickstarter. 

## Analysis and Challenges: 

### Analysis of Outcomes Based on Launch Date
I created a pivot table Keeping the Parent Category and Year in the filters. This can help refocus my analysis on only Theater Category which is more relevant to Louise’s Project. I organized the Pivot table to show the outcomes in columns and the Dates Launch (I only kept the months here) in rows. Representing months would show a clearer trend of when is the best time to Launch Theater related projects that are successful. 

![Theater Outcomes by Launch Date Pivot table](https://user-images.githubusercontent.com/88908758/131285620-5daefcc9-bd55-485b-8a09-5fc29481d619.PNG)

Next, I created a pivot chart and found the line chart to be best when demonstrating fluctuation during a a period of time. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/88908758/131285638-0bb84388-0555-47a0-87b3-6355876dd3e7.png)

### Analysis of Outcomes Based on Goals
When comparing outcomes to goals, its important to categorize goals into ranges in order to identify a trend or even a relationship between successfull projects and their goals.
I have used a “countifs” formula to tell excel to grab the value from the kickstarter worksheet that has a specific range of goal values, has an outcome of “successful” & has a subcatergory of “play”. I copied this formula across different outcome categories and different goal ranges. I then divided the number of successful outcomes for each goal range by the total number of projects to come up with the percentage of successful campaigns for that given goal range and duplicated the same process to the other columns and rows respectively while doing some adjustment to the formulas as shown in the image below: 

![Outcomes based on Goals Analysis](https://user-images.githubusercontent.com/88908758/131285667-d1badd9b-ec53-4449-bb26-b2ebcd172ae8.PNG)

Using the Percentage of outcomes based on goals I have prepared the below line chart:

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/88908758/131285700-bfbb2cae-ccec-4fc5-ae99-e170bbac8b16.png)

### Challenges and Difficulties Encountered
1-	The UNIX Timestamps were challenging to use as they were unreadable, therefore I used a formula to convert “launch date” & “End date” from UNIX Timestamps to readable dates in order to identify trends related when the campaign was launched. The formula takes the timestamp value and converts it from seconds to a readable date as shown below. 

![Converting time](https://user-images.githubusercontent.com/88908758/131285737-efd10766-fb9b-4401-9b59-81a2fdb0d02f.PNG)

2-	The Category column has both Parent Category & Subcategory clubbed together which is a drawback as you cannot analyze outcomes based on a more relevant category (Theater), nor can you drill down to (Plays) as a Subcategory. To resolve this challenge, I used “convert text to column” tool to Extract “Parent Category” & “Subcategory” in two separate columns.

## Results

### What are two conclusions you can draw about the Outcomes based on Launch Date?
1-	You can notice a spike in successful Theater Campaigns in Q2 of the calendar year (April, May & June). This is demonstrated in the chart where the count of successful theater campaigns reached the highest level of 111 & 100 in the months of May & June.

2-	You also can notice that by the end of the calendar year (more specifically December) the successful campaigns for Theater go down reaching to almost same level as the failed number of campaigns. This could be explained by backers closing up ties with campaigns committed to throughout the year. 

### What can you conclude about the Outcomes based on Goals?
1-	You can notice the percentage of successful campaigned plays is highest when the goal ranges between less than $1000 and less than $5,000 and constantly dropping down after that. In vice versa, the percentage of failed campaigned plays constantly increases from above $5,000. Therefore, you can assume the higher the funded goal is for a play the less possibility the campaign will meet its goal. 

2-	You can also notice that the number of plays is very low when the goal is above $25,000. This leads to having an exaggerated increases and decreases in percentage of successful plays anywhere above a the goal of $25,000 and vice versa for percentage of failed.

### What are some limitations of this dataset?
1-	The dataset is very broad and requires to be refocused to more related areas to Louise campaign. For instance, her project to be funded is a play, however the number of plays in the theater category are very little compared to the total number of campaigns in the sample making our analysis less tackling that specific Niche. 

2-	When looking at the year which Theater Campaigns were launched you can notice that anywhere before 2014 there was only a few campaigns. When doing an outcome based on launch date the analysis takes into account those years when trying to find trends to outcomes based on launch date.


### What are some other possible tables and/or graphs that we could create?
1-	We could calculate the mean, median & standard deviation of goals that are successful and are in Theater Category. This can be presented through a histogram

2-	Calculate the InterQuartile Range IQR for goals that are successful and are in Theater Category and identify Outliers using a Box plot.
