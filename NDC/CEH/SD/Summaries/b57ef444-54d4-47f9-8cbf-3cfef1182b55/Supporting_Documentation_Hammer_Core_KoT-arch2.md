# Supporting documentation for data resource Hammer_Cores_KoT.csv

- Project and leadership
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funding: NERC (NE/R010846/1)
  - Staff responsible: Craig Smeaton
  - Research team: Craig Smeaton; Luis Rees-Hughes; Natasha L.M. Barlow; William E.N. Austin (affiliations noted)

- Data resource name and description
  - Name: Sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh (Hammer cores)
  - Description: Bulk density, water content, porosity, and organic carbon content for 39 soil samples across 4 hammer cores collected from the Kyle of Tongue saltmarsh

- Location and site boundaries
  - Site: Kyle of Tongue, Scotland
  - Geographic references: WGS84 decimal coordinates; OSGB36 grid references; easting/northing coordinates
  - No repeat sampling planned

- Variables observed
  - Water Content (%)
  - Wet Bulk Density (g cm^-3)
  - Dry Bulk Density (g cm^-3)
  - Porosity (Φ)
  - Organic Carbon content (% by weight)
  - Simplified Troels-Smith soil description (classification)

- Sampling and analysis methods
  - Core collection: 150 cm PVC cores, sharpened edge, driven to 100 cm depth; top sealed for vacuum; cores extracted with a tractor jack
  - Core handling: split lengthways into working and archive sections
  - Physical measurements: fixed 4 cm^3 volumetric samples at 10 cm intervals; weighed for wet density; dried at 60°C for 72 hours to obtain dry density and water content; porosity calculated
  - Soil description: Troels-Smith (1955) classification; classifications independently performed by two team members
  - Elemental analysis: 10 mg milled samples acidified with 10% HCl to remove carbonates; dried and sealed; organic carbon measured with Elemental Analyzer (Vario EL Cube); three replicates per sample
  - Calibration and standards: Acetanilide used for calibration; repeated analysis of standard (medium Organic Soil standard B2178)

- Data processing and quality control
  - QA approach: Troels-Smith descriptions determined by two independent assessors; combined result reported
  - Calculations and references: density, porosity calculations guided by Athy (1930) and Dadey et al. (1992)
  - Data format: CSV files

- Data management and accessibility
  - File formats: .csv
  - Data linkage: associated with Smeaton et al. (2020) Geoderma paper on best practices for blue carbon stock estimation
  - Data resource description schema: Hammer_Core_KoT.csv with clearly defined fields (Core ID, collection date, lat/long in multiple formats, grid reference, depths, sampling method, soil description, physical properties, OC replicates and statistics)

- Data resource schema (Hammer_Core_KoT.csv)
  - Core: Core ID
  - Collection_date: Date of sample collection
  - Lat_dec_deg / Long_dec_deg: Latitude/Longitude in decimal degrees (WGS84)
  - Grid_Reference: OS National Grid reference (OSGB36)
  - X_easting / Y_northing: Planimetric coordinates
  - Depth_cm / Mid_Point_Depth_cm: Sample depths
  - Sampling_Method: Hammer Core
  - Simplified_Troels_Smith: Soil description
  - Water_Content_perc / Wet_Bulk_Density_g_cm_3 / Dry_Bulk_Density_g_cm_3 / Porosity: Physical measurements
  - OC_perc_Rep1 / OC_perc_Rep2 / OC_perc_Rep3: Replicate organic carbon contents
  - Mean_OC_perc / Std_Dev: Mean and standard deviation across OC replicates

- Reuse considerations and integration
  - Designed for standardised, QA’d environmental monitoring data
  - Emphasizes connection to broader datasets and literature to enhance value beyond single-use
  - Accessibility: underlying data and metadata enable independent verification and cross-dataset analyses

- References and related materials
  - Related data and methods cited, including foundational works (Athy 1930; Dadey et al. 1992; Verardo et al. 1990; Nieuwenhuize et al. 1994; Kennedy et al. 2005) and the 2020 Geoderma article on best practices for blue carbon stock estimation
  - Full reference list available in the documentation

- Contact and provenance
  - Responsible researchers and institutions: University of St Andrews; University of Leeds; Scottish Association of Marine Science
  - Documentation linked to published methods and ongoing environmental monitoring programs