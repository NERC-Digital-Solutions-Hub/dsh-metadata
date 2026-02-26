# Supporting documentation for data resource Belowground_Biomass_Carbon_Scot.csv

- Overview
  - Physical and biogeochemical measurements of belowground biomass and organic carbon content from Scottish salt marshes, 2021.
  - Gouge sediment cores used to quantify belowground root biomass and organic carbon in blue carbon environments across Scotland.

- Dataset scope and location
  - Geographic extent: Scotland (four saltmarsh sites representative of coastline) with observations described in decimal degrees (WGS84) and corresponding X (easting) and Y (northing) coordinates.
  - Year of sampling: 2021 (Year of sample collection).
  - Site characteristics: marshes classified by National Vegetation Classification (NVC) and various Marsh_Type categories (Estuarine, Back-Barrier, Fringing, Embayment, etc.).

- Sampling methods and measurement procedures
  - Field sampling: Eight root cores collected from three Scottish saltmarshes using a 5.7 cm gouge corer to 10 cm depth.
  - Vegetation and site description: Core descriptions recorded using Troels-Smith (1955) scheme; vegetation characterized with the British National Vegetation Classification (NVC) framework; locations recorded with Differential GPS (DGPS).
  - Sample processing: Roots washed in 10% Calgon to remove sediment, weighed fresh and then oven-dried at 60°C for 72 hours to determine belowground biomass (kg m^-2).
  - Carbon quantification: Dried root material milled to powder; 50 mg used per crucible; total organic carbon (TOC) measured with a Soli total organic carbon analyzer using the temperature gradient method; subsamples analyzed in triplicate; belowground carbon calculated from biomass and OC data.
  - Calibration and standards: TOC measurements calibrated with CaCO3, and TIC/ROC/OC standards (B2290); lab calibration performed per established practices.
  - Quality assurance: Laboratory equipment calibrated in accordance with University of St Andrews practices; no statistical treatment details provided (NA for statistical treatment field).

- Data structure and formats
  - Data resource content includes:
    - Dataset identifier and details (Belowground_Biomass_Carbon_Scot.csv; .csv file format).
    - Variables/parameters observed: Belowground biomass (kg m^-2), organic carbon content (%), and belowground carbon (kg C m^-2), alongside field metadata.
    - Data resource description fields (examples): Marsh_ID, Year, Sample_Archive_Location, Local_Authority, Marsh_Type, Core_ID, Sampling_Method, Sample_Depth_cm, Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, NVC_Class, Dry_Root_Biomass_kg_m_2, Belowground_Biomass_kg_m_2, OC_Perc, Belowground_C_kgC_m_2.
  - Data formats: CSV for the main dataset; descriptive fields outline the cell formats (Text or Number) for each column.

- Data quality, checks, and provenance
  - Measurements tied to standardized field and lab protocols (Troels-Smith classification; NVC framework; DGPS coordinates).
  - Calibration and QA procedures cited; equipment calibration ensured; methodology aligned with referenced standards and literature.
  - Data note: “NA” used where statistical treatment is not applied or not available; “NA indicates no data in cells.”

- Utility, reuse, and access
  - Purpose aligns with monitoring environmental health and blue carbon stock assessment in Scotland.
  - Data prepared to be stored and uploaded to appropriate data portals; standardized outputs facilitate cross-site and temporal comparisons.
  - Potential applications include monitoring above/belowground carbon stocks, assessing spatial variability of carbon within Scottish saltmarshes, and supporting policy-relevant ecological assessments.

- References and methodological context
  - Methodologies and classifications reference: Troels-Smith (1955); Rodwell (2000); Ford et al. (2019); Natali et al. (2020); Smeaton et al. (2021); DIN 19539 (2015); and related calibration and analytical standards (CaCO3, TOC/TIC/ROC).
  - Notes on measurement practices and the scientific basis for carbon quantification and biomass estimation.