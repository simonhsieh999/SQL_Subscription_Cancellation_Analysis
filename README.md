# Subscription Cancellation Analysis

This project is from Jess Ramos's [Big SQL Energy course](https://bigdataenergycourses.com/p/bigsqlenergy).

## Executive Summary

The technology company has subscription-based products in which after customers have enrolled in the subscription for 1 year, they then have the option to either renew the subscription or they can leave and churn. Currently the company has been dealing with a retention crisis where many customers have been cancelling their subscriptions instead of renewing, leading to a big loss in company revenue.  This analysis uses SQL to analyze the user's cancellation reasons to identify any trends and interesting insights in order to provide business recommendations that will improve future customer retention.

## Business Problem

The company leadership has noticed a large churn issue this year that is higher than expected, and wants to look into the reasons behind the subscription cancellations in order to improve customer retention to prevent any future loss in revenue. There is customer-reported data available where after the cancellation, the customer will have to select at least 1 reason up to 3 reasons why they decided to cancel their subscription. We will work on the data of the cancellation reasons and the cancel date to analyze any trends and interesting insights.

## Methodology
The Subscriptions and Cancellations tables from Jess Ramo's database using Hex were used for the analysis. Using SQL, the tables were extracted, cleaned, and transformed. The following steps were formed:
- Counting how many users selected a first, second, and third reason for cancelling to determining the completeness of the data.
- Identify the user intention by computing the average number of reasons, and the average number of additional reasons submitted by a user (additional reasons is good to show user engagement since they're taking the time to provide feedback).
- Combining all 3 cancellation reasons of each subscription into 1 column using Unions, and creating a CTE of it in order to perform further analysis such as determining the count of each cancellation reason.
- Using a view of the Unions CTE to enable us to reuse it in multiple queries.
- Created a visualization outlining the number of each cancellation reason type for each of the 3 reasons provided, and identifying any reason number trends (faceting).
- Computing the percentage of each cancellation reason for each year, and creating a line graph.
- For the coding process, click [here](https://github.com/simonhsieh999/SQL_Subscription_Cancellation_Analysis/blob/main/Coding%20Process).

## Skills
- SQL (Joins, aggregate functions, CTEs, Windows functions, Union, View creation)
- Data Cleaning
- Data Wrangling
- Data Visualization

## Results

- For the completeness of the data, there are 22 cancelled subscriptions, with all of them selecting the 1st cancellation reason. 18 of them selected a 2nd cancellation reason, and 8 of them selected a 3rd cancellation reason. The users who didn't select the additional 2nd or 3rd reason could indicate frustration or a lack of interest for the user to provide feedback.
- The average total reasons submitted by subscription (on a scale of 3) is 2.18, and the average additional reasons submitted by subscription is 1.18, which is a good number of users willing to provide feedback.
- Here is a bar chart of the count of each cancellation reason for each of the 3 reason numbers:
![image](https://github.com/user-attachments/assets/13ccf000-7261-43b7-8c71-42be59dbdc0a)
The 1st cancellation reason can be the primary reason that users feel strongly about since that reason would be the first reason that they think about. For the user's 1st cancellation reason, "not useful" was the biggest reason, followed by "expensive". For the 2nd cancellation reason, "went to a competitor" was the biggest reason.

- Here is a line chart of the trends in 2022, 2023, and 2024:
  ![image](https://github.com/user-attachments/assets/149757aa-de78-4652-a559-cd70364a46c6)

Also, here are the trends in 2022, 2023, and 2024 in table format:

|                    | 2022 | 2023 | 2024 |
|--------------------|------|------|------|
|None                |33%   |42%   |24%   |
|Not Useful          |33%   |17%   |20%   |
|Went To A Competitor|33%   |17%   |20%   |
|Bad Customer Service|-     |8%    |14%   |
|Expensive           |-     |17%   |24%   |

From the table, in 2024, the cancellation reason "expensive" showed the biggest increase from 17% to 24%. This can indicate that customers are more cost-conscious overtime, probably due to the increase in the cost of living, and would want more value for their product.
Also, the number of null responses have been decreasing from 42% to 24%, which indicates the increase in willingness for users to provide additional feedback.

## Business Recommendations
- In order to address the user's top cancellation reasons "not useful" and "expensive", we should ensure the users are getting value of the product and finding it useful. A way to do that are to have better onboarding for the users so that they understand more about the product features and how they can benefit from it.
- Another idea is to have company events relating to the product to build a community so that the users can gain more interest and find it more useful in using the product when they see others also benefiting from the product.
- At the end of the subscription, there can be an incentive for a user to renew their subscription. Ways to do that are offering a discount, reward, or adding any additional features for those that renew.
- To deal with competitors, the company can do market research to keep up with the trends, and figure out what the competitors are doing that the company is not. Also the company can figure out their unique factors on what makes them different than the competition, and use that to their advantage.

## Next Steps
- We could find ways to better support the user by asking for their feedback of the product during their subscription in order to resolve any issues that come up rather than knowing at the end of the subscription what the issues are. This would lead to them likely renewing their subscription.
- Explore the user's engagement of the subscription by figuring out which features of the product they used and didn't use, and how often they used the product. If they didn't use the product for sometime, we could contact the user for their feedback.
- Consider factors outside of our control such as their personal situation. Maybe they decided to take a break from using the product and will consider renewing their subscription later down the road. We can work on maintaining that relationship with the user, and send them any updates if they wish to receive them.











