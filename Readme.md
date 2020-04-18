## Description
This repository is created to accompany the classifier/predictor described in the manuscript *Fronza R Lucic B*, "**Spatial-temporal variations of atmospheric factors contribute to SARS-CoV-2 outbreak**". It contains the daily predictions of the simple ANN model on the escalation risk of the SARS-Cov-2 in 154 spots in the major European countries.
### The map
In the folder `Figures`, we regularly place an animated gif map that shows the likelihood of an outbreak given the concentration of PM2.5 and ozone in the previous month.
The map represents a graphical illustration of the evolution of the expected escalation in all the areas under surveys. Each point on the map represents the location of the main city in the examined area. Daily, fifteen predictions were performed on each area, and the ratio r=#Escalation/#predictions is determined as a simple measure of the predicted risk of an escalation. The size of the point represents this risk. If the risk is lower or equal than 0.2 ( *r<=0.2*) the point is green; if the risk is comprised between 0.2 and 0.5 ( *0.2 < r <= 0.5*) the point is yellow; if the risk is bigger than 0.5 ( *r > 0.5*) the point is red. This last value matches the notion that the likelihood of an escalation is bigger than 1.


