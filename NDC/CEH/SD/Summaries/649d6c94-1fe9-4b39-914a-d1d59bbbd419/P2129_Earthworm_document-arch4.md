# Earthworm data from Sourhope field experiment site, Scotland, 1999 and 2001 [NERC Soil Biodiversity Programme] H.O. Bishop, I. C. Grieve, J. A. Chudek, & D. W. Hopkins

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (started 1999) studying soil biodiversity at Sourhope, Scotland.
- Focus of this document: earthworm data collected in 1999 and 2001 as part of broader soil biodiversity research (24 projects).
- Data represent baseline and endpoint earthworm surveys from limed and unlimed plots on a controlled field experiment site.

## Site description
- Location: Sourhope Research Station, Scottish Borders; upland grassland on Brown Forest Soils derived from glacial till.
- Site features: north-facing slope, 300–320 m above sea level, 30 plots (20 m x 12 m) in five blocks with six treatments.
- Treatments: Control and Limed (liming with 6 t CaCO3 ha^-1 annually from 1999–2002); grazing excluded since 1998; grass mown monthly May–Sep with cuttings removed.

## Earthworm census and data collection
- Method: Intact soil blocks (42 cm x 30 cm x 25 cm) were hand-sorted to extract earthworms from five limed and five control plots.
- Processing: Specimens refrigerated to void guts, blotted dry, killed in 40% ethanol, identified to species level using Sims & Gerard (1985) taxonomy.
- Data scope: Abundances include adults and juveniles; juveniles unable to be speciated are excluded.

## Data structure and access
- Data sets: 1011 (Baseline) and 1012 (Endpoint) earthworm survey data.
- Data file: P2129_ALL_SURVEY.csv (Baseline and endpoint surveys for Control and Lime plots at Sourhope).
- Key columns:
  - SUID: Unique Sampling Unit Identifier (block/main-plot/sub-plot/cell, with date and sampling unit details).
  - SAMPLING_DATE: Date of sampling.
  - BLOCK: Block number (1–5).
  - MAIN_PLOT: Main plot identifier (A–F).
  - SUB_PLOT: Sub-plot identifier.
  - CELL_X, CELL_Y: Cell grid coordinates.
  - TREATMENT: C = Control, L = Limed.
  - SPECIES: Earthworm species (per Gerard & Sims 1985).
  - ABUNDANCE: Total abundance per m^2 (adults + juveniles).
  - TYPE: Baseline or endpoint.
- Data provenance: Linked to Scott et al. 2003 Sourhope Field Data Handbook; supports data context and comparability with other Sourhope datasets.

## Data quality and governance
- Quality control: Numeric range checks, formatting checks, and logical integrity assessments implemented.
- Limitations and liability: Despite QA procedures, data accuracy is not guaranteed; NERC disclaims liability for data accuracy or suitability for any use.
- Accessibility: Described as available as Supporting Information via the EIDC catalogue record (contextual data availability alongside related publications).

## References and further reading
- Key publications and sources for methods, context, and related analyses, including:
  - Bishop et al. 2008 on liming effects on earthworm communities.
  - Scott et al. 2003 Sourhope Field Data Handbook.
  - Usher et al. 2006 on UK Soil Biodiversity Programme.
  - Sims & Gerard 1985 earthworm identification keys.

## Implications for data leaders (data system, governance and reuse)
- Data system considerations:
  - Clear linkage between sampling units (SUID) and hierarchical plot structure (block, main plot, sub-plot, cell) enhances traceability and reuse.
  - Baseline vs endpoint distinction is explicit (TYPE field), enabling robust temporal analyses.
  - Data provenance is well-documented via associated handbooks and project codes.
- Metadata and discoverability:
  - Rich contextual metadata embedded in the dataset (sampling dates, treatments, location, soil type, methods) supports discovery and reuse across studies.
  - Reference to established taxonomic keys and related publications improves interpretability.
- Data quality and governance:
  - QA steps described, with explicit liability statements from the data provider (NERC), highlighting the need for users to assess fitness for purpose.
  - Availability through an institutional information catalog (EIDC) suggests a structured approach to data access and potential for cross-dataset linking.
- Practical recommendations for data leadership:
  - Maintain and publish comprehensive metadata, including site description, treatment regime, sampling design, and data processing steps.
  - Preserve unique identifiers (SUID) and hierarchical plotting information to support reproducibility and cross-study comparisons.
  - Document data lineage and provide accession paths to related datasets and publications to facilitate integrated analyses.
  - Include clear data-use licensing and disclaimers to manage expectations about accuracy and applicability.