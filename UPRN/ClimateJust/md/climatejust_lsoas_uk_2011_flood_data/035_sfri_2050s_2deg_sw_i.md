### Surface water | Individual | Future 2050s 2℃ scenario

**Description:** 
This field (underlying alias: `SFRI2SWI` or `SFRI_2050s_2Deg_SW_I`) represents the Social Flood Risk Index (SFRI) for surface water (pluvial) flooding under a future 2050s climate scenario, which assumes a 2°C rise in Global Mean Temperature (GMT) from a 1961-90 baseline. The SFRI is a measure of geographic flood disadvantage, identifying areas where physical exposure to flooding and high social vulnerability coincide.

**The "Individual" Measure:** 
Unlike the "Group" measure which looks at total accumulated risk, the "Individual" measure provides an "average" or "per person" risk estimate for the neighbourhood. It incorporates the chance of flooding occurring in the floodplain (accounting for any existing flood defences) combined with the overall social vulnerability of the neighbourhood (NFVI). 

It is calculated by dividing the SFRI Group measure by the total floodplain population, which is equivalent to multiplying the Expected Annual Probability of Flooding for an individual by the NFVI. This metric is highly useful for identifying neighbourhoods where the vulnerability of the exposed residents is very high, even if the actual total number of people exposed to the surface water flood hazard is relatively small.

**Vulnerability Rationale / Score Interpretation:** 
The SFRI is a relative index and has no defined units. 
* **High positive scores** indicate neighbourhoods where the individuals exposed to flooding are highly socially vulnerable (NFVI is above the UK average). 
* **Negative values** indicate that although people are exposed to surface water flooding in that area, the neighbourhood's overall social vulnerability is relatively low (NFVI is below the UK average). 
* **A value of zero** indicates that there is no population living in the floodplain for this scenario.

**Data Source:** 
The data is derived from the 2017 UK-scale assessment of present and future flood vulnerability, risk, and disadvantage produced by Sayers and Partners LLP for the Joseph Rowntree Foundation. The future climate scenarios are based on UKCP09 climate projections. The spatial data is mapped down to the neighbourhood level, corresponding to Lower Super Output Areas (LSOAs) in England and Wales, Data Zones (DZs) in Scotland, and Super Output Areas (SOAs) in Northern Ireland.