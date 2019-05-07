# New York City Taxi Fare Prediction Android App

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

![](https://github.com/ec500-software-engineering/project-16-NYC-Taxi-Fare-Prediction/blob/master/image/Pick%20up%20locations%20in%20NYC%20.jpg)

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

1. Add a Map to our application using the Maps SDK for Android. The map includes a marker (pin), to indicate a specific location.

![](https://github.com/ec500-software-engineering/project-16-NYC-Taxi-Fare-Prediction/blob/master/image/marker.jpg)

2. Select current location and display details of the place at that location. When the user clicks on search box, it will offer the user a list of likely places to choose from.
3. UI Controls
4. Map Gestures
5. Location Data

！[](https://github.com/ec500-software-engineering/project-16-NYC-Taxi-Fare-Prediction/blob/master/image/location%20data.jpg)

One of the unique features of mobile applications is location awareness. Adding location awareness to the app offers users a more contextual experience because mobile users bring their device with them everywhere.

***Location permissions***: Allows the API to determine as precise a location as possible from the available location providers, including the Global Positioning System (GPS) as well as WiFi and mobile cell data.

***The My Location layer***: Shows the user’s current position on the map. Once it’s enabled, the My Location button appears in the top right corner of the map. When a user clicks the button, the camera centers the map on the current location of the device. The location is indicated on the map by a small blue dot if the device is stationary, or as a chevron if the device is moving.

* **Google Places SDK for Android**

The Places SDK for Android allows us to build location-aware apps that respond contextually to the local businesses and other places near the device. 



