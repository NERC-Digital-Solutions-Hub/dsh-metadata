# Physical_geochemical_properties_wide_cores.csv

## Overview
- Dataset from the Carbon Storage in Intertidal Environments (C-SIDE) project.
- Physical and geochemical properties of saltmarsh soils from 33 wide-diameter gouge cores (60 mm) across 19 UK saltmarshes, collected 2018–2021.
- Used to calculate organic carbon burial rates across UK saltmarsh ecosystems.

## Data Resource Details
- Core identifiers and site info: Core_ID, Saltmarsh, Marsh_type (Natural or Realigned), Marsh_zone (Low LM or High HM), Nation (Scotland, Wales, England).
- Temporal and locational data: Collection_year, Lat_dec_deg, Long_dec_deg (WGS84 coordinates), X_easting, Y_northing (local grid), Elevation_above_OD__m (metres).
- Sub-sampling and depth: Sample_depth_cm, Mid_Point_depth_cm (depth interval details).
- Substrate and density: Substrate (Troels-Smith classification), Wet_bulk_density_g_cm_3, Dry_bulk_density_g_cm_3.
- Geochemical measurements: OC_perc (organic carbon %), N_Perc (nitrogen %), CN (carbon/nitrogen ratio), NC (nitrogen/carbon ratio), d13C_per_mil (δ13C org), d15N_per_mil (δ15N).
- Data format: CSV file with a detailed data resource description and a data dictionary for columns.
- Documentation of site coverage: sites chosen to represent UK saltmarsh diversity in terms of sediment types and carbon content.

## Methods and Quality Assurance
- Sampling: 33 cores from 19 saltmarshes using a 60 mm gouge corer; DGPS used for precise site locations; samples frozen at -20°C until analysis.
- Core processing: Troels-Smith classification for descriptions; cores sectioned into 1 cm intervals (n = 1952 samples).
- Bulk density: measured by drying sub-samples (60°C for 72 hours) to compute bulk density.
- Carbon and isotopes: 
  - OC quantified by digesting milled sediment (50 mg) and analyzing with Elementar Soli TOC using the temperature gradient method (DIN 19539) and related standards.
  - Stable isotopes: approximately 12 mg per tin capsule for OC and δ13C_org; 12 mg per silver capsule for N and δ15N; silver capsules acid-fumigated to remove carbonate prior to measurement; analyses performed with EA-IRMS at James Hutton Institute.
- Calibration and QA: TOC calibration with CaCO3 and soil standards; isotope calibration with appropriate standards; quality control via repeated analysis of a high OC sediment standard; lab practices aligned with University of St Andrews protocols.
- Data handling notes: Some sections in the description are marked NA (e.g., statistical treatment, data checking), indicating limited or no detailing in those areas.

## Data Model and Metadata
- Data structure: Physical_geochemical_properties_wide_cores.csv with a comprehensive column set describing core identity, location, depth, substrate, densities, and geochemical measurements.
- Coordinate reference: Lat/Long in decimal degrees (WGS84); Easting/Northing provided for alternative spatial reference.
- Units and data types: Numeric values for densities, depths, and concentrations; text fields for identifiers and classifications.
- Metadata coverage: Includes collection year, sample depths, instrumentation, calibration references, and isotope methodology, enabling reproducibility and cross-study comparability.

## Access, Reuse and Documentation
- File format: CSV.
- Data dictionary: Explicit column definitions and formats are provided in the dataset description.
- Licensing and access: Not specified in the provided excerpt; users should verify licensing terms and data access conditions with the data provider.
- Provenance: Methods, standards, and references cited for all major analytical steps and calibrations.

## Governance and Standards
- Methodological alignment with established practices for soil carbon and isotope analyses (Troels-Smith sediment classification; TOC analysis; EA-IRMS).
- Calibration and QA procedures reference standard materials and published methodologies.
- Multi-institutional collaboration (University of St Andrews, University of Glasgow, University of York, UK CEH, University of Leeds, Bangor University) supports governance and data integrity.

## Challenges and Considerations for Data Stewards
- Metadata completeness: Some sections (e.g., statistical treatment, data checks) are NA; consider completing for full auditability.
- Interoperability: Consistency of units and formats across related datasets; ensure standardized units for density, OC, N, isotopes.
- Licensing and access: Clarify data usage rights and any embargoes or restrictions to enable reuse.
- Updates and versioning: Dataset covers 2018–2021; establish version control if updates or additional cores are added.
- Data quality traceability: Document links from raw samples to final OC% and isotope values, including any data transformations.

## References
- Dadey, K.A., Janecek, T., Klaus, A. (1992). Dry-bulk density: its use and determination.
- DIN 19539 (2015). Investigation of solids: TOC/ROC/TIC standards.
- Harris, D., Horwáth, W.R., Van Kessel, C. (2001). Acid fumigation of soils to remove carbonates prior to TOC/isotope analysis.
- Natali, C., Bianchini, G., Carlino, P. (2020). Thermal stability of soil carbon pools.
- Smeaton, C., Hunt, C.A., Turrell, W.R., Austin, W.E. (2021). Marine Sedimentary Carbon Stocks in UK EEZ.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments.