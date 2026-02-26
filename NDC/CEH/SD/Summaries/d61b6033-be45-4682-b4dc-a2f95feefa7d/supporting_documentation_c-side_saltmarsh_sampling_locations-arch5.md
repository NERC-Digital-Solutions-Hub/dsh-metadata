# Carbon Storage in Intertidal Environments (C-SIDE)

- A NERC-funded project with staff responsible for data collection and management (Craig Smeaton and a multi-institution research team across St Andrews, Glasgow, York, Leeds, Bangor, and UK CEH).
- Dataset summarizes GPS locations and elevations of soil sampling sites across UK saltmarshes collected between 2018 and 2021.

## Dataset scope and content

- Contains global positioning system (GPS) locations and elevations for 1,323 sampling sites across UK saltmarshes.
- Key identifiers and descriptors:
  - Marsh_ID (saltmarsh name), Site_ID (sample identifier), Nation (Scotland, England, Wales), Local_authority, Marsh_type (Natural, Historic Breach, Managed Realignment), Collection_year.
- Spatial data representations:
  - Latitude and Longitude in decimal degrees (WGS84).
  - X_easting and Y_northing coordinates (grid reference).
  - Elevation_AOD_m (Elevation Above Ordnance Datum).
- Observed/recorded variables:
  - Latitude, Longitude, Easting, Northing, Elevation, Sampling_method, Core_length_cm, Purpose.
  - Common sampling methods include syringe sampler, narrow (30 mm) gouge corer, wide (60 mm) gouge corer.
  - Purposes include Surficial OC stock calculations, Soil C stocks and burial rates, Belowground biomass (roots).
- Data record details:
  - Spatial extent described by UK coordinates: roughly between 60.97°N, -8.02°W and 49.84°N, 2.18°W.
  - Data stored as .csv files.
- Observational specifics:
  - Data were collected using Juniper Systems, Leica, and Trimble DGPS; recorded in WGS84 (decimal degrees) with OD Newlyn-based elevations.
  - Real-time calibration corrections used (Juniper RTK, Leica Infinity RT, Trimble GNSS corrections).

## Geographic and temporal coverage

- Location: United Kingdom saltmarshes (Scotland, England, Wales).
- Timeframe: 2018–2021 for sampling; no further processing noted post-collection.

## Data collection, formats, and provenance

- Provenance:
  - Research team includes members from University of St Andrews, University of Glasgow, University of York, University of Leeds, Bangor University, and UK CEH.
- Data collection specifics:
  - GPS data gathered with multiple GNSS platforms; data recorded in decimal degrees (WGS84) with projection to Easting/Northing; elevation relative to Ordnance Datum Newlyn.
  - Calibration procedures employed in real time (RTK and GNSS correction services).
- Data processing:
  - No subsequent processing has been undertaken beyond initial collection and formatting.
- Format:
  - Primary data format is CSV (.csv).

## Metadata and data schema

- Key fields and their formats:
  - Marsh_ID (Text), Site_ID (Text), Nation (Text: Scotland, England, Wales), Local_authority (Text), Marsh_type (Text: Natural, Historic Breach, Managed Realignment), Collection_year (Number).
  - Lat_dec_deg, Long_dec_deg (Number; decimal degrees, WGS84).
  - X_easting, Y_northing (Number).
  - Elevation_AOD_m (Number).
  - Sampling_method (Text: Syringe Sampler, Narrow gouge, Wide gouge).
  - Core_length_cm (Number).
  - Purpose (Text: Surficial OC stock calculations, Soil C stocks and burial rates, Belowground biomass).
- Observations and data descriptions clearly link coordinates, altitude, and sampling details to saltmarsh sites across the UK.

## Use cases and governance considerations for Data Stewards

- Potential applications:
  - Surficial organic carbon stock estimations and burial rate analyses for UK saltmarshes.
  - Spatial analyses requiring consistent coordinate references (WGS84) and elevation data.
- Data governance and sharing:
  - Metadata indicates raw data with limited processing; standardization of coordinate representations (lat/long vs. easting/northing) is important for interoperability.
  - Calibration and instrument details are essential provenance information; ensure these are captured in metadata for future reuse.
- Data quality and limitations:
  - No data quality checks documented (Data checking procedures indicated as NA); post-collection processing not performed.
  - Multiple GNSS platforms and real-time corrections introduce potential inter-system variability; document harmonization steps if integrating with other datasets.
- Documentation and maintenance:
  - Dataset includes detailed field descriptions and method notes; consider formalizing a metadata schema (data types, units, and valid ranges) and versioning.
  - Opportunity to upload and catalog the dataset in shared portals; maintain records of dataset updates and any future reprocessing.

## Practical actions for Data Stewards

- Ensure metadata completeness and consistency, especially for coordinate systems (WGS84) and elevation reference (OD Newlyn).
- Capture and document calibration procedures and GNSS correction methods to support reproducibility and interoperability.
- Plan for data updates or reprocessing, and maintain clear versioning and change logs.
- Facilitate data sharing by preparing standard data access records and mapping variables to common domain standards (e.g., location, elevation, sampling method, and purpose).
- Highlight limitations (e.g., lack of QC procedures) and intended uses to guide appropriate reuse.