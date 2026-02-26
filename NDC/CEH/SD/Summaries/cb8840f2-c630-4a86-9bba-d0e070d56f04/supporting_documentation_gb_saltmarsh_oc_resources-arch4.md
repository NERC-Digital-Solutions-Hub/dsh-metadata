# Supporting document for: GB_saltmarsh_OC_resources.zip

- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Staff/Team: Craig Smeaton et al. (multidisciplinary team across St Andrews, CEH, Glasgow, York, Bangor)
- Data Resource: Spatial mapping of surficial (top 10 cm) soil OC storage and stocks across Great British saltmarshes

## Purpose and scope
- Provides a mapped dataset of organic carbon (OC) storage and stocks in surficial saltmarsh soils (top 10 cm) across Great Britain.
- Aims to quantify OC density (kg OC m^-2) and OC stocks (tonnes OC) for 438 marshes within 451.65 km² of saltmarsh habitat.
- Integrates sentinel data from national saltmarsh extents and zonation maps with soil property data to create bespoke GIS layers of OC storage.

## Data contents and structure
- Observations and variables
  - Saltmarsh surficial soil OC stock (tonnes OC)
  - Organic Carbon Storage (kg OC m^-2) for top 10 cm
  - Sample locations with Lat/Long and X/Y coordinates
  - Marsh area (km²)
  - OC content (% wt) and dry bulk density (kg m^-3) as drivers for calculations
- Spatial context
  - Coverage: Great Britain (Scotland, England, Wales)
  - Locations derived from saltmarsh maps and vegetation classifications (English, Scottish, Welsh datasets)
  - Spatial units linked to 438 marshes; 451.65 km² total area
- Data formats
  - GIS-friendly formats: .cpg, .dbf, .prj, .sbn, .sbx, .shp, .shp, .shx

## Methods and processing
- Calculations
  - OC storage and stock calculations performed per saltmarsh vegetation class and marsh zone
  - Utilized OC content and dry bulk density data to compute per-class/zone OC metrics
  - Combined with existing marsh mapping to produce a complete OC storage layer for GB saltmarsh soils down to 10 cm
- Statistical treatment
  - Monte Carlo Markov Chain (MCMC) framework used for stock calculations
  - 1,000,000 samples drawn from normal distributions of area, OC content, and bulk density to populate stocks
- Data provenance
  - Key inputs from NERC C-Side project (Ruranska et al., 2020, 2022) and Marine Scotland data (Miller et al., 2022)
  - Saltmarsh extent and zonation sources: Environment Agency (2021), Haynes (2016), Natural Resources Wales (2016)

## Software, projection, and accessibility
- Software: ESRI ArcGIS used for analysis and mapping
- Spatial projection: OSGB 1936
- Location descriptions
  - Observations provided as decimal degrees (WGS84) and as projected X/Y coordinates

## Data quality, governance, and metadata
- Data quality notes
  - Calibration and verification procedures outlined via MC-MCMC approach
  - Derived from established soil property datasets (OC content, bulk density) and validated saltmarsh maps
- Metadata and discoverability
  - Linked to external saltmarsh datasets and government/national datasets
  - Clear documentation of variables, units, and geographic scope to support reuse and integration with broader data ecosystems
- Provenance and reuse
  - Data designed to support carbon storage assessments in intertidal environments, with potential applications in policy, conservation planning, and carbon budgeting across networks of partners

## Spatial and temporal context
- Geography: Great Britain (Scotland, England, Wales)
- Temporal context: Integrates 2019–2022 data from cited sources; exact time points per marsh may vary by source datasets
- Geographic scope emphasizes continuity with national saltmarsh extents and zonation

## Implications for data leaders and data ecosystems
- Supports a holistic data system approach: integrates multiple data sources (soil properties, vegetation, marsh extents) into a single OC storage product
- User needs and co-ownership: dataset serves researchers, policymakers, and conservation practitioners; potential to collaborate across networks to maintain and update OC maps
- Data quality and standards: relies on standardized soil metrics and established regional bedrock datasets; documented processing promotes reproducibility and future updates
- Discoverability and access: GIS formats with explicit coordinate systems and metadata support broad discoverability within land/ocean carbon inventories
- Gaps and coordination: model highlights need for consistent data on OC content, bulk density, and marsh zonation across regions to maintain comparable products; potential for expanding to other depth intervals or broader tidal environments

## References and related materials
- Environment Agency (2021) Saltmarsh extent and zonation
- Haynes, T.A. (2016) Scottish saltmarsh survey national report
- Natural Resources Wales (2016) Saltmarsh extent
- Ruranska et al. (2020, 2022) C-Side soil carbon and bulk density datasets
- Miller et al. (2022) Scottish saltmarsh soils properties (Marine Scotland Data)