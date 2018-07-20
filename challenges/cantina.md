# QA Challenge

In an effort to diversify its business, Smove has decided to move on from car sharing and open a cucumber farm instead. Since innovative technology is a big part of what we do, we tasked our tech team with building a cucumber tracking system to make sure our growing is as efficient as possible.

To ensure each and every cucumber is given the attention it deserves, our engineers put together a simple dashboard that the cucumber operations team will use to view the status of each cucumber.

The engineers say that the site is 100% flawless and ready to deploy to production, but we noticed some funky behaviour with some early prototypes.

**For this challenge, it's your job to play around with the site they built to see if you can spot any bugs!**

Check out the site [here](https://cantina.smove.sg).

It's completely up to you _how_ you want to hunt for the bugs. Clicking around / trial & error works, but if you want to show off your experience with tools like Selenium, then go for it!

### Submission

If you manage to find any of the bugs that somehow slipped through code review, note them down and send us bug reports.

It's up to you what format you want to use for the bug report, but we suggest including things like *steps to reproduce*, *expected result*, *actual result*, etc for each bug.

**When you're done, send us:**
* Your bug reports in a format of your chosing, e.g. a bug tracking tool, compiled into a single document (pdf preferred!), etc.
* A short write up of your bug-hunting methodology, including any tools / frameworks you used and how / why you used them
* Any supporting scripts / tool configurations that you might have developed for testing
* Additional things that would like to do in a real production/QA scenario, but there was not enough time to do it

### Bonus points

The site hits a few simple endpoints to get the displayed data. Here's the specification that the engineers worked off when implementing the API:

```
GET /cucumbers

Description:
  Returns a list of cucumber objects.
  Supports pagination via skip and limit query params.

Query params:
  skip  [integer]  (required)
  limit [integer]  (required)

Expected responses:
  Status: 200
  Body: Object[]
    an array of cucumber objects
    number of results should always be <= limit

  Status: 400
  Description: when skip or limit query params are not provided
```

```
GET /cucumber

Description:
  Returns a single cucumber object whose name partially matches the given search term.
  Search should be case insensitive.

Query params:
  name  [string]  (required)

Expected responses:
  Status: 200
  Body: Object
    a single cucumber object

  Status: 400
  Description: when name query param is not provided

  Status: 400
  Description: when name query param is empty string

  Status: 404
  Description: when no matches are found
```

If you're keen for some bonus points, put together a simple integration test script that checks whether the engineers actually read the spec.

You can use any framework you'd like, such as Postman, Cucumber, Jest, etc., and include your scripts in the submission along with the bug reports.
