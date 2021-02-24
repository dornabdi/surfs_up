# surfs_up

## Overview of Project

### Purpose
For this project, I analyzed weather and climate trends trends before opening a surf and ice cream shop in Oahu. We did this analysis because both of these services are weather-dependent and we want to ensure that this is a sustainable business venture. We specifically performed summary statistics analysis on the months of June and December. 

## Results

### Three key differences between June and December
 
- The mean temperature in Oahu for the month of June is 74.9 degrees Fahrenheit while the mean temperature for December is 71.0 degrees.

- The minimum temperature in Oahu for the month of June is 64.0 degrees Fahrenheit while the minimum temperature for December is 56.0 degrees.

- The maximum temperature in Oahu for the month of June is 85.0 degrees Fahrenheit while the maximum temperature for December is 83.0 degrees.

There are clear distintions between temperature trends between the two months, please view the summary statistics for each month below: 

<br/> ![june_temps](june_temps.png) 


<br/> ![dec_temps](dec_temps.png) 

## Summary 
Two additional queries to gather more weather data for June and December 
(do precipitation because that will impact surf shop)
In addiition to analyzing temperature data, it is also important to view summary statistics data for precipitation. It is much less likely for customers to patronize a surf or an ice cream shop when it is pouring rain. 

I ran the following queries to find summary statistics on precipitation in the busy tourist months of June and December. 

results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all() <br/>
results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()

Once I did that, I got the following results. 


<br/> ![june_prcp](june_prcp.png) 


<br/> ![dec_prcp](dec_prcp.png) 
