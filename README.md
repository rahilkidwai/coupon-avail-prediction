# Coupon Avail Prediction

- [Coupon Avail Prediction](#coupon-avail-prediction)
  - [Problem Statement](#problem-statement)
  - [Dataset](#dataset)
    - [Data Attributes](#data-attributes)
    - [Missing Values](#missing-values)
  - [Data Preprocessing](#data-preprocessing)
  - [Techniques / Evaluation](#techniques--evaluation)
    - [Methodology](#methodology)
    - [Results](#results)

## Problem Statement
Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?
Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?
The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.
## Dataset
- Record Count: 12684
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
| coupon | | Restaurant(<20), Coffee House, Carry out & Take away, Bar, Restaurant(20-50) |
| expiration | | 1d, 2h |
| gender | Female, Male |
| age | | 21, 46, 26, 31, 41, 50plus, 36, below21 |
| maritalStatus | | Unmarried partner, Single, Married partner, Divorced, Widowed |
| has_children | | 1, 0 |
| education | | Some college - no degree, Bachelors degree, Associates degree, High School Graduate, Graduate degree (Masters or Doctorate), Some High School |
| occupation | | Unemployed, Architecture & Engineering, Student, Education&Training&Library, Healthcare Support, Healthcare Practitioners & Technical, Sales & Related, Management, Arts Design Entertainment Sports & Media,Computer & Mathematical, Life Physical Social Science, Personal Care & Service, Community & Social Services,Office & Administrative Support, Construction & Extraction, Legal, Retired, Installation Maintenance & Repair, Transportation & Material Moving, Business & Financial, Protective Service, Food Preparation & Serving Related, Production Occupations, Building & Grounds Cleaning & Maintenance, Farming Fishing & Forestry |
| income | | $37500 - $49999, $62500 - $74999, $12500 - $24999, $75000 - $87499, $50000 - $62499, $25000 - $37499, $100000 or More, $87500 - $99999, Less than $12500 |
| car | | nan, Scooter and motorcycle, crossover, Mazda5, do not drive, Car that is too old to install Onstar :D |
| Bar | Number of times that he/she goes to a bar | never, less1, 1 ~ 3, gt8, nan, 4 ~ 8 |
| CoffeeHouse | Number of times that he/she goes to a coffee house | never, less1, 4 ~ 8, 1 ~ 3, gt8, nan |
| CarryAway | Number of times that he/she buys takeaway food | nan, 4 ~ 8, 1 ~ 3, gt8, less1, never |
| RestaurantLessThan20 | Number of times that he/she eats at a restaurant with average expense less than $20 per person | 4~8, 1~3, less1, gt8, nan, never |
| Restaurant20To50 | | 1 ~ 3, less1, never, gt8, 4 ~ 8, nan |
| toCoupon_GEQ5min | | 1 |
| toCoupon_GEQ15min | | 0, 1 |
| toCoupon_GEQ25min | | 0, 1 |
| direction_same | | 0, 1 |
| direction_opp | | 1, 0 |
| Y | | 1, 0 |

### Missing Values

## Data Preprocessing
## Techniques / Evaluation
### Methodology
### Results
