# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Project title: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Staff Responsible: Craig Smeaton
- Research team: Multidisciplinary collaboration among the University of St Andrews, University of Glasgow, University of York, University of Leeds, Bangor University, and UK CEH, with researchers across multiple institutions

## Data Resource Summary
- Data Resource ID: GPS locations and elevations of soil sampling sites across UK saltmarshes (2018–2021)
- Dataset description: GPS locations and elevations recorded for 1,323 sampling sites across UK saltmarshes; raw observations with minimal processing
- Geographic extent and locations: UK (focus on Scotland for representative saltmarsh variation; coordinates provided as decimal degrees and also as X_Easting/Y_Northing in data)
- Location details: Sites selected across Scotland to reflect saltmarsh diversity in sediment types and organic carbon content
- Variables and structure: Includes Marsh_ID (saltmarsh name), Site_ID, Nation (Scotland, England, Wales), Local_authority, Marsh_type (Natural, Historic Breach, Managed Realignment), Collection_year, Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_AOD_m, Sampling_method, Core_length_cm, Purpose
- Observations and methods: GPS locations collected with Juniper Systems, Leica, and Trimble DGPS; data recorded in WGS84 decimal degrees and corresponding easting/northing; Elevation above Ordnance Datum (m); Real-time corrections used where applicable (RTK, Trimble GNSS service)
- Data format and quality indicators: File format is .csv; no subsequent processing noted; Data checking procedures not specified; NA entries indicate missing or not applicable data
- Purpose of data: Surficial organic carbon stock calculations, soil carbon stocks, burial rates, and belowground biomass (roots)

## Data Content and Variables
- Spatial identifiers: Marsh_ID (saltmarsh name), Site_ID (sample identifier)
- Administrative and classification fields: Nation (Scotland, England, Wales), Local_authority, Marsh_type (Natural, Historic Breach, Managed Realignment)
- Temporal coverage: Collection_year (2018–2021)
- Geospatial measurements: Lat_dec_deg, Long_dec_deg (WGS84 decimal degrees); X_easting, Y_northing (map projections); Elevation_AOD_m (Elevation Above Ordnance Datum)
- Sampling details: Sampling_method (Syringe Sampler; Narrow 30 mm gouge; Wide 60 mm gouge); Core_length_cm
- Data context: Purpose (Surficial OC stock calculations; Soil C stocks and burial rates; Belowground biomass)

## Methods and Processing
- GPS and datum: WGS84; Elevation relative to Ordnance Datum Newlyn
- Quality and processing: Data described as not processed beyond initial collection; calibration/real-time correction methods referenced (RTK corrections, Trimble GNSS service)
- Metadata and provenance: Metadata fields present (names, locations, methods, units); some fields marked NA where not applicable

## Geographic and Temporal Coverage
- Geographic: United Kingdom saltmarshes with a focus on Scotland for representative conditions; includes sites across Scotland, England, and Wales
- Temporal: Data collected between 2018 and 2021

## Data Format, Access, and Governance Considerations
- Format: CSV
- Data sharing and governance: Public sharing of underlying data is a consideration; alignment with data governance and openness standards is implied; dataset is raw with limited processing noted
- Metadata and interoperability: Some metadata completeness issues may arise (as per typical monitoring framework challenges); transformation to standard schemas may be required for integration with broader monitoring dashboards

## Relevance for Monitoring Frameworks
- Use cases: Provides spatially explicit estimates of saltmarsh carbon stocks and burial rates; supports policy evaluation of coastal carbon storage and land management practices (e.g., natural marsh preservation vs. managed realignment)
- Strengths: Rich geospatial and descriptive metadata; links carbon stock calculations to specific marsh types and management contexts
- Challenges for frameworks: Data gaps and metadata completeness; access and governance considerations; potential need for data standardization, ongoing updates, and transparency about processing steps

## Key Takeaways for Policy and Decision Makers
- The C-SIDE dataset offers location-specific information essential for assessing saltmarsh carbon storage under different management scenarios.
- When used in monitoring frameworks, account for data provenance, potential gaps, and governance requirements to ensure transparency, reproducibility, and timely updates.