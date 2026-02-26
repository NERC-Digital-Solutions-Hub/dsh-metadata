# Supporting documentation for data resource Scotland_SM_Surficial.csv

- Project and provenance
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funding: NERC (NE/R010846/1)
  - Staff Responsible: William Austin
  - Research Team: Paulina Ruranska; Lucy C. Miller; Carolyn Hindle; Cai J.T. Ladd; Craig Smeaton; Martin W. Skov; William E.N. Austin; C-SIDE Citizen Science Team

- Data resource and scope
  - Data resource name: Dry bulk density, loss on ignition and organic carbon content of surficial soils from Scottish salt marshes, 2018-2020
  - Content: 471 surficial soil samples (top 10 cm) from 46 Scottish salt marshes
  - Geographic scope: Scotland (excluding Outer Hebrides and Shetland)
  - Site description: Sites selected to represent contrasting habitats (sediment types, vegetation, sea level history)

- Monitoring and sampling
  - Sampling period: January 2018 – December 2019 (Scottish portion of C-SIDE and CarbonQuest citizen science)
  - Sampling approach: 50 ml syringe to 10 cm depth or 30 mm gouge corer; GPS coordinates captured; samples frozen at -20°C
  - No repeat sampling planned

- Variables and measurements
  - Observed parameters:
    - Soil Texture (Sandy / Not-Sandy)
    - Dry Bulk Density (g cm-3)
    - Organic Matter Content (LOI, % wt.)
    - Organic Carbon Content (OC, % wt.) via Elemental Analysis
  - Data structure: Data available with fields such as Saltmarsh_Name, Lat_dec_deg, Long_dec_deg, Year, X_easting, Y_northing, Depth_cm, Dry_Bulk_Density_g_cm_3, OC_Perc, LOI_Perc, Soil_Texture, etc.

- Laboratory procedures and calibration
  - Soil texture classification: Ford et al., 2019 methodology
  - Dry Bulk Density: derived from dried samples (60 °C, 72 h) and sample volume
  - Loss on Ignition (LOI): dried and combusted at 450°C for 4 h to estimate organic matter
  - Organic carbon analysis: Elemental Analysis (Carlo Erba Vario EL Cube) after HCl acidification to remove carbonates
  - Calibration and QA: Acetanilide calibration; repeated analysis of standard organic soil (B2178)

- Data quality assurance
  - Citizen Science data QC: visual inspection by experienced salt marsh scientists prior to drying
  - Geospatial QC: GPS coordinates cross-checked against habitat maps and aerial imagery
  - Multi-person verification: four team members independently assessed grid reference classifications
  - Documentation of data fields: detailed header descriptions and variable formats included

- Data formats and storage
  - File format: CSV
  - Coordinate formats: decimal degrees (WGS84), and OSGB36 grid references with corresponding easting/northing
  - Data management: datasets stored and uploaded to appropriate data portals (as part of standard monitoring/data portal practices)

- Relevance for environmental monitoring
  - Provides standardized, quality-checked measurements of salt marsh soil properties linked to carbon storage
  - Enables temporal and spatial comparisons of soil carbon-related metrics across Scottish salt marshes
  - Supports integration with other datasets (e.g., habitat maps, vegetation data) for broader environmental health assessments

- References (methodology and calibration)
  - Craft, C.B., Seneca, E.D. and Broome, S.W., 1991
  - Dadey, K.A., Janecek, T. and Klaus, A., 1992
  - Ford, H., Garbutt, A., Duggan-Edwards, M., Harvey, R., Ladd, C. and Skov, M.W., 2019
  - Kennedy, P., Kennedy, H. and Papadimitriou, S., 2005
  - Nieuwenhuize, J., Maas, Y.E. and Middelburg, J.J., 1994
  - Verardo, D.J., Froelich, P.N. and McIntyre, A., 1990