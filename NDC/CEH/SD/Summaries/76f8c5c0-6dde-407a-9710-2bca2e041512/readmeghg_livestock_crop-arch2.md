# Gridded data of greenhouse gas emissions from livestock and crops for year 2000

## Purpose and monitoring value
- Provides gridded estimates of greenhouse gas emissions (CO2e) for 172 crops and 7 livestock commodities at 5 arc-minute resolution global coverage, around year 2000.
- Includes emission sources for crops (peatland drainage, rice, manure and synthetic fertilizer on cropland) and for livestock (enteric fermentation, manure on grassland, manure management, and feed-related emissions).
- Supplies both total GHG emissions and emission intensities (GHG per unit of animal product) to support environmental health assessment and policy performance monitoring over time.

## Scope and components
- Livestock commodities: bovine meat and milk, small ruminants (sheep and goat) meat and milk, pig meat, and poultry meat and eggs.
- Crop list is detailed in the file cropnames.
- Temporal scope around year 2000 (1997–2003 window) with annual resolution.

## Methodology (overview)
- Overall method described in Dalin et al. (in prep); uses a linear model for N2O emissions from cropland and grassland.
- Crop emissions: sum of peatland drainage, rice cultivation, and fertilizer/manure on cropland, with manure inputs guided by Herrero et al. (2013) and updated by Dalin et al. (in prep.), aligned with Carlson et al. (2016) methodologies.
- Livestock emissions: farm-level methane from enteric fermentation; methane and nitrous oxide from manure management; nitrous oxide from manure on pasture; plus feed-related nitrous oxide from synthetic fertilizer and manure applied to cropland; accounting for diet, feed origin, and grassland productivity.
- Two N2O modeling approaches produced; results shown for the linear model (EFs: 0.31% for flooded rice, 1% for other crops).

## Data inputs and formats
- Input file types: .xlsx, .tif, .nc4.
- Processed in Matlab (and tested in R); outputs saved as .csv.
- Each output file corresponds to the GHG emissions and emission intensities for all seven livestock commodities.

## Outputs, usability, and formats
- Outputs are in CSV format for easy processing; includes instructions to convert to raster format using convert_csv_to_raster.R for GIS applications.
- Designed to be imported into MATLAB, Python, or R for mapping and analysis.

## Quality control
- Independent, parallel coding and computations by two co-authors using Matlab and R with matching results.
- National-scale averages cross-validated against FAOSTAT values.

## Data characteristics and access
- Spatial scope: global; spatial resolution: 5 arcmin; coordinate system: WGS 84.
- Temporal scope: 1997–2003 (circa year 2000); temporal resolution: annual.
- Units: tonnes CO2e for emissions; tonnes CO2e per kilogram of product for emission intensities.
- Data format: CSV files suitable for processing and visualization; GIS-ready after conversion.

## References (key sources)
- Herrero et al. 2013; Carlson et al. 2016; Carlson et al. 2017; Gerber et al. 2016; IPCC guidelines (De Klein et al. 2006); FAOSTAT data; Chang et al. 2016; Dalin et al. (in prep).