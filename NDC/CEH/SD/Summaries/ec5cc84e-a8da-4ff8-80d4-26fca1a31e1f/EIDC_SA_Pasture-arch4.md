# Pasture_2050.csv

- Aim
  - Analyze how changes in water availability will affect cropland/pasture land availability in 2050 by combining projections of water scarcity with current pasture extent to identify country-level vulnerabilities.

- Data sources and collection methods
  - Global maps of change in annual runoff (%) and water scarcity (index 1–4; 1 not water scarce, 4 severely water scarce) derived from five GCMs, provided by Prof. N. Arnell.
  - Current pasture land area maps obtained from Earthstat (open access).
  - Global cropland maps created from a mix of satellite-derived data and census statistics, on a global 5 arcminute grid (see Monfreda et al., 2008; Ramankutty et al., 2008).

- Fieldwork and instrumentation
  - Desk-based study using a PC; no field or laboratory work.

- Calibration and data preparation
  - No calibration performed; all data are pre-published (Section 2 references).
  - Runoff change values: percentage change from baseline (1960–1990) to 2050.
  - Water scarcity values: scaled 1–4 (1 not water scarce, 4 severely water scarce).
  - Cropland areas provided in hectares.

- Analysis methods
  - Overlay global maps in ArcGIS to identify vulnerable areas.
  - Vulnerable pasture land defined where both criteria are met: (i) runoff percentage is declining, and (ii) the watershed is water scarce (2050).
  - Calculate the country-level percentage of pasture land that is vulnerable.

- Data values and units
  - Pasture_2050.csv presents the percentage of total pasture area in each country classified as vulnerable.
  - Country names align with FAOSTAT nomenclature.

- Quality control
  - Datasets sourced directly from data owners to prevent modification.

- Data structure
  - Country-level estimates averaged across the five GCM models.
  - Includes standard deviation across models.

- Additional information and references
  - Climate models used: CSIRO Mk3, Hadley Centre HADGEM, INMCM4, IPSL-CM5, MRIOC_CM3 (as listed).
  - References for underlying datasets and methods include Arnell et al. (2011), Gosling & Arnell (2016), Gosling et al. (2010), Monfreda et al. (2008), Ramankutty et al. (2008).