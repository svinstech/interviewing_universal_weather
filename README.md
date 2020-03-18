# Universal Weather - Compare Alaska weather to Mars
---
## Problem statement
> Your goal is to build a Proof Of Concept app that will collect weather data for Mars and Fairbanks, Alaska. The app should be able to produce a JSON array from the collected data that shows the daily max and daily min temperature for Mars and Fairbanks, Alaska for the last 7 days.

For example (not real data):
```
[
  {
    "date":  "2020-01-01",
    "min_mars_temp":  -10,
    "max_mars_temp":  -1,
    "min_fairbanks_temp":   12,
    "max_fairbanks_temp":  17
  },
  {
    "date":  "2020-01-02",
    "min_mars_temp":  -17,
    "max_mars_temp":  -11,
    "min_fairbanks_temp":   14,
    "max_fairbanks_temp":  21
  }
]
```
## Data sources
### Mars
NASA’s Mars Insight Mission provides daily temperature readings from the surface of Mars.
* The data can be accessed via API here: [https://api.nasa.gov/](https://api.nasa.gov/)
* Look at the documentation for [InSight: Mars Weather Service API.](https://api.nasa.gov/assets/insight/InSight%20Weather%20API%20Documentation.pdf)
  * Api_key = `1SVv7ZFZhGafR3BT4Q7ClcjhWmhp9DGt49ALovOL`

### Fairbanks, Alaska
A snapshot of last 90+ days of data recordings have been provided in a file in this repo: `fairbanks data.csv`

---

## Setup:

A simple `docker-compose` is provided for you in this repo that includes postgres. If you're not familiar with [docker compose](https://docs.docker.com/compose/), here are a few quick commands to get you started

* `docker-compose up -d` - brings up the docker-compose environment and services (just postgres)
* `docker-compose ps` - list of running services

Once the compose file is running, you should be able to connect locally. The postgres user password is _<insert the name of this repo>_
