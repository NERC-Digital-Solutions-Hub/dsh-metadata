# Gridded data of greenhouse gas emissions from livestock and crops for year 2000

## Aim and scope
- Provides gridded greenhouse gas (GHG) emissions and emission intensities for the year 2000, across 172 crops and 7 livestock commodities.
- Global coverage at a 5 arc-minute spatial resolution; temporal focus around year 2000 (1997–2003); annual temporal resolution.
- Outputs include total GHG emissions (tonnes CO2e) and emission intensities (tonnes CO2e per kg of product).

## Data coverage and commodities
- Spatial scope: global land area; coordinate reference system: WGS 84.
- Commodities: seven livestock categories (bovine meat and milk, small ruminant meat and milk, pig meat, poultry meat and eggs) and a defined crop list via the file cropnames.

## Methodology
- Overall approach developed in a forthcoming publication by Dalin et al. (in prep).
- Crop emissions (5 arcmin) = peatland drainage + rice cultivation + manure and synthetic fertilizer on cropland.
- Livestock emissions = farm-level GHGs (enteric fermentation, manure management, manure on pasture) + feed-related GHGs (from cropland and grassland) including manure on feed crops and fertilizer on grassland/feed crops.
- Emissions factors use IPCC linear method (0.31% for flooded rice; 1% for other crops).
- Diet composition (Herrero et al. 2013), feed crop origins (FAOSTAT), and grassland productivity (ORCHIDEE) inform calculations.
- Data inputs formats: .xlsx, .tif, .nc4; processed in Matlab (and tested in R).
- Final outputs saved as .csv; guidance provided for converting to raster via an R script (convert_csv_to_raster.R).

## Quality control and validation
- Independent parallel coding and computations by two co-authors using Matlab and R; results matched.
- National-level averages compared with FAOSTAT values for validation.

## Data structure, formats, and access
- Units: tonnes CO2e (emissions) and tonnes CO2e per kg of product (emission intensities).
- Temporal scope: circa year 2000; period 1997–2003; annual resolution.
- Data structure and accessibility: CSV files; designed for import into MATLAB, Python, or R; CSVs can be converted to GIS-ready rasters.
- File naming indicates that outputs cover all seven livestock commodities.

## References and provenance
- Herrero et al. 2013; FAOSTAT 2022; Chang et al. 2016; Carlson et al. 2016; Gerber et al. 2016; Dalin et al. (in prep); IPCC guidelines (De Klein et al. 2006).

## Relevance for monitoring frameworks
- Demonstrates end-to-end data pipeline from source data to policy-relevant outputs (maps and summaries).
- Emphasizes data provenance, multi-source integration, and reproducibility (parallel implementations, validation against FAOSTAT).
- Addresses data governance considerations such as data formats, metadata scope (scope, resolution, units, temporal range), and the potential need for data transformation for GIS use.
- Provides transparent documentation of processes, assumptions, and references, aiding replication and transparency in environmental monitoring, while highlighting data handling and sharing considerations that align with monitoring framework challenges.