# Surfs Up

## Overview

The purpose of this analysis is to practice with sqlite to work with databases inside a jupyter notebook with pandas. SQLAlchemy was used to achieve this and Flask was used to create a simple local page to present the data. The analysis is on Hawaii weather data do determine differences in the months of June and December.

## Results

The June and Decemeber summary data can be found below:

![june_temps.PNG](https://github.com/mcwatts88/surfs_up/blob/main/Resources/june_temps.PNG) ![dec_temps.PNG](https://github.com/mcwatts88/surfs_up/blob/main/Resources/dec_temps.PNG)

* The mean temp in June is roughly 75(U+00B0)F and the mean temp in December is 71(U+00B0)F.

* The range of temperatures in December is higher with a 27(U+00B0) difference between the minimum and maximum temperature. The range in June is only 21(U+00B0).

* The standard deviation further shows the variance in temperature is higher in December than in June.

## Summary

The weather between June and December didnt change much overall for Hawaii, though the temperature did vary slightly more in December than it did in June. The precipitation for June and Decemeber can be found with the following two queries:

```
# June precipitation
session.query(Measurement.date, Measurement.prcp).where(extract("month", Measurement.date ) == '06')
```

```
# December precipitation
session.query(Measurement.date, Measurement.prcp).where(extract("month", Measurement.date ) == '12')
```