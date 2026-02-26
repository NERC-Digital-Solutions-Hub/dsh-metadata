# GMEP_TOPSOIL_MESOFAUNA_2013_14.csv

- A dataset documenting counts of soil mesofauna collected under the Glastir Monitoring & Evaluation Programme (GMEP) for 2013–2014 across Wales.
- Part of a rolling 4-year survey designed to capture spatial and temporal changes in soil biodiversity and its drivers (land use, climate, pollution).

## Overview of purpose and context

- Aimed to monitor soil quality and mesofauna as indicators of ecosystem health, informing Glastir outcomes on climate, biodiversity, soil and water quality, and woodland expansion.
- Data complement broader GMEP objectives to quantify status and trends in soil ecosystems and to link changes to drivers beyond Glastir interventions.
- Sampling aligns with the Countryside Survey methodology to enable future integration and national estimates.

## Spatial design and sampling framework

- Rolling 4-year cycle with two components:
  - Wider Wales component for baseline estimation and national trends.
  - Targeted component focusing on Glastir priority areas.
- Common spatial unit: 1 km x 1 km squares.
- A total of 300 1 km squares sampled over the cycle; half randomly sampled within landscape strata and half targeted at Glastir priority areas.
- Exclusions: squares with >75% urban land or >90% sea excluded from sampling.
- Spatial distribution: map of 1 km survey squares across Wales plotted at 10 km resolution for confidentiality.
- Sampling frame draws on the Land Classification of Great Britain to ensure heterogeneity within strata and comparability with GB surveys.

## Sample collection and processing workflow

- In each 1 km square, 5 pre-determined randomly dispersed soil locations are sampled.
- Soil cores extracted with a white plastic core (F-core), 8 cm long, co-located with vegetation surveys, and sent to CEH laboratories for faunal extraction.
- Dry extraction using Tullgren funnels (6+ units per setup) over 5 days with a 40 W heat source and 70% ethanol in collection bottles.
- Recording of core metadata (SQXN, depth, start/stop times) and careful labeling for traceability.
- Post-extraction handling: storage of soil and fauna in labeled containers; subsequent transfer to labeled vials with SQXN on labels.

## Invertebrate identification and data capture

- Objective: separate mesofauna from debris and identify to broad taxonomic groups.
- Broad groups include: Acari (Oribatid Box mites, Oribatid Others, Mesostigmatid, Other mites), Collembola (Poduromorpha, Entomobryomorpha, Symphypleona/Neelipleona), and totals for mites and Collembola.
- Specimens sorted into glass blocks or vials with ethanol; counts tallied in a recording notebook.
- Data entry into Excel templates for integration into the CEH Bangor database.
- Quality control: duplicate identifications for 1 in 20 samples to ensure comparability; full QA checks conducted by a second staff member.

## Data management, QA, and integration

- Data managed with Excel recording and then integrated into the CEH Bangor database.
- Alignment with the DEFRA Joint Code of Practice for Research (JCoPR) for quality assurance.
- Ongoing data management and sample tracking coordinated by GMEP data management personnel and field teams.
- Data outputs include a CSV (GMEP_TOPSOIL_MESOFAUNA_2013_14.csv) with explicit column definitions and derived totals.

## Data schema and key outputs

- Columns cover: YEAR, SQ_ID, PLOT_TYPE, PLOTNUM, EASTING_10KM, NORTHING_10KM, LC (Land Classification), CORE_TAKEN, counts for broad groups (MITE_ORIB_BOX, MITE_ORIB_OTHER, MITE_MESO, MITE_OTHER, COL_POD, COL_ENTO, COL_SYMP, ENCHY, OTHERS), and derived totals:
  - MITE_ORIB_TOTAL (sum of Oribatid box and other)
  - TOTAL_MITES (sum of Poduroid, Entomobryoid, Symphypleona/Neelipleona)
  - TOTAL_COLL (sum of Poduroid, Entomobryoid, Symphypleona/Neelipleona)
  - TOTAL_MESO (mites + Collembola)
  - TOTAL_INVERT (TOTAL_MITES + TOTAL_COLL)
- Data describe counts per square, plot, and year, enabling national and sub-national analyses and integration with other GMEP and Countryside Survey datasets.

## Training, health & safety, and quality assurance

- Training: staff receives at least one week of training in broad-group identification, voucher specimen handling, and mock sample processing before routine work.
- Health & Safety: ethanol handling is treated as a health hazard; risk assessments per SOP are followed.
- QA: two-person cross-checks (1 in 20 samples in early phase) to ensure consistent identification and counting; subsequent reductions in frequency as the process stabilizes.

## Appendices: Roles, tasks, and field teams

- Appendix 1 lists roles and responsibilities, including:
  - Soil meso-fauna topic leader, data management, sample management, field coordination, and project management.
  - Field survey teams and field coordinators contributing to sample collection across Wales.
- Document reflects collaborative governance between field teams and research staff to ensure data quality and traceability.

## Relevance for GIS specialists

- Clear spatial framework: 1 km square sampling units with precise Easting/Northing coordinates and land classification metadata.
- Data designed for map-based visualization and analysis of spatial patterns (e.g., distribution of mesofauna across Wales, coverage of Wider Wales vs. Glastir priority areas).
- Map-ready outputs and confidentiality considerations (10 km plotting) to support policy briefings, client reports, or public-facing dashboards.
- Integration potential with Countryside Survey and broader GMEP datasets for multi-scale spatial analyses.