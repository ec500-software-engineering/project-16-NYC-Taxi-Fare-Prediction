# New York City Taxi Fare Prediction Andord App

> Project overview: 
https://www.kaggle.com/c/new-york-city-taxi-fare-prediction

We will build ***a mobile Android app*** that predict the fare amount (inclusive of tolls) for a taxi ride in New York City given the pickup and dropoff locations. Our app would ask Google to figure out how to predict the estimated fare amount by using a few features to determine the expected fare amount. The information that Google has obtained are past taxi rides that include:Pickup Time/Date, Pickup Latitude/Longitude, Dropoff Latitude/Longitude, Passenger Count, Fare Amount.

To process the pickup and dropoff location information, we need to add a map to our Android app, and Android Studio would be the development environment we choose for building our app with the Maps SDK for Android. We get an API key with restriction for Android apps to access the Google Maps servers.

# User stories: 
As a passenger，I would like to know my estimated taxi fare which is as more precise as possible.

As a driver, I'd like to see how much I can earn from a trip.

# Definition of First Sprint: 

Definition of the modular architecture of first sprint:
![draw](https://user-images.githubusercontent.com/43126280/54558538-64677500-4994-11e9-80a4-03c2d716ee34.jpeg)

## Dataset instruction

> pickup_longitude - float for longitude coordinate of where the taxi ride started.
> pickup_latitude - float for latitude coordinate of where the taxi ride started.
> dropoff_longitude - float for longitude coordinate of where the taxi ride ended.
> dropoff_latitude - float for latitude coordinate of where the taxi ride ended.
> passenger_count - integer indicating the number of passengers in the taxi ride.

In our task, the aim is to predict fare_amount - float dollar amount of the cost of the taxi ride. This value is only in the training set; this is what you are predicting in the test set and it is required in your submission CSV.

## Model Selection

* Linear Regression: Based on the absolute longitude and latitude value to predict the fare amount by using linear regression.

* XGBoost: It’s one of the gradient boost method called eXtreme Gradient Boost used for supervised Machine Learning. The weak learner used in XGBoost is generally the decision tree.

## App Implementation
* **Google Maps SDK for Android**
* **Google Places SDK for Android**


