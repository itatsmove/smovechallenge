# Bookings API
Here you'll find a simple endpoint that you can use to get a list of Smove bookings. It returns an array of bookings with some interesting information like start / end times, user, assigned car, and pickup / dropoff locations.

### Endpoint
```
GET https://challenge.smove.sg/bookings
```

### Example Response
```
[
  {
    "id": 57602,
    "car": {
      "id": 8602,
      "licence_plate": "SKK5326K"
    },
    "book_start": 1527964722,
    "book_end": 1528000423,
    "pickup": {
      "id": 50,
      "code": "KVL",
      "lat": 1.302,
      "lng": 103.769
    },
    "dropoff": {
      "id": 36,
      "code": "BLT",
      "lat": 1.276,
      "lng": 103.797
    },
    "user": {
      "id": 13132,
      "name": "Cloud Strife"
    }
  },
  . . .
]
```

Note that the data is randomly generated on each call, so don't be alarmed if it keeps changing!
