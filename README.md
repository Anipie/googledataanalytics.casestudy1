# googledataanalytics.casestudy1

We are trying to improve the finances of the company, which is sought to be strengthening membership rather than getting new customers.
Our insights can determine whether annual riders provide more income than casual riders so we can know how to focus our marketing strategy.

The data used is open-sourced from the website  https://divvy-tripdata.s3.amazonaws.com/index.html, but in a real scenario, the data will be closed as only the company would know their customer's transactions. 
The data shows the type of membership each customer has as well as how often they travel over the course of 12 months. In this scenario, I was only able to do 1 quarter of the year, Jan to March because the data set was too large. 
There is no issue with bias because the data is random.
I can verify the data's integrity by checking the format of the data.
The problem I see with the data is that there are different naming conventions between the datasets. I would have to make them the same if I want to combine the datasets. For the 2020 data, I am not sure what Start_lat, Start_Lng, end_lat, or end_Ing means.

The tool I will be using is google sheets to generate pivot tables. I can verify the data's integrity by checking for duplicate values using  the COUNTIF formula. 
I used filter for rideable type.
For each month of each file I import the csv files to google sheets then cleaned the data with the following; the start time and end time should be formatted into yy mm dd format.
I've removed Start_lat, Start_Lng, end_lat, or end_Ing because they had a lot of decimals and negative values, which wouldn't make sense in terms of time.
Before removing trip and ride id, I made sure there weren't any duplicates.
I checked for dupicates using conditional formatting and using the formula, =countif(A:A,A1)>1 .

We do not need trip duration if we have ride length
we also need the columns to be similar before we aggregate the data and can do so by appending.
I also kept the subscriber/customer (2019) and member/casual (2020) differentiated so we can see the differences between the two years.

From the basic google sheets formulas, I found that;
The average ride length is around 19 minutes and 44 seconds
The most common day of the week that a bike trip occurs is on Wednesday.

From the pivot tables, I found that:
casual riders have more average ride time by making a pivot table with membership status as the rows and average ride length as the values
people ride the most on wednesday (also supported by the google sheets formula) with a pivot table with rows day of the week and values as membership status.
The most popular biking starts at Canal St & Adams St with a pivot table containing rows as the name of the station that people started biking and the values as membership status.

In conclusion, from the data I would reccommend:
1) The company's initial focus on transforming regular customers into members instead of making ads targeting new potential bikers was the right decision because on average the ride time for regular customers is more than members, so they would more likely be interested in upgrading.
2) The best place and time to advocate would be on Wednesday at Canal St & Adams St
