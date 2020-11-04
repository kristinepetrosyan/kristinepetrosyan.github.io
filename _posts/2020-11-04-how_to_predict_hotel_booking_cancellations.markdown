---
layout: post
title:      "How to predict Hotel booking cancellations!"
date:       2020-11-04 18:07:00 +0000
permalink:  how_to_predict_hotel_booking_cancellations
---




After going over Hotel booking demand dataset on a Kaggle Kernel we see data of two types of hotels. One is a resort hotel, and the other is a city hotel; both have more than 200 rooms and are classified as four star hotels.

## Problem Statement
Predict whether a booking will be canceled or not to allow the hotel’s manager to make better decisions in order to improve overbooking strategies and cancellation policies.
Methodology | CRISP-DM methodology
![](http://)
![](http://)
## Data
This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things. The total number of bookings in the database in question is about 119,390. Analysis of the data revealed several issues that had considerable influence on the model performance:
- Data Leakage, identified by “reservation status” which was similar values to the target variable. This was addressed during modeling to improve overfitting issues.
- Class imbalance, identified by “city hotel” was not addressed. However, future work can address this issue to improve performance
- Data quality problems, identified by “IsVIP” and “Company” had very few observations; ADR had outliers; “ReservedRoomType,” and “AssignedRoomType” variables had missing values; and some variables were not used in some of the hotels “RequiredCarParkingSpaces,” “TotalOfSpecialRequests,” and “DaysInWaitingList.”

## EDA
A first step in any data science project is to dig into what the data actually look like. We typically use a wide variety of data visualization techniques for this. In most examples, we have divided our dataset into reservations that were successfully booked versus reservations that were cancelled.
Build visualizations to answer the following questions:
· Where do the guests come from?
· Which are the most busy month?
· How many bookings were canceled?
· Which month have the highest number of cancellations?
· Which hotel has more cancellations?
· Would Deposit Type makes a difference?
· Any difference in market segments?
· How about distribution channels?

## Hypothesis Testing
Claim: Cancellation probability is higher when booking in advance.
In summary, the hypothesis testing in this project explores the various tests used to reject the null hypothesis statement and accept the alternative statement — “that booking in advance does increase the probability of cancellation”.
Machine Learning
This project built several classification models to predict each booking’s cancellation outcome. RandomForest Classifier is creates a set of decision trees from randomly selected subset of training set. It then aggregates the votes from different decision trees to decide the final class of the test object. Random decision forests correct for decision trees’ habit of overfitting to their training set.The model accuracy performance using RandomForest classifier was better than any other classifier:
Image for post

## Conclusion
With 88% accuracy, more than eight times out of ten, our model correctly predicts whether a reservation will be successfully booked or cancelled.
This study provides evidence of the probability to cancel a hotel booking, based on data originating directly from a booking system in Lisbon, Portugal. The results of the hypothesis claim, where the likelihood of cancellations is significantly related to booking lead time become the top predictive feature in the model’s ability to predict cancellation probabilities.
Another factor of importance is the channel, where those who book via directly or through corporate travel agencies were more likely to keep their reservations than those who book online via OTA, such as booking.com, TripAdvisor, Orbitz, Expedia, etc.
Also, the role of booking lead time and country of residence of the presumptive hotel guest in determining the cancellation probability is more pronounced for online than for offline or travel agency bookings.
By exposing these cancellation drivers, machine learning models can help hoteliers to better understand booking cancellation patterns and enable the adjustment of a hotel’s cancellation policies and overbooking tactics according to the characteristics of its bookings. Moreover, this work shows that if hotel managers had access to an application (GUI) then they could act on bookings with high cancellation probability and contain the associated revenue losses. Leading to other benefits, such as, improve overbooking/cancellation policies, and have more assertive pricing and staffing allocation strategies.
_________________________
Contact me at kristinelpetrosyan@gmail.com

https://kristinelpetrosyan.medium.com/how-to-predict-hotel-booking-cancellations-2ef66ad0262a

