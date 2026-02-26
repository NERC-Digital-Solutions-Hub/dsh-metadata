# Global positioning system (GPS) locations and elevations of soil sampling sites across UK saltmarshes between 2018 - 2021

- Project context and funding
  - Part of Carbon Storage in Intertidal Environments (C-SIDE)
  - Funded by NERC (NE/R010846/1)
  - Staff Responsible: Craig Smeaton
  - Research team includes researchers from University of St Andrews, University of Glasgow, University of York, University of Leeds, Bangor University, and UK Centre for Ecology & Hydrology (UK CEH)

- Data resource overview
  - GPS locations and elevations for 1323 soil sampling sites across UK saltmarshes (2018–2021)
  - Location extent covers UK saltmarshes with coordinates provided in both geographic (WGS84 decimal degrees) and projected (Eastings/Northings) systems
  - Data file format: .csv
  - No post-collection processing indicated in the dataset

- Spatial and temporal coverage
  - Geographic extent: UK-wide saltmarsh regions ( extents provided as latitude/longitude bounds and corresponding OS grid coordinates )
  - Temporal scope: Sampling collected across years (Collection_year field)

- Dataset structure and key variables
  - Spatial coordinates and elevation
    - Lat_dec_deg, Long_dec_deg (decimal degrees, WGS84)
    - X_easting, Y_northing (projected coordinates)
    - Elevation_AOD_m (Elevation Above Ordnance Datum in meters)
  - Site and locality identifiers
    - Marsh_ID (saltmarsh name)
    - Site_ID (sample identifier)
    - Nation (England, Scotland, Wales)
    - Local_authority (responsible authority)
  - Marsh characteristics
    - Marsh_type (Natural, Historic Breach, Managed Realignment)
  - Sampling details
    - Sampling_method (Syringe Sampler; Narrow gouge core; Wide gouge core)
    - Core_length_cm (length of core retrieved)
  - Purpose and metadata
    - Purpose (Surficial OC stock calculations; Soil C stocks and burial rates; Belowground biomass)
    - Collection_year (year of sample collection)
  - Additional notes
    - Elevation referenced to Ordnance Datum Newlyn (AOD)
    - All site locations described as representative of similar environmental regions (notably Scotland) to facilitate comparability

- Data collection and quality aspects
  - GPS equipment and corrections
    - Instruments used: Juniper Systems, Leica, Trimble DGPS
    - Real-time corrections: Lecia Infinity RTK and Trimble GNSS correction service
  - Data processing and quality checks
    - No subsequent processing reported for the dataset
    - Data checking procedures listed as NA (not provided)

- Practical considerations for analysts
  - Data intended for surficial organic carbon stock calculations, soil carbon stocks and burial rates, and belowground biomass analyses
  - Cross-site comparability may require standardisation due to variation in marsh_type and regional representation
  - Some metadata fields have limited quality-control information (NA), so consider complementary QC when integrating with other datasets

- Notes on location descriptors
  - While Nation field includes Scotland, England, and Wales, the Location Descriptions emphasize Scotland as a reference region for comparable data, with sites chosen to represent saltmarsh conditions across Scotland.