# Gridded data of greenhouse gas emissions from livestock and crops for year 2000

## Overview
- Global gridded dataset of greenhouse gas (GHG) emissions for the year 2000 at 5 arc-minute resolution, covering 172 crops and 7 livestock commodities.
- Emissions represented for nitrous oxide (N2O), methane (CH4), and carbon dioxide (CO2).
- Provides both total GHG emissions and emission intensities (GHG per unit of product) for livestock products.
- Spatial scope: global; temporal scope: circa year 2000 with annual resolution (1997–2003 context).

## Scope and contents
- Livestock commodities: bovine meat and milk; small ruminant meat and milk (sheep/goat); pig meat; poultry meat and eggs.
- Crop list is defined in the file named cropnames.
- Outputs include GHG emissions at farm and feed levels, including feed-related emissions and crop-associated emissions.
- Outputs formatted as CSV files for easy import into MATLAB, Python, or R; recommended GIS workflow includes converting CSVs to raster for mapping.

## Methodology
- Overall methodology discussed in a forthcoming publication by Dalin et al. (in prep).
- Cropland emissions (for crops) are the sum of:
  - Peatland drainage
  - Rice cultivation
  - Manure and synthetic fertilizer application to cropland
- Rice and manure-cropland emissions depend on manure amounts estimated from Herrero et al. 2013 (re-estimated by Dalin et al.), aligned with methods in Carlson et al. 2016.
- Two versions of cropland N2O emissions were produced (linear and non-linear models); this summary presents the linear model:
  - Emissions factor (EF) uses IPCC linear method: 0.31% for flooded rice, 1% for all other crops.
- Livestock emissions include:
  - Farm-level GHG: methane from enteric fermentation (bovine, sheep, goat), methane and N2O from manure management, N2O from manure on pasture
  - Feed-related GHG: N2O from synthetic fertilizer on cropland and grassland, and manure applied to cropland
- Diet composition, country of origin of feeds (FAOSTAT), and forage efficiency/productivity of grasslands (ORCHIDEE) are incorporated.
- Input data formats: .xlsx, .tif, .nc4; processing performed in MATLAB (and tested in R).
- Outputs saved as .csv using MATLAB R2023a; convert_csv_to_raster.R provides a path to generate rasters for GIS.

## Data formats and access
- Spatial resolution: 5 arcminutes; coordinate reference system: WGS 84.
- Temporal scope: around year 2000 (1997–2003 window; annual resolution).
- Units:
  - Emissions: tonnes CO2 equivalent (tCO2e)
  - Emission intensities: tonnes CO2e per kilogram of product (tCO2e/kg)
- Data structure and access:
  - Input formats: .xlsx, .tif, .nc4
  - Output format: .csv
  - Files are named to reflect GHG emissions and intensities for all seven livestock commodities
  - Conversion to raster via convert_csv_to_raster.R for GIS applications

## Quality control and validation
- Independent, parallel coding and computations by two co-authors; results cross-validated between MATLAB and R implementations.
- National-scale averages compared against FAOSTAT for validation.

## Data provenance and references
- Methodology and data are anchored to multiple sources:
  - Herrero et al. 2013 (biomass use, feed efficiencies, and GHG emissions in global livestock systems)
  - FAOSTAT (detailed trade matrix)
  - Chang et al. 2016 (process-based vegetation modeling for grassland management)
  - De Klein et al. 2006; IPCC Guidelines for National GHG Inventories
  - Carlson et al. 2016, 2017 (N2O emissions, cropland GHG intensity)
  - Gerber et al. 2016 (fertilizer management mitigation opportunities)
- Data and methodology cited in the forthcoming Dalin et al. publication (in prep).