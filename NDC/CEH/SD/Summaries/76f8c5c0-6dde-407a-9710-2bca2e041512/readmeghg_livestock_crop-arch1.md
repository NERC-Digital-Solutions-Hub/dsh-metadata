# Gridded data of greenhouse gas emissions from livestock and crops for year 2000

## Overview
- Global gridded dataset of greenhouse gas (GHG) emissions (nitrous oxide, methane, carbon dioxide) associated with annual production of 172 crops and 7 livestock commodities for around year 2000.
- Includes emission processes for crops (peatland drainage, rice cultivation, manure and synthetic fertilizer on cropland) and livestock (enteric fermentation, manure on grassland, manure management on farm; feed-related emissions from manure on feed crops and fertilizer on grassland/feed crops; additional cropland emissions for feed crops).
- Also provides GHG emission intensities (GHG per unit mass of animal product) for livestock products.

## Data and scope
- Spatial resolution: 5 arc-minute global grid.
- Temporal scope: circa year 2000 (1997–2003 with annual resolution).
- Units: tonnes CO2 equivalent (CO2e) for emissions; tonnes CO2e per kilogram of animal product for emission intensities.
- Livestock commodities: bovine meat and milk, small ruminant (sheep and goat) meat and milk, pig meat, poultry (meat and eggs).
- Crop list: provided in the file cropnames.

## Methodology
- Emissions for crops: sum of peatland drainage (from Carlson et al. 2016), rice cultivation, and manure/synthetic fertilizer on cropland; manure-based and fertilizer-based emissions depend on the amount of manure available for cropland (based on Herrero et al. 2013, re-estimated by Dalin et al. in prep.).
- Emissions for livestock: farm-level GHGs (enteric methane for ruminants; manure management methane and nitrous oxide) plus nitrous oxide from manure left on pasture; feed-related GHGs include nitrous oxide from synthetic fertilizer on cropland and grassland, and manure on cropland.
- Two nitrous oxide modeling approaches considered (linear and non-linear); results presented using the linear model with IPCC-style emission factors (EFs): 0.31% for flooded rice, 1% for all other crops.
- Diet composition, feed crop origins (FAOSTAT), and grassland productivity inputs (ORCHIDEE) are incorporated.

## Data formats and processing
- Input formats: .xlsx (e.g., Herrero et al. 2013), .tif (e.g., Monfreda et al. 2008), .nc4 (e.g., Chang et al. 2016).
- Processing: imported into MATLAB (and tested in R); final outputs saved as CSV.
- Output accessibility: CSV files can be imported into MATLAB, Python, or R; a companion R script (convert_csv_to_raster.R) converts CSVs to raster format for GIS tools.
- File naming: each file corresponds to the GHG emissions and GHG emission intensities for all seven livestock commodities.

## Quality control
- Independent, parallel coding and computations by two co-authors using MATLAB and R with matching results.
- National-scale averages compared against FAOSTAT values for validation.

## Temporal and spatial details
- Spatial scope: global; Coordinate Reference System: WGS 84.
- Temporal resolution: annual (1997–2003; around 2000).
- Outputs expressed in tonnes CO2e (emissions) and tonnes CO2e per kg of product (intensities).

## Content details and usage
- Livestock commodities covered: bovine meat/milk, small ruminant meat/milk, pig meat, poultry meat/eggs.
- Crop emissions depend on a defined crop list (cropnames file).
- Data can be used to map regional emission patterns, compare intensities across products, and support life cycle or policy assessments related to global livestock and crop emissions.

## References
- Herrero, M., et al. Biomass use, production, feed efficiencies, and greenhouse gas emissions from global livestock systems. PNAS, 2013.
- FAOSTAT. FAO, 2022.
- Chang, J., et al. Biogeosciences, 2016.
- Dalin, et al. (in prep).
- De Klein, C., et al. IPCC Guidelines, 2006.
- Carlson, K.M., et al. Nature Climate Change, 2017.
- Gerber, J.S., et al. Glob. Change Biol., 2016.