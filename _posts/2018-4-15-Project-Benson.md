---
layout: post
title: Project Benson
categories:
  - Metis
tags:
  - Metis
  - Data Science
  - Project
---

First week at Metis, first project. :scream: \
Gotta run... :running: \ 
...Better... :bulb: \
...Gotta ride.  :bicyclist: :smiley: \
  

### Turning turnstiles data in two-wheeled return of investment
 
The goal of the project was to analyze the NYC Metropolitan Transportation Authority (MTA) [turnstile data](http://web.mta.info/developers/turnstile.html "MTA Turnstile"). \

We were to come up with a project proposal for possible customers and help them with new business opportunities analyzing the MTA turnstile data.\

Our team of four decided to target bike sharing companies by offering them detailed analysis of the exits from the metro stations.\

The final results shows at least two potential customer of the bike sharing service:

* The workers needing to blow out the traffic during the work days
* The people searching recreative activities during the weekend

### You need to clean up before you run...

The start of the project immediately halt when we found that the data presented several problems.
The data were logs of the number of exits and entries at every turnstile at every station approximately every 4 hours.
However the sampling did not take place at the same hours and there were same issues to take into account:

* Duplicate number of exits (and entries) at the same turnstile at the same time
* Turnstiles counters decrementing instead of incrementing the counter
* Turnstile counters resetting at arbitrary 
* Counters whose value was too high to be reasonable

Bacause of these issues, we have to devise ways to get all the data cleaned up.

### ... but then, you can start the race !

We evaluated first the top 10 stations with regard to the number of exits.\
We want to provide bike to the people exiting from the metro stations, and so we focused on the exits data.\
The top 10 daily stations are summarized in the table below.

![_config.yml]({{ site.baseurl }}/images/benson/CumulativeBarChart.png)

The same stations in the map of Manhattan, the diameter is proportional to the number of exits.
![_config.yml]({{ site.baseurl }}/images/benson/Top 10 MTA Stations NYC Pic 1.JPG)
The analysis shows the possibility of using the cluster information to aggregate smaller stations in wider groups. 

### Go smooth !

We move than into the analysis of median of the exits during the months. The shapes are pretty smooths, with dips near the holidays, and this indicates good forecasting potential.\ 
![_config.yml]({{ site.baseurl }}/images/benson/MedianExitsMonthsLine.png)
The results are confirmed by increasing the granularity of the analysis.
![_config.yml]({{ site.baseurl }}/images/benson/MedianExitsWeeksLine.png)

### And after the work days, enjoy the weekend !!!
In this graph we take a look of the daily  mean exits of the top 10 station.
![_config.yml]({{ site.baseurl }}/images/benson/MedianExitsDayLine.png)
What immediately stands out is the presence of two different trending, one related to the working days and the other to the weekend.\
This point directly to two different customer population, the working commuters and the people using it for recreation during the weekend.

### What's on the Horizon?

The analysis open up to short term promising scenarios:

* Incorporate data of bike sharing companies
* Evaluate cluster of small station for better management of the bike fleet
* Last but not least ... Who doesn' t love to take a ride in a park? We plan to add public park data to widen the customer population!
