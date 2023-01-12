# Calculating Satellite Orbital Parameters from TLEs

Investigating the accuracy decay of orbital information over time on the Suomi NPP Satellite

## **Introduction**

The goal of this project is to confirm the necessity of obtaining satellite orbital information on a regular basis, as the predictions for future states become less certain over time. As orbital real estate becomes more and more crowded, this is a vital step to prevent collisions and maintain a safe operating environment. 


## **Method**

I acquired several historical TLEs for the Suomi NPP satellite from Space-Track.org ranging from January 2021 to present. I used each of these TLEs in combination with pyorbital to predict what the orbital characteristics of the craft would be today, and compared to the current ground truth longitude, latitude, and altitude as of 1/11/2023 13:38:26 UTC. These parameters were calculated at intervals of 1 week, 2 weeks, 3 weeks, 4 weeks, 2 months, 4 months, 8 months, and 2 years ago. Finally, I plotted the errors at each interval to see if the prediction accuracy truly worsens over time.  


## **Results**

*Figure 1* shows a table of the raw data — the latitude, longitude, and altitude of the satellite on 1/11/2023, as well as the predictions for these parameters at each interval.

![](./images/img01.png)

> Figure 1

*Figure 2* shows the percent error of these calculations compared to the ground truth.


![](./images/img02.png)

> Figure 2

Finally, *Figure3* contains a plot of the error for each paramater vs the time interval at which the prediction was made.

![](./images/img03.png)


## **Conclusions**

The plots clearly show the prediction errors grow to an unacceptable margin rather quickly. Even fractions of a percent can lead to miles of error at this scale. Therefore the process of updating these measurements consistenly will continue to be of vital importance.


## **Links**


[Jupyter Notebook](https://github.com/LindstromKyle/Calculating-Satellite-Orbital-Paramaters-from-LTEs/blob/main/Historical_TLEs.ipynb)  





