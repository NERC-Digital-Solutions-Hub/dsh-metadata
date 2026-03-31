### Change in mean summer maximum temperature baseline to 2050s (90th percentile) (z-score)

#### Description

This field represents a measure of **heat hazard-exposure** for a given 25km grid cell in England. It provides the projected change in the mean summer maximum temperature from the climate baseline (1961-1990) to the 2050s. The data has been standardized into a **z-score**. Specifically, this metric uses the "High estimate" or 90th percentile probability level from the climate projections.

#### Z-Score & Exposure Context

Unlike raw temperature values, a z-score is a statistical measurement that shows how an individual grid cell's projected temperature change relates to the average (mean) value across the entire country. This standardization process is used to provide a uniform scale so that the physical heat exposure data can be equally weighted and combined with socio-spatial heat vulnerability scores to calculate the final "heat disadvantage" indices.

#### Interpretation

* **High positive values:** Denote grid cells where the projected increase in the mean summer maximum temperature is higher than the English average, indicating a greater relative physical potential for exposure to rising temperatures.
* **90th Percentile Context:** Because climate models have inherent uncertainties, the UK Climate Projections 2009 (UKCP09) provide probabilistic estimates. The "90th percentile" represents a high-end estimate for the temperature change, meaning that the projected temperature increases are 90% likely to be *below* this threshold.

#### Data Source

This field is derived from the UK Climate Projections 2009 (UKCP09) 25km grid data for the 2050s. In the dataset, these probabilistic indicators are calculated across low, medium, and high emissions scenarios.
