# Supporting documentation for data resource Scotland_SM_Surficial.csv

- A data resource detailing dry bulk density, loss on ignition (LOI), and organic carbon content for surficial soils from Scottish salt marshes (top 10 cm), collected 2018-2020 as part of the Carbon Storage in Intertidal Environments (C-SIDE) project.

## Project and funding
- Funding: NERC (NE/R010846/1).
- Staff Responsible: William Austin.
- Research team includes researchers from University of St Andrews, University of Glasgow, Bangor University, and the Scottish Association of Marine Science, plus a C-SIDE Citizen Science Team.

## Data resource name and description
- Name: Scotland_SM_Surficial.csv (surficial soil data resource).
- Description: 471 surficial soil samples (top 10 cm) from 46 Scottish salt marshes; measurements include dry bulk density, LOI (organic matter content), and organic carbon content.

## Location and scope
- Geography: Scotland (excluding Outer Hebrides and Shetland).
- Site coordinates provided in multiple formats: decimal degrees (WGS84), OSGB36 Easting/Northing.
- Site locations presented to represent contrasting habitats (sediment types, vegetation, sea level history).
- Sampling period: January 2018 – December 2019 (Scottish portion of C-SIDE and the CarbonQuest Citizen Science program).
- Number of sites: 46 salt marshes.
- Number of samples: 471.

## Sampling, variables, and depth
- Depth of samples: top 10 cm.
- Variables observed:
  - Soil Texture (Sandy / Not-Sandy)
  - Dry bulk density (g cm^-3)
  - Organic matter content (% LOI)
  - Organic carbon content (% C, measured by elemental analysis)
- Sampling methods:
  - 50 ml syringe (modified) or 30 mm gouge corer to 10 cm depth.
  - GPS locations recorded; samples frozen at -20°C until analysis.
  - Soil texture classified using Ford et al. (2019) methodology; expert judgement also used.

## Analytical procedures and calibration
- Dry bulk density: dried at 60°C for 72 hours; calculated from dry mass and original sample volume.
- LOI: dried samples milled to powder; combusted at 450°C for 4 hours; mass loss indicates organic matter content.
- Organic carbon: 10 mg milled samples analyzed with Elemental Analyzer (Elementar Vario EL Cube) after acidification with 10% HCl to remove carbonates.
- Calibration: elemental analyzer calibrated with Acetanilide; repeated analysis of medium organic soil standard (B2178).

## Data quality control and provenance
- Citizen Science samples underwent quality control: visual inspection by salt marsh scientists prior to drying.
- GPS coordinates checked against habitat maps and aerial imagery to ensure samples originate from salt marshes.
- Data checks include multiple team members verifying grid references (Ordnance Survey National Grid) and coordinate accuracy (Lat/Lon in decimal degrees; X_Easting and Y_Northing in OSGB36).
- Documentation includes multiple fields to capture data provenance, classifications, and units; explicit note of potential NA values where data are missing.

## Data formats and field structure
- File format: CSV (Scotland_SM_Surficial.csv).
- Key fields (examples): Saltmarsh_Name, Lat_dec_deg, Long_dec_deg, Grid_Reference, X_easting, Y_northing, Sampling_Method, Depth_cm, Dry_Bulk_Density_g_cm_3, OC_Perc, LOI_Perc, Soil_Texture.
- Data descriptions and header descriptions provided in the resource documentation, including field formats and repeated QC notes.

## References
- Foundational methodological sources for LOI, dry bulk density, and organic carbon analyses:
  - Craft et al. 1991; Dadey et al. 1992; Ford et al. 2019; Kennedy et al. 2005; Nieuwenhuize et al. 1994; Verardo et al. 1990.

## Monitoring and future data
- No repeat sampling is planned within this documentation; the data reflect the specified sampling period (2018-2019 Scottish portion) and protocols.