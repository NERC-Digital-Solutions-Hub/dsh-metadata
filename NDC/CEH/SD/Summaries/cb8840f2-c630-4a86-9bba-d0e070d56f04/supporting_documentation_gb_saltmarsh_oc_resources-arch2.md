# Supporting document for: GB_saltmarsh_OC_resources.zip

## Objective and scope
- Provides spatial mapping of surficial (top 10 cm) soil organic carbon (OC) storage and stocks across Great British saltmarshes.
- Covers 451.65 km² across 438 individual saltmarshes in Great Britain (Scotland, England, Wales).

## Data resource details
- Data Resource ID: Spatial mapping of surficial (top 10cm) soil OC storage and stocks across Great British saltmarshes.
- Description: Maps OC density (kg OC m^-2) and OC stocks (tonnes OC) for surficial soils across 438 GB saltmarshes; based on top 10 cm soil data; integrates saltmarsh vegetation maps and existing soil data.
- Data sources integrated:
  - OC content and dry bulk density data from NERC C-Side project (Ruranska et al., 2020, 2022) and Marine Scotland (Miller et al., 2022).
  - Saltmarsh vegetation maps: Environment Agency 2021; Haynes 2016; Natural Resources Wales 2016.

## Location and coverage
- Geographic scope: Great Britain (Scotland, England, Wales).
- Observations coordinates provided (latitude/longitude in decimal degrees; also X/Y in OS grid).

## Variables and observations
- Saltmarsh surficial soil OC stock (tonnes OC).
- Marsh area (km²).
- Organic Carbon Storage (kg OC m⁻²) for the top 10 cm of saltmarsh soil.
- Calculations are performed per saltmarsh vegetation class and marsh zone.

## Procedures and calculations
- OC storage per class/zone computed using OC content (%) and dry bulk density (kg m⁻³) from cited data sources.
- Depth for storage: 10 cm.
- Stock calculations aggregated across marshes using mapped areas and class-specific densities.

## Calibration and statistical treatment
- Stocks calculated within a Monte Carlo Markov Chain (MCMC) framework.
- 1,000,000 samples drawn from distributions (e.g., area, OC content, bulk density) out of 100,000,000 possible samples to populate stock estimates.

## Data quality and metadata
- Calibration procedures: Not applicable (NA).
- Quality control: Not reported (NA).
- File formats included: .cpg, .dbf, .prj, .sbn, .sbx, .shp, .shp, .shx.
- Spatial projection: OSGB 1936.
- Software: ESRI ArcGIS.

## Outputs and accessibility
- GIS-ready layers mapping OC storage across Great British saltmarsh soils to a depth of 10 cm.
- Outputs cover 451.65 km² and 438 marshes, with OC storage and densities suitable for integration with other environmental datasets.

## References and data provenance
- Key data sources and references include:
  - Environment Agency (2021) saltmarsh extent and zonation.
  - Haynes (2016) Scottish saltmarsh survey national report.
  - Natural Resources Wales (2016) saltmarsh extent.
  - Ruranska et al. (2020, 2022) surficial soil OC content and bulk density (English/Welsh and Scottish marshes).
  - Miller et al. (2022) Scottish saltmarsh soils data.

## Relevance for environmental monitoring
- Provides standardized, spatially explicit OC storage metrics suitable for temporal monitoring and policy evaluation.
- Facilitates integration with other environmental datasets and supports monitoring of carbon storage in intertidal environments.
- Data is structured for GIS analyses and potential submission to data portals consistent with environmental monitoring workflows.