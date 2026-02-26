# Physical_geochemical_properties_wide_cores_essex.csv

## Overview
- Dataset arising from the Carbon Storage in Intertidal Environments (C-SIDE) project funded by NERC.
- Describes physical and geochemical properties of saltmarsh soils from 19 wide-diameter gouge cores across 8 Essex, UK sites.
- Collected in 2019 to enable cross-site comparisons of saltmarsh carbon stocks and related soil properties.
- Sites represent different marsh origins: natural, historic breach, and managed realignment.

## Data content and scope
- Variables observed or simulated include:
  - Core_ID, Saltmarsh (site name), Marsh_type (Natural, Historic Breach, Managed Realignment)
  - Location: Lat_dec_deg, Long_dec_deg (WGS84), X_easting, Y_northing, Elevation_above_OD__m
  - Depth-related: Sample_depth_cm, Mid_Point_depth_cm
  - Substrate (Troels-Smith classification), Dry_bulk_density_g_cm_3, OC_perc (organic carbon content, % wt)
- Data derived from 19 cores cut into 1 cm sections (n = 1952 observations across all cores).

## Location and sampling details
- Geographic focus: Essex coast, United Kingdom.
- Sampling method: 60 mm gouge corer; cores described using Troels-Smith scheme; sections prepared for analysis.
- Core locations recorded with DGPS; samples frozen at -20°C prior to analysis.

## Data formats and structure
- Primary data file: Physical_geochemical_properties_wide_cores_essex.csv
- Data resource descriptions indicate two sections: Description and Cell Format, outlining each column’s name and data type (e.g., Lat_dec_deg as Number, Substrate as Text).
- Columns include:
  - Core_ID (Text), Saltmarsh (Text), Marsh_type (Text)
  - Lat_dec_deg (Number), Long_dec_deg (Number), X_easting (Number), Y_northing (Number)
  - Elevation_above_OD__m (Number)
  - Sample_depth_cm (Number), Mid_Point_depth_cm (Number)
  - Substrate (Text)
  - Dry_bulk_density_g_cm_3 (Number)
  - OC_perc (Number)

## Methods and quality control
- Sampling and descriptions:
  - 19 cores collected from 8 Essex sites; cores cut into 1 cm sections (n = 1952).
  - Core descriptions follow Troels-Smith classification (1955).
- Laboratory analysis:
  - Samples dried at 60°C for 72 hours; bulk density calculated from weight changes.
  - Organic carbon quantified by Elementar Soli TOC using temperature gradient method (DIN 19539) with calibration standards (CaCO3, silty soil TOC/ROC/TIC standards).
- Quality assurance:
  - Isotopic values validated through repeat analyses of high OC sediment standard (B2151) with reference C/N values.
  - Laboratory equipment calibrated per standard practices; data checks performed.
- Data handling:
  - NA handling noted as "NA" where applicable in the data resource descriptions.

## Data resource structure and metadata
- Each variable is described with header and cell format in the accompanying data resource description.
- Descriptions cover units, formats (Text vs Number), and the meaning of each field (e.g., Lat_dec_deg, Long_dec_deg use WGS84; Elevation above ordnance datum in meters).

## Provenance, references, and context
- Project and data provenance:
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funding: NERC (NE/R010846/1)
- Key references for methods and context:
  - Troels-Smith (1955) sediment classification
  - Dadey et al. (1992) Dry-bulk density methods
  - DIN 19539 (2015) TOC fractionation methodology
  - Natali et al. (2020); Smeaton et al. (2021) supporting TOC methodology and marine carbon stocks

## Potential data products and usage
- Enable self-serve exploration of soil physical and geochemical properties by marsh type and depth.
- Cross-site comparisons of organic carbon content and bulk density in Essex saltmarshes.
- Support carbon stock estimation and modeling in intertidal environments.
- Foundation for further data products and visualizations (e.g., depth profiles, substrate distribution, spatial mapping).

## Practical considerations and limitations
- Data gaps indicated by NA fields in metadata; depth-specific measurements limited to the 1 cm segment scheme.
- Spatial coverage limited to eight sites within Essex; applicability to other regions may require caution.
- Temporal scope limited to 2019 sampling; calibration and QA procedures are well-documented to support reproducibility.