Overview:
This project focuses on the analysis of room nights in a hospitality business. The goal is to evaluate key metrics such as booked room nights, sellable room nights, and occupancy rates to provide insights into the business performance. The analysis helps identify trends in bookings, occupancy, and overall hotel capacity utilization.

Data Sources:
Daily Booked Room Nights: Represents the total number of rooms booked by guests on any given day.
Daily Sellable Room Nights: Refers to the number of rooms available to be sold on a daily basis, excluding rooms under maintenance or blocked.
Occupancy Rate: A calculated metric representing the ratio of booked room nights to sellable room nights, typically expressed as a percentage.
Data Modeling:
The project uses a star schema model for efficient querying and reporting, consisting of:
Fact Table:
Fact_Booking: Contains daily booking data including total booked rooms, sellable rooms, and other financial information (e.g., revenue, ADR).
Dimension Tables:
dim_date: Date table used to perform time-based analysis.
dim_hotel: Hotel-related data including hotel ID, location, and capacity.
dim_customer: Contains customer information such as customer ID, demographics, and booking preferences.
Key Performance Indicators (KPIs):
Several KPIs were created to measure performance in the hospitality business:

Occupancy Rate: (Booked Room Nights / Sellable Room Nights) * 100 - This is the percentage of available rooms that are booked.
ADR (Average Daily Rate): The average revenue earned per booked room night.
RevPAR (Revenue Per Available Room): Measures revenue generated per sellable room and is calculated as (Total Room Revenue / Sellable Room Nights).
Bookings by Region: Analysis of room bookings segmented by different regions or hotels.
Bookings by Customer Type: Breakdown of room bookings by customer types (e.g., business travelers, vacationers, etc.).
DAX Measures (for Power BI):
Occupancy Rate: DIVIDE([Booked Room Nights], [Sellable Room Nights], 0) * 100
ADR (Average Daily Rate): DIVIDE([Total Revenue], [Booked Room Nights], 0)
RevPAR (Revenue Per Available Room): DIVIDE([Total Revenue], [Sellable Room Nights], 0)
Data Transformation:
Power Query: Used for cleaning and transforming the raw booking and room availability data.
Combined and cleaned data from multiple sources to ensure accuracy and consistency.
Created aggregated tables to support KPI calculations and time-based analysis.
Tools & Technologies:
Power BI: Used to visualize the key metrics, enabling dynamic filtering by hotel, region, date, and other dimensions.
DAX: Dynamic expressions were used for calculating various metrics such as occupancy rate, ADR, and RevPAR.
Power Query: Employed for data transformation and preparation, ensuring clean and structured data ready for analysis.
Insights:
Occupancy Trends: Identified periods with high and low occupancy rates, helping the business adjust pricing and marketing strategies during off-peak times.
Revenue Analysis: The ADR and RevPAR metrics helped analyze which hotels and regions were performing well and driving revenue.
Customer Behavior: Segmenting bookings by customer type provided insights into customer preferences, allowing for tailored marketing strategies.
Forecast Accuracy: Insights into forecasted vs. actual room demand help with inventory planning and staffing decisions.
