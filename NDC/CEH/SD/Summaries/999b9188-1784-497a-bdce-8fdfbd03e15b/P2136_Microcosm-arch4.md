# Soil bacterial cell counts and moisture content from a water stress experiment [NERC Soil Biodiversity Programme] -Supporting Information

## Overview and aims
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) aiming to understand both soil biota diversity and the functional roles of soil organisms in key ecological processes.
- Focused on soil bacteria responses to drying and rewetting, using intact soil monoliths from Sourhope field site to monitor activity and diversity under perturbation.
- Data capture includes two main facets: bacterial cell counts (culturable and total via flow cytometry) and soil moisture content over a controlled drying/rewetting experiment.

## Experimental design and setting
- Location: Sourhope (Macaulay/JHI farm, Scottish Borders, grid NT8545019630). Soil: organic rich brown forest soil, pH 4.5–5.0.
- Microcosms: nine grassland monoliths (approx. 15 cm depth; 45 cm diameter) arranged as three replicates across three treatments.
- Treatments (July–October 2001; 11 sampling times S1–S11):
  - A: continual wetting
  - B: drying
  - C: drying followed by rewetting
- Sampling schedule: weekly intervals with natural rainfall initially (S1–S3), then imposed drought (S4 onward) with a rewetting event (S6) and continued treatment.
- Procedure details: monoliths transported to lab, pore water drainage controlled, standardised plant material removed, and moisture levels monitored to maintain specified conditions per treatment.

## Data collected and measurement methods
- Bacterial data (culturable counts):
  - Sample processing: soil dispersed in PBS, diluted, and plated on TSBA, 1/10-strength TSBA, and PSA with cycloheximide.
  - Incubation: 10 days at 18°C; colonies counted for culturability.
  - Biomass recovery: biomass from plates collected for nucleic acid analysis and stored for downstream processing.
  - Total bacterial cells: isolated from soil via Nycodenz density gradient, fixed in paraformaldehyde, stained with SYBR Green II, and enumerated by flow cytometry.
- Moisture data:
  - Soil moisture measured by oven-drying at 105°C for 24 hours.
- Data structure:
  - Two CSV files:
    - P2136_Culturable_cells.csv: microcosm ID, treatment, sampling date, media used (psa, tsba, 1/10 tsba), cell count (per g dry weight).
    - P2136_Microcosm_Soil_Moisture.csv: microcosm ID, treatment, sampling date, moisture content (%).
- Data lineage and references:
  - Related methodological publications: Whiteley et al. 2003; Griffiths et al. 2003.
  - Additional context: Sourhope Field Data Handbook (2003); Understanding soil biodiversity programs (Usher et al. 2006).
  
## Data quality, governance, and usage notes
- Quality assurance: data subject to QA procedures; no warranty on accuracy or fitness for a specific use.
- Liability disclaimer: NERC not liable for losses or damages arising from data use.
- Metadata and discoverability: data described with explicit field definitions, units, data types, and sampling dates to support reuse and cross-study analyses.
- Potential for integration: data structured to facilitate cross-comparison with other soil biodiversity datasets and related ecological studies from the Sourhope site.

## Implications for data strategy and leadership
- Demonstrates clear data assets with defined schemas, enabling discoverability and reuse by policy or research teams.
- Highlights importance of meticulous metadata (field names, data types, units, sampling dates) for cross-project data integration.
- Illustrates end-to-end data capture—from field sampling through laboratory analyses to structured data outputs—relevant to coordinating data across networks and ensuring consistent data quality.
- Emphasizes explicit disclaimers and data governance to manage expectations and risk when sharing ecological datasets.