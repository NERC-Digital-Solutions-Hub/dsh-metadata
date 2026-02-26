# Supporting documentation for data resource Belowground_Biomass_Carbon_Scot.csv

- Overview
  - Physical and biogeochemical measurements of belowground biomass and organic carbon content from Scottish salt marshes, 2021.
  - Gouge sediment cores used to quantify belowground biomass and organic carbon in blue carbon environments across Scotland.
  - Location data provided in decimal degrees (WGS84) and projected coordinates (X/Y); aims for regional representativeness across Scotland.

- Data content and structure
  - Key variables include:
    - Marsh_ID, Year, Sample_Archive_Location, Local_Authority
    - Marsh_Type, Core_ID, Sampling_Method, Sample_Depth_cm
    - Lat_dec_deg, Long_dec_deg, X_easting, Y_northing
    - NVC_Class, Dry_Root_Biomass_kg_m_2, Belowground_Biomass_kg_m_2
    - OC_Perc, Belowground_C_kgC_m_2
  - Data resource description fields specify formats and definitions (e.g., Lat/Long in decimal degrees, biomass and carbon metrics, and class labels).

- Data collection methods and provenance
  - Sampling: Eight root core samples collected from three Scottish saltmarshes using a gouge corer (diameter ~5.7 cm) to 10 cm depth.
  - Descriptions and vegetation classification: Troels-Smith (1955) characterization; British National Vegetation Classification (NVC) used for vegetation communities.
  - Location data: Differential GPS (DGPS) for precise site coordinates.
  - Sample preparation: Roots washed to remove sediment in 10% Calgon solution; roots weighed, then oven-dried at 60°C for 72 hours.
  - Carbon quantification: Samples milled; 50 mg analyzed with a Soli total organic carbon (TOC) instrument via temperature gradient method (DIN 19539). Triplicate analysis for sub-samples.
  - Calibration: Soli TOC calibrated with CaCO3 and standard soils (TOC/ROC/TIC) where applicable.
  - References for methods include DIN 19539, Natali et al. (2020), Smeaton et al. (2021), and related methodological sources.

- Data quality, QA, and metadata
  - Laboratory equipment calibrated following University of St Andrews practices.
  - Calibration materials and standards documented for carbon quantification.
  - Metadata structure includes clear field definitions, units, and formats to support data discovery and reuse.
  - Some fields indicate missing data (NA) or not applicable (e.g., statistical treatment NA); explicit notes clarify data gaps.

- Data formats, storage, and accessibility
  - Primary file format: .csv
  - Metadata describes column formats (e.g., Lat/Lon as numbers, text fields for IDs and classifications).
  - Data intended for upload to relevant portals and catalogues to support discovery and reuse.

- Access considerations and reuse
  - Metadata captures site locations, marsh types, and sampling details to enable reproducibility and lineage tracing.
  - Documentation supports appropriate data sharing while noting calibration and methodological provenance; user should refer to provided references for method replication.
  - Potential inconsistencies noted: document mentions four saltmarshes for core collection but eight cores from three saltmarshes for some procedures; this discrepancy should be resolved or clarified during data governance and ingestion.

- Limitations and considerations for stewardship
  - Inconsistencies in site counts (four sites vs. three) and potential data gaps (NA fields) require clarification during dataset curation.
  - Outdated or legacy classifications (e.g., NVC from Rodwell, 2000) may influence comparative analyses; consider versioning or mapping to current classifications if needed.
  - Some fields indicate missing data; ensure downstream users understand NA conventions and data completeness.

- References
  - Din 19539; Natali et al. 2020; Smeaton et al. 2021; Rodwell 2000; Troels-Smith 1955; Ford et al. 2019; Dadey et al. 1992.