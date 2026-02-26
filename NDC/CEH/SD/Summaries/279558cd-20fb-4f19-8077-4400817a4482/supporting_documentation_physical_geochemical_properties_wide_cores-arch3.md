Physical_geochemical_properties_wide_cores.csv

## Overview
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project.
- Funded by NERC (NE/R010846/1); Staff Responsible: Craig Smeaton.
- Objective: measure physical and geochemical properties of saltmarsh soils from 33 wide-diameter gouge cores across 19 UK saltmarshes (2018–2021) to calculate organic carbon burial rates in UK saltmarsh ecosystems.

## Project and Data Scope
- Data resource: Physical and geochemical properties of saltmarsh soils from 33 wide-diameter gouge cores across 19 UK saltmarshes.
- Core details: 60 mm diameter gouge cores; 33 cores collected 2018–2021.
- Study area: United Kingdom; sites chosen to represent saltmarsh biodiversity, sediment types, and organic carbon content across Scotland, England, and Wales.

## Data Collection and Site Details
- Sampling framework: 33 gouge cores collected from 19 saltmarshes; core descriptions recorded on collection.
- Geolocation: DGPS used to record site locations; coordinates provided as decimal degrees (WGS84) with X (easting) and Y (northing) values.
- Site metadata: Marsh_type (Natural or Realigned); Marsh_zone (Low or High); Nation (Scotland, Wales, England); Collection_year.

## Methods and Procedures
- Sample handling: Cores sectioned at 1 cm intervals (n = 1952 sub-samples); cores frozen at -20°C prior to analysis.
- Physical measurements: Elevation above ordnance datum (m); Wet and Dry bulk density (g cm^-3); Substrate classified by Troels-Smith scheme.
- Chemical analyses:
  - Organic carbon: 50 mg sub-samples analyzed with Elementar SOLi TOC using a temperature gradient method (DIN 19539; Natali et al. 2020; Smeaton et al. 2021) to quantify OC.
  - Stable isotopes: approximately 12 mg per sample for OC and N; Tin and Silver capsules; acid fumigation on Silver capsules to remove carbonate; EA-IRMS used for δ13C_org (‰) and δ15N (‰).
- Calibration and QA:
  - TOC calibration with CaCO3 and silty soil standards (B2290); isotopic analyses quality controlled via repeat analyses of a high-OC standard (B2151).
  - All laboratory equipment calibrated according to university practices.
- Data processing: Samples dried at 60°C for 72 hours to derive bulk densities; isotopic analyses calibrated with reference materials.

## Variables and Data Products
- Data resource: Physical_geochemical_properties_wide_cores.csv
- Key variables (per core sub-sample or core-level): 
  - Core_ID, Saltmarsh, Marsh_type, Marsh_zone, Nation, Collection_year
  - Lat_dec_deg, Long_dec_deg; X_easting, Y_northing; Elevation_above_OD_m
  - Sample_depth_cm, Mid_Point_depth_cm
  - Substrate (Troels-Smith), Wet_bulk_density_g_cm_3, Dry_bulk_density_g_cm_3
  - OC_perc, N_Perc, CN, NC
  - d13C_per_mil, d15N_per_mil
- Data format: CSV
- Observational scope: 1952 sub-samples across 33 cores from 19 saltmarshes; geospatial and depth-resolved data enable carbon burial rate assessments.

## Data Quality, Standards, and Governance
- Metadata and standardization:
  - Geolocations provided in a consistent coordinate framework (WGS84; lat/long, plus easting/northing).
  - Troels-Smith substrate classification used for consistency in sediment description.
  - Depth discretization (1 cm intervals) with mid-point depth recorded.
- Calibration and QA:
  - TOC and isotopic analyses calibrated with established standards; QA through repeat measurements of high-OC standards.
  - Instrument calibration aligned with institutional laboratory practices.
- Data governance and accessibility:
  - Data structured with a clear data dictionary and standardized file format (.csv) to facilitate reuse and integration with monitoring frameworks.
  - Emphasizes the use of openly described methods and standards to support comparability and reproducibility across sites and studies.

## Relevance for Monitoring Frameworks
- Indicator suite for environmental health and carbon storage monitoring:
  - Organic carbon content (OC_perc) and nitrogen content (N_Perc) with carbon-to-nitrogen ratios (CN, NC) as indicators of soil organic matter characteristics.
  - Stable isotopes (d13C, d15N) to infer carbon sources and processing within saltmarsh soils.
  - Bulk density (wet/dry) and elevation to support carbon burial rate calculations and sediment dynamics interpretation.
  - Geospatial metadata and depth-resolved measurements enable spatial and vertical trend analyses across UK saltmarshes.
- Data management and standardization:
  - Use of standardized sampling (60 mm gouge cores), depth segmentation, and Troels-Smith classification supports harmonization with other monitoring datasets.
  - Calibrated analytical methods and QA procedures provide reliable data for monitoring frameworks and policy evaluation.
- Practical considerations for monitoring programs:
  - Multi-site UK coverage (Scotland, England, Wales) supports regional baseline establishment and trend detection.
  - Clear data documentation and open-format outputs facilitate integration into dashboards, reports, and governance processes for environmental health monitoring.

## References
- Dadey, K.A., Janecek, T., & Klaus, A. (1992). Dry-bulk density: its use and determination. Proceedings of the Ocean Drilling Program, Scientific Results.
- DIN 19539 (2015-08). Investigation of solids temperature-dependent differentiation of total carbon (TOC, ROC, TIC).
- Harris, D., Horwáth, W.R., & Van Kessel, C. (2001). Acid fumigation of soils to remove carbonates prior to total organic carbon or carbon-13 isotopic analysis. Soil Science Society of America Journal.
- Natali, C., Bianchini, G., & Carlino, P. (2020). Thermal stability of soil carbon pools: Inferences on soil nature and evolution. Thermochimica Acta.
- Smeaton, C., Hunt, C.A., Turrell, W.R., & Austin, W.E. (2021a). Marine Sedimentary Carbon Stocks of the United Kingdom's Exclusive Economic Zone. Frontiers in Earth Science.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments. Reitzels Forlag.