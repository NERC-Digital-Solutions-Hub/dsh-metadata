# Croplands_2050.csv

- Objective
  - Combine projections of changes in water scarcity with the current extent of croplands to identify potential country-level vulnerabilities of cropland to water scarcity in 2050.

- (1) Experimental design / Sampling regime
  - Desk-based analysis integrating hydrological projections with cropland extent to assess country-level vulnerabilities by 2050.

- (2) Collection methods
  - Global maps of change in annual runoff (%) and water scarcity (scale 1–4; 1 = not water scarce, 4 = severely water scarce) derived from five GCMs (global climate models), provided by Prof. N. Arnell.
  - Global cropland area maps downloaded from earthstat.org, created from satellite data combined with census statistics, on a global 5 arc-minute grid (Monfreda et al. 2008; Ramankutty et al. 2008).

- (3) Fieldwork and laboratory instrumentation
  - Desk-based study; no fieldwork or laboratory instruments used.

- (4) Calibration steps and values
  - No new calibration; all data are pre-published.
  - Runoff: percent change relative to baseline (1960–1990) to 2050.
  - Water scarcity: 1–4 scale (1 not scarce, 4 severely scarce).
  - Cropland areas: expressed in hectares.

- (5) Analytical methods
  - Overlay cropland maps with GCM-specific projections of water scarcity and runoff using ArcGIS.
  - Define land as vulnerable if cropland lies in areas with: (i) declining annual runoff and (ii) water-scarce watershed.
  - Calculate the country-level percentage of cropland that is vulnerable by averaging across the 5 GCMs.

- (6) Nature and Units of recorded values
  - Croplands_2050.csv contains the percentage (%) of total cropland per country classified as vulnerable.
  - Country names align with FAOSTAT formatting.
  - Figure 1 describes the spatial overlays of hydrological model outputs (5 GCMs) and cropland maps.

- (7) Quality control
  - Datasets sourced directly from data owners to ensure original versions were used.

- (8) Details of data structure
  - Country-level estimates averaged across the 5 GCMs.
  - Standard deviation provided to reflect inter-model variability.

- (9) Any other information useful to interpretation
  - GCM models used: CSIRO Mk3, Hadley Centre HADGEM, INMCM4, IPSL CM5 (listed as IPSML_MR), and MRIOC_CM3.
  - References for underlying data: Arnell et al. 2011; Gosling & Arnell 2016; Gosling et al. 2010; Monfreda et al. 2008; Ramankutty et al. 2008.