# Physical_geochemical_properties_wide_cores_essex.csv

## Overview
- Data resource describing physical and geochemical properties of saltmarsh soils from 19 wide-diameter gouge cores across 8 Essex, UK sites, collected in 2019.
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project funded by NERC (NE/R010846/1).

## Data provenance and project context
- Project focus: carbon storage in intertidal environments; dataset supports characterisation of saltmarsh soil properties.
- Data resource ID and details summarize the sampled material, locations, and laboratory analyses performed.

## Location and extent
- Location: Essex, United Kingdom.
- Geographic extent provided as four corner coordinates and also as X (Easting) and Y (Northing) values (WGS84).
- Sites chosen to represent different origins of saltmarsh (natural, historic breach, managed realignment).

## Variables and data structure
- Core-level identifiers: Core_ID; Saltmarsh; Marsh_type (Natural, Managed Realignment, Historic Breach).
- Spatial identifiers: Lat_dec_deg; Long_dec_deg; X_easting; Y_northing.
- Elevation: Elevation_above_OD__m (meters).
- Depth and sampling: Sample_depth_cm; Mid_Point_depth_cm.
- Substrate and density: Substrate (Troels-Smith classification); Dry_bulk_density_g_cm_3.
- Chemistry: OC_perc (organic carbon content %).
- Data structure descriptors: Header; Cell Format (definitions of description and data types).

## Sampling and methods
- Sampling: 19 cores from 8 sites using a 60 mm gouge corer; cores sectioned into 1 cm intervals (n = 1952 sub-samples).
- Location recording: DGPS used to record sample sites.
- Sample handling: cores frozen at -20°C until analysis.
- Core descriptions: assigned using Troels-Smith (1955) scheme.
- Lab processing: drying at 60°C for 72 hours; bulk density calculated from pre/post-drying weights.
- Carbon quantification: samples milled to powder; 50 mg analyzed with Elementar Soli TOC using a temperature-gradient method (DIN 19539) for OC; calibration with CaCO3 and standard soils (B2290); isotopic QA via repeat analyses of high OC standard (B2151).
- QA: laboratory equipment calibrated per University of St Andrews practices.
- Statistical treatment: not reported (NA) in this description.

## Data quality and governance
- Documentation of calibration procedures and QA measures (laboratory standards, isotopic QA).
- Metadata includes detailed file structure and parameter definitions to support reproducibility and auditability.

## Data sharing and updating
- File format: .csv, with accompanying data resource description detailing descriptions and cell formats, enabling straightforward sharing and portal ingestion.
- Metadata framework implies readiness for uploading to data portals and catalogues; structured headers and descriptions facilitate data discovery and reuse.

## Standards and references
- Troels-Smith (1955) sediment classification used for core descriptions.
- DIN 19539 (2015/08) for TOC/ROC/TIC analyses and solids differentiation.
- Calibration and QA references: Dadey et al. (1992) on dry bulk density; Natali et al. (2020); Smeaton et al. (2021) for soil carbon contexts.

## Considerations for Data Stewards
- Ensure metadata completeness and consistency across fields (descriptions, units, formats) to support interoperability.
- Maintain stable Core_ID and site identifiers to preserve provenance across updates.
- Preserve coordinate reference system (WGS84) and ensure Lat/Long and X/Y values remain synchronized.
- Document future updates or additions (new cores/sites) to maintain a consistent data provenance trail.
- Ensure access controls and publication of QA notes accompany data releases, given measurements of OC and isotopic values.