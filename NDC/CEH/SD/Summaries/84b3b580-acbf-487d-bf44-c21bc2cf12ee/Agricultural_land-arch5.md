# The data included in Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv and Wheat_2050.csv relates to an analysis of the impact changes in water availability will have on the suitability of land used in the production of these commodities in 2050.

## Purpose and scope
- Objective: Combine projections of changes in water scarcity with current land-use extent for selected commodities to identify country-level vulnerabilities of pasture land to water scarcity in 2050.
- Outputs: Country-level estimates of land area vulnerable to water scarcity for six commodities, expressed as a percentage of total land area used for each commodity per country.

## Data sources and provenance
- Water projections: Global maps of change in annual runoff (%) and water scarcity (scale 1–4) derived from five GCMs (global climate models), provided by Prof. N. Arnell.
- Land-use inputs: Current pasture land area from Earthstat; cropland maps produced from a mix of satellite data and census statistics.
- Spatial resolution: Global maps on a 5 arc-minute grid.
- Key references for data sources: Arnell et al. (2011); Monfreda et al. (2008); Ramankutty et al. (2008).
- FAOSTAT naming convention used for country identifiers.

## Data processing workflow and methods
- Study design: Desk-based, using GIS to overlay outputs.
- Processing steps:
  - Overlay land area associated with each commodity with 2050 projections of water scarcity and annual runoff.
  - Define vulnerable land where both criteria are met (declining runoff and water-scarce in 2050).
  - Compute the percentage of each country’s total land area that is vulnerable for each commodity.
- Tools: ArcGIS used for spatial overlays.
- Output files: Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv, Wheat_2050.csv.

## Calibration, units, and data interpretation
- Calibration: None required; all data are pre-published.
- Runoff change: Percent change relative to baseline (1960–1990) for 2050.
- Water scarcity: Index scale 1 (not water scarce) to 4 (severely water scarce) for 2050.
- Units: Vulnerable land area expressed as a percentage of total country area suitable for each commodity.
- Data alignment: Country names correspond to FAOSTAT formatting.

## Data structure and uncertainty
- Structure: Country-level estimates averaged across five GCM models.
- Uncertainty: Standard deviation provided for each country-commodity estimate, reflecting inter-model variability.
- GCM ensemble models used: CSIRO_Mk3, HADGEM, INMCM4, IPSL_CM4, MRIOC_CM3.

## Quality control and provenance assurance
- Quality assurance: Datasets used were obtained directly from data owners to avoid modified versions.
- Provenance: Clear linkage to original data sources and published methodologies (Arnell et al. 2011; related hydrology and agricultural datasets).

## Reuse considerations and governance implications for data stewards
- Metadata and discoverability: Datasets are clearly labeled by commodity and country, with links to original data sources and methods.
- Versioning and updates: Averaging across five GCMs; stewardship should document model choices and provide versioned updates if newer GCM ensembles become available.
- Metadata standards: Include baseline period, climate model names, spatial resolution, aggregation method (country-level, averaged across GCMs), and uncertainty (standard deviations).
- Data sharing and licensing: Data derived from multiple public sources; clearly note provenance and any usage restrictions from source datasets; ensure that derived data maintain traceability to original inputs.
- Usability and interoperability: Ensure compatibility with common GIS and statistical tools; provide clear field definitions (country, commodity, vulnerable_area_pct, std_dev, run_off_change, water_scarcity_2050).
- Operational considerations: Be prepared to address data access challenges from original data owners and synthetic recombinations if model ensembles or land-use datasets are updated.

## References and accompanying documentation
- Arnell N.W., van Vuuren D.P., Isaac M. 2011. The implications of climate policy for the impacts of climate change on global water resources. Global Environmental Change, 21, 592–603.
- Gosling et al. and Monfreda/Ramankutty et al. related works on global hydrology modeling and agricultural land distribution.
- Figure 1 schematic illustrating the spatial overlays of hydrological model outputs with global agricultural land maps.