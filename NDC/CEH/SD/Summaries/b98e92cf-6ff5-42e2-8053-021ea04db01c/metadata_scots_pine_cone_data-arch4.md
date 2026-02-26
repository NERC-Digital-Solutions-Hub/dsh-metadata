# Long-term multisite Scots pine trial, Scotland: cone and seed phenotypes, 2024

## Overview
- Data from one site of a long-term multisite provenance-progeny trial in the Scottish Borders.
- Seeds collected in 2007 from eight mother trees per population across 21 Scots pine populations (covering the species range in Scotland; three populations per seed zone).
- Saplings planted in 2012; trial uses a complete randomized block design with four blocks of eight rows; 672 trees from 168 families (four replicates per family).
- Cone abundance measured in Feb 2024; cone and seed traits measured between May–July 2024.
- Data intended to support understanding of phenotypic variation and data-system governance around complex, provenance-based trials.

## Dataset structure
- File: Scots_pine_cone_data.csv
- Columns capture hierarchical trial metadata and detailed phenotypic measurements, including:
  - Trial structure: Order, Block, Id (tree ID), Fam (family code)
  - Cone measurements: Cone_number, Cone_id, Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number, Cone_ratio, Cone_Angle
  - Color and texture: Hue, Value, Chroma, Profile (scale flatness)
  - Openness: Openness (cone openness after drying)
  - Seed measurements: Seed_number, Filled_seed_number, Seed_viability
  - Date fields: Date of data collection
- Coding and metadata conventions documented (e.g., family code derived from population code + mother tree; NA usage for unavailable fields).

## Sampling and measurements
- Cone abundance: counted on the southern-facing half of each tree; five cones sampled per tree from previous-year whorl branches where possible; if fewer than five cones, sampling from elsewhere on the tree; branches sampled up to ~3 m height.
- Cone processing: cones stored at 4°C at UK Centre for Ecology & Hydrology (Penicuik); dried at 35°C before seed extraction.
- Trait measurements (May–July 2024):
  - Cones: length, width, stalk length, scale length, scale width, number of scales, cone ratio (width/length), cone angle, colour scores (Munsell-based: Hue, Value, Chroma), profile (1–4).
  - Seeds: count of seeds per cone, number of filled seeds, seed viability (filled seeds/total seeds).
- Seed trait data coverage: measured for seven populations (one from each seed zone) due to time constraints.

## Data collection timeline and provenance
- Seed origin: 2007, eight mother trees per population (21 populations total).
- Planting and experimental layout: germination/growth in 2007; saplings planted in 2012; trial maintained with randomized blocks.
- Measurements: cone counts Feb 2024; phenotypic trait measurements May–July 2024.
- Location coordinates provided for the site in the Scottish Borders.

## Data quality, metadata, and accessibility
- Dataset provides a detailed schema with explicit units (e.g., mm for measurements; ratios; 1–4 scales for profiles and openness) and descriptive labels.
- Contains a mix of measured data and categorical scores (e.g., color and scale profiles) with clear documentation of scoring methods (Munsell charts for color; 1–4 scales for profile and openness).
- Data hosted with explicit provenance to Beaton et al. 2022 Sci Data as context for the long-term experiment.
- Limitations include partial seed trait coverage (seven populations) and potential gaps where cones were scarce or sampling constrained.

## Data governance and reuse considerations for Data Leaders
- The dataset exemplifies a well-documented, single-CSV data product with rich metadata and a clear lineage, suitable for governance around data discoverability and reuse within a broader data system.
- Potential uses include cross-population phenotypic analyses, family-level (provenance) trait variation studies, and integration into multi-site analyses for a system-wide view of data quality, standards, and interoperability.
- Considerations for future data products:
  - Expand seed trait measurements to all populations or provide a documented plan for when data will be completed.
  - Maintain consistent measurement protocols across sites to enable direct cross-site comparisons.
  - Ensure ongoing metadata updates (e.g., updates to measurement methods or units) to support long-term data stewardship.

## References
- Beaton, J., Perry, A., Cottrell, J., Iason, G., Stockan, J., Cavers, S. 2022. Phenotypic trait variation in a long-term multisite common garden experiment of Scots pine in Scotland. Sci Data. 9, 671. https://doi.org/10.1038/s41597-022-01791-8