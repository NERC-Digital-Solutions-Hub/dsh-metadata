# Long-term multisite Scots pine trial, Scotland: cone and seed phenotypes, 2024

## Overview
- A data report from a long-term multisite provenance-progeny trial in the Scottish Borders, focusing on cone and seed phenotypes measured in 2024.
- Seeds were collected in 2007 from 21 Scots pine populations (covering Scotland’s range and seed zones) and grown as saplings before planting in 2012.
- The dataset captures phenotypic traits from one site of the trial in 2024, with a complete randomized block design.

## Trial design and provenance
- Populations: 21 native Scots pine populations sourced to cover the full species range; three populations from each of seven seed zones.
- Family structure: saplings from seeds collected from eight mother trees per population, treated as half-sibling families.
- Plot design: complete randomized block structure with four blocks; four replicates per family; 3 m spacing with a guard row to minimize edge effects.
- Population and family totals: 672 trees from 168 families (four replicates per family in each block).

## Data collection and sampling (2024)
- Cone abundance: counted on the southern-facing half of each tree in late February 2024.
- Cone sampling: five cones per tree sampled from previous-year whorl branches; sampling prioritized the southern-facing half but used other parts of the tree if fewer than five cones were available.
- Cone handling: cones stored at 4°C in a refrigerated facility.
- Measurements window: cone and seed traits measured between May and July 2024.

## Traits measured and processing
- Cone traits (measured on all cones):
  - Cone_length (mm), Cone_width (mm)
  - Stalk_length (mm)
  - Scale_length (mm), Scale_width (mm), Scale_number
  - Cone_ratio (cone width / cone length)
  - Cone_Angle (degrees)
  - Hue, Value, Chroma (color scoring via Munsell charts) 
  - Profile (scale flatness): 1 (flat) to 4 (very raised)
  - Openness (post-drying): 1 (closed) to 4 (very open)
- Seed traits (measured on seven populations due to time constraints):
  - Seed_number
  - Filled_seed_number
  - Seed_viability (Filled_seed_number / Seed_number)
- Processing: cones dried at 35°C; seeds extracted after drying; measurements involved digital calipers for size metrics and Munsell charts for color.

## Dataset contents
- File: Scots_pine_cone_data.csv
- Key fields include:
  - Block, Id (tree ID), Fam (family code), Cone_number, Cone_id
  - Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number
  - Cone_ratio, Cone_Angle, Hue, Value, Chroma, Profile, Openness
  - Seed_number, Filled_seed_number, Seed_viability
  - Date (data collection date), Order (tree order in trial)
- Units:
  - Length/width measurements in millimeters (mm)
  - Scale_number, Cone_number, Seed_number as numeric counts
  - Cone_ratio as numeric ratio; Cone_Angle as numeric
  - Color fields (Hue, Value, Chroma) treated as categorical/NA where applicable
- Data provenance: linked to Beaton et al. 2022 Sci Data for phenotypic trait variation in this long-term experiment.

## Data quality, metadata, and provenance considerations
- Metadata coverage: includes block, family, tree, cone identifiers and measurement contexts; some color fields are NA where not applicable.
- Quality assurance: standardized measurement procedures (calipers, Munsell charts) and controlled drying conditions; data organized in a single consolidated CSV.
- Gaps and limitations: seed-trait data available for only seven populations due to time constraints; potential limitations in extending seed-trait comparisons across all populations.
- Provenance: dataset derived from a well-documented long-term provenance-progeny trial with explicit sampling and measurement protocols; published context provided via Beaton et al. 2022.

## Access, sharing, and governance considerations
- Dataset format: CSV, single file, suitable for ingestion into monitoring dashboards or analyses.
- Location and stewardship: measurements stored and managed via the UK Centre for Ecology & Hydrology as part of the trial’s data management workflow.
- Implications for monitoring frameworks:
  - The study exemplifies a structured, replicated field design with clear trait definitions suitable for policy-relevant environmental health monitoring.
  - Highlights the importance of complete metadata, standardized measurement protocols, and accessible data formats to support transparency and reuse.
  - Demonstrates data governance considerations such as data sharing readiness, metadata completeness, and the need to address data gaps (e.g., limited seed-trait coverage) in monitoring plans.
  - Underlines potential barriers noted in monitoring frameworks contexts: data gaps, data access timeliness, silos across organizations, reliance on public sharing of datasets, and metadata adequacy for verifying suitability of data for policy decisions.