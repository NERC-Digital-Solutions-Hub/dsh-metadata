# Long-term multisite Scots pine trial, Scotland: cone and seed phenotypes, 2024

## Overview
- Data from one site of a long-term multisite provenance-progeny trial in the Scottish Borders (lat 55.603625, lon -2.893025).
- Seeds collected in 2007 from eight mother trees per population across 21 native Scots pine populations, spanning three seed zones (seven seed zones total represented).
- Trial design: complete randomized block with four blocks, 3 m x 3 m spacing, 672 trees from 168 families (4 replicates per family).
- In Feb 2024, cone abundance was counted on the southern-facing half of each tree; five cones per tree sampled from previous-year whorl branches for trait measurement.
- Cone and seed traits measured May–July 2024; seeds measured in seven populations due to time constraints.
- Data stored in a single CSV file: Scots_pine_cone_data.csv.

## Data structure and fields
- File: Scots_pine_cone_data.csv
- Key tree-level fields:
  - Order: numerical order of trees in the trial
  - Block: randomized block code
  - Id: tree identification code
  - Fam: family code (two-letter population code + mother tree number)
- Cone-level fields:
  - Cone_number: number of cones on the southern side of the tree
  - Cone_id: cone identifier
  - Cone_length, Cone_width: cone dimensions (mm)
  - Stalk_length: stalk length from attachment to cone (mm)
  - Scale_length, Scale_width: single scale dimensions (mm)
  - Scale_number: total scales per cone
  - Cone_ratio: cone width / cone length
  - Cone_Angle: angle from stalk to tip
  - Profile: scale flatness (1 flat, 2 slightly raised, 3 raised, 4 very raised)
  - Openness: cone openness after drying (1–4)
- Color and quality fields:
  - Hue, Value, Chroma: color scored using Munsell charts (Hue/Chroma/Value may be NA)
- Seed-level fields (for seven populations):
  - Seed_number: total seeds per cone
  - Filled_seed_number: filled seeds per cone
  - Seed_viability: filled seeds / total seeds
- Date: data collection dates
- Notes: data include measurements taken from cones stored at 4°C in the UK Centre for Ecology & Hydrology (Penicuik)

## Spatial context
- Site location provided; trial layout includes:
  - Four blocks in a randomized arrangement
  - Each tree spaced 3 x 3 meters with a guard row
- Data do not include per-tree GPS coordinates; tree positions are defined by Order, Block, and Id within the trial layout.
- Potential GIS use:
  - Visualizing trait variation across blocks and families within the site
  - Linking tree-level data to population/seed-zone provenance
  - Integrating with environmental or site-condition layers (if available)

## Temporal coverage
- Cone abundance measured in February 2024
- Cone and seed trait measurements conducted May–July 2024
- Cones dried at 35°C prior to seed measurement
- Storage details: 4°C at UKCEH Penicuik

## Methods and data collection
- Sampling:
  - Cone counts from the southern-facing half of each tree; five cones sampled per tree when possible
  - Sampling from different branches at varying heights up to 3 m
- Measurements:
  - Cone traits: length, width, stalk length, scale length/width, scale number, cone ratio, cone angle, color (Munsell Hue/Value/Chroma), profile, openness
  - Seed traits: total seeds per cone, number of filled seeds, seed viability
- Processing:
  - Cones dried before seed extraction
- Provenance and trial design:
  - Seeds from 21 populations, 8 mother trees per population (total 168 families)
  - Four replicates per family in a randomized block design

## Data quality, provenance, and scope
- Data come from a peer-reviewed provenance-progeny trial; referenced Beaton et al. 2022 Sci Data for trait variation context.
- Dataset consists of a single CSV file with clearly described fields and units; some color-related fields may be NA.
- Seven populations include seed measurements; cone measurements cover all populations.
- Site-specific data; multi-site comparisons would require integration with additional site data from the full trial.

## GIS-focused usage and analyses
- Map-ready aspects:
  - Tree-level data linked by Order, Block, Id within the site layout; can be plotted to approximate tree positions if block/layout mapping is supplied.
  - Population and family grouping (Fam) enables choropleth or symbol-based visuals by origin.
- Potential analyses:
  - Spatial patterns of cone traits across the trial block structure
  - Variation of cone/seed phenotypes by population, seed zone, or family
  - Correlations between physical cone traits and seed metrics (seed viability, filled seed numbers)
  - Integration with environmental layers to explore habitat or provenance effects
- Data preparation tips:
  - If exact tree coordinates are needed, obtain block layout coordinates from the trial documentation or Beaton 2022 Sci Data dataset to reconstruct positions
  - Derive additional metrics (e.g., averages per tree, per family, or per population) for mapping
  - Handle NA values in color metrics appropriately during visualization

## References
- Beaton, J., Perry, A., Cottrell, J., Iason, G., Stockan, J., Cavers, S. 2022. Phenotypic trait variation in a long-term multisite common garden experiment of Scots pine in Scotland. Sci Data. 9, 671. https://doi.org/10.1038/s41597-022-01791-8