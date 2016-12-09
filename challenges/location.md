# Car Location API
This is a simple endpoint which returns the location and status of a set of cars at the current time. Each car has a latitude, longitude, and a flag denoting whether the car is currently on a trip. 

Use the endpoint to build whatever you'd like, be it some real time visualisation, interactive reporting tool, or even a video game! Feel free to use any language/framework you'd like, but make sure it's easy for us to build!

**When you're done, [Email us](mailto:hr@smove.sg) with either a link to your repo or your zipped solution, including your source code and any generated output (e.g. visualisations, reports, etc.)**

### Endpoint
```
http://challenge.smove.sg/carlocations
```

### Example Response
```
[
	{
		id: 9,
		latitude: 1.352,
		longitude: 103.819,
		is_on_trip: 0
	},
	{
		id: 12,
		latitude: 1.332,
		longitude: 103.821,
		is_on_trip: 1
	},
	. . .
]
```
