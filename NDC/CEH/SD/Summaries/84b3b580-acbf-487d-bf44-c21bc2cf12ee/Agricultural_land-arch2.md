# The data included in Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv and Wheat_2050.csv relates to an analysis of the impact changes in water availability will have on the suitability of land used in the production of these commodities in 2050.

## Aim and scope
- Combine projections of changes in water scarcity with current land-use extent for selected commodities to identify potential country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources
- Water scarcity and annual runoff maps based on projections from five global climate models (GCMs) provided by N. Arnell (University of Reading); models include CSIRO_Mk3, HADGEM, INMCM4, IPSL_MR, and MRIOC_CM3.
- Current pasture land area from Earthstat (open access).
- Cropland maps derived from satellite data plus national/state/country census statistics (Monfreda et al., 2008; Ramankutty et al., 2008).
- Commodity land areas aggregated by country ( FAOSTAT-aligned naming).

## Methodology
- Overlay land-use maps with GCM projections of water scarcity and runoff using ArcGIS.
- Define vulnerability where: (i) pasture land lies in areas with declining runoff, and (ii) the watershed is water scarce in 2050.
- Compute for each country the percentage of total land area for each commodity that is vulnerable by averaging across the five GCMs.

## Outputs and data structure
- Files: Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv, Wheat_2050.csv.
- Values represent the percentage of total area for each commodity in a country classified as vulnerable.
- Country names aligned with FAOSTAT conventions; results include standard deviation across GCMs.
- Figure 1 illustrates the spatial overlay of hydrological model outputs with global agricultural land maps.

## Calibration, quality control, and provenance
- No calibration applied; all data are pre-published as described.
- Quality control: datasets sourced directly from data owners to ensure unmodified versions.

## Units, interpretation, and notes
- Units: percentage (%) of land area per country.
- Runoff change: percentage change versus the baseline period 1960–1990.
- Water scarcity: index on a scale from 1 (not water scarce) to 4 (severely water scarce).
- Data are averaged across the 5 GCMs; accompanying standard deviation conveys uncertainty.

## Additional context and references
- Uses standardized, globally referenced datasets and methodologies to support cross-country environmental monitoring and policy evaluation.
- Key references include Arnell et al. (2011), Gosling et al. (2016), Monfreda et al. (2008), Ramankutty et al. (2008).