# Supporting documentation for data resource Aboveground_Biomass_Carbon_UK.csv

## Overview
- Dataset of physical and biogeochemical measurements of aboveground vegetation biomass and organic carbon content from ten UK saltmarshes, 2019–2020.
- 144 vegetation surveys conducted across UK saltmarsh sites to quantify aboveground biomass and OC content (blue carbon environments).

## Data content and structure
- Location and sampling
  - Sites chosen across the UK coastline to represent saltmarsh vegetation, sediment types, and OC content (including Scotland).
  - Locations provided as decimal degrees (WGS84) and as X (Easting) / Y (Northing) coordinates.
  - Harvested area per sample: 0.125 m2 within 1 m2 quadrats; sampling described using British National Vegetation Classification (NVC) scheme.
- Key variables (examples)
  - Marsh_ID, Nation, Collection_Date
  - Latitude_dec_degree, Longitude_dec_degree, X_easting, Y_northing
  - Elevation_above_OD_m, NVC, Marsh_Zone
  - Harvested_Area_m_2, Biomass_g, Aboveground_biomass_g_m_2
  - OC_Perc (organic carbon content %), Aboveground_carbon_g_C_m_2
- Data resource descriptions and header details
  - Data resource description and headers specify field descriptions and formats (Description vs. Cell Format).
  - Columns include textual (e.g., Marsh_ID, Nation, NVC) and numeric fields (e.g., Biomass_g, OC_Perc).

## Methods and procedures
- Field sampling
  - 144 vegetation surveys; 1 m2 quadrats; in each, 0.125 m2 sub-area harvested for biomass.
  - Live vegetation cut at soil level; dead litter collected from soil surface.
  - DGPS used for precise site location and elevation above datum.
- Laboratory processing
  - Harvested biomass oven-dried (60°C for 72 h), weighed to compute dry biomass (g) and then aboveground biomass (g/m2).
  - Sub-samples milled; 50 mg analyzed with Soli TOC (DIN 19539 gradient method) to quantify OC.
  - Aboveground carbon calculated from OC% and biomass data.
- Calibration and QA
  - TOC instrument calibrated with CaCO3 and standard materials (B2290).
  - Laboratory equipment calibrated per institutional QA practices at University of St Andrews.
- Documentation and standards
  - Observational procedures aligned with established field and lab protocols; references include Rodwell (NVC), Harvey et al. (2029), Natali et al. (2020), Smeaton et al. (2021).

## Data management and metadata
- Data formats
  - Primary format: .csv
  - Data resource includes structured metadata with header descriptions and cell formats.
- Provenance and references
  - Data resource entries include description blocks and references to the methods and standards used (e.g., DIN 19539; Rodwell 2000; related Frontiers and Thermochimica Acta papers).

## Data quality and limitations
- Quality control
  - Laboratory equipment calibrated according to specified QA practices.
- Data gaps and notes
  - Some fields are indicated as NA when not applicable (e.g., statistical treatments).
  - The dataset represents a specific temporal window (2019–2020) and a defined set of saltmarsh sites; extrapolation beyond these sites/times should be treated with caution.

## Use and reuse considerations for Data Stewards
- Discoverability and usability
  - Comprehensive metadata including precise geolocations, sampling dates, and a detailed data dictionary facilitates discovery and reuse.
  - Clear linkage between field methods, lab analyses, and resulting biomass/OC calculations enhances reproducibility.
- Interoperability and standards
  - Use of WGS84 coordinates and explicit field definitions supports integration with other blue-carbon datasets.
- Data governance
  - Maintain versioned metadata and data dictionaries; preserve calibration and QA notes; document any data updates or site additions.
  - Ensure data resource descriptions remain aligned with dataset contents and provide clear provenance for users.
- Potential governance actions
  - Consider aligning with broader data standards (e.g., Darwin Core or domain-specific carbon datasets) for enhanced interoperability.
  - Track and communicate any data limitations or embargoes affecting sharing or updates.
- References and transparency
  - Include full references for methods and standards to support auditability and methodological transparency.