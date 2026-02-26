# Soil biochemical measurements from saltmarshes of different ages on the Essex coast, UK 2011..

- Overview
  - A chronosequence study of saltmarsh soils across sites aged 16 to 114 years since restoration or breach on the Essex coast, including natural salt marsh references and fields on former salt marsh.
  - Aims to document soil biogeochemical properties and how they change with marsh age; data intended for governance, discovery, and reuse by researchers and practitioners.

- Dataset contents and key variables
  - Measured properties (per 30 cm soil cores): bulk density, moisture content, pH, electrical conductivity, available ammonium (NH4+), total oxidised nitrogen (TON NO3-), organic matter content (loss on ignition), below-ground biomass to 30 cm depth, soil carbon (%), soil nitrogen (%).
  - Data are organized for 30 cm depth cores, with multiple sampling locations per site.
  - Two CSV datasets: Saltmarsh_Chronosequence_data_2011.csv and Saltmarsh_Chronosequence_data_2010_2017.csv.
  - Dataset field descriptions are provided in two formats (Dataset Field Descriptions 1 and 2) to support interpretation and reuse.

- Sampling design and sites
  - Sampling conducted in October 2011 for salt marsh sites; Tollesbury field samples collected in July 2010; other sites sampled in 2017.
  - Three restored salt marshes and six accidentally breached sites chosen to form a chronosequence (16 to 114 years since breach/restoration).
  - Natural salt marshes sampled as reference; adjacent fields on former salt marsh included where access permitted to provide baseline timepoint data.
  - No planned repeat sampling.

- Field and laboratory methods
  - Field sampling: random locations within marshes above 1.5 m OD; 4 cm diameter soil cores, 30 cm long; three cores per sampling location; four sampling locations per marsh; 2–6 locations for fields on former marshes.
  - Laboratory processing: soils air-dried, ground, and sieved to <2 mm; batch analyses conducted with standard methods.
  - Measurements:
    - Electrical conductivity (EC) and pH in 1:2.5 deionised water suspension.
    - Organic matter by loss on ignition at 375°C for 16 hours.
    - NH4+ and NO3- by 1M KCl extraction with colorimetric analysis.
    - Total soil C and N by combustion (CN analyzer).
    - Below-ground biomass estimated by washing, drying at 80°C for 72 hours, and weighing.
  - Calibration and QA: all laboratory equipment calibrated per Centre for Ecology & Hydrology (CEH) Bangor practices; results checked for outliers; noted that blank data cells indicate missing data due to sample loss or non-analysis.
  - File formats: CSV files; dataset field headers defined with explicit description and units in the field descriptions.

- Data structure, provenance, and metadata
  - Site-level metadata includes SiteName, SiteCode, grid coordinates (Easting/Northing) for each site, and age-related fields (Year of breach, Years since breach to 2011).
  - Restored and breached sites include grid references for both site and surrounding features; natural marsh and fields have corresponding coordinates.
  - Dataset includes Human-readable notes on missing data and data provenance, with references to original methodological sources.

- Location coordinates and site details
  - Detailed grid references (Easting/Northing) for all restored/breached sites, natural marsh references, and fields on former salt marsh.
  - Specific site examples include Tollesbury, Orplands, NortheyMR, Barrow Hill, Ferry Lane (B), Wallasea Island, North Fambridge, Brandy Hole, with breach years ranging from 1897 to 1995 and years since breach to 2011 from 16 to 114 years.
  - Natural marsh references and field sites are clearly distinguished with corresponding coordinates.

- Documentation and references
  - Methods and analytical techniques aligned with established practices, with references:
    - Avery, B.W., and Bascombe, C.L. 1974. Soil Survey Technical Monograph No.6.
    - Ball, D.F. 1964. Loss-on-ignition as a measure of organic matter and carbon.
  - Dataset documentation includes two levels of dataset field descriptions to aid interpretation and reuse.

- Data governance and stewardship considerations for Data Stewards
  - Ensure metadata completeness: site identities, coordinates, breach ages, and variable definitions with units are clearly documented.
  - Preserve data provenance: link measurements to specific sites, sampling events, and laboratory methods; maintain versioning for the two CSV datasets.
  - Standardize metadata and file formats: provide consistent field names, units, and descriptions; maintain CSV delivery for easy reuse.
  - Manage data quality: maintain calibration and QA records; document data checks and handling of missing data, including notes that blank cells indicate missing due to sample loss or non-analysis.
  - Support discoverability and reuse: ensure dataset descriptions, field definitions, and site metadata are accessible in data portals; include references for methods and clear licensing/status (not specified in the source).
  - Plan for future updates: given no repeat sampling planned, consider documenting the temporal scope and potential for future resampling to extend the chronosequence.