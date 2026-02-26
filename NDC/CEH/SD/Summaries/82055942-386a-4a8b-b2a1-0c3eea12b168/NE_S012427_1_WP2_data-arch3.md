# Flood risk assessment of the Luanhe river basin under different development strategies and climate scenarios

## Study scope and significance
- Assesses flood risk in the Luanhe river basin (northeast North China Plain) under varying development strategies and climate scenarios.
- Aims to inform socio-economic planning and regional risk management for the Beijing–Tianjin–Hebei area.
- Integrates climate projections, historical event validation, land-use data, and population exposure to produce flood risk assessments by 2030.

## Data and methods used
- Climate uplifts to 2030 derived from NASA Earth Exchange Global Daily Downscaled Projections (NEX-GDDP) to represent future 100-year design rainfall.
- Validation of flood model using a historical 2012 flood event with remote sensing data.
- Flood inundation predictions to 2030 using the HiPIMS hydrodynamic model under different development strategies and climate scenarios.
- Overlay of inundation results with population data to generate local resident flood risk maps.

## Data sources, formats, and structure
- Primary data are open data or author-generated; widely used open datasets are employed for baseline inputs.
- Data formats:
  - Climate uplifts: CSV (one column for city, one for uplift value).
  - Other data: TIFF files.
- Data structure details are described in accompanying Tabs 1 and 2.
- Key datasets include:
  - Flood model validation: validation.tif and RemoteSensing_validation.tif (historical 2012 event).
  - Climate change uplifts: rcp45.csv and rcp85.csv (City-wide uplifts from NEX-GDDP).
  - Inundation maps: flood simulation results for various strategies and climate scenarios.
  - Population data: resampled GPWv4 population data.
- Licensing: Open Government Licence for the datasets.

## Quality control and validation
- HiPIMS model previously applied successfully in multiple flood risk projects.
- The flood risk dataset is well documented and has been submitted to peer-reviewed journals, with robust estimates demonstrated.
- Donor datasets (NEX-GDDP and GPWv4) are widely used open data sources.

## Scenarios and data details
- Land use and design rainfall scenarios for 2015 baseline and 2030 projections, with multiple climate pathways:
  - 2030 scenarios include Baseline, Trend, Expansion, Sustainability, and Conservation.
  - Each scenario evaluated under RCP4.5 and RCP8.5 pathways.
- Reservoirs considered in scenarios:
  - P represents Panjiakou Reservoir (including Daheiting).
  - S denotes Shuangfengsi Reservoir.
- Outputs include inundation maps and associated metrics (in meters) under different combinations of land use, design rainfall, and climate scenarios.

## Outputs and policy relevance
- Generates flood risk maps for the Luanhe basin toward 2030 by overlaying inundation results with GPWv4 population data.
- Enables assessment of population exposure under multiple development and climate pathways to inform policy decisions, infrastructure planning, and risk mitigation strategies.
- Demonstrates a reproducible workflow with open datasets and clear data governance, supporting ongoing monitoring and updates.

## Data availability and governance implications for monitoring frameworks
- Emphasizes data openness and accessibility, with licensing enabling reuse.
- Highlights reliance on metadata quality, standard formats (CSV, TIFF), and transparent data provenance.
- Addresses potential barriers noted in monitoring work (data access, metadata completeness, interoperability, and governance) by using established open datasets and well-documented workflows.
- Provides a model for integrating climate projections, historical validation, and population exposure into actionable risk assessments for decision-makers.