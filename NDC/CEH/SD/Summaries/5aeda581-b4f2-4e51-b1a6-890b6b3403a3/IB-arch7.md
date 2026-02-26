# IB Protocol

## Overview
- Purpose: Monitor butterfly abundance using transect methods from the Butterfly Monitoring Scheme (BMS).
- Rationale: Butterflies are easy to identify and respond quickly to vegetation changes; ECN aims to align with 15 years of national monitoring data for trend and phenology comparisons, including climate relationships.
- Output focus: Map-based and dataset-ready records to support spatial analyses and comparisons across sites and years.

## Spatial Design and Sampling Framework
- Fixed transect routes are established at each ECN site and followed on every sampling occasion.
- Transects aim to be representative of the ECN site and typically follow existing paths or boundaries, including areas under different management regimes.
- Transect length: site conditions allow 1–2 km, walkable in 30–90 minutes.
- Transect structure: divided into up to 15 sections, each with distinct vegetation/structure/management; sections act as sampling strata.
- Spatial data captured: route length per section, habitat types, abundant plants (especially butterfly food plants), and nearby management operations.
- Reproducibility: if needed, routes are marked to ensure the same path is used each time.
- Recording window: weekly from 1 April to 29 September; time window 10:45–15:45 BST; weather-based timing rules apply.

## Data Collected and Attributes
- Core metadata (for each recording occasion):
  - Site Identification Code (e.g., T05)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling Date/time
  - Start time
  - Temperature at end of recording
  - Percentage sunshine (section-by-section and overall)
  - Wind speed at end of recording (Beaufort scale)
- Transect-level (per section):
  - Transect section number
  - Species code and species name
  - Number of individuals seen
  - Habitat description (coded 1–15)
  - BMS code and common name
  - BMS method (coding details)
  - Recording precision (as applicable)
- Data collection methodology emphasizes consistency with BMS coding and documentation
- Recording details include recording time, environmental conditions, and section-specific observations to aid interpretation

## Temporal Metadata
- Frequency: weekly observations across the 26-week sampling period
- Time sensitivity: start times and environmental conditions recorded to support phenology and abundance analyses
- Data windows and weather constraints influence when transects are conducted (e.g., temperature and sunshine considerations)

## Data Standards, Formats, and Access
- Core identification fields must accompany all datasets to enable spatial and temporal linking:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Sampling Date/time
- Data formats and transfer conventions are defined in accompanying Data Transfer documentation (ECN site restricted extranet).
- The protocol references the standard BMS coding system and habitat descriptions as per the BMS handbook.
- Recording forms: Standard BMS recording forms available from the Butterfly Monitoring Scheme (BMS) managed by the Biological Records Centre, ITE Monks Wood.
- Data are designed for integration into GIS workflows and cross-site comparisons, with attention to consistent resolution and unit conventions.

## GIS and Data Product Considerations
- Spatial features to model:
  - Transect routes (line features) and per-section boundaries (sub-line features)
  - Habitat types and plant associations within sections
  - Management operations proximity and impact zones
- Attributes for GIS analyses:
  - Temporal attributes (date, time, season)
  - Species-level counts and codes
  - Environmental covariates (temperature, sunshine, wind)
  - Site/section identifiers and coding schemes
- Data quality and integration:
  - Rigorous alignment with BMS data standards to facilitate aggregation across years and sites
  - Potential to combine with climate datasets to analyze relationships between butterfly abundance/phenology and climate variables
  - Consideration of multi-source data cleaning due to data being collected at multiple sites and by multiple recorders
- Outputs:
  - Spatial maps of transects, section-level habitat types, and butterfly sightings
  - Time-series datasets of counts by species and section
  - Metadata-rich data products enabling reproducible GIS analyses

## Quality Assurance and Challenges
- Data quality relies on early testing and iteration, standardization of recording practices, and adherence to BMS conventions.
- Challenges include:
  - Variation in data sources and multiple recorders, requiring robust QA/QC processes
  - Data gaps or missing resolutions, necessitating careful handling for spatial analyses
  - Maintaining consistent data standards across sites and years
  - Ensuring transects remain representative as management regimes or site conditions change

## References and Documentation
- Core protocol references:
  - Hall, M.L. 1981. Butterfly Monitoring Scheme instructions
  - Pollard et al. 1986, 1988, 1991; Thomas 1991 (context on butterfly monitoring and climate relationships)
  - Pollard, Hall & Bibby 1986 (monitoring abundance)
- Data exchange:
  - ECNCCU data transfer documentation (restricted access)
  - Data transfer documentation for ECN dataset formats
- Habitat and plant considerations:
  - Guidance on habitat description and emphasis on butterfly food plants and nectar sources as qualitative context for results