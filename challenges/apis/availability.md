# Booking Availability API
Here you'll find a simple endpoint that you can use to check for booking availability. Given a start time and an end time, it returns a set of possible start locations for a booking, each with the number of cars available at that location, and a set of possible drop off locations.

### Endpoint
```
GET https://challenge.smove.sg/availability?startTime=[startTime]&endTime=[endTime]
```

### Request Parameters
| Field        | Type         | Description  |
| ------------- |-------------| -----|
| [startTime]      | Number | The desired start time of the booking, as a unix timestamp |
| [endTime]      | Number | The desired end time of the booking, as a unix timestamp |

### Example Response
```
{
	data: [
		{
			id: 42,
			location: [1.352, 103.819],
			available_cars: 3,
			dropoff_locations: [
				{
					id: 42,
					location: [1.352, 103.819]
				},
				{
					id: 51,
					location: [1.331, 103.721]
				},
				. . .
			]
		},
		. . .
	]
}
```
