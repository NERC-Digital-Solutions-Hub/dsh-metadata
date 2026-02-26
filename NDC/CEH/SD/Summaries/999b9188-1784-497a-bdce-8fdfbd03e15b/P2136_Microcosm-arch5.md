# Soil bacterial cell counts and moisture content from a water stress experiment [NERC Soil Biodiversity Programme] -Supporting Information

## Overview
- Describes the NERC Soil Biodiversity Thematic Programme study focused on how soil bacterial communities respond to drying and rewetting in intact grassland monoliths from Sourhope, Scotland.
- Provides experimental design, sampling regime, and data structures for two datasets: (1) microcosm culturable bacterial cell counts across different media, and (2) soil moisture contents over time.
- Context includes broader aims to link soil biodiversity to ecosystem processes and nutrient cycling under water stress.

## Experimental design and sampling
- Location and material: intact grassland monoliths (~15 cm depth) from Sourhope field site; soil classified as organic-rich brown forest soil (pH 4.5–5.0).
- Microcosm setup: nine microcosms (three replicates × three treatments) placed in Oxford; treatments A (continual wetting), B (drying), C (drying and rewetting).
- Timeline: 3 months (July–October 2001) with 11 sampling events (S1–S11).
- Sampling protocol: four 1-cm-diameter cores per pot to ~7 cm depth; samples mixed, roots/materials removed; aliquots taken for analysis.
- Treatment schedule: initial natural rainfall and regular watering (S1–S3); rainfall excluded with UV covers starting 14 Aug; drying commenced after 20 Aug; rewetting on 18 Sep (S6), then continued wetting regimen.

## Data components (two CSV datasets)
- Drought experiment. Microcosm culturable cell counts (P2136_Culturable_cells.csv)
  - Fields: MICROCOSM_ID, TREATMENT, SAMPLING_DATE, MEDIA_USED, CELL_COUNT
  - Media: PSA, 1/10-strength TSBA, full-strength TSBA (all with cycloheximide)
  - Cell counts expressed per gram dry weight soil; data types include numeric, date, and text.
- Drought experiment. Microcosm moisture contents of soil samples (P2136_Microcosm_Soil_Moisture.csv)
  - Fields: MICROCOSM_ID, TREATMENT, SAMPLING_DATE, MOISTURE_CONTENT
  - Moisture content measured by oven-drying at 105°C for 24 hours; data types include numeric, date, and text.

## Methods and data processing
- Bacterial cultivability and total cell counts
  - Soil (0.5 g):

    - Dispersed in PBS with glass beads; serial dilutions plated on TSBA, 1/10-TSBA, and PSA with cycloheximide.
    - Incubated 10 days at 18°C; colonies counted; diverse biomass recovered from plates for nucleic acid work.
  - Total bacterial cells: density gradient separation (Nycodenz), fixation, SYBR Green II staining, and enumeration by flow cytometry.
- Moisture content
  - Soil moisture determined by oven-drying at 105°C for 24 hours.
- Data handling
  - Datasets supplied as two CSVs with structured fields and documented units; QA procedures applied, but no warranty on data fitness for a given use.
  
## Data governance, provenance, and access
- Source: NERC Soil Biodiversity Programme; Supporting Information accompanying primary publications.
- Accessibility: Provided as supporting information; noted availability via EIDC catalogue (SOURHOPE FIELD DATA HANDBOOK references and related materials).
- Quality and liability disclaimer: NERC states it cannot warrant accuracy or fitness for purpose; no liability for misuse or reliance on data.

## Metadata and documentation
- Dataset structure includes explicit descriptions of fields, data types, and units to support interoperability and reuse.
- Key identifiers: MICROCOSM_ID; temporal dimension via SAMPLING_DATE; treatment and media descriptors.
- Related literature and context: primary analyses and related studies cited (e.g., Whiteley et al., Griffiths et al. 2003; Usher et al. 2006) to aid interpretation and cross-referencing.

## Practical considerations for Data Stewards
- Ensure consistency of field naming, units, and dates across the two datasets for interoperability.
- Preserve experimental context (treatment definitions, sampling schedule, soil type, and site) to support reuse in meta-analyses.
- Maintain linkage to related supporting information and publications for provenance and methodological transparency.
- Note potential limitations in data completeness and the lack of warranty when integrating into larger datasets or repositories.