# Physical and geochemical properties of saltmarsh soils produced from 33 wide diameter gouge cores spanning 19 UK saltmarshes collected between 2018-2021

## Project and aims (GIS context)
- Part of the Project: Carbon Storage in Intertidal Environments (C-SIDE), funded by NERC (NE/R010846/1).
- Multidisciplinary team across UK universities and external partners.
- Data collected to calculate organic carbon burial rates across UK saltmarsh ecosystems; emphasis on spatial distribution and variation.

## Data resource overview
- Dataset: Physical and geochemical properties of saltmarsh soils from 33 wide-diameter gouge cores across 19 UK saltmarshes (2018–2021).
- Purpose for GIS: Provides georeferenced observations and properties suitable for map-based analysis of OC burial across sites.

## Spatial coverage and coordinates
- Sites across the United Kingdom (Scotland, Wales, England) with varied saltmarsh types and zones.
- Location data provided in:
  - Latitude/Longitude (decimal degrees, WGS84)
  - X_easting and Y_northing coordinates
  - Elevation above ordnance datum (m)
- Site metadata includes marsh name, nation, marsh_type (Natural or Realigned), and marsh_zone (Low or High).

## Data fields and variables (for GIS integration)
- Core_ID, Saltmarsh, Marsh_type, Marsh_zone, Nation, Collection_year
- Spatial: Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_above_OD__m
- Sampling metadata: Sample_depth_cm, Mid_Point_depth_cm
- Substrate (Troels-Smith classification)
- Physical properties: Wet_bulk_density_g_cm_3, Dry_bulk_density_g_cm_3
- Geochemical properties: OC_perc (Organic Carbon %), N_Perc (Nitrogen %), CN (Carbon/Nitrogen), NC (Nitrogen/Carbon)
- Isotopes: d13C_per_mil (δ13C_org), d15N_per_mil (δ15N)
- Core descriptive fields to link samples to locations and contexts

## Data collection and laboratory methods
- Field sampling: 33 cores (60 mm gouge corer); core descriptions recorded; DGPS used for precise site locations.
- Core processing: Sediment sliced into 1 cm sections (n ≈ 1952).
- Sample handling: Cores frozen at -20°C until analysis.
- Laboratory analyses:
  - Drying to determine bulk densities (60°C, 72 h)
  - Carbon quantification: Elementar Soli TOC (DIN 19539, with calibration standards)
  - Stable isotopes: EA-IRMS; carbonate removal via acid fumigation for certain analyses
- Calibration and QA:
  - TOC calibrated with CaCO3 and soil standards (B2290)
  - Isotopic analyses calibrated with high OC sediment standards (B2151)
  - QA via repeat analyses and adherence to established lab practices

## Data formats and structure
- Primary file: Physical_geochemical_properties_wide_cores.csv
- Data types:
  - Text: Core_ID, Saltmarsh, Marsh_type, Marsh_zone, Nation, Collection_year
  - Numeric: Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_above_OD__m, Sample_depth_cm, Mid_Point_depth_cm, Wet_bulk_density_g_cm_3, Dry_bulk_density_g_cm_3, OC_perc, N_Perc, CN, NC, d13C_per_mil, d15N_per_mil
- File format: CSV (comma-separated values)

## Data quality and provenance
- Observations and measurements tied to 19 saltmarshes across the UK with standardized sampling and laboratory procedures.
- Quality control procedures implemented for carbon and isotope analyses, using reference standards and calibration procedures.
- Documentation includes detailed methodological notes and references for reproducibility.

## How this data supports GIS analysis
- Enables creation of precise point datasets for sampling sites with rich contextual attributes (marsh type, zone, nation, elevation, substrate).
- Facilitates spatial joins with elevation models, land cover, hydrology, and other biogeochemical layers.
- Supports mapping and calculation of organic carbon stocks and burial rates across UK saltmarshes.
- Useful for identifying spatial patterns in OC content, nutrient ratios, and stable isotopes across different marsh zones and substrates.

## References and methodological notes
- Core sampling and dating methods follow Troels-Smith classification and established soil carbon/isotope protocols.
- Key references include works on dry bulk density determination, carbonate removal for isotopic analysis, and targeted standards (CaCO3, B2290, B2151).
- Specific methodological details and calibration references are provided in the resource description (e.g., Natali et al., Smeaton et al., Harris et al., Troels-Smith).