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

