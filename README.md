# Hotel_booking_analysis_Project_abhiram
The project contains the real world data record of hotel bookings of a city and a resort hotel containing details like bookings, cancellations, guest details etc. from year 2015, 2016 and 2017. In this project we are going to analyze Hotel Booking Data in order to find out valuable insights and give suggestions to increase revenue of hotels.

Programming Language : Python

Libraries used : Pandas, Numpy, Matplotlib, Seaborn

NoteBook : Google Colab

Dataset Source : Provided by Almabetter themself.


## Objective
We are provided with a hotel bookings dataset.

The main purpose of this study is to perform EDA on the given dataset and draw useful conclusions about the trends in hotel bookings and how factors that control hotel bookings influence each other.

## Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record.
- meal: Type of meal chosen
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed
- reservation_status_date: Date of making reservation status.


- Total number of rows in data: 119390
- Total number of columns: 32


## Data Cleaning


### (1) Removing duplicate rows if any

All duplicate rows were dropped.

### (2) Handling missing values

- Null values in columns 'company','agent', 'country' and 'children' were replaced by 0.
- There are some rows with total number of 'adults' , 'children' and 'babies' is equal to zero. So we will remove such rows is equal 0.


### (3) Converting columns to appropriate data types

- Changed data type of `children`, `company`, `agent` float to int type.
- Changed data type of 'reservation_status_date' to datetime format.


### (5) Adding important columns

- Creating new column `Total_stay_in_nights` by adding `stays_in_weekend_nights`+`stays_in_week_nights`.
- Creating new column `Total_people` by adding `adults`+`children`+`babies`.


## Exploratory Data Analysis

Performed EDA and tried answering the following questions:


 Q1) In which week number most of the people arrived ?
 Q2) Find the relation between Avarage daily Rate (adr) and total stays in nights?
 Q3) lets see which month generate highes revenue ?
 Q4) Describe the highest number of bookings yearly for both hotel ?
 Q5) Describe the highest number of bookings monthly for both hotel ?
 Q6) Describe the highest number of bookings week number wise for both hotel ?
 Q8) Describe the number of bookings year and month wise for both hotel ?
 Q9) From Where the most guests are coming ?
 Q10) Find the correlation between the numerical data ?
 Q11) Which hotel is mostly preferred for short stay or long stay ?
 Q12) Which channel is mostly used for the booking of hotels?
 Q13) Find the correlation between the numerical data ?
 Q14) What are the overall cancellation rates and cancellation rates with leading years in both the hotels ?
 Q15) Which hotel has the highest number of stays in term of weekend nights and weekday nights ?
 Q16) Which types of rooms are mostly preferred by guests ?
 Q17) Which room type has the highest Average Daily Rate (adr) ?
 Q18) In which month the average daily rate of Resort Hotel is highest ?
 Q19) In which month the average daily rate of City Hotel is highest ?


The following plots had been used:

   - Bar Plot.
   - Scatter Plot.
   - Pie Chart.
   - Line Plot.
   - Heatmap.
   - Box Plot


## Analysis:

Performed analysis and made following conclusions:

1. A city hotel has more bookings than a resort. Offer packages and promotions to promote bookings for the resort hotel.

2. BB is the most requested food. The hotel should maintain food quality while also offering discounts on other foods to promote other food types, reducing the burden on kitchen management and keeping a variety of food options available to customers.

3. Most of the bookings are made through the online platform. Hotels can cut costs by eliminating market segments such as complementary and aviation because bookings through these segments are very low.

4. Because most bookings made through TA/TO distribution are followed by corporate distribution, hotels should invest in both TA/TO and corporate distribution channels. The GDS distribution channel can be eliminated by hoteliers because bookings made through it are extremely low.

5. Very few customers (4%) visited again. So hotels can increase repeat bookings by offering the right repeat booking incentives, understanding the motivations behind repeat bookings, marketing to your guests’ past interests, and assessing past bookings to identify priority guests.

6. Because rooms A and D are the most popular with customers, the hotel should maintain their quality. The hotel should promote rooms E, F, and G to increase demand by offering discounts. Because customers do not prefer to book room types B, C, H, and L, the hotel can eliminate them, lowering the cost of these rooms.

7. People typically book rooms for two people, so encourage family and group bookings. You can maximize revenue by promoting it with a discounted offer for group bookings.


## Conclusion


(1). The majority of guests come from western europe countries.We should spend a significant amount of our budget on those area.

(2). Around 61% bookings are for City hotel and 39% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel.

(3). Majority of the hotels booked are city hotel. Definitely need to spend the most targeting fund on those hotel.

(4). We should also target months between May to Aug. Those are peak months due to the summer period.

(5). Given that we do not have repeated guests, we should target our advertisement on guests to increase returning guests.
approax 80% distribution_channel is TA/TO

(6). Most common stay length is less than 4 days and generally people prefer City hotel for short stay, but for long stays, Resort Hotel is preferred.

(7). November,Descember, February And January are the months which has less booking so in this perios you can get rooms with less average daily rate. And Avoid most busiest months for hotels (June,July,August)


## Challenges

(1) Lot of null values were present in the dataset.

(2) Data type of some Data was in wrong format.

(3) Lot of duplicate data.

(4) Which visualization techniques to use was a challenge?
