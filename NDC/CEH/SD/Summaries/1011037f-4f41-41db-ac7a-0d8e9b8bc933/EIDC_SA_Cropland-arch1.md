# Croplands_2050.csv

## Aim
- Analyze how changes in water availability affect cropland availability in 2050 at the country level.
- Identify country-level vulnerabilities by combining projections of water scarcity with current cropland extent.

## Data sources and collection methods
- Water scarcity and annual runoff projections derived from five global climate models (GCMs) and based on Arnell et al. (2011); data provided by Prof. N. Arnell (University of Reading).
- Current cropland extent obtained from Earthstat.org; cropland maps created from satellite data combined with national/state/country census data (5 arc-minute grid); references Monfreda et al. (2008) and Ramankutty et al. (2008).

## Experimental design and calibration
- Desk-based study; no fieldwork.
- No new calibration performed; all data were previously published.

## Analytical methods
- Overlay cropland maps with GCM projections of water scarcity and with annual runoff changes using ArcGIS.
- Define vulnerability for cropland in a country as cropland located in areas that meet both criteria: (i) runoff percentage declines, and (ii) watershed classified as water scarce.
- Compute the percentage of total cropland in each country that is vulnerable.
- Results are averaged across the five GCMs, with the standard deviation reported to reflect model agreement.

## Nature and units of recorded values
- Croplands_2050.csv contains the percentage (%) of a country’s cropland classified as vulnerable.
- Country names follow FAOSTAT naming conventions.
- Values include country-level means across GCMs and their standard deviations.

## Data structure and accessibility
- Data are country-level estimates averaged over five GCMs; standard deviation provided.
- Figure 1 illustrates the spatial overlay concept linking hydrological model outputs with cropland maps.

## Quality control
- Datasets were obtained directly from data owners to prevent use of modified versions.

## Interpretation and use
- Provides a metric of potential cropland vulnerability to future water scarcity by country.
- Useful for informing policy and planning under climate-change scenarios, with explicit uncertainty across GCMs shown via standard deviations.

## References and data provenance
- Arnell N.W., van Vuuren D.P., Isaac M. (2011); Gosling et al. (2016); Gosling et al. (2010); Monfreda et al. (2008); Ramankutty et al. (2008).