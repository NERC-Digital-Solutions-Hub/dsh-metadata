# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil organic matter content from three soil depths on saltmarsh sites at Morecambe Bay and Essex

## Overview
- Dataset describing soil organic matter (SOM) content from three soil depths (0–10 cm, 10–20 cm, 20–30 cm) assessed by Loss-on-Ignition (LOI) using bulk density samples.
- Part of the CBESS program; staff responsible: Hilary Ford.
- Time frame: Winter and Summer 2013; Essex winter samples include an additional sampling window (2–6 March 2013).

## Data scope and content
- Locations and sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitats: Mudflat (MF) and Saltmarsh (SM)
- Sampling details:
  - Quadrats numbered 1–22 per site
  - Spatial scales coded A–D (A = 1 m, B = 1–10 m, C = 10–100 m, D = 100 m and up)
- Primary variable: Soil organic matter (%) at three depth intervals
  - OM_10-20 and OM_20-30 fields described; documentation indicates depth mapping ambiguities (0–10 cm, 10–20 cm, 20–30 cm) within field descriptions
- Data file format: Excel workbook
- Data completeness: “NA” cells indicate no data

## Methods and provenance
- Sample collection and analysis:
  - LOI applied to bulk density samples to determine SOM
  - Bulk density rings used (3.1 cm high, 7.5 cm diameter)
  - Depths quantified: 0–10 cm, 10–20 cm, 20–30 cm
  - Samples dried at 105°C for 72 hours; sub-samples dried at 375°C for 16 hours
- Operational details:
  - Essex winter samples collected within 2–6 March 2013, in addition to general winter/summer 2013 campaign
  - Staff and site selection reflect contrasting soil types (clay in Essex vs. sandy in Morecambe Bay) and differing inundation, creek structure, and vegetation
- Metadata notes:
  - Calibration procedures, data checks, and quality-control procedures are not documented in the provided extract

## Spatial and temporal coverage
- Geographic coordinates provided for each site (Essex and Morecambe Bay)
- Temporal coverage includes Winter and Summer 2013, with an additional Essex winter sampling window (early March 2013)

## Data structure and field descriptions
- Dataset fields include:
  - Row Number (sorting index)
  - Season (Winter W or Summer S)
  - Location (Morecambe M or Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (MF or SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100 m and up)
  - OM_10-20: SOM percentage corresponding to a depth interval (documentation notes potential depth-mapping inconsistency with respect to 0–10 cm vs 10–20 cm)
  - OM_20-30: SOM percentage corresponding to a depth interval (likely 20–30 cm; documentation indicates possible depth-mapping ambiguity)
- Documentation gaps:
  - Calibration procedures, data checking, and quality-control procedures are not specified in the extract
- Data format note:
  - NA cells indicate missing data

## Quality, standards, and reuse considerations
- Strengths for data leadership:
  - Clear linkage of SOM to specific sites, habitats, and sampling depths
  - Structured field descriptors and site coordinates facilitate cross-site comparisons
  - Explicit sampling periods and grazing/land-use context aid interpretation
- Considerations and potential gaps:
  - Inconsistencies in depth labeling (0–10, 10–20, 20–30 cm vs. OM_10-20 and OM_20-30 fields) require clarification for consistent analysis
  - Absence of documented calibration, QA/QC, and metadata standards may affect data reliability assessments
  - Some fields (calibration, QC) are not described in the provided extract; additional metadata needed for robust data governance
- Potential reuse opportunities:
  - Cross-site comparisons of SOM across contrasting soil types and grazing regimes
  - Integration with other CBESS datasets to model coastal soil organic matter dynamics and ecosystem services
  - Longitudinal analyses if additional temporal data become available

## Key takeaways for data leaders
- This dataset provides SOM measurements across two coastal regions, three depths, and multiple saltmarsh sites, with contextual information on habitat, grazing, and site characteristics.
- Ensure clarification of depth mappings in OM_10-20 and OM_20-30 fields before cross-dataset integration.
- Assess data quality by requesting missing calibration and QA/QC procedures and by confirming metadata completeness.
- Leverage the explicit site, habitat, and spatial-scale coding to enable reproducible analyses and discoverability within the CBESS data ecosystem.