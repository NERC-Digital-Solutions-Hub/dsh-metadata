# Flood risk assessment of the Luanhe river basin under different development strategies and climate scenarios

## Overview
- A flood risk assessment framework applied to the Luanhe river basin in northeast North China Plain, examining future climate scenarios up to 2030 and various development strategies.
- Uses open data and author-produced data to generate flood risk maps by overlaying inundation with population density (GPWv4).
- Aims to support understanding of potential flood risk under different growth and climate pathways for informing decision-making and governance.

## Data collection and generation methods
- Future climate uplifts to 2030 derived from NASA Earth Exchange Global Daily Downscaled Projections (NEX-GDDP) and applied to 100-year design rainfall.
- Validation of the flood model using a historical 2012 flood event.
- Flood inundation predictions to 2030 produced with the HiPIMS hydrodynamic model across multiple development strategies and climate scenarios.
- Spatial resident density (GPWv4) overlay used to evaluate local flood risk.
- Data are mostly open data or produced by the authors; all data support near-term flood risk assessment (2030).

## Data content and units
- Uplifts of future climate scenarios to 2030: dimensionless numbers describing climate impact on the future 100-year design rainfall.
- 2012 flood validation: remote sensing data (unit not specified, marked as -) and inundation results in meters (m).
- Flood inundation prediction to 2030: model results from HiPIMS; inundation results in meters (m).
- Population density: residents per square kilometer (persons/km^2) used to evaluate risk to local residents.

## Data structure and formats
- Data are provided in:
  - CSV format for climate uplifts.
  - TIFF (GeoTIFF) files for other data (inundation, validation, etc.).
- Descriptions refer to two tabs (Tab 1 and Tab 2) detailing dataset structure and contents.

## Datasets and licensing
- Flood model validation
  - Description: validation data and remote sensing validation for the 2012 flood event.
  - Format: validation.tif and RemoteSensing_validation.tif.
  - Contributing authors: Loughborough University.
  - Licensing: Open Government Licence.
- Climate change uplifts
  - Description: city-wide uplifts (rcp45.csv, rcp85.csv) derived from NEX-GDDP; columns: city, uplift value.
  - Contributing authors: Loughborough University.
  - Licensing: Open Government Licence.
- Inundation map (flood scenarios)
  - Description: flood simulation results for different climate and infrastructure scenarios.
  - Contributing authors: Loughborough University.
  - Licensing: Open Government Licence.
- Population data
  - Description: GPWv4-derived population data; resampled.
  - Contributing authors: Loughborough University.
  - Licensing: Open Government Licence.

## Data scenarios and developments
- Datasets cover a range of development strategies and climate pathways, including:
  - Baseline land use with 100-year design rainfall (2015).
  - Trend (2030) scenarios under RCP4.5 and RCP8.5.
  - Expansion (2030) scenarios under RCP4.5 and RCP8.5, with downstream P (Panjiakou Reservoir including Daheiting) and S (Shuangfengsi Reservoir) designations.
  - Sustainability and Conservation variants for 2030 under RCP4.5 and RCP8.5, with regional breakdowns (P, P_S, S_S, etc.).
- These scenarios enable comparative assessment of flood risk under combined land-use, infrastructure, and climate changes up to 2030.

## Quality control and provenance
- HiPIMS model has prior validated use in flood risk assessments (references to 2019 works by Xia et al., Xing et al.).
- Datasets are well-documented and have been submitted to peer-reviewed venues (e.g., Zhao et al., 2021) with robust estimates.
- NEX-GDDP and GPWv4 are established, widely used open datasets, supporting reproducibility.
- Clear references provided for data sources and methodologies.

## Governance, reuse, and maintenance considerations for Data Stewards
- Metadata and documentation: ensure comprehensive documentation of data formats, units, projections, temporal coverage, and processing steps (HiPIMS workflow, validation steps).
- Provenance: track data origins (NEX-GDDP, GPWv4, remote sensing sources) and transformation steps to enable traceability.
- Interoperability: maintain consistent coordinate reference system, resolution, and naming conventions across datasets to support integration with other systems.
- Access and licensing: Open Government Licence facilitates sharing and reuse; monitor for any scope changes or embargoes in future updates.
- Update strategy: define when and how climate uplifts, population data, and inundation predictions should be refreshed as new scenarios or datasets become available.
- Data quality assurance: continue validating model outputs with historical events and remote sensing as new validation cases arise.
- Data governance: document roles, responsibilities, and workflows for dataset maintenance, updates, and user support.

## Key challenges relevant to Data Stewards
- Incomplete view of user needs and priorities across stakeholder groups.
- Timely acquisition of data from varied sources and formats.
- Achieving consistent metadata and standardization across diverse data types and formats.
- Handling large datasets and non-interoperable legacy data or bespoke formats.
- Aligning updates with evolving climate scenarios, land-use changes, and infrastructure developments.

## Summary of relevance for Data Stewards
- This dataset suite exemplifies end-to-end data lifecycle management for flood risk assessment, including data collection from climate projections, historical validation, model-produced inundation maps, and population exposure assessment.
- Emphasizes the importance of open data licensing, thorough documentation, and reproducible data structures to support discovery, reuse, and governance in large-scale environmental datasets.