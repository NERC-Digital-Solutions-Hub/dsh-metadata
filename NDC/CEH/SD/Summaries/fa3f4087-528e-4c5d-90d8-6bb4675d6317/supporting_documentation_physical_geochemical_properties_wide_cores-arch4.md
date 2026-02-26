# Data resource description for Physical_geochemical_properties_wide_cores_essex.csv

## Overview
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project; funded by NERC (NE/R010846/1).
- Describes physical and geochemical properties of saltmarsh soils from 19 wide-diameter gouge cores across 8 Essex sites with different origins (natural, historic breach, managed realignment).

## Dataset scope and content
- Observations cover physical and geochemical measurements from saltmarsh cores.
- Key variables include:
  - Core_ID, Saltmarsh, Marsh_type (Natural, Managed Realignment, Historic Breach)
  - Lat_dec_deg, Long_dec_deg (WGS84)
  - X_easting, Y_northing (map/grid coordinates)
  - Elevation_above_OD_m (meters)
  - Sample_depth_cm, Mid_Point_depth_cm (depth measurements)
  - Substrate (Troels-Smith classification)
  - Dry_bulk_density_g_cm3
  - OC_perc (Organic Carbon content, %)
- Locations represent Essex coastline sites chosen to compare different marsh origins; data allow cross-site comparability.

## Methods and observations
- Sampling: 19 wide-diameter gouge cores (60 mm diameter) from 8 sites; cores described per Troels-Smith (1955).
- Sub-sampling: Cores cut into 1 cm intervals (n = 1952 subsamples).
- Location and storage: DGPS recorded site locations; samples frozen at -20°C until analysis.
- Laboratory procedures:
  - Drying: 60°C for 72 hours to determine bulk density.
  - Carbon quantification: Elementar Soli TOC analyzed via temperature gradient method (DIN 19539; Natali et al. 2020; Smeaton et al. 2021).
  - Calibration and QA: Calibrations with CaCO3 and TOC/ROC/TIC standards; isotopic values quality controlled through repeat analysis of high OC standards; laboratory equipment calibrated per University of St Andrews practices.

## Data format and metadata
- File format: CSV (Physical_geochemical_properties_wide_cores_essex.csv).
- Metadata structure includes:
  - Core_ID, Saltmarsh, Marsh_type
  - Lat_dec_deg, Long_dec_deg
  - X_easting, Y_northing
  - Elevation_above_OD_m
  - Sample_depth_cm, Mid_Point_depth_cm
  - Substrate
  - Dry_bulk_density_g_cm3
  - OC_perc
- Data resource description and header definitions accompany the dataset to aid discoverability and use.

## Provenance and references
- References informing methods and context:
  - Dadey, Janecek, Klaus (1992) on dry-bulk density
  - DIN 19539 (2015) on TOC/ROC/TIC methodology
  - Natali, Bianchini, Carlino (2020) on soil carbon pools
  - Smeaton et al. (2021a) on UK marine sedimentary carbon stocks
  - Troels-Smith (1955) on sediment classification

## Relevance for Data Leaders
- Demonstrates a well-documented, multi-site data resource with clear lineage, standardized metadata, and robust QA/QC practices.
- Supports data-system thinking through explicit data types, units, coordinate references, and data provenance, enabling discoverability, interoperability, and reuse across networks and partners.
- Provides a concrete example of comprehensive data description that helps identify data gaps, standardization needs, and opportunities for broader data integration within a data strategy.