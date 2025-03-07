# Taxi-Cab-Insights
## Problem statement
 Provide Insights to Chief of Operations in Transportation Domain

Domain: Transportation & Mobility	    Function: Operations

Goodcabs, a cab service company established two years ago, has gained a strong foothold in the Indian market by focusing on tier-2 cities. Unlike other cab service providers, Goodcabs is committed to supporting local drivers, helping them make a sustainable living in their hometowns while ensuring excellent service to passengers. With operations in ten tier-2 cities across India, Goodcabs has set ambitious performance targets for 2024 to drive growth and improve passenger satisfaction.

As part of this initiative, the Goodcabs management team aims to assess the company's performance across key metrics, including trip volume, passenger satisfaction, repeat passenger rate, trip distribution, and the balance between new and repeat passengers

## Business Requests

# Business Request - 1: City-Level Fare and Trip Summary Report

Generate a report that displays the total trips, average fare per km, average fare per trip, and the percentage contribution of each city’s trips to the overall trips. This report will help in assessing trip volume, pricing efficiency, and each city’s contribution to the overall trip count.
Fields:

•	city name

•	totaI_trips

•	avg_fare_per_km

•	avg fare per trip

•	%_contribution_to_totaI_trips









# Business Request - 2: MonthIy City-Level Trips Target Performance Report

Generate a report that evaluates the target performance for trips at the monthly and city level. For each city and month, compare the actual total trips with the target trips and categorise the performance as follows:

•	If actual trips are greater than target trips, mark it as "Above Target".
•	If actual trips are less than or equal to target trips, mark it as "Below Target".

Additionally, calculate the % difference between actual and target trips to quantify the performance gap.
Fields:

•	City_name

•	month name

•	actual trips

•	target_trips

•	performance status

•	% difference
 
# Business Request - 3: City-Level Repeat Passenger Trip Frequency Report

Generate a report that shows the percentage distribution of repeat passengers by the number of trips they have taken in each city. Calculate the percentage of repeat passengers who took 2 trips, 3 trips, and so on, up to 10 trips.

Each column should represent a trip count category, displaying the percentage of repeat passengers who fall into that category out of the total repeat passengers for that city.

This report will help identify cities with high repeat trip frequency, which can indicate strong customer loyalty or frequent usage patterns.

•	Fields: city name, 2-Trips, 3-Trips, 4-Trips, 5-Trips, 6-Trips, 7-Trips, 8-Trips, 9-Trips, 10-Trips


# Business Request - 4: Identify Cities with Highest and Lowest Total New Passengers

Generate a report that calculates the total new passengers for each city and ranks them based on this value. Identify the top 3 cities with the highest number of new passengers as well as the bottom 3 cities with the lowest number of new passengers, categorizing them as "Top 3" or "Bottom 3" accordingly.
Fields

•	city name

•	totaI_new_passengers

•	city_category ("Top 3" or "Bottom 3")


# Business Request - 5: Identify Month with Highest Revenue for Each City

Generate a report that identifies the month with the highest revenue for each city. For each city, display the month name, the revenue amount for that month, and the percentage contribution of that month’s revenue to the city’s total revenue.
Fields

•	city_name

•	highest revenue month

•	revenue

•	percentage contribution (%)
 
# Business Request - 6: Repeat Passenger Rate Analysis Generate a report that calculates two metrics:
1.	Monthly Repeat Passenger Rate: Calculate the repeat passenger rate for each city and month by comparing the number of repeat passengers to the total passengers.
2.	City-wide Repeat Passenger Rate: Calculate the overall repeat passenger rate for each city, considering all passengers across months.

These metrics will provide insights into monthly repeat trends as well as the overall repeat behavior for each city.

Fields:

•	city name

•	month

•	totaI_passengers

•	repeat_passengers

•	monthly repeat	passenger rate (%): Repeat passenger rate at the city and month level

•	city repeat_passenger rate (%): Overall repeat passenger rate for each city, aggregated across months







## Solution :

# Business Request - 1: City-Level Fare and Trip Summary Report

Generate a report that displays the total trips, average fare per km, average fare per trip, and the percentage contribution of each city’s trips to the overall trips. This report will help in assessing trip volume, pricing efficiency, and each city’s contribution to the overall trip count.
Fields:

•	city name

•	totaI_trips

•	avg_fare_per_km

•	avg fare per trip

•	%_contribution_to_totaI_trips





# Average Fare per KM 


