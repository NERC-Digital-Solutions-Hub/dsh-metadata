# Historic reconstructions of monthly groundwater levels for 54 boreholes in the UK (1981-2015)

## Project purpose and context
- Four-year, £1.5m project (2014–2018) under the Historic Droughts program to understand past UK droughts from hydrometeorological, environmental, regulatory, and socio-cultural perspectives.
- Aims to improve tools for managing droughts in the future by linking hydrometeorological and social systems.
- Produces an interdisciplinary knowledge base (Historic Droughts Inventory) of past drought characteristics, impacts, and responses.

## Dataset scope and content
- Reconstructed groundwater levels (GWL) for 54 observation boreholes in the UK, relative to Ordnance Datum (maOD).
- Time period: 1891–2015; monthly time steps.
- For each site: 90th and 10th percentile confidence bounds on the reconstructed GWL.
- Most boreholes located on Principal Aquifers (predominantly Chalk), with sites across southern and eastern England.

## Data sources integrated
- Groundwater level data from the National Groundwater Level Archive (NGLA).
- Precipitation data from UKCP09-based datasets; grid-cell resolution 5x5 km.
- Potential evapotranspiration (PET) estimated from temperature data via McGuinness-Bordne method.
- Drought modelling and reconstruction conducted with BGS AquiMod (Monte Carlo framework).

## Methodology and uncertainty estimation
- Groundwater levels reconstructed using AquiMod following established methods; calibration via Monte Carlo simulations (1,000,000 parameter sets).
- Parameter ranges based on published aquifer properties and expert judgment.
- Uncertainty quantified with Generalised Likelihood Uncertainty Estimation (GLUE); parameter sets deemed behavioural if Nash-Sutcliffe Efficiency > 0.5.
- For each date, 10th and 90th percentiles of GWL across behavioural simulations provided as confidence bounds (Cl10_GWL and Cl90_GWL).

## Dataset format and access
- Data delivered as individual CSV files per site with headers:
  - Date (YYYY-MM-DD, first day of month)
  - GWL (maOD)
  - Cl90_GWL (90th percentile)
  - Cl10_GWL (10th percentile)
- File naming convention examples: HistoricDroughts_BGSAquiMod_Output_Feb2018_GWL_Rockleyver1, etc.
- An additional metadata file: Metadata_forGWLandSGI_reconstructions.csv listing sites and basic site metadata:
  - Site_name, Easting, Northing, BGS_WellMaster_ID, Full_BGS-site_name, Aquifer, MORECS_ID, etc.
- Spatial and site metadata designed to facilitate GIS integration and cross-referencing with SGI inventories.

## Data sources and formats in the metadata
- Metadata fields include: Site_name, Easting, Northing, BGS_WellMaster_ID, Full_BGS_site_name, Aquifer (nine principal aquifers), and MORECS_ID (location code).

## Usage and GIS relevance
- Enables map-based visualization and spatial analysis of groundwater drought signals across multiple boreholes.
- Part of the Historic Droughts Inventory, supporting cross-sector analyses and long-term drought planning.
- Data can be integrated with GIS workflows to examine spatial patterns of groundwater response and to compare with hydrometeorological indicators and regulatory/drivers.

## Practical considerations for GIS specialists
- Data are monthly and may require handling irregularities in underlying records (interpolation from irregular NGLA data to monthly).
- Uncertainty bounds (10% and 90%) are available per date, enabling risk-aware visualization.
- Coordinates provided in metadata (Easting/Northing) support precise mapping on British National Grid.
- Dataset covers late 19th to mid-20th century drought context, useful for historical comparisons and planning scenarios.

## Acknowledgements and references
- Funded by the Natural Environment Research Council (NERC) under the Historic Droughts project (NE/L010151/1).
- Key methodological references include AquiMod modelling work and GLUE uncertainty framework; foundational aquifer property sources and UKCP09 datasets cited in the project documentation.