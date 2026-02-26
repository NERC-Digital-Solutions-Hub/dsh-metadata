# Croplands_2050.csv

- Aim: Combine projections of changes in water scarcity with current cropland extent to identify potential country-level vulnerabilities of cropland to water scarcity in 2050.

- Data sources and maps:
  - Global maps of change in annual runoff (%) and water scarcity (scale 1–4) from five GCMs, provided by Arnell et al. (2011).
  - Current global cropland area maps from EarthStat (5 arc-minute grid), derived from satellite data and census statistics (Monfreda et al. 2008; Ramankutty et al. 2008).

- Fieldwork and calibration:
  - Desk-based study; no field data collection.
  - No calibration required; data are pre-published.
  - Runoff changes are relative to 1960–1990 baseline; water scarcity scaled 1–4; cropland area in hectares.

- Analytical methods (GIS workflow):
  - Overlay cropland with GCM-specific projections of water scarcity and annual run-off in ArcGIS.
  - Define vulnerability where cropland lies in areas with: (i) declining runoff and (ii) water scarcity.
  - Calculate the percentage of cropland within each country that is classified as vulnerable.

- Outputs and units:
  - Croplands_2050.csv reports the percentage of cropland per country that is vulnerable.
  - Country names align with FAOSTAT formatting.
  - Figure 1 illustrates the spatial overlays linking hydrological model outputs and cropland maps.

- Data structure and uncertainty:
  - Country-level estimates averaged across the five GCMs.
  - Includes standard deviation to reflect cross-model uncertainty.

- Quality control:
  - Datasets sourced directly from data owners to avoid modified versions.

- Data details and models:
  - GCMs used: CSIRO Mk3, HADGEM, INMCM4, IPSL_MR, MRIOC_CM3.

- References and context:
  - Arnell et al. 2011; Gosling et al. 2016; Gosling et al. 2010; Monfreda et al. 2008; Ramankutty et al. 2008.