## Description
This document is an attempt to observe the classifier/predictor described in the manuscript Fronza R Lucic B, "Spatial-temporal variations of atmospheric factors contribute to SARS-CoV-2 outbreak" in predicting the escalation risks of the SARS-Cov-2  in 154 spots in the major European countries.

## Artefacts and their usage
In the folder `Figures` we regularly place a heatmap called `heatmap2020MMDD.pdf` and a dendrogram `dendro2020MMDD.pdf` where `MMDD` the last updating timepoint.

### The heatmap
The heatmap represents a graphical illustration of the evolution of the expected escalation in all the areas under surveys. Each row represents the expectation for a particular region as a vector of comulative predictions (escalation vector; no escalation=0/yellow,escalation=1-50/red gradient). Each column represents the likely escalation at that day.
### The dendrogram

The dendrogram combines the regions based on a hierarchical cluster derived from the patterns of the escalation vectors. We predefined the number of groups up to 7.