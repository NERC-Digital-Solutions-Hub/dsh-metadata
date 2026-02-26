# Long-term multisite Scots pine trial, Scotland: cone and seed phenotypes, 2024

## Overview
- A component of a long-term multisite provenance-progeny trial in Scotland (Scottish Borders; 55.6036, -2.8930).
- Seeds (2007) from eight mother trees for each of 21 native Scots pine populations, spanning the species range and seed zones.
- Saplings planted in 2012; trial site established with a complete randomized block structure (4 blocks; 8 rows per block).
- Purpose: monitor phenotypic variation in cone and seed traits across populations and time, enabling cross-site/environmental health assessments.

## Trial design and location
- Site: one site of a multisite trial, established using seeds collected in 2007 and grown/planted in the field in 2012.
- Families: trees from 168 families (21 populations x 8 mother trees); full replication with four replicates per family.
- Layout: complete randomized block design; four blocks of eight rows; trees spaced 3 x 3 m; guard rows to mitigate edge effects.
- Sampled material: cones collected from the southern-facing half of each tree; field measurements conducted in 2024.

## Data collected and measurements
- Cone abundance: counted all visible cones on the southern-facing half of each tree (late February 2024).
- Cone sampling: five cones sampled per tree from previous-year whorl branches (preferentially southern-facing; if fewer than five, sampled from elsewhere on the tree); samples taken from different branches up to 3 m height.
- Storage: cones stored at 4°C at the UK Centre for Ecology & Hydrology in Penicuik.
- Traits measured (May–July 2024):
  - Cone traits: Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number, Cone_ratio (cone width/length), Cone_Angle, Profile (1 flat to 4 very raised), Openness (cone openness after drying; 1–4).
  - Color: Hue, Value, Chroma (scored with Munsell charts; categories not always numeric).
  - Seed traits (measured for seven populations only due to time): Seed_number, Filled_seed_number, Seed_viability (Filled/Total seeds).
- Methods: measurements taken with digital calipers; color via Munsell charts; seed traits derived after drying cones.

## Dataset file and data fields
- Dataset file: Scots_pine_cone_data.csv
- Key fields (selected):
  - Order, Block, Id, Fam: identifiers for tree position and family.
  - Cone_number, Cone_id: cone-level identifiers.
  - Date: data collection date.
  - Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number, Cone_ratio, Cone_Angle: cone morphology metrics.
  - Hue, Value, Chroma: cone color metrics (Munsell-based).
  - Profile: scale flatness score (1–4).
  - Openness: cone openness score after drying (1–4; higher indicates more open).
  - Seed_number, Filled_seed_number, Seed_viability: seed metrics (seven populations).
- Notes on fields: 
  - Fam uses a two-letter population code plus mother tree number.
  - Units include millimeters for length measurements; numerical values for counts/ratios; NA for color channels where not applicable.

## Relevance for environmental monitoring
- Provides standardized, long-term phenotypic data across a structured, replicated design to monitor environmental responses and adaptive variation in Scots pine.
- Enables comparisons across populations and sites when integrated with climate, soil, and management data, supporting assessment of environmental health and policy performance over time.
- Data quality follows a clear QA/standardized measurement protocol; datasets are designed to be stored and accessible within monitoring portals.

## Data quality, accessibility and references
- Field QA, standardized measurement protocols, and careful sample handling (cool storage, consistent timing) to ensure data integrity.
- Data intended to be stored in appropriate data portals and made accessible for researchers and policymakers; designed to be integrable with other environmental datasets.
- Key reference: Beaton, Perry, Cottrell, Iason, Stockan, Cavers (2022). Phenotypic trait variation in a long-term multisite common garden experiment of Scots pine in Scotland. Scientific Data, 9, 671. DOI: 10.1038/s41597-022-01791-8.