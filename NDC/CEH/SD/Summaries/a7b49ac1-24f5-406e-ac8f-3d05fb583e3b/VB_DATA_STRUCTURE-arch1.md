# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Baseline (VB) Dataset

## Overview
- Purpose: Baseline vegetation dataset to understand environmental change; supports research and practical decision-making.
- Scope: Site-based vegetation data collected via a standardized grid and infill strategy for long-term monitoring; data are intended for map generation and detailed plot analyses.

## Data collection design
- Grid-based sampling: Approximately 400 sample positions aligned with the National Grid; up to 100 randomly located infill points to balance under-represented vegetation types.
- Plot setup: Each point has a 2 m × 2 m plot; plots oriented (N, E, S, W) and permanently marked if selected for continuous monitoring.
- Survey goals: One-off survey to generate vegetation maps and select plots for long-term monitoring (coarse-grain, fine-grain, and woodland vegetation surveys).
- Data quality: Analyze with accompanying quality information; quality metadata accompanies the dataset.

## Data structure and storage
- Core storage: Oracle database with 12 site-specific tables.
  - Core metadata tables: D1VB_xxx (site metadata) and D2VB_xxx (plots), where xxx is the site code.
  - Key fields: SITECODE, SYEAR, PLOTPID, PLOTTYPE (S = standard, W = woodland), FIELDNAME, VALUE, SDATE, FEATURES (e.g., Path, Wall, Stream, Hedge, etc.).
- Metadata and provenance: Core metadata documented separately; accompanying quality metadata included to aid proper use.
- Dictionaries and crosswalks: Species and features are coded with crosswalks linking numeric codes to Latin names and taxonomic concepts; dictionaries include mappings for features and thousands of species codes with synonyms and updated nomenclature.

## Sites and temporal coverage
- 12 sites with varying years, typically from early 1990s to late 1990s (e.g., Drayton 1993, Glensaugh 1994, Hillsborough 1994, Moor House 1993–1994, Rothamsted 1993, Snowdon 1995–2000, Cairngorms 1998–2000, etc.).
- Temporal scope supports cross-site comparisons and long-term trend analyses.

## Species and features coding
- Features codes: P (Path), W (Wall), S (Stream), H (Hedge), D (Ditch), F (Fence), B (Bank), N (Natural boundary), X (No feature).
- Species codes: Extensive crosswalks map numeric species codes to Latin names and related concepts; includes numerous synonyms and taxonomic mappings (examples include Salix species, Sambucus nigra, Sanguisorba, Saxifraga, Salix viminalis, etc.).
- Practical impact: Analysts must use the crosswalks to translate FIELDNAME and VALUE observations into species identities and interpret ecosystem composition accurately.

## Quality codes and metadata
- Standard ECN quality codes (examples):
  - 100 No information available
  - 101 No sample/reading taken
  - 102 Sample lost or discarded
  - 103 Partial loss of sample
  - 104 Sample frozen
  - 105–191 various in-field and laboratory issues (e.g., debris, weather, sampling disturbances)
  - 200–239 various operational or measurement issues (e.g., adverse weather, misidentifications, confidence levels)
  - 501–508 laboratory or processing problems
  - 999 Unusual event (with accompanying text in quality metadata)
- Use: Quality metadata should be consulted prior to analysis, especially when combining data across sites or years.

## Data access, usage, and outputs
- Availability: Data co-located with the ECN Data Centre and Environmental Information Platform; continuous-monitoring results accessible through these portals.
- Provenance and reuse: Data sources tracked; datasets can be made discoverable with metadata; documentation included to aid correct analysis and interpretation.
- Publication and citation: Acknowledgement requested for data use; one reprint of any publication citing the data should be provided.

## Practical notes for analysts
- Data integration: Harmonize across multiple site tables; ensure consistent plot identifiers, plot types, and sampling year alignment.
- Scale and density: Site-level data with grid and infill; local-scale analyses should account for sampling density and potential biases.
- Data quality: Always review accompanying quality metadata before cross-site or cross-year analyses.
- Administrative boundaries: Be aware that some datasets may lack detailed boundary information; cross-check against site metadata.

## Challenges and considerations (analysts’ perspective)
- Data availability at the right scale or local levels can be limited.
- Data stored in journals, reports, or disparate local authority sources can hinder access.
- Datasets may be known only within specific circles; comprehensive discovery requires cross-referencing dictionaries and metadata.
- Unifying data from multiple sources/formats requires careful standardization and domain expert sense checks.
- IT barriers (permissions, old software, computational demands) can impede analysis, especially for large datasets.
- Translating findings into impact and ensuring effective dissemination can be challenging, particularly for academic users.
- Data may lack detailed administrative boundary information for some analyses.

## Publication and citation guidance
- Acknowledge ECN data use in publications.
- Provide one reprint of any publication citing the dataset.