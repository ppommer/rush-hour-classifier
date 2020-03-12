# Rush Hour Classifier

Analytics competition in the course of the lecture _Business Analytics_ (IN2028) at the Technical University of Munich.

## Objective
The dataset consists of recent taxi trips taken in the city of Chicago. The objective of the analytics competition was to build a model that correctly classifies whether trips in the test set happened during 'rush hour' or not. A trip is a rush-hour trip if it started between 7am and 9am or between 4pm and 6pm on a working day. A working day is defined as a weekday (Monday-Friday) that is not a public holiday in the city of Chicago, i.e. neither an Illinois public holiday or a United States federal public holiday. ’between’ is defined as inclusive on both sides, i.e. trips started at 7:00:00am or 9:00:00am on a workday both count
as rush hour trips.

## Data

Attribute | Description
--- | ---
ID | (Integer) Unique identifier for the trip
Taxi ID | (String) A unique identifier for the taxi.
Trip Start Timestamp | (Train: Data & Time; Test: Date only) When the trip started, rounded to the nearest 15 minutes.
Trip End Timestamp | (Training: Date & Time; Test: Date only) When the trip ended, rounded to the nearest 15 minutes.
Trip Seconds | (Number) Time duration of the trip in seconds.
Trip Miles | (Number) Distance of the trip in miles.
Pickup Community Area | (Integer) The Community Area where the trip began. This column will be blank for locations outside Chicago.
Dropoff Community Area | (Integer) The Community Area where the trip ended. This column will be blank for locations outside Chicago.
Fare | (Number) The fare for the trip in USD.
Tips | (Number) The tip for the trip. Cash tips generally will not be recorded.
Tolls | (Number) The tolls for the trip.
Extras | (Number) Extra charges for the trip.
Trip Total | (Number) Total cost of the trip, the total of the previous columns.
Payment Type | (String) Type of payment for the trip.
Company | (String) The taxi company.
Pickup Centroid Latitude | (Number) Approximate latitude of the start of the trip. Blank for locations outside Chicago.
Pickup Centroid Longitude | (Number) Approximate longitude of the start of the trip. Blank for locations outside Chicago.
Dropoff Centroid Latitude | (Number) Approximate latitude of the end of the trip. Blank for locations outside Chicago.
Dropoff Centroid Longitude | (Number) Approximate longitude of the end of the trip. Blank for locations outside Chicago.

## Evaluation
The predictions are evaluated based on the _**balanced accuracy**_ - the arithmetic mean of sensitivity (true positive rate) and specificity (true negative rate).
