# Supporting documentation for data resource Belowground_Biomass_Carbon_Scot.csv

## Overview
- Describes a data resource of physical and biogeochemical measurements of belowground biomass and organic carbon content from Scottish salt marshes, collected in 2021.
- Aims to quantify belowground biomass and carbon content to support understanding of blue carbon stores across Scotland.

## Data Resource Description
- Marsh_ID: Saltmarsh name.
- Year: Year of sample collection.
- Sample_Archive_Location: Where samples are stored.
- Local_Authority: Local authority jurisdiction for the saltmarsh.
- Marsh_Type: Estuarine (with possible variants such as Back-Barrier, Fringing, Embayment).
- Core_ID: Soil core identification.
- Sampling_Method: Method used to collect samples.
- Sample_Depth_cm: Depth range of the sample (cm).
- Lat_dec_deg: Latitude in decimal degrees (WGS84).
- Long_dec_deg: Longitude in decimal degrees (WGS84).
- X_easting: X (Easting) coordinate.
- Y_northing: Y (Northing) coordinate.
- NVC_Class: National Vegetation Classification.
- Dry_Root_Biomass_kg_m_2: Dry weight of root biomass (kg m^-2).
- Belowground_Biomass_kg_m_2: Belowground biomass (kg m^-2).
- OC_Perc: Organic carbon content (% wt).
- Belowground_C_kgC_m_2: Belowground carbon (kg C m^-2).

## Data Content and Variables
- Variables include: Marsh_ID, Year, Sample_Archive_Location, Local_Authority, Marsh_Type, Core_ID, Sampling_Method, Sample_Depth_cm, Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, NVC_Class, Dry_Root_Biomass_kg_m_2, Belowground_Biomass_kg_m_2, OC_Perc, Belowground_C_kgC_m_2.
- Measurements reported: belowground biomass, organic carbon percentage, and belowground carbon, linked to site location and vegetation classification.

## Methods and Quality Assurance
- Field sampling: Gouge sediment cores from four Scottish saltmarshes, 5.7 cm diameter, to 10 cm depth; eight cores per set from three marshes.
- Vegetation and site characterization: Troels-Smith (1955) classification; DGPS for precise locations.
- Sample processing: Rinsed roots in 10% Calgon solution to remove sediment; dried roots at 60°C for 72 hours; weighed for belowground biomass.
- Carbon quantification: Samples milled; 50 mg weighed for analysis with Elementar Soli total organic carbon (TOC) using a temperature gradient method; triplicate sub-samples for root portions.
- Calibration and standards: Soli TOC calibrated with CaCO3 and suitable TOC/ROC/TIC standards.
- Data quality: Laboratory equipment calibrated per university practices; no statistical treatment reported in the dataset (NA).

## Spatial and Temporal Coverage
- Location: Scotland; observations across four saltmarshes around the coastline to capture variation in saltmarsh types, sediment, and organic carbon content.
- Coordinates provided: Lat/Lon (WGS84) and X/Y (Easting/Northing).
- Temporal scope: Year(s) of sample collection recorded (Year field included).

## Data Format and Metadata
- File format: .csv.
- Metadata: Includes detailed field descriptions and data types (text and numeric), with explicit definitions for each variable.
- Location referencing: Geographic coordinates in WGS84, plus local administrative and marsh-type classifications.
- Observations: Belowground biomass (kg m^-2), Belowground carbon (kg C m^-2), and OC content (%).

## Data Access, Provenance, and References
- Data resource describes the provenance of observations, laboratory procedures, and calibration/quality checks.
- References include standards and related methodological sources:
  - Dadey et al., 1992
  - DIN 19539: 2015-08
  - Ford et al., 2019
  - Natali et al., 2020
  - Rodwell, 2000
  - Smeaton et al., 2021
  - Troels-Smith, 1955

## Potential Limitations and Considerations for Analysts
- Some fields are NA (e.g., statistical treatment), potentially limiting certain analyses.
- Spatial and temporal coverage may be constrained to four marshes and a specific collection period in 2021, affecting broader generalizations.
- Data standardization across marsh types and coordinates (lat/lon vs. projected) should be checked when merging with other datasets.
- Access to domain expertise may be required to interpret vegetation classifications and sampling context correctly.

## References
- Dadey, K.A., Janecek, T., & Klaus, A. (1992). Dry-bulk density: its use and determination.
- DIN 19539 (2015). Investigation of solids Temperature dependent differentiation of Total Carbon (TOC400, ROC, TIC900).
- Ford, H. et al. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type.
- Natali, C. et al. (2020). Thermal stability of soil carbon pools: Inferences on soil nature and evolution.
- Rodwell, J. S. (2000). British plant communities, Maritime Communities and Vegetation of Open Habitats.
- Smeaton, C. et al. (2021). Marine Sedimentary Carbon Stocks of the United Kingdom's Exclusive Economic Zone.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments.