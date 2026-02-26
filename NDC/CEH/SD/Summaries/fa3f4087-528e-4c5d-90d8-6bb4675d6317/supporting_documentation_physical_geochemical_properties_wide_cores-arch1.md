# Physical_geochemical_properties_wide_cores_essex.csv

## Overview
- Data resource from Carbon Storage in Intertidal Environments (C-SIDE); funded by NERC (NE/R010846/1)
- Physical and geochemical properties of saltmarsh soils from 19 wide-diameter gouge cores across 8 Essex sites
- Collected in 2019; sites represent different saltmarsh origins: natural, historic breach, and managed realignment
- Geographic scope includes precise coordinates (lat/long in WGS84) and alternative X/Y grid references

## Data Content
- Core_ID: core identifier
- Saltmarsh: saltmarsh name
- Marsh_type: Natural, Managed Realignment, Historic Breach
- Lat_dec_deg, Long_dec_deg: decimal degree coordinates (WGS84)
- X_easting, Y_northing: grid coordinates (Easting, Northing)
- Elevation_above_OD__m: elevation above ordnance datum (m)
- Sample_depth_cm: depth interval of sub-sample (cm)
- Mid_Point_depth_cm: depth interval mid-point (cm)
- Substrate: Troels-Smith classification
- Dry_bulk_density_g_cm_3: dry bulk density (g cm^-3)
- OC_perc: organic carbon content (%)
- File format: CSV

## Data Collection and Methods
- Sample design: 19 cores collected from 8 sites; cores are 60 mm gouge cores
- Laboratory processing: cores sectioned into 1 cm intervals (n = 1952 sub-samples)
- Location recording: DGPS used for site locations
- Sample handling: samples frozen at -20°C until analysis
- Carbon analysis: total organic carbon quantified using Elementar Soli TOC with temperature gradient method
- Calibration and QA: Soli TOC calibrated with CaCO3 and appropriate standards; isotopic values quality controlled via repeat analyses of high OC standards
- General QC: laboratory equipment calibrated per University of St Andrews practices
- Data architecture: headers and data types described (e.g., Lat/Long as numbers, Substrate as text)

## Data Structure and Metadata
- Data resource description provides detailed header definitions and formats for CSV
- Observations located in environmentally similar regions to enable comparability
- Metadata supports traceability from core IDs to geographic and geochemical measurements

## Potential Analyses and Uses
- Examine correlations between organic carbon content (OC_perc) and depth (Sample_depth_cm / Mid_Point_depth_cm)
- Compare OC distribution across Marsh_type categories (Natural vs Historic Breach vs Managed Realignment)
- Assess relationships between OC_perc and substrate type, elevation, and spatial position (lat/long or easting/northing)
- Inform carbon storage assessments in saltmarsh soils and comparisons with UK-wide datasets (e.g., related studies cited)
- Use as a basis for cross-site comparisons across Essex saltmarshes and integration with broader environmental datasets

## provenance and References
- References include: Dadey et al. (1992); DIN 19539 (2015); Natali et al. (2020); Smeaton et al. (2021); Troels-Smith (1955)