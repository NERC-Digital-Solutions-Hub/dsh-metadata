# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Soil state and environmental parameters across geo linked sampling locations

## Executive summary
- Presents soil state and environmental parameters from samples collected at 32 UK grassland sites, spanning paired intensive and extensive management with low and high pH parent soils.
- Sampling occurred in winter–spring 2015–2016; samples were subdivided for analysis of total Nitrogen, total Carbon, total organic Carbon, total Phosphorus, soil pH, soil moisture, loss on ignition, sand, silt, clay, FT-IR spectra, and bulk density.
- Project aims to understand soil functional change under different management and climate scenarios as part of the NERC U-GRASS program.

## Field sampling and provenance
- 32 sites across the UK with land-use contrasts (low vs. high intensity nearby).
- Soil cores (15x5 cm) collected along 100 m interface, every 25 m, yielding 5 paired replicates per site.
- Cores collected Nov 2015–Feb 2016; stored frozen at -20°C prior to analysis.

## Analytical measurements (how/what)
- Total Nitrogen, total Carbon, total organic Carbon: ball-milled, oven-dried samples analyzed by Elementar Vario EL; decarbonation with HCl for OC.
- Total Phosphorus: H2O2/H2SO4 digestion, followed by colorimetric analysis (molybdate/antimony tartrate) and absorbance at 880 nm.
- Soil pH: measured in deionised water after equilibration.
- Soil moisture and LOI: moisture by drying; LOI by combustion to estimate organic matter content.
- Texture: sand, silt, clay percentages (to sum 100%), measured by NRM Laboratories.
- FT-IR spectra: mid-infrared MIR-ATR (4000–650 cm-1) on dried, milled samples; specific peak areas used to estimate clay bonds, saturated carbon, and carbonate.
- Bulk density: calculated from core weight and corrected volume after removing stones.
- Analyses conducted by CEH Lancaster, CEH Wallingford, CEH Lancaster/Wallingford, and NRM Laboratories; results compiled and deposited as CSV.

## Data structure and contents
- File: UgrassSoilStateAndEnvironmentalParameters.csv
- 450 data rows, 19 columns
- Key fields include:
  - Id, latitude, longitude: geolocated identifiers for cross-referencing
  - organic_C, total_C, total_N, total_P
  - pH, soil_moisture, LOI
  - sand, silt, clay (texture)
  - FT-IR derived: clay1_IR, clay2_IR, clay_quality_IR, sat_C_IR, calc_IR
  - bulk_density
- NA entries indicate missing data
- Units and descriptions provided for each column

## Data provenance and management
- Samples stored at -20°C; analyses performed across CEH sites; results compiled into an Excel file and then exported to CSV.
- Deposition: data prepared for and deposited into the Environmental Information Data Centre (EIDC).
- Authors/institutions: Griffiths, R.I.; Puissant, J.; Dos Santos Pereira, G.; Goodall, T.I.; Centre for Ecology & Hydrology (Bangor, Wallingford, Lancaster).

## GIS and mapping relevance
- Geolocated soil state and environmental parameters across 32 UK sites enable map-based visualization of chemical, physical, and spectral soil properties.
- Data supports spatial analyses of soil functions, carbon/nutrient dynamics, and responses to land-use management and climatic scenarios.
- Suitable for integration with other GIS layers (land use, climate grids, soil maps) to assess soil ecosystem services and resilience.

## Associated files
- Analysis outputs: UgrassSoilStateAndEnvironmentalParameters.csv