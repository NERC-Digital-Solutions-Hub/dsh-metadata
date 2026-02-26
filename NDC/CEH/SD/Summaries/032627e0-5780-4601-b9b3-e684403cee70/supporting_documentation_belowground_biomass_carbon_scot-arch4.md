# Supporting documentation for data resource Belowground_Biomass_Carbon_Scot.csv

## Overview
- Physical and biogeochemical measurements of belowground biomass and organic carbon content from Scottish salt marshes, collected in 2021.
- Dataset derived from gouge sediment cores taken from four saltmarshes across Scotland to quantify belowground biomass and carbon in blue carbon environments.
- Location data provided in both decimal degrees (WGS84) and projected X/Y coordinates; marsh sites chosen to reflect diverse saltmarsh environments around Scotland.

## Data Content and Structure
- Core measurements include:
  - Belowground biomass (kg m^-2)
  - Organic carbon content (OC, %)
  - Belowground carbon (kg C m^-2)
  - Dry root biomass (kg m^-2)
- Key descriptive fields include:
  - Marsh_ID, Year, Sample_Archive_Location, Local_Authority
  - Marsh_Type (Estuarine, Back-Barrier, Fringing, Embayment)
  - Core_ID, Sampling_Method, Sample_Depth_cm
  - Lat_dec_deg, Long_dec_deg, X_easting, Y_northing
  - NVC_Class (National Vegetation Classification)
- Data resources are stored as CSV files (.csv). A separate data resource description outlines field definitions and units.

## Sampling and Laboratory Methods
- Field sampling:
  - Eight root cores collected from three Scottish saltmarshes using a gouge corer (diameter ~5.7 cm) to a depth of 10 cm.
  - Sample locations recorded with Differential GPS (DGPS).
  - Vegetation communities classified using the British National Vegetation Classification (NVC) scheme.
- Sample processing:
  - Roots washed to remove sediment, dried at 60°C for 72 hours, weighed to determine belowground biomass.
  - Roots milled to fine powder; 50 mg analyzed for organic carbon content.
- Carbon quantification:
  - Total Organic Carbon (TOC) measured with a Soli total organic carbon instrument using a temperature gradient method (DIN 19539; Natali et al., 2020; Smeaton et al., 2021).
  - Sub-samples analyzed in triplicate; calibration performed using Calcium Carbonate (CaCO3) and relevant TOC/ROC/TIC standards.
- Calibration and quality control:
  - Soli TOC calibrated with appropriate standards; laboratory equipment calibrated per University of St Andrews practices.
  - No statistical treatment details provided (NA in that field).

## Metadata and Data Management
- Location and site metadata:
  - Lat/Long provided in decimal degrees (WGS84); accompanying X/Easting and Y/Northing coordinates.
  - Marsh_Type descriptions cover multiple estuarine settings.
- Data quality and notes:
  - “NA” indicates no data in cells for certain fields.
  - Clear documentation of methods and calibration procedures enhances traceability and reproducibility.
- Data provenance:
  - References linked to methods and standards used for sampling, analysis, and classification.

## Data Format, Access, and Use
- Primary data format: .csv
- Additional descriptor:
  - A separate data resource description lists field formats and data types (e.g., Lat/Long as numbers, Marsh_ID as text).
- Access considerations:
  - No paywalls or restricted access indicated within the documentation; data is described for discoverability and reuse with explicit methodological context.

## Usage, Limitations, and Reuse
- Suitable for analyses of belowground biomass and carbon stocks in Scottish saltmarshes, spatial comparisons across marsh types, and integration with vegetation classifications (NVC).
- Limitations:
  - Data limited to four marshes (and root-focused subsamples from three marshes); year-specific (2021) dataset scope.
  - Some fields marked as NA (missing) in statistical treatment or other descriptive sections.
- Reuse considerations:
  - Calibration and measurement methods well-documented; units and field definitions provided to support proper interpretation and reproducibility.
- References for methods and standards:
  - Dadey et al. (1992), DIN 19539 (2015), Ford et al. (2019), Natali et al. (2020), Rodwell (2000), Smeaton et al. (2021), Troels-Smith (1955).