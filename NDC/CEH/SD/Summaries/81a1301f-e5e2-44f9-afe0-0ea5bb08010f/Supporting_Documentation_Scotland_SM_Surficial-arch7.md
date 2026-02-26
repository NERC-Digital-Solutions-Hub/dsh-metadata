# Supporting documentation for data resource Scotland_SM_Surficial.csv

## Overview
- Dataset of surficial soils from Scottish salt marshes (top 10 cm).
- Variables: dry bulk density, loss on ignition (LOI), and organic carbon content.
- 471 soil samples from 46 salt marshes across Scotland (excluding Outer Hebrides and Shetland).
- Timeframe: 2018–2020; Scottish portion of C-SIDE sampling plus the CarbonQuest citizen science program.
- Aims to support map-based analysis of soil properties and carbon stocks in salt marshes.

## Data resource details
- Project and funding: Carbon Storage in Intertidal Environments (C-SIDE); funded by NERC (NE/R010846/1).
- Staff and team: William Austin; researchers from University of St Andrews, University of Glasgow, Bangor University, and C-SIDE Citizen Science Team.
- Data resource name: Dry bulk density, loss on ignition and organic carbon content of surficial soils from Scottish salt marshes, 2018-2020.
- Location scope: Scotland (Latitude/Longitude and OSGB coordinates provided; includes country-level mapping and grid references).
- Geographic boundaries and projection: WGS84 coordinates; OSGB 1936 (British National Grid) with easting/northing values available.
- Monitoring period: 2018–2019 (Scottish portion of C-SIDE sampling); no repeat sampling planned.

## Sampling and data collection methods
- Sampling depth: 0–10 cm (top 10 cm of soil).
- Sampling method: 50 mL syringe (modified) or 30 mm gouge corer; four team members contributed to classification and data verification.
- GPS and positioning: Locations recorded with multiple devices (mobile phones, handheld units, RTK systems); coordinates cross-validated against habitat maps and aerial imagery.
- Sample handling: Samples frozen at -20°C prior to analysis.
- Soil texture classification: Sandy vs. Not-Sandy (based on Ford et al., 2019) and expert judgement.
- Depth and location fields: Depth_cm; Lat_dec_deg; Long_dec_deg; Grid_Reference; X_easting; Y_northing.

## Variables and data schema
- Saltmarsh_Name: Saltmarsh name (Text).
- Year: Year of sampling.
- Lat_dec_deg / Long_dec_deg: Decimal degrees (WGS84) for sample location.
- Grid_Reference: Ordnance Survey National Grid coordinates (Text).
- X_easting / Y_northing: OSGB36 grid coordinates (Numeric).
- Sampling_Method: 50 mL syringe or gouge corer (Text/Numeric codes).
- Depth_cm: Depth of soil sample (cm) (Numeric).
- Dry_Bulk_Density_g_cm_3: Dry bulk density (g/cm^3) (Numeric).
- LOI_Perc: Loss on ignition (organic matter content, %wt) (Numeric).
- OC_Perc: Organic carbon content (% wt) measured by elemental analysis (Numeric).
- Soil_Texture: Sandy / Not-Sandy (Numeric coding and/or Text).
- File_formats_used: File formats of data (CSV, etc.) (Text).
- Other notes: Any missing data (NA) indicating insufficient sample material for OC content, etc.
- Calibration and standards: Elemental Analyzer calibrated with Acetanilide; repeated analysis with standard B2178 during runs.
- References for methods: Calibrations and procedures cited (e.g., Craft et al., 1991; Nieuwenhuize et al., 1994; Verardo et al., 1990; Ford et al., 2019).

## Geospatial relevance for GIS work
- Provides geolocated soil property data suitable for mapping salinity marsh carbon stocks and sediment characteristics.
- Coordinates provided in multiple systems (WGS84 lat/long and OSGB36 grid), enabling integration with common UK GIS datasets.
- Spatial scope includes 46 marshes across Scotland, enabling landscape-scale analyses of habitat types and carbon storage.
- Data quality checks align coordinates with habitat maps, improving reliability for map-based applications.

## Quality assurance and data quality
- Citizen Science samples undergo visual QC by experienced salt marsh scientists before drying.
- GPS coordinates validated against habitat maps and aerial imagery.
- Four team members contributed to data classification and grid reference accuracy.
- OSGB36 coordinates and grid references cross-validated to ensure spatial consistency.
- Notes include handling of missing data (e.g., NA for OC content when sample material insufficient).

## Data formats and accessibility
- Primary data format: CSV with fields for location, depth, and soil property measurements.
- Geographic coordinates represented in decimal degrees (WGS84) with OSGB36/easting-northing equivalents available.
- Data provenance and methodological details documented, including sampling, analysis, calibration, and QC procedures.

## References
- Craft, C.B., Seneca, E.D., and Broome, S.W. (1991). Loss on ignition and Kjeldahl digestion for estimating organic carbon and total nitrogen in estuarine marsh soils.
- Dadey, K.A., Janecek, T., and Klaus, A. (1992). Dry-bulk density: its use and determination.
- Ford, H. et al. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type.
- Kennedy, P., Kennedy, H., and Papadimitriou, S. (2005). Effects of acidification on determination of organic carbon and nitrogen.
- Nieuwenhuize, J. et al. (1994). Rapid analysis of organic carbon and nitrogen in particulate materials.
- Verardo, D.J. et al. (1990). Determination of organic carbon and nitrogen in marine sediments using elemental analysis.