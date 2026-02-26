# Supporting documentation for data resource Hammer_Cores_KoT.csv

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Staff Responsible: Craig Smeaton
- Research Team: 
  - Craig Smeaton (University of St Andrews)
  - Luis Rees-Hughes (University of Leeds)
  - Natasha L.M. Barlow (University of Leeds)
  - William E.N. Austin (University of St Andrews/Scottish Association of Marine Science)

## Data resource description
- Name: Sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh (Hammer cores)
- Scope: 39 soil samples from 4 hammer cores
- Location: Kyle of Tongue, Scotland
- Observations: Bulk density (wet and dry), water content, porosity, organic carbon content
- Coordinates and framing: Site coordinates provided; observed in decimal degrees (WGS84), British National Grid, and easting/northing
- Sampling: No repeat sampling planned
- Variables (observed): Water Content (%), Wet Bulk Density (g cm^-3), Dry Bulk Density (g cm^-3), Porosity (Φ)
- Data references: Linked to Smeaton et al. (2020) Geoderma; foundational references for methods include Athy (1930), Dadey et al. (1992), Kennedy et al. (2005), Nieuwenhuize et al. (1994), Tröels-Smith (1955)

## Methods and procedures
- Core collection:
  - Core tubes: 150 cm length, 6.16 cm inner diameter, 0.24 cm wall
  - Insertion: Driven to 100 cm depth; top sealed to create vacuum; extracted with tractor jack
  - Handling: Cores split lengthways into working and archive sections
- Sampling and description:
  - 4 cm^3 fixed-volume samples collected at 10 cm intervals
  - Soils described using Troels-Smith classification (simplified to dominant class)
  - GPS locations recorded (DGPS)
- Physical properties:
  - Wet bulk density determined by weighing samples
  - Dry bulk density after drying at 60°C for 72 hours
  - Water content calculated from wet/dry masses; porosity derived from water content and densities
- Organic carbon content:
  - 10 mg milled samples acidified with 10% HCl to remove carbonates
  - Dried and analyzed with Elemental Analyzer (Carlo Erba NA-1500/ Vario EL Cube protocol) following Verardo et al. and Nieuwenhuize et al.
  - Three replicates per sample; calibration with Acetanilide
  - Repeated analysis of medium organic soil standard (B2178) for accuracy
- Quality control:
  - Troels-Smith soil descriptions independently performed by two team members; combined result reported
  - Replication for OC analyses to ensure accuracy

## Data formats and metadata
- Primary data format: CSV
- Data resource description (Hammer_Core_KoT.csv) provides column definitions:
  - Core, Collection_date, Lat_dec_deg, Long_dec_deg, Grid_Reference
  - X_easting, Y_northing, Depth_cm, Mid_Point_Depth_cm
  - Sampling_Method, Simplified_Troels_Smith
  - Water_Content_perc, Wet_Bulk_Density_g_cm_3, Dry_Bulk_Density_g_cm_3, Porosity
  - OC_perc_Rep1, OC_perc_Rep2, OC_perc_Rep3, Mean_OC_perc, Std_Dev
- Data lineage and provenance:
  - Linked publication: Smeaton, C., Barlow, N. L., & Austin, W. E. (2020). Coring and compaction: Best practice in blue carbon stock and burial estimations. Geoderma, 364, 114180
  - Related methodology references provided (Athy 1930; Dadey et al. 1992; Kennedy et al. 2005; Nieuwenhuize et al. 1994; Tröels-Smith 1955)

## Data quality and governance considerations
- Data verification:
  - Independent cross-check of Troels-Smith classifications
  - Replicate measurements for OC content to ensure analytical accuracy
- Metadata completeness and usability:
  - Comprehensive field and laboratory metadata included (locations, depths, sampling method, descriptions, and replicates)
  - Challenges noted in broader monitoring contexts include metadata gaps, data standardization, and the need for clear data governance to enable sharing
- Accessibility and sharing:
  - Public sharing of datasets can be a barrier; the document references data openness and governance considerations relevant to monitoring frameworks
- Reproducibility:
  - Detailed procedural descriptions for core collection, sampling, and analyses support reproducibility and comparability with other monitoring efforts

## Notes for monitoring framework design
- This resource provides a vetted example of end-to-end data collection, processing, and QA for soil carbon and physical properties in a coastal environment
- Contains explicit replication and calibration steps essential for robust trend detection and uncertainty assessment
- Demonstrates integration of field measurements with laboratory analyses and standardized soil descriptions (Troels-Smith), which is valuable for cross-site comparability
- Highlights the importance of documenting data lineage, methods, and QC procedures to support transparent governance and data sharing in monitoring programs