![AVERAGE FARE PER KM](https://github.com/user-attachments/assets/e1fc2ca5-4670-4915-90f5-368db7c05d0d)


# total fare vs city 
![total fare by city](https://github.com/user-attachments/assets/d16984be-1f8f-45a5-be55-f56b713db907)


# average fare per trip vs city 

![average fare per trip vs city](https://github.com/user-attachments/assets/7fcd3913-a51f-4237-ba48-db449452b7cb)


# city level fare and trip summary 

![city level fare and trip summary](https://github.com/user-attachments/assets/5a26fe12-ed19-4301-b405-50d2835f13ff)





# Business Request - 2: MonthIy City-Level Trips Target Performance Report

Generate a report that evaluates the target performance for trips at the monthly and city level. For each city and month, compare the actual total trips with the target trips and categorise the performance as follows:

•	If actual trips are greater than target trips, mark it as "Above Target".
•	If actual trips are less than or equal to target trips, mark it as "Below Target".

Additionally, calculate the % difference between actual and target trips to quantify the performance gap.
Fields:

•	City_name

•	month name

•	actual trips

•	target_trips

•	performance status

•	% difference



  dax used :
  monthyear = FORMAT(fact_trips[date].[Date],"MMMM YYYY")
  
   performance vs target = IF(fact_trips[total actual trip count]>fact_trips[total target trip],"above the target","below the target")

   # month-city level target performance report

   ![monthly city target performance report](https://github.com/user-attachments/assets/f57aefcb-3392-4076-8c7d-04da0e62051d)


   # DEMAND VARIES WITH CITY AND MONTH
   ![image](https://github.com/user-attachments/assets/0e63f58f-79ae-49d6-94cc-5a44ef80eeeb)


   For Chandigarh city ,Feb. month have highest demand and April month lowest .
   
For Jaipur city ,Feb. month have highest demand and June have lowest.



![image](https://github.com/user-attachments/assets/3dbff762-589a-499d-8d6f-65c18edeac8c)





# Business Request - 3: City-Level Repeat Passenger Trip Frequency Report
Generate a report that shows the percentage distribution of repeat passengers by the number of trips they have taken in each city. Calculate the percentage of repeat passengers who took 2 trips, 3 trips, and so on, up to 10 trips.

Each column should represent a trip count category, displaying the percentage of repeat passengers who fall into that category out of the total repeat passengers for that city.

This report will help identify cities with high repeat trip frequency, which can indicate strong customer loyalty or frequent usage patterns.

• Fields: city name, 2-Trips, 3-Trips, 4-Trips, 5-Trips, 6-Trips, 7-Trips, 8-Trips, 9-Trips, 10-Trips






![mutiple trip data](https://github.com/user-attachments/assets/d3bb5e8f-5b09-423b-8dcd-b01b2f6c854f)


# Mutiple trips taken by repeated passenger by city
![Picture7](https://github.com/user-attachments/assets/28e64feb-3441-4dec-a47d-5857dfb7ca48)




# Business Request - 4: Identify Cities with Highest and Lowest Total New Passengers

Generate a report that calculates the total new passengers for each city and ranks them based on this value. Identify the top 3 cities with the highest number of new passengers as well as the bottom 3 cities with the lowest number of new passengers, categorizing them as "Top 3" or "Bottom 3" accordingly.
Fields

•	city name

•	totaI_new_passengers

•	city_category ("Top 3" or "Bottom 3")




dax used 

categoric name = 
SWITCH(
    TRUE(), 
    [rank] >= 1 && [rank]<=3, "Top",
    [rank] >= 7&& [rank]<=10, "Bottom",
    "Middle"
)



rank = rankx(ALL(dim_city[city_name]),[Total_New_Passengers], ,DESC)



![Picture8](https://github.com/user-attachments/assets/32605b53-9e30-46c8-931f-24886e18085a)



# Business Request - 6: Repeat Passenger Rate Analysis Generate a report that calculates two metrics:
1.	Monthly Repeat Passenger Rate: Calculate the repeat passenger rate for each city and month by comparing the number of repeat passengers to the total passengers.
2.	City-wide Repeat Passenger Rate: Calculate the overall repeat passenger rate for each city, considering all passengers across months.

These metrics will provide insights into monthly repeat trends as well as the overall repeat behavior for each city.

Fields:

•	city name

•	month

•	totaI_passengers

•	repeat_passengers

•	monthly repeat	passenger rate (%): Repeat passenger rate at the city and month level

•	city repeat_passenger rate (%): Overall repeat passenger rate for each city, aggregated across months


![picture 10](https://github.com/user-attachments/assets/b42139e7-967f-485c-b202-bc251de609cc)



![picture 11](https://github.com/user-attachments/assets/b5d43139-f4d1-44c7-a18f-57646164e369)


















 	 
 
 
 
 
 
 
 
 
 
 
 	 
 
 
 
 
 
 
 
 
 


 	 
 
 
 
 
 
 
 
 
 


 	 
 
 
 
 
 
 
 
 
 

