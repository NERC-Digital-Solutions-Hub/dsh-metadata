# Pasture_2050.csv

## Aim
- Combine projections of changes in water scarcity with current pasture land extent to identify country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources
- Global maps of changes in annual runoff (%) and water scarcity (scale 1–4; 1 = not water scarce, 4 = severely water scarce) from five GCMs/GCM projections, provided by Prof. N. Arnell (University of Reading). Methodology detailed in Arnell et al. (2011).
- Global maps of current pasture land area downloaded from Earthstat (open access).
- Global cropland maps created from a mix of satellite-derived data and national/state/country census statistics, on a global 5 arcminute grid; details in Monfreda et al. (2008) and Ramankutty et al. (2008).

## Data collection and preprocessing
- Desk-based study; no fieldwork (computing environment: PC).
- All data used were previously published; no recalibration of data required.
- Annual runoff: percent change between baseline (1960–1990) and 2050.
- Water scarcity: scaled 1–4 (1 = not water scarce; 4 = severely water scarce).
- Cropland areas: provided on a hectare basis.

## Analytical methods
- Overlay global maps in ArcGIS to combine pasture land with projections of water scarcity and runoff.
- Define vulnerable land where pasture land lies in areas that (i) show declining runoff and (ii) are water scarce in 2050.
- For each country, calculate the percentage of all pasture within areas meeting both criteria; classify that portion as vulnerable.

## Data outputs, structure, and units
- Pasture_2050.csv values represent the percentage of total pasture area in each country classified as vulnerable.
- Country names follow FAOSTAT naming conventions.
- Data are country-level estimates averaged across the five GCM models; standard deviation provided to reflect model spread.

## Quality control and provenance
- Datasets sourced directly from data owners to avoid modified versions.
- Documented list of GCM models used: CSIRO_Mk3, HADGEM, INMCM4, IPSML_MR, MRIOC_CM3.

## Notes on interpretation and references
- Underlying sources and methodologies:
  - Arnell N.W., van Vuuren D.P., Isaac M. (2011). Global Environmental Change.
  - Gosling et al. (2016); Gosling et al. (2010).
  - Monfreda et al. (2008); Ramankutty et al. (2008).
- Data interpretation depends on the assumption that overlapping classifications accurately reflect vulnerability of pasture lands to future water scarcity.