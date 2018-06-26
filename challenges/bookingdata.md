# Booking Data
Here you'll find a file containing one week's worth of booking data. A single booking consists of:

| Field        | Type         | Description  |
| ------------- |-------------| -----|
| id      | Number | Unique ID of the booking |
| car      | Number | ID of the car |
| start      | Number | Start time of the booking<br />*Time is in blocks of 15 minutes, starting at Sunday 6am. <br />E.g 4 = Sunday 7am, 96 = Monday 6am, etc.* |
| end      | Number | End time of the booking |
| start_location      | Number | ID of the bookings start location |
| end_location      | Number | ID of the bookings end location |

There are 1486 bookings, on 141 cars, using 54 locations.

You can use this data in any way you'd like, such as building a platform to visualise it, performing some analysis, or even trying to optimise it to find better car/booking assignments. Feel free to use any language/framework you'd like, but make sure it's easy for us to build!

### File
[bookingdata.json](bookingdata.json)
