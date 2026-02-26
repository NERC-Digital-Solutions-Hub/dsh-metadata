# Supporting documentation for data resource Eng_Wales_SM_Surficial.csv

## Overview
- Dataset covering dry bulk density, loss on ignition (LOI), and organic carbon content of surficial soils from English and Welsh saltmarshes (2019).
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project; supports monitoring and assessment of saltmarsh carbon stocks and related environmental health indicators.
- Data resource includes both field sampling and citizen science contributions, with detailed laboratory analyses and quality checks.

## Scope and sampling design
- Samples and sites: 212 surficial soil samples from 49 English and Welsh saltmarshes.
- Timeframe: January 2018 – December 2019; no repeat sampling planned.
- Location data: Observations with precise coordinates (Lat/Long in WGS84), plus British National Grid (OSGB 1936) and easting/northing formats.
- Site selection: Chosen to represent contrasting habitats across England and Wales (sediment types, vegetation, sea level history).

## Variables measured
- Soil Texture (Sandy / Not-Sandy / Organic)
- Dry Bulk Density (g cm-3)
- Organic Matter content (LOI, %)
- Organic Carbon content (OC_Perc, %)
- Depth of sampling: 10 cm (topsoil)

## Methods and procedures
- Sampling method: 50 ml syringe into soil to 10 cm depth; GPS locations recorded; samples frozen at -20°C until analysis.
- Texture classification: Based on Ford et al., 2019; four team members independently classified, with combined result used.
- Dry Bulk Density: Calculated from dried samples (60°C, 72 h) using sample mass and volume.
- LOI: Dried samples milled, combusted at 450°C for 4 h; mass loss used to estimate organic matter.
- Organic Carbon: Milled samples acidified to remove carbonates, then measured with an Elemental Analyzer (Carlo Erba/Verardo et al. methodologies).
- Calibration and QA: Elemental analyzer calibrated with Acetanilide; repeated analysis of a medium organic soil standard (B2178) across runs.
- Data quality checks: Citizen Science samples QC’d by Salt Marsh scientists; GPS coordinates cross-checked against habitat maps; texture classifications independently performed by four team members.

## Data format and metadata
- File format: .csv
- Data resource description fields include: Saltmarsh_Name, Nation, Year, Lat_dec_deg, Long_dec_deg, Grid_Reference, X_easting, Y_northing, Sampling_Method, Depth_cm, Dry_Bulk_Density_g_cm_3, Soil_Texture, OC_Perc, LOI_Perc.
- Metadata scope: Location, sampling, measurement methods, QC procedures, and references provided.

## Data governance and accessibility
- Public sharing and transparency emphasized through sharing underlying data and clear documentation of methods and quality checks.
- Data provenance and standards are addressed via detailed procedures, calibration practices, and independent quality assessments.
- Some potential barriers noted in the broader context (data access, metadata completeness, and data governance) are mitigated here by explicit QA steps and comprehensive variable definitions.