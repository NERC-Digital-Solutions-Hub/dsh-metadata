# Extensive_Intensive_Spatial_README.docx

## Overview
- Single time-point spatial dataset detailing site characteristics, soil parameters, and soil greenhouse gas emissions for two sites: Extensive and Intensive.
- Aims to support environmental monitoring and analysis of soil GHG fluxes and soil properties in a standardised, comparable format.
- Data collected on grid-based sampling across each site, with detailed site-specific measurement and analysis protocols.

## Study design and sites
- Extensive site: 11.5 ha with 112 sampling points on a 30 m × 30 m grid, plus 3 random points (total n = 115).
- Intensive site: 1.78 ha with 78 points on a 15 m × 15 m grid, plus 21 points on a 25 m × 25 m grid (total n = 99).
- Location and sampling markers recorded in the field using GPS/RTK equipment.
- Elevation, slope, and aspect derived from 1 m LiDAR data; Compound Topographic Index (CTI) calculated from LiDAR-derived terrain information.

## Data collected and measurement techniques
- Soil GHG measurements:
  - Air-tight static chambers used at both sites to sample soil headspace gas; timing differed by site (Extensive: 0 and 60 min; Intensive: 0 min approximated ambient, 40 min after closure).
  - CO2, N2O, and CH4 concentrations measured with a Perkin Elmer Clarus 580 Gas Chromatograph (N2O via ECD; CO2 and CH4 via FID).
  - Two-point sampling employed to handle large numbers of chambers; assumed linear increases in headspace concentrations.
  - CO2 flux reflects soil and plant respiration without photosynthesis due to chamber opacity.
- Soil and bulk properties:
  - Bulk density determined from cores (Extensive: 100 cm³, 0–5 cm; Intensive: 0–10 cm); samples stored at 4 °C prior to analysis.
  - Volumetric water content used to calculate soil percentage water-filled pore space (WFPS) and soil porosity assumptions differ by site (Extensive uses mixed organic/mineral density; Intensive assumes 2.65 g cm⁻³).
  - Gravimetric soil moisture from oven-dried samples (Extensive ~4 g; Intensive ~20 g).
  - Soil organic matter by loss-on-ignition (Extensive: 450 °C, 16 h; Intensive: 400 °C, overnight).
  - Soil pH measured with site-specific extraction/media: Extentive uses fresh soils with water; Intensive uses air-dried, ground soils with deionised water.
- Nutrient analyses:
  - Extensive site: 0.5 M K2SO4 extraction; nitrate (NO3⁻) and ammonium (NH4⁺) determined colorimetrically; extractable total oxidised nitrogen inferred as NO3⁻ (via conversion from NO3⁻/NO2⁻).
  - Intensive site: 2 M KCl extraction; NH4⁺ via Berthelot reaction; NO3⁻/NO2⁻ via reduction and Griess reaction; measurements on an Aquakem 250.
- Soil carbon and nitrogen:
  - Extensive site total C and N quantified with TruSpec® Analyzer (Leco).
  - Intensive site total C and N measured on sieved, oven-dried soils with Carlo Erba NA2000 elemental analyzer linked to an isotope ratio mass spectrometer (IRMS).
- Vegetation and manuring context:
  - Veg_type/Org_Spread field header captures vegetation type at the Extensive site and manure spreading details at the Intensive site (within specified buffer distances from boundaries or watercourses).

## Spatial data and derived variables
- Data headers include:
  - Site, Sample_ID, Grid, Easting, Northing
  - N2O_flux (µg N2O-N m⁻² h⁻¹), CO2_flux (mg CO2-C m⁻² h⁻¹), CH4_flux (µg CH4-C m⁻² h⁻¹)
  - Bulk_density (g cm⁻³), WFPS (%), Soil_moisture (%)
  - Organic_Matter (%), Soil_pH, Soil_NO3N (mg NO3⁻-N kg⁻¹ soil DW), Soil_NH4N (mg NH4⁺-N kg⁻¹ soil DW)
  - Total_C (%), Total_N (%), CtoN
  - Elevation (m), Slope (degrees), CTI, Aspect (degrees)
  - Veg_type/Org_Spread (site-specific vegetation or manure_spread context)
- Grid references and coordinates recorded for spatial mapping and integration with other geographic data.

## Data processing, quality, and storage
- Data from established, standardised methods designed for comparability across sites and studies.
- QA considerations include standardized sampling times, consistent chamber methods, and uniform laboratory analyses where feasible.
- Samples and data were stored and processed following site-specific protocols; soil samples refrigerated at 4 °C prior to analysis.
- Data intended for storage in appropriate portals and datasets, enabling sharing and re-use to support environmental monitoring and policy assessment.

## Analytical methods and references
- Headspace gas analysis and chamber methodology guided by established literature to ensure comparability (e.g., De Klein & Harvey; Chadwick et al.; De Klein et al.).
- Soil organic matter and carbon/nitrogen determinations via established loss-on-ignition protocols and elemental analysis.
- Nutrient extraction and colorimetric/photometric analyses aligned with standard soil analysis references (Miranda et al.; Mulvaney; Krom; MAFF reference book 427; Searle).
- Topographic and hydrological indices derived from LiDAR data; CTI calculations referenced to Moore et al.; Sørensen et al.; Evans et al.
- References cited within the dataset description provide methodological grounding for each measurement and calculation.

## Key takeaways for analysts
- A well-documented, site-comparative dataset designed for monitoring environmental health and policy performance over time.
- Two contrasting management scenarios (Extensive vs. Intensive) with harmonised data structure to facilitate cross-site analyses of soil GHG fluxes and soil properties.
- Comprehensive metadata supports robust spatial analyses, reproducibility, and integration with other environmental datasets.