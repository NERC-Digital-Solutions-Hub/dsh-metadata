# Supporting documentation for data resource Scotland_SM_Surficial.csv

## Overview
- Data resource for dry bulk density, loss on ignition (LOI), and organic carbon content of surficial soils from Scottish salt marshes (top 10 cm), 2018–2020.
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project; includes Scottish portion of the C-SIDE program and the CarbonQuest citizen science component.
- Dataset comprises 471 soil samples from 46 salt marshes across Scotland (excluding Outer Hebrides and Shetland).

## Data Resource Details
- Data resource name: Scotland_SM_Surficial.csv
- Geographic coverage: Scotland (excluding Outer Hebrides and Shetland)
- Site metadata: Saltmarsh_Name; coordinates provided in multiple formats (decimal degrees WGS84, OSGB36 easting/northing)
- Sampling period: January 2018 – December 2019 (Scottish portion of C-SIDE and CarbonQuest)
- Sampling plan: No repeat sampling planned

## Variables and Measurements
- Soil_Texture: Sandy or Not-Sandy (based on Ford et al., 2019)
- Dry_Bulk_Density_g_cm_3: Dry bulk density
- LOI_Perc: Organic matter content (% wt.) determined via LOI
- OC_Perc: Organic carbon content (% wt.) measured by elemental analysis
- Depth_cm: Depth of soil sample (10 cm target)
- Other data fields include: grid references, X and Y coordinates (OSGB36), and sampling method details

## Methods and Procedures
- Sampling methods: 50 mL syringe used to collect samples or 30 mm gouge corer; top 10 cm subsampled for analysis
- Sample handling: GPS coordinates recorded; samples frozen at -20°C until analysis
- Soil texture determination: Classification into Sandy or Not-Sandy per Ford et al. (2019)
- Dry Bulk Density: Dried at 60°C for 72 hours; density calculated from dry mass and sample volume
- LOI: Dried and milled; combusted at 450°C for 4 hours; mass loss attributed to organic matter
- Organic Carbon: 10 mg milled samples acidified with 10% HCl to remove carbonate, dried, and analyzed with Elemental Analyzer (Elementar Vario EL Cube)
- Calibration/standards: Acetanilide used for elemental analyzer calibration; repeated analysis of standard (B2178) included
- Data quality checks: Citizen Science samples undergo QC by experienced salt marsh scientists; GPS coordinates cross-checked against habitat maps and aerial imagery; soil texture and grid references reviewed by team

## Data Formats and Access
- File format: CSV with detailed header descriptions
- Location data: Latitude/Longitude (WGS84) and Osgb36 coordinates (British National Grid) provided; multiple representations to support GIS use
- Documentation depth: Extensive metadata fields and descriptions accompany the dataset, including sampling_method, depth, coordinates, and quality checks

## Data Governance and Stewardship
- Project governance: Collaborative effort among multiple institutions and a citizen science team; data management practices align with project standards
- Metadata richness: Comprehensive metadata supports traceability, reproducibility, and reuse
- Data sharing: Core dataset is prepared with clear provenance and QC procedures to facilitate reuse in policy evaluation and monitoring frameworks

## Team and Collaboration
- Project leadership/staff: William E.N. Austin and a cross-institutional team
- Research partners: University of St Andrews, University of Glasgow, Bangor University, Scottish Association for Marine Science
- Citizen science involvement: C-SIDE Citizen Science Team and CarbonQuest participants

## References (related methods and calibration)
- Craft et al. (1991); Loss on ignition and Kjeldahl digestion calibrations
- Dadey et al. (1992); Dry-bulk density methods
- Ford et al. (2019); Large-scale predictions of salt-marsh carbon stock
- Kennedy et al. (2005); Effects of acidification on carbon analysis
- Nieuwenhuize et al. (1994); Rapid analysis of organic carbon and nitrogen
- Verardo et al. (1990); Determination of organic carbon and nitrogen in marine sediments using Carlo Erba NA-1500
- Additional methodological references as listed in the dataset documentation