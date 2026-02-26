# Radiocarbon dating of charcoal pieces collected from soil in the Amazon Basin

## Data overview
- Dataset of radiocarbon dating for macrocharcoal pieces (≥ 1 mm) collected in Guyana, Peru, and Brazil within Amazon forest plots that are part of the RAINFOR network.
- Total samples: 60 charcoal pieces dated.
- Field campaigns: 2015, 2017, 2018, 2019.
- Data stored in C14.csv; generated with support from NERC and CAPES, Brazil.
- Related publications listed, providing context and methods.

## Sampling and collection methods
- Charcoal fragments collected at each site from soil profiles in three replicate pits, spaced 100 m apart, just outside the 1 ha plots.
- Macrocharcoal sampling: soil excavated in 1 cm depth increments up to 70 cm; charcoal separated, air-dried, stored in plastic containers.
- Per pit, 4 charcoal pieces selected for dating:
  - Prefer the sample nearest the surface from each pit.
  - Then select three samples from progressively deeper 5 cm depth increments.
- Northern Peru site includes an additional date at 46 cm depth from a fourth pit to balance sample size.

## Data analysis and laboratory methods
- Sample preparation: scrape surface soil from charcoal.
- Pre-treatment at UK NERC facility using standard acid-base-acid protocol.
- Samples combusted to CO2, cryogenically purified, and converted to graphite via Fe/Zn reduction.
- 14C dating performed with Accelerator Mass Spectrometry (AMS) at:
  - NERC Radiocarbon Facility (UK)
  - Physics Institute of Universidade Federal Fluminense (Brazil)

## Recorded values and units
- Units: radiocarbon age in years before present (BP).
- Key columns in C14.csv:
  - Location, Plot, Latitude, Longitude
  - Soil_Pit, Depth
  - C-14_age_yr_BP, C-14_age_Uncertainty
  - Lab_ID

## Data quality and missing data
- Runs that failed or did not converge were discarded.
- Missing data labeled as NA; some field-record information may be unavailable.

## Dataset structure and references
- CSV file: C14.csv with columns as described (location, plot, coordinates, pit, depth, age, uncertainty, lab ID).
- Method reference: Slota et al. 1987 (preparation of small samples for 14C targets).
- Related publications documenting dataset context:
  - Feldpausch et al. 2022, Frontiers in Forests and Global Change
  - Goulart et al. 2017, Quaternary Geochronology

## Potential GIS applications and considerations
- Spatial mapping: latitude and longitude enable plotting radiocarbon ages across Amazon plots; tie ages to specific plots (RAINFOR).
- Depth-resolved visualization: depth and soil_pit enable vertical profiling of ages within pits.
- Data integration: can be combined with other RAINFOR data (soil properties, vegetation, carbon dynamics) for spatial analyses.
- Data quality awareness: consider age uncertainties and missing data when building maps or analyses; account for discarded failed runs.