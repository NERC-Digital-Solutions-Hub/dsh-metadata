### Change in temperature of the warmest night baseline to 2050s (10th percentile) (z-score)

**Description:**
This field represents a measure of **heat hazard-exposure** for a given 25km grid cell in England. It provides the projected change in the temperature of the warmest summer night from the climate baseline (1961-1990) to the 2050s. The data has been standardized into a **z-score**. Specifically, this metric uses the "Low estimate" or 10th percentile probability level from the climate projections.

**Z-Score & Exposure Context:**
Unlike raw temperature values, a z-score is a statistical measurement that shows how an individual grid cell's projected temperature change relates to the average (mean) value across the group. This standardization process provides a uniform scale so that the physical heat exposure data can be equally weighted and combined with socio-spatial heat vulnerability scores to calculate the final "heat disadvantage" indices. 

**Interpretation:**
*   **High positive values:** Denote grid cells where the projected increase in the temperature of the warmest night is higher than the average, indicating a greater relative physical potential for exposure to rising nighttime temperatures. 
*   **10th Percentile Context:** Because climate models have inherent uncertainties, the UK Climate Projections 2009 (UKCP09) provide probabilistic estimates representing a spread of outcomes. The "10th percentile" represents a low-end estimate for the temperature change, meaning that the projected temperature increases are 90% likely to be *above* this threshold. 

**Data Source:**
This field is derived from the UK Climate Projections 2009 (UKCP09) 25km grid data for the 2050s. In the dataset, these probabilistic estimates are provided across low, medium, and high emissions scenarios.