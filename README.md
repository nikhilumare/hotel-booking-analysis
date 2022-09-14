
# Hotel booking analysis
## objective

The main objective behind this project is to explore and analyze data to discover important factors that govern the bookings and give  insights to hotel management ,which can perform various campaigns  to boost the business and performance.


## Dataset

We are given a hotel bookings dataset.
This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things.

 It contains the following features.

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
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
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

Total number of rows in data: 119390

Total number of columns: 32
## Data Cleaning and Feature Engineering
**1) Removing Duplicate rows**

All duplicate rows were dropped.

**2) Handling null values**

Null values in columns company and agent were replaced by 0.

Null values in column country were replaced by 'others'.

Null values in column children were replaced by the mean of the column.

**3) Converting columns to appropriate data types**

Changed data type of children, company, agent to int type.

Changed data type of reservation_status_date to date type.

**4) Removing outliers**

One outlier was found in the adr column. Simply dropped it.

**5) Creating new columns**

Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.

Created new column total_people by adding adults+children+babies
## Exploratory Data Analysis
**Performed EDA and tried answering the following questions:**

1) Which type of hotel is mostly prefered by the guests?
2) Which Distribution channel is mostly used for hotel bookings?
3) Which agent made the maximum bookings?
4) What is the Percentage of repeated guests?
5) Which type of food is mostly preferred by the guests?
6) What is the percentage distribution of required_car_parking_spaces?
7) What is the percentage distribution of "Customer Type"?
8) Which is the most preferred room type by the customers?
9) What is the pecentage of cancellation?
10) What is Percentage distribution of Deposite type ?
11) From which country the most guests are coming?
12) In which month most of the bookings happened?
13) Which year had the highest bookings?
14) Which hotel has highest percentage of booking cancellation?
15) Which hotel type has the more lead time?
16) Which Hotel type has the highest ADR?
17) Which Hotels has the most repeated guests?
18) Which hotel has longer waiting time?
19) What is the ADR across the different month?
20) Which Market Segment has the higest cancellation rate?
21) Which distribution channel has the higest cancellation rate?
22) Which distribution channel contributed more to adr in order to increase the the income?

Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:


Bar Plot.

Histogram.

Scatter Plot.

Pie Chart.

Line Plot.

Heatmap.

Box Plot

## Univariate Analysis:
Performed univariate analysis and made following conclusions:
1) City Hotel is most preffered hotel by guests.
2) Most 79% people prefer'TA/TO' for booking.
3) Agent ID no: 9 made most of the bookings.
4) only 4% people are repeated guests.
5) The most preferred meal type by the guests is BB( Bed and Breakfast).
6) 91.6 % guests did not required the parking space. only 8.3 % guests required only 1 parking space.
7) Transient customer type is more whcih is 82.4 %.
## Bivariate Analysis 
We tried to answer following questions

1) Overall adr of City hotel is slightly higher than Resort hotel and no. of bookings of City hotel is also higher than Resort hotel. Hence, City hotel is makes more      revenue.
 2) City hotel has slightly higher median lead time. Also median lead time is significantly higher for both hotels, this means customers generally plan their hotel         visits way early.
 3) Almost 30 % of City Hotel bookings got canceled.
 4) Both hotels have very small percentage that customer will repeat, but Resort hotel has slightly higher repeat % than City Hotel.
 5) TA/TO is mostly used for planning Hotel visits well ahead of time. 
 6) While booking via TA/TO one may have to wait a little longer to confirm booking of rooms.
 7) GDS channel brings higher revenue generating deals for City hotel, in contrast to that most bookings come via TA/TO. City Hotel can work to increase outreach on       GDS channels to get more higher revenue generating deals.
 8) TA/TO has highest booking cancellation %. Therefore, a booking via TA/TO is 30% likely to get cancelled.
 9) Longer lead time has no affect on cancellation of bookings.
 10) Not getting same room as demanded is not the case of cancellation of rooms. A significant percentage of bookings are not cancelled even after getting different       room as demanded.
 11) Not getting same room do affects the adr, people who didn't got same room have paid a little lower adr. 
 12) Arrivals in hotels increases at weekends and also the avg adr tends to go up as month ends. 
 13) Mostly bookings are done by couples(bookings have two adults.)

## Conclusion
1. City hotels are the most preferred hotel type by the guests. We can say City hotel is the busiest hotel.

2. 79.1 % bookings were made through TA/TO (travel agents/Tour operators).

3. Only 3.9 % people were revisited the hotels. Rest 96.1 % were new guests. Thus retention rate is low.

4. BB( Bed & Breakfast) is the most preferred type of meal by the guests.

5. Maximum number of guests were from Portugal, i.e. more than 25000 guests.

6. 27.5 % bookings were got cancelled out of all the bookings.

7. The percentage of 0 changes made in the booking was more than 82 %. Percentage of Single changes made was about 10%.

8. Most of the customers (91.6%) do not require car parking spaces.

9. Most of the bookings for City hotels and Resort hotel were happened in 2016.

10. Average ADR for city hotel is high as compared to resort hotels. These City hotels are generating more revenue than the resort hotels.

11. Booking cancellation rate is high for City hotels which almost 30 %.

12. Average lead time for resort hotel is high.

13. Waiting time period for City hotel is high as compared to resort hotels. That means city hotels are much busier than Resort hotels.

14. Resort hotels have the most repeated guests.

15. Optimal stay in both the type hotel is less than 7 days. Usually people stay for a week.

16. Almost 19 % people did not cancel their bookings even after not getting the same room which they reserved while booking hotel. Only 2.5 % people cancelled the booking.
## Challenges
(1) There was a lot of duplicate data.

(2) Data was present in wrong datatype format.

(3) Choosing appropriate visualization techniques to use was difficult.

(4) A lot of null values were there in the dataset.
