# Infrastructure Case Study

## Sensors

SomeCompany® has developed sensors capable of taking readings of the environment, including temperature, humidity, and atmospheric pressure.

During the day (from 07:00 to 19:00), the sensors take readings every 5 seconds. During the evening (from 19:00 to 07:00), the sensors take readings every 15 seconds.

The readings are stored as json. An example reading is as follows:

```
{
  "sensor_id": "DQoOCAcMAgMJBQoNBAsDCA",
  "timestamp": 1445356800,
  "readings": {
    "temp": 26.3,
    "humd": 0.88,
    "pres": 1010
  }
}
```

The sensors are connected to the internet via 3G/4G capable SIM cards.

## Backend

SomeCompany® has also developed a backend, written in JavaScript, capable of processing these readings.

On average, the code is able to process a reading in 125ms.

The code is only able to process one reading at a time.

## Database

The readings processed by the backend are stored in a database. You can assume that the code is already capable of connecting to and inserting into a database of any type.

## Task

Your task is to design a simple infrastructure in which the readings taken by the sensors are made available for the code to process and store in the database.

The readings should be sent and processed in _soft_ real time (i.e. when they are generated, every 5/15 seconds).

Assume that the number of sensors is variable, and could scale up to a maximum of 5000.

Your solution should take into account:
* How the sensors send readings to the backend
* How the backend is hosted
* What type of database is used and how it is hosted

The infrastructure should predominantly use services available from AWS.

You may describe the proposed infrastructure using text, diagrams, a presentation, configuration scripts, or any other medium you'd like!

Bonus points are awarded for solutions that discuss scalability, security, performance, high availability, costs, monitoring and disaster recovery.

**When you're done, [email us](mailto:jamesw@smove.sg) with either a link to a repo containing the solution, or a PDF of your write up.**

Cheers,

smove's geeks

P.S: take as little or as much time as you want.
