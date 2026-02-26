# Gridded data of greenhouse gas emissions from livestock and crops for year 2000

- Global gridded dataset of GHG emissions (CO2e) and emission intensities for crops and livestock around year 2000
- Spatial resolution: 5 arcminutes; global extent; coordinate system: WGS 84
- Temporal scope: annual data around year 2000 (1997–2003)
- Livestock commodities covered: bovine meat and milk, small ruminant meat and milk, pig meat, poultry meat and eggs (seven categories)
- Crop list available in the cropnames file
- Data formats and outputs: inputs in .xlsx, .tif, .nc4; final outputs saved as .csv (Matlab R2023a) and convertible to raster for GIS

## Data provenance, methodology and modeling

- Methodology developed in a forthcoming publication by Dalin et al. (in prep.)
- Emissions estimation approach:
  - Crops: sum of peatland drainage, rice cultivation, and manure/synthetic fertiliser application on cropland
  - Livestock: farm-level GHG emissions plus feed-related GHG emissions
  - Feed-related emissions account for diet composition, origin of feed crops, and grassland productivity
- Emissions factors and models:
  - Uses IPCC linear method for N2O from cropland and manure/synthetic fertiliser (0.31% for flooded rice, 1% for other crops)
  - Two versions considered for N2O (linear and non-linear), with results presented for the linear model
- Data sources referenced for inputs:
  - Herrero et al. 2013 (animal production and emissions)
  - FAOSTAT (feed crop origins)
  - ORCHIDEE (grassland productivity)
  - Carlson et al. 2016/2017 and Gerber et al. 2016 (relating to N2O and cropland emissions)
- Output includes both total GHG emissions (tonnes CO2e) and emission intensities (tonnes CO2e per kg of product)

## Data structure, formats and documentation

- Outputs for each dataset: CSV files that can be imported into MATLAB, Python, or R
- Optional GIS workflow: convert CSV to raster using provided R script convert_csv_to_raster.R; then import into GIS software
- File naming convention: each file refers to emissions and emission intensities for all seven livestock commodities
- Data quality and verification:
  - Independent parallel coding and computations in MATLAB and R with matching results
  - National-scale averages compared to FAOSTAT values for validation

## Quality control and governance

- Quality assurance includes cross-validation between independent implementations and alignment with FAOSTAT national benchmarks
- Clear documentation of data structure, units, and spatial/temporal resolution to support reproducibility
- Metadata should capture:
  - data sources and versions
  - calculation procedures and model choices (linear vs non-linear)
  - spatial and temporal extents, coordinate system, and units
  - file formats, processing steps, and script references (e.g., convert_csv_to_raster.R)

## Accessibility, reuse and stewardship considerations

- Dataset designed for easy reuse in statistical analyses and GIS workflows
- Supporting materials available that describe:
  - input data formats and processing pipeline
  - methods to convert CSVs to raster formats and to map results
  - crop and livestock commodity coverage and naming conventions
- Stewardship notes:
  - Maintain traceability to original data sources and methodological choices
  - Versioning and clear provenance for updates or future iterations
  - Consider licensing and data-sharing terms to enable broad discovery and use

## References (key sources)

- Herrero, M. et al. 2013; FAOSTAT 2022; Chang, J. et al. 2016; Carlson, K.M. et al. 2016/2017; Gerber, J.S. et al. 2016
- IPCC guidelines and related modelling frameworks referenced for emission factors and methodology