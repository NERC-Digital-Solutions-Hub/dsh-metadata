# Supporting documentation for data resource Aboveground_Biomass_Carbon_UK.csv

- Purpose of the dataset: Physical and biogeochemical measurements of aboveground vegetation biomass and organic carbon content from UK saltmarshes ( ten sites, 2019–2020 ), intended to quantify blue-carbon stocks in the United Kingdom.
- Sample and site coverage: 144 vegetation surveys across ten UK saltmarshes; sites chosen to represent coastal saltmarsh vegetation, sediment types, and carbon content in Scotland and other regions.
- Location and spatial detail: Site locations provided as decimal degrees (WGS84) and also as X (Easting) and Y (Northing). Includes marsh name, nation, and precise geographic coordinates.

## Data resource content

- Observations and measurements:
  - Biomass metrics: Biomass (g) and Aboveground_biomass_g_m_2 (g m^-2)
  - Organic carbon: OC_Perc (%) and Aboveground_carbon_g_C_m_2 (g C m^-2)
  - Harvesting details: Harvested_Area_m_2 (area of vegetation harvested per quadrat)
- Site and habitat metadata:
  - Marsh_ID, Nation, Marsh_Zone (e.g., High/Low/Pioneer marsh), NVC (British National Vegetation Classification)
  - Elevation_above_OD_m (elevation above ordnance datum)
- Collection and sampling specifics:
  - Collection_Date (date of sample collection)
  - Latitude_dec_degree, Longitude_dec_degree (decimal degrees, WGS84)
  - X_easting, Y_northing (alternative coordinate system)
- Data quality and formatting:
  - File format: .csv
  - Headers describe each column (Description; Cell Format)
  - NA indicates no data in cells
  - Data checks: Laboratory equipment calibrated according to University of St Andrews practices

## Methods and procedures

- Field sampling:
  - 1 m^2 quadrats placed at each site; within each quadrat, 0.125 m^2 area harvested
  - Vegetation described following the British National Vegetation Classification (NVC) scheme
  - DGPS used to record precise location and elevation
- Sample processing:
  - Harvested vegetation oven-dried at 60°C for 72 hours; dry biomass mass (g) calculated from biomass per harvested area
  - Sub-samples milled; 50 mg analyzed with Soli TOC for total organic carbon using a DIN 19539 thermal method
  - Aboveground carbon calculated from OC content and biomass data
- Calibration and quality control:
  - Soli TOC calibration with CaCO3 and standard TOC/ROC/TIC materials
  - Equipment calibration performed in accordance with lab practices
- References informing methods:
  - DIN 19539 (TOC analysis)
  - Harvey et al. 2019; Natali et al. 2020; Rodwell 2000; Smeaton et al. 2021

## Data structure and variables (data dictionary)

- Marsh_ID: Saltmarsh name (Text)
- Nation: Nation of site (Text)
- Collection_Date: Date of sample collection (Date/Number)
- Latitude_dec_degree: Latitude in decimal degrees (Number)
- Longitude_dec_degree: Longitude in decimal degrees (Number)
- X_easting: X (Easting) coordinate (Number)
- Y_northing: Y (Northing) coordinate (Number)
- Elevation_above_OD_m: Elevation above ordnance datum (m) (Number)
- NVC: National Vegetation Classification (Text)
- Marsh_Zone: Saltmarsh zone classification (High/Low/Pioneer) (Text)
- Harvested_Area_m_2: Harvested vegetation area per sample (m^2) (Number)
- Biomass_g: Dry biomass harvested (g) (Number)
- Aboveground_biomass_g_m_2: Aboveground biomass per unit area (g m^-2) (Number)
- OC_Perc: Organic carbon content (% of biomass) (Number)
- Aboveground_carbon_g_C_m_2: Aboveground carbon (g C m^-2) (Number)

## Data governance, accessibility, and reuse

- Data format and discoverability: Provided as a CSV with descriptive headers; explicit column definitions included to aid interoperability.
- Metadata clarity: Includes descriptive field names and units; notes about data checks and calibration aid understanding and reuse.
- Versioning and provenance: References list supports methodological transparency and traceability of analytical approaches.

## Practical implications for data leadership

- Observational richness: A robust, field-validated dataset combining biomass and carbon metrics across multiple sites, suitable for tracking blue-carbon stocks and temporal/spatial comparisons.
- interoperability: Standardized coordinates (WGS84) and explicit units support integration with other datasets and GIS workflows.
- data quality and standards: Clear QA steps and calibration references help establish confidence in data quality and enable reproducibility.
- potential gaps and considerations:
  - Data gaps may exist where data fields are NA; plan for gap handling in analyses.
  - Access barriers (noted as paywalls/barriers in some contexts) are not explicit here but should be considered when seeking supplementary data or metadata.
  - Ongoing data stewardship should maintain metadata alignment with evolving standards (e.g., NVC classifications) and ensure discoverability across data networks.