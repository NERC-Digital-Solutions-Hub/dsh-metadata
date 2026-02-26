# Gridded data of greenhouse gas emissions from livestock and crops for year 2000

- Purpose and scope
  - Global gridded estimates of greenhouse gas (GHG) emissions for the year 2000 at 5 arc-minute resolution.
  - Includes GHG emissions and emission intensities per unit of mass for seven livestock commodities (bovine meat and milk, small ruminant meat and milk, pig meat, poultry meat and eggs) and 172 crops (crop list provided in cropnames).
  - Temporal scope: around year 2000 (period 1997–2003) with annual resolution.
  - Units: tonnes CO2 equivalents for emissions; tonnes CO2e per kilogram of animal product for emission intensities.
  - Spatial scope and format: global, gridded data in CSV format, compatible with MATLAB, Python, or R.

- Methodology (core approach)
  - Croplands: emissions sum of peatland drainage, rice cultivation, and manure/synthetic fertiliser application on cropland; two potential nitrous oxide (N2O) modelling approaches (linear and non-linear), with results shown for the linear model (IPCC factors: 0.31% for flooded rice, 1% for other crops).
  - Livestock: farm-level GHGs from enteric fermentation (methane) for ruminants; methane and nitrous oxide from manure management; nitrous oxide from manure left on pasture.
  - Feed-related emissions: N2O from synthetic fertilisers on cropland and grassland, and manure applied on cropland; account for diet composition, feed crop origins (FAOSTAT), and grassland productivity (ORCHIDEE).
  - Livestock feed and land-use data are integrated with crop emissions to yield total livestock farm-level and feed-related GHGs.
  - Data sources and inputs include: .xlsx (e.g., Herrero et al. 2013), .tif (e.g., Monfreda et al. 2008), .nc4 (e.g., Chang et al. 2016). 

- Data processing and outputs
  - Data handled in Matlab (and tested in parallel in R).
  - Final outputs saved as CSV via writematrix (Matlab R2023a).
  - Outputs include both total GHG emissions and emission intensities for each commodity type.
  - File naming convention: each file corresponds to the GHG emissions and emission intensities for all seven livestock commodities.

- Data formats and accessibility
  - Input formats: .xlsx, .tif, .nc4.
  - Output format: .csv; can be imported into MATLAB, Python, or R for analysis.
  - GIS readiness: provides a conversion script (convert_csv_to_raster.R) to transform CSVs into raster format suitable for GIS software.
  - Coordinate reference system: WGS 84 (Earth coordinates).
  - Spatial resolution: 5 arc-minute global grid.

- Quality control and validation
  - Independent parallel implementations by two co-authors (MATLAB and R) yield matching results.
  - National-scale averages compared with FAOSTAT values for validation.

- Data structure and components
  - Spatial scope: global; temporal scope: 1997–2003 (centered on 2000); temporal resolution: annual.
  - Units: tonnes CO2e for emissions; tonnes CO2e per kg of product for emission intensities.
  - Core data products: gridded emissions and gridded emission intensities for all seven livestock commodities and 172 crops.
  - Supporting elements: a cropnames file listing crops; documentation of methodology, data sources, and references.

- How this supports data use and re-use
  - Demonstrates end-to-end data integration from diverse sources, consistent unit handling, spatially explicit aggregation, and production of user-ready CSV and GIS-compatible formats.
  - Provides reproducible workflow cues (e.g., use of Matlab/R, data format conversions, and validation steps) to enable others to explore spatial emission patterns and compare against benchmarks.

- References (selected)
  - Herrero et al. 2013; FAOSTAT; Chang et al. 2016; Carlson et al. 2016/2017; De Klein et al. 2006; Gerber et al. 2016.