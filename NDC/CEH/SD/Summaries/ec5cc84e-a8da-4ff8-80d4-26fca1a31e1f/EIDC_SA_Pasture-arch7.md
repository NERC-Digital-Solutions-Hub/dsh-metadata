# The data included in Pasture_2050.csv relates to an analysis of the impact changes in water availability will have on cropland availability in 2050.

## Overview
- An analysis combining projections of water scarcity with current pasture extent to identify country-level vulnerabilities of pasture land to water scarcity in 2050.
- Uses GIS-based spatial overlays to assess vulnerability across countries.

## Data sources
- Global maps of:
  - Change in annual runoff (%)
  - Water scarcity index (1–4; 1 = not water scarce, 4 = severely water scarce)
  - Derived from 5 general circulation models (GCMs) provided by Arnell and colleagues (Arnell et al., 2011).
- Current pasture land area maps from Earthstat (open-access platform).
- Cropland maps created from a mix of satellite-derived data and census statistics (global 5 arcminute grid); details in Monfreda et al., 2008 and Ramankutty et al., 2008.

## Experimental design
- Desk-based study to project country-level vulnerabilities by overlaying pasture land with future water-scarcity/change projections.

## Data collection and sources
- Data published prior to this analysis; no new calibration performed.
- Runoff change: baseline 1960–1990 to 2050 (percent change).
- Water scarcity: scaled 1–4 (1 = not water scarce, 4 = severely water scarce).
- Cropland areas: reported on a hectare (ha) basis.

## Data processing and analysis
- Spatial overlays performed in ArcGIS produced a schematic linkage between hydrological model outputs (from five GCMs) and global pasture land maps (Figure 1).
- Vulnerability definition: pasture land must reside in areas that (i) show declining annual runoff and (ii) are water scarce in 2050.
- Vulnerable percentage: the share of all cropland within a country that lies in areas meeting both criteria is classified as vulnerable.

## Data structure and units
- Pasture_2050.csv: percentage of total pasture area in each country classified as vulnerable.
- Country names follow FAOSTAT conventions.
- Data are country-level estimates averaged across the 5 GCMs; standard deviation provided.

## Quality control
- Datasets sourced directly from data owners to prevent modification or versioning issues.

## GIS considerations and reproducibility
- Resolution: global data on a 5 arcminute grid; country-level summaries derived from model aggregation.
- Multi-model approach using five GCMs: CSIRO_Mk3, HADGEM, INMCM4, IPSL_CM5, MRIOC_CM3.
- Projections and methods referenced from Arnell et al. (2011) and related datasets; detailed methodology available in cited literature.

## Additional information and references
- Arnell N.W., van Vuuren D.P., Isaac M. 2011. The implications of climate policy for the impacts of climate change on global water resources. Global Environmental Change, 21, 592–603.
- Gosling N., Arnell N.W. 2016. Global assessment of the impact of climate change on water scarcity. Climatic Change, 134, 371–385.
- Gosling S.N. et al. 2010. Global hydrology modelling and uncertainty: running multiple ensembles with a campus grid. Phil. Trans. R. Soc. A.
- Monfreda C., Ramankutty N., Foley J.A. 2008. Farming the plant: Part 2—Geographic distribution of crop areas... Global Biogeochemical Cycles, 22, GB1022.
- Ramankutty N., et al. 2008. Farming the plant: 1. Geographic distribution of global agricultural lands in the year 2000. Global Biogeochemical Cycles, GB1003.