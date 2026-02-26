# Supporting documentation for data resource Scotland_SM_Surficial.csv

- Overview: Document detailing the Scotland_SM_Surficial.csv data resource, part of the Carbon Storage in Intertidal Environments (C-SIDE) project, including data collection (2018-2020), variables, methods, quality control, and references.

## Project and funding
- Project: Carbon Storage in Intertidal Environments (C-SIDE).
- Funding: NERC (NE/R010846/1).
- Staff Responsible: William Austin.
- Research Team: Multiple collaborators from University of St Andrews, University of Glasgow/Bangor University, Bangor University, and the Scottish Association of Marine Science, plus C-SIDE Citizen Science Team.

## Data resource name and description
- Data resource name: Dry bulk density, loss on ignition and organic carbon content of surficial soils from Scottish salt marshes, 2018-2020.
- Description: 471 surficial soil samples (top 10 cm) from 46 Scottish salt marshes, measuring:
  - Dry bulk density (g cm-3)
  - Loss on ignition (LOI, %)
  - Organic carbon content (% by weight, via elemental analysis)

## Geographic scope and locations
- Region: Scotland (excluding Outer Hebrides and Shetland).
- Coordinates: Site locations provided in decimal degrees (WGS84), with OSGB grid references and easting/northing equivalents.
- Site selection: Chosen to represent contrasting habitats across Scotland (sediment types, vegetation, sea-level history).

## Monitoring and sampling framework
- Sampling period: January 2018 – December 2019.
- Part of: Scottish portion of the C-SIDE sampling program and the CarbonQuest Citizen Science program.
- Repeat sampling: Not planned.

## Variables and parameters observed
- Soil texture (Sandy / Not-Sandy)
- Dry bulk density (g cm-3)
- Organic matter content via LOI (% wt.)
- Organic carbon content (% wt.) via Elemental Analysis
- Location identifiers: Saltmarsh_Name, Lat_dec_deg, Long_dec_deg, Year, X_easting, Y_northing
- Grid and location data: Grid_Reference Location (OS National Grid)
- Sampling and data fields: Sampling_Method, Depth_cm
- Data format indicators: File formats used, with details on accompanying fields

## Sampling methods and laboratory procedures
- Field sampling tools: 50 ml syringe (modified) or 30 mm gouge corer to 10 cm depth.
- GPS: Recorded via various methods (mobile devices, handheld units, RTK).
- Sample handling: Frozen at -20°C until analysis.
- Soil texture classification: Based on Ford et al. (2019) methodology and expert judgment.
- Dry bulk density: Dried at 60°C for 72 hours; density calculated from dry mass and initial volume.
- LOI: Dried, milled to powder, combusted at 450°C for 4 hours; LOI represents organic matter content.
- Organic carbon: 10 mg milled samples analyzed with Elemental Analyzer (Vario EL Cube) after acidification to remove carbonates (HCl 10%).
- Calibration: Elemental analyzer calibrated with Acetanilide; repeated analysis of standard organic soil (B2178) across runs.

## Data quality control and checks
- Citizen Science samples QC: Visual checks by experienced salt marsh scientists before drying.
- Spatial validation: GPS coordinates cross-checked against habitat maps and aerial imagery to confirm saltmarsh origin.
- Team-based validation: Four team members conducted Grid_Reference Location assessments (OS grid).
- Data fields and format checks: Consistency across Lat/Long, X/Y coordinates, texture classifications, and metadata fields.
- Handling of missing data: Explicit notes on NA for certain measurements where material was insufficient (OC_Perc, LOI_Perc).

## Data structure, formats, and reference framework
- Data structure: Includes Saltmarsh_Name, Year, Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Depth_cm, Dry_Bulk_Density_g_cm_3, OC_Perc, LOI_Perc, Soil_Texture, Sampling_Method, and related header fields.
- File formats: CSV data format used for the resource; accompanying descriptions for headers and formats are provided.
- References and calibration standards:
  - Craft et al. 1991 (LOI and Kjeldahl for OC/N)
  - Dadey et al. 1992 (dry-bulk density)
  - Ford et al. 2019 (salt-marsh carbon stock predictions)
  - Kennedy et al. 2005; Nieuwenhuize et al. 1994; Verardo et al. 1990 (calibration and analytical methodologies)

## Additional notes
- Site-level data and sampling details emphasize representativeness across habitat types and careful QA of field and laboratory procedures.
- The dataset is designed to enable self-service analysis and comparison across Scottish salt marsh sites, with robust documentation of methods and QC processes.