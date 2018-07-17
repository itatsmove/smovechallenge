# Bookings API
Here you'll find a simple endpoint that you can use to get a list of Smove bookings. It returns an array of bookings with some interesting information like start / end times, user, assigned car, and pickup / dropoff locations.

Use the endpoint to build whatever front end application you'd like - it's up to you to make it as simple or complex as you want!

What we're looking for is something that shows your creativity, deep understanding of front end design patterns, an eye for performance, and your ability to develop something you'd be proud to put into production.

### Frameworks

Our only requirement is that you use either [Angular 1](https://code.angularjs.org/1.5.0/docs/guide) or [React](https://reactjs.org/).

Any CSS pre-processing libraries, testing frameworks, build frameworks, state management libraries, etc. is completely up to you!

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

**When you're done, send us back a link to a repository with your source code, with a description of what you've done and any build instructions in the readme!**
