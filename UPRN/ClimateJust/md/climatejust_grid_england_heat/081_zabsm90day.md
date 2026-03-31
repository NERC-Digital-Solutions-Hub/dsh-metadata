### Mean summer maximum temperature 2050s (90th percentile) (z-score)

#### Description

This field represents a measure of **heat hazard-exposure** for a given 25km grid cell in England. It provides the projected mean summer maximum temperature (the expected average daily maximum temperature across June, July, and August) for the 2050s. The data has been standardized into a **z-score**. Specifically, this metric uses the "High estimate" or 90th percentile probability level from the climate projections.

#### Z-Score & Exposure Context

Unlike raw temperature values, a z-score is a statistical measurement that shows how an individual grid cell's projected temperature relates to the average (mean) value across the entire country. This standardization process is used to provide a uniform scale so that the physical heat exposure data can be equally weighted and added to socio-spatial heat vulnerability scores to calculate the final combined "heat disadvantage" indices.

#### Interpretation

* **High positive values:** Denote grid cells where the projected mean summer maximum temperature is significantly higher than the English average, indicating a greater physical potential for exposure to high temperatures.
* **90th Percentile Context:** Because climate models have inherent uncertainties, the UK Climate Projections (UKCP09 and UKCP18) provide probabilistic estimates. The "90th percentile" represents a high-end estimate for the expected temperature, meaning that projected temperatures are 90% likely to be *below* this threshold.

#### Data Source

This field is derived from the UK Climate Projections 2009 (UKCP09) 25km grid data for the 2050s. In the dataset, these probabilistic z-score indicators are calculated across low, medium, and high emissions scenarios.
