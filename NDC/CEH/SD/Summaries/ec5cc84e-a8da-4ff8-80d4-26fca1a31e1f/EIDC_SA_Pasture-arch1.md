# Pasture_2050.csv

- Aim
  - Combine projections of changes in water scarcity with current pasture extent to identify country-level vulnerabilities of pasture land to water scarcity in 2050.

- Data sources and variables
  - Global maps of change in annual runoff (%) and water scarcity index (1–4; 1 = not water scarce, 4 = severely water scarce) from projections of five GCMs (from Arnell et al. 2011).
  - Global pasture land area maps from earthstat.org.
  - Global cropland maps derived from satellite data plus national/state/country census data, on a 5 arcminute grid; details in Monfreda et al. 2008 and Ramankutty et al. 2008.

- Fieldwork and instrumentation
  - Desk-based study; analysis performed on a PC.

- Calibration steps and values
  - No new calibration; data are published sources.
  - Runoff change expressed as percent change from 1960–1990 baseline to 2050.
  - Water scarcity scaled 1–4.
  - Cropland areas provided per hectare (ha).

- Analytical methods
  - Overlay analyses in ArcGIS to combine pasture land with GCM projections of water scarcity and runoff.
  - Vulnerable pasture defined as areas that (i) show declining runoff percentage and (ii) are water scarce in 2050.
  - For each country, compute the percentage of total cropland that lies in areas meeting both criteria; classify that portion as vulnerable.

- Nature and units of recorded values
  - Pasture_2050.csv reports the percentage of total pasture area in each country classified as vulnerable.
  - Country names follow FAOSTAT formatting.

- Quality control
  - Datasets sourced directly from data owners to avoid modified versions.

- Details of data structure
  - Country-level estimates averaged across the five GCMs; standard deviation provided.

- Other information useful for interpretation
  - GCMs used: CSIRO_Mk3, HADGEM, INMCM4, IPSML_MR, MRIOC_CM3.
  - References and data provenance include Arnell et al. 2011; Gosling & Arnell 2016; Gosling et al. 2010; Monfreda et al. 2008; Ramankutty et al. 2008.