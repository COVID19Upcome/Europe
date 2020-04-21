## Description
This repository is created to accompany the classifier/predictor described in the manuscript *Fronza R Lucic B*, "**Spatial-temporal variations of atmospheric factors contribute to SARS-CoV-2 outbreak**". It contains the daily predictions of the simple ANN model on the escalation risk of the SARS-Cov-2 in 154 spots in the major European countries.

### The map
In the folder `Figures`, we regularly place the png daily maps and an animated gif map that shows the risk of an outbreak given a measure of the concentration of PM2.5 and ozone in the previous month.

The maps represents a graphical illustration of the evolution of the escalation predicted by the model, in all the areas under surveys. Each point on the map represents the location of the main city in the examined area. Daily, fifteen predictions were performed on each area. A prediction can be 0 (no escalation conditions) or 1 (escalation conditions), and the ratio 

~~~
         # Escalations
r = ------------------------
    # Total Predictions (50)
~~~

is determined as a measure of the predicted risk of escalation. 

The size and color of a point represents this risk:

- if the risk is lower or equal than 0.2 ( *r<=0.2*) the point is green; 
- if the risk is comprised between 0.2 and 0.5 ( *0.2 < r <= 0.5*) the point is yellow; 
- if the risk is bigger than 0.5 ( *r > 0.5*) the point is red. 

This last value matches the notion that the likelihood of an escalation in a particular region is bigger than 1 if more than half of the 50 trials are one.
