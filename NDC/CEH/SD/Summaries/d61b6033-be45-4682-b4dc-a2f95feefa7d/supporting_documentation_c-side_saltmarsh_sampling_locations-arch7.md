# Global positioning system (GPS) locations and elevations of soil sampling sites across UK saltmarshes between 2018 - 2021

- Project context: Carbon Storage in Intertidal Environments (C-SIDE); funded by NERC (NE/R010846/1). Lead and contributing institutions include University of St Andrews, University of Glasgow, University of York, UK CEH, University of Leeds, Bangor University, among others.
- dataset purpose: GPS locations and elevations for saltmarsh soil sampling sites to support soil carbon stocks calculations and related analyses.

## Spatial scope and coordinate systems

- Geographic extent: United Kingdom saltmarshes (UK-wide sampling); notes indicate focus on Scotland for comparability, with sites also described by Nation as Scotland, England, Wales.
- Coordinate reference systems:
  - Lat/Lon: decimal degrees using WGS84
  - Spatial coordinates provided as X (Easting) and Y (Northing) (likely in a local/transverse projection) with elevations relative to Ordnance Datum Newlyn (AOD meters).
- Spatial granularity: 1323 sampling sites across UK saltmarshes (2018–2021).

## Dataset structure and key variables

- Identifiers: Marsh_ID (saltmarsh name), Site_ID (sample identifier)
- Location fields: Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_AOD_m
- Metadata: Nation (Scotland, England, Wales), Local_authority, Marsh_type (Natural, Historic Breach, Managed Realignment)
- Sampling and methods: Collection_year, Sampling_method (Syringe Sampler; Narrow (30mm) gouge core; Wide (60 mm) gouge core)
- Measurements and purpose: Core_length_cm, Purpose (e.g., Surficial OC stock calculations, Soil C Stocks and burial rates, Belowground biomass)
- Data format: CSV
- Data provenance notes: All GPS locations recorded using Juniper Systems, Leica, and Trimble DGPS; real-time corrections via Juniper RTK, Leica Infinity, and Trimble GNSS corrections; observations stored in raw form with no subsequent processing.

## Data quality and processing notes

- Processing status: No subsequent processing beyond initial data collection
- Quality checks: Not specified (NA for data checking procedures)
- Calibration data: Real-time GNSS corrections used during collection
- Potential considerations: Raw data may require cleaning/standardization prior to integration with other datasets; varying sampling methods and marsh types may affect comparability.

## Uses and GIS relevance

- Primary use: Spatial analysis of soil carbon stocks and burial rates in UK saltmarshes; supports map-based data visualization of sampling sites, elevations, and related attributes.
- GIS considerations:
  - Multiple coordinate representations (lat/lon and easting/northing) facilitate integration with different GIS workflows
  - Broad UK coverage with regional metadata (nation, local authority) supports stratified analyses and policy-relevant mapping
  - Data may require reprojection or harmonization and quality checks before advanced analyses due to raw/uncleaned status

## Access, provenance, and limitations

- Source project: C-SIDE, funded by NERC; contributors span several UK universities and research institutes
- Temporal coverage: 2018–2021
- Limitations to note:
  - Raw data with no explicit quality control documented
  - Absence of post-collection processing means users should implement their own QA/QC
  - Some fields contain NA or non-uniform data formats; cross-check variable definitions when merging with other datasets

## Relevance for GIS Specialists

- Provides a rich, georeferenced dataset for mapping saltmarsh sampling sites and analyzing spatial patterns of soil carbon metrics.
- Suitable as a base layer for GIS-based analyses, when properly cleaned and reconciled with consistent coordinate systems and QA procedures.