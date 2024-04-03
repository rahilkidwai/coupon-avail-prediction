# Coupon Avail Prediction

- [Coupon Avail Prediction](#coupon-avail-prediction)
  - [Problem Statement](#problem-statement)
  - [Dataset](#dataset)
    - [Data Attributes](#data-attributes)
    - [Missing Values](#missing-values)
  - [Data Exploration](#data-exploration)
    - [Coupons Utilization](#coupons-utilization)
    - [Weather Histogram](#weather-histogram)
    - [Bar visits utilizing coupons](#bar-visits-utilizing-coupons)
    - [Coffee shop visits utilizing coupons](#coffee-shop-visits-utilizing-coupons)

## Problem Statement
Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?
Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?
The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.
## Dataset
- Record Count: 12,684
- Input Attributes: 25
- Output Attributes: 1
### Data Attributes
| Attribute | Description | Unique Values |
| --------- | ----------- | ------------- |
| destination | Driving destination | No Urgent Place, Home, Work |
| passanger | | Alone, Friend(s), Kid(s), Partner |
| weather | | Sunny, Rainy, Snowy |
| temperature | | 55, 80, 30 |
| time | | 2PM, 10AM, 6PM, 7AM, 10PM |
| coupon | coupon offered | Restaurant(<20), Coffee House, Carry out & Take away, Bar, Restaurant(20-50) |
| expiration | time before coupon expires | 1d, 2h |
| gender | Female, Male |
| age | | 21, 46, 26, 31, 41, 50plus, 36, below21 |
| maritalStatus | | Unmarried partner, Single, Married partner, Divorced, Widowed |
| has_children | | 1, 0 |
| education | | Some college - no degree, Bachelors degree, Associates degree, High School Graduate, Graduate degree (Masters or Doctorate), Some High School |
| occupation | | Unemployed, Architecture & Engineering, Student, Education&Training&Library, Healthcare Support, Healthcare Practitioners & Technical, Sales & Related, Management, Arts Design Entertainment Sports & Media,Computer & Mathematical, Life Physical Social Science, Personal Care & Service, Community & Social Services,Office & Administrative Support, Construction & Extraction, Legal, Retired, Installation Maintenance & Repair, Transportation & Material Moving, Business & Financial, Protective Service, Food Preparation & Serving Related, Production Occupations, Building & Grounds Cleaning & Maintenance, Farming Fishing & Forestry |
| income | Annual income | $37500 - $49999, $62500 - $74999, $12500 - $24999, $75000 - $87499, $50000 - $62499, $25000 - $37499, $100000 or More, $87500 - $99999, Less than $12500 |
| car | Type of car driven | nan, Scooter and motorcycle, crossover, Mazda5, do not drive, Car that is too old to install Onstar :D |
| Bar | Number of times that he/she goes to a bar | never, less1, 1 ~ 3, gt8, nan, 4 ~ 8 |
| CoffeeHouse | Number of times that he/she goes to a coffee house | never, less1, 4 ~ 8, 1 ~ 3, gt8, nan |
| CarryAway | Number of times that he/she buys takeaway food | nan, 4 ~ 8, 1 ~ 3, gt8, less1, never |
| RestaurantLessThan20 | Number of times that he/she eats at a restaurant with average expense less than $20 per person | 4 ~ 8, 1 ~ 3, less1, gt8, nan, never |
| Restaurant20To50 | Number of times that he/she eats at a restaurant with average expense between $20 to $50 per person | 1 ~ 3, less1, never, gt8, 4 ~ 8, nan |
| toCoupon_GEQ5min | | 1 |
| toCoupon_GEQ15min | | 0, 1 |
| toCoupon_GEQ25min | | 0, 1 |
| direction_same | | 0, 1 |
| direction_opp | | 1, 0 |
| Y | | 1, 0 |

### Missing Values
- The column "car" has over 90% null values (12,576) and can be dropped from the dataset
- Following columns "Bar", "CoffeeHouse", "CarryAway", "RestaurantLessThan20", "Restaurant20To50" all have null values ranging from 1% to 2%. For these columns all the rows with null can be dropped.
  - Bar                       107 nulls
  - CoffeeHouse               217 nulls
  - CarryAway                 151 nulls
  - RestaurantLessThan20      130 nulls
  - Restaurant20To50          189 nulls

## Data Exploration
### Coupons Utilization 
![Coupons Utilization](/images/coupons_utilization.png))

### Weather Histogram
![Weather Histogram](/images/weather_hist.png))

### Bar visits utilizing coupons
- People are likely to visit bar in general, if they get a coupon (41% acceptance)
- People who visit bar occasionally (<3 / mo) are more likely to accept the bar coupon
- People without accompanying Kids are more likely to accept the bar coupon
- People not widowed are more likely to accept the bar coupon
- Low income people are less likely to accept the bar coupon

### Coffee shop visits utilizing coupons
- People are likely to buy coffee, if they get a coupon (50% acceptance)
- People will more likely to buy coffee when temperature is above 55
- Gender does not effect the decision
- Coffee coupon are very much likely to be utilized in morning and afternoon
- High income people (>50K) are highly likely to avail coupon when not alone

![Coffee acceptance by time slot](/images/coffee_y_time_slot.png))
