# Pasture_2050.csv

## Aim
- Analyze how changes in water availability will affect cropland (pasture land) availability in 2050 by combining projections of water scarcity with current pasture extent to identify country-level vulnerabilities.

## Data sources and collection methods
- Global projections of change in annual runoff (%) and water scarcity (1 = not water scarce to 4 = severely water scarce) derived from 5 GCMs, provided by Prof. N. Arnell (University of Reading) with methodology from Arnell et al. 2011.
- Current global pasture land area maps from earthstat.org (5 arcminute grid).
- Global cropland maps created from a mix of satellite data and census statistics; aligned to FAOSTAT country names.

## Experimental design
- Overlay pasture land with GCM-based projections of water scarcity and runoff to identify vulnerable pasture areas at the country level for 2050.

## Fieldwork and calibration
- Desk-based study; no fieldwork.
- No calibration required since all data were previously published; runoff change relative to 1960–1990 baseline; water scarcity on a 1–4 scale; cropland areas in hectares.

## Analytical methods
- Spatially overlay datasets in ArcGIS.
- Define vulnerability where pasture land lies in areas with: (i) declining runoff and (ii) water-scarce watershed in 2050.
- Calculate the percentage of a country’s pasture area that is vulnerable.

## Nature and units of recorded values
- Pasture_2050.csv records the percentage (%) of total pasture area in each country classified as vulnerable.
- Country names follow FAOSTAT formatting.

## Quality control
- Data sourced directly from data owners to ensure unmodified versions.
- Results are averaged across five GCMs.

## Data structure and interpretation
- Country-level estimates averaged over 5 GCMs, with standard deviation provided to indicate inter-model variability.

## Additional information and references
- Models used: CSIRO_Mk3, HADGEM, INMCM4, IPSML_MR, MRIOC_CM3.
- Key references: Arnell et al. 2011; Gosling et al. 2016; Gosling et al. 2010; Monfreda et al. 2008; Ramankutty et al. 2008.