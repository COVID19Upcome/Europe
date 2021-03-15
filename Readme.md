Readme
## Updates 15/03/2021
Our simple model expects that we will enter in the last wave of the european sars-cov-2 outbrake.  As usual the predictions are purely made using the two variable model trained with the early 2020 italian data. The predicitons of todays (from 11/02/2021 to 18/03/2021) nicely show the general increase of the predicted viral activity.
## Updates 06/01/2021
Our model is the original version trained with the thin data collection gathered in Feb-Mar 2020. The variables used to predict the viral outbreak (PM2.5 and O3) are now consistently outside the observed boundaries signalling a general intensification of the pandemic. We are planning to update the model based on a whole year data in Mar-Apr 2021. As the ozone concentration is low in all the countries monitored and will remain low until April (based on previous years data), our model suggests that the viral activity will be consistent till then. The PM2.5 values are expected to reach maximal values in Jan-Feb,  making the infections potentially even more aggressive.
## Description
This repository is created to accompany the classifier/predictor described in the manuscript *Fronza R Lucic B*, "**Spatial-temporal variations of atmospheric factors contribute to SARS-CoV-2 outbreak**". It contains the daily predictions of the simple ANN model on the escalation risk of the SARS-Cov-2 in 154 spots in the major European countries.

The model is trained using both PM2.5 and ozone concentration. We found that a threshold effect, due to the PM2.5 level (PM2.5 < 30 ug/m3), abolish the ozone predictive capacity. We showed in the study that in the period under survey (21.02-18.03), the PM2.5 concentration in southern Italian regions (latitude < 41.5N) and in most of the European regions, are below this threshold; the predictions in these areas are enriched in false positives (false escalation). The model with both the predictive variables is safer as it overestimates the escalating conditions (red points).

### The map
In the folder `outbrake_predictions`, we regularly place (weekly) the png daily maps and an animated gif map that shows the risk of an outbreak given a measure of the concentration of PM2.5 and ozone in the previous month.

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

## Warnings
The results of this examination represent an attempt to find underlying variables that drive the spatial and temporal SARS-Cov-2 activity. The model used is still at an elementary stage, where no data conditioning is made (it is also a remarkable aspect). 

The temporal pattern of the predictions is accurate and follow quite well the general activity of the virus. It is clear the synchronicity between the prediction and the viral activity. 

The geographical pattern is less precise and can be seen as the combination of factors that are not modelled in this attempt. Such factors are

1. Environmental background conditions. As an example, it is apparent that  Puglia (a south-east Italian region) has a singular combination of climatic factors that deviate from the rest of the country.
2. Population variables. The model does not use any variable directly connected to the population. As a consequence, it is possible to find a "red" area in a location that is not populated. 
3. Social variables. Behavioural differences in different areas could explain differences in the infection incidence.