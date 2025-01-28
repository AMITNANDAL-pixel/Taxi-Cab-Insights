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




  
 	 
 
 
 
 
 
 
 
 
 
 
 	 
 
 
 
 
 
 
 
 
 


 	 
 
 
 
 
 
 
 
 
 


 	 
 
 
 
 
 
 
 
 
 

