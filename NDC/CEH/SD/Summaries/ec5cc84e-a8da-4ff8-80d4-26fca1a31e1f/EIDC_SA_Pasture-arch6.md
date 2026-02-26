# Pasture_2050.csv

## Aim
- Combine projections of changes in water scarcity with current pasture land extent to identify country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources and collection
- Global maps of change in annual runoff (%) and water scarcity (scale 1–4; 1 not water scarce to 4 severely water scarce) from five GCMs, provided by Prof. N. Arnell (University of Reading).
- Current pasture land area maps from Earthstat (open access; global 5 arcminute grid).
- Cropland maps created from satellite-derived data, national/state/country census statistics (Monfreda et al., Ramankutty et al., 2008).

## Experimental design
- Desk-based study overlaying pasture land with GCM projections of water scarcity and runoff to identify vulnerable areas.
- Vulnerable land defined where pasture lies in areas with (i) declining runoff and (ii) water scarcity in 2050.

## Calibration steps and values
- No calibration required; all data are previously published.
- Runoff change expressed as percentage change from baseline (1960–1990) to 2050.
- Water scarcity on a 1–4 scale (1 not scarce, 4 severely scarce).
- Cropland areas provided on a hectare basis.

## Analytical methods
- Overlay spatial data in ArcGIS to produce country-level vulnerability estimates.
- Vulnerable land per country is based on pasture areas meeting both criteria (declining runoff and water scarcity in 2050).
- Output: the percentage of total pasture area within each country classified as vulnerable.

## Nature and units of recorded values
- Pasture_2050.csv: percentage of total pasture area in each country that is vulnerable.
- Country names aligned with FAOSTAT formatting.
- Includes standard deviation across the five GCM models for each country.

## Quality control
- Datasets sourced directly from data owners to prevent modification.

## Details of data structure
- Country-level estimates averaged across the five GCM models.
- Includes standard deviation for each value.

## Any other information useful to interpretation
- List of GCM models used: CSIRO Mk3, HADGEM, INMCM4, IPSL_CM5, MRIOC_CM3 (as named in the document).
- References for underlying datasets and methods include Arnell et al. (2011), Gosling et al. (2016, 2010), Monfreda et al. (2008), Ramankutty et al. (2008).