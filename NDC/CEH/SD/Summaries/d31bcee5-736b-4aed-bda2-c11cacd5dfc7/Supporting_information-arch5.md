# Biodiversity value of native reforestation sites in the Scottish Highlands

## Overview
- Study scope: plant species cover, carabid beetle species counts (2018) and bird species counts (2019) across fourteen native reforestation sites in Glen Affric and Glen Moriston, Scottish Highlands.
- Purpose: assess biodiversity value of reforestation sites relative to unforested and mature Caledonian pineforest habitats; evaluate effects of grazing exclusion (deer) on forest regeneration and biodiversity.
- Context: sites established 1990–2012; fencing to exclude grazing; planting from local seed sources; landscape includes mature pineforest, plantations, heathland, and regenerating forest.

## Study design and site details
- Experimental design: hierarchical, with treatments representing forest status (reforestation, unforested, mature forest) and grazing status (grazed, ungrazed). Reforestation × grazed combination not present due to deer pressure. Five mature-forest plots (grazed and ungrazed) included to reflect target habitat.
- Plot structure:
  - Plants and carabid beetles: 10 × 10 m plots.
  - Birds: 50 m radius plots.
  - Each treatment combination sampled across plots; bird surveys conducted at a subset of reforestation sites.
- Site specifics:
  - Central Scottish Highlands; fenced to exclude deer; mature forest present at several sites.
  - Reforestation sites replanted with native Caledonian Pineforest species; some areas with Alnus glutinosa and Salix spp. in wetter zones.
  - Geographic coordinates and site metadata captured for each site; year of establishment and planting method recorded.

## Data collection methods and timing
- Plant surveys:
  - Dates: 22 June – 5 July 2018.
  - Method: three randomly placed 1 × 1 m quadrats per plot; species recorded (DOMIN scale for cover); full plot survey for additional species; vascular plants to species level; some non-vascular plants identified to genus/morphospecies.
- Carabid beetle surveys:
  - Dates: 7 June – 18 August 2018.
  - Method: six pitfall traps per plot (two traps per quadrat location); traps filled with propylene glycol/water; sampling intervals of two weeks; specimens identified to species; voucher specimens deposited (Oxford University Museum of Natural History, ENT-OUMNH-2021-001).
- Bird surveys:
  - Dates: two surveys per plot in May–June 2019 (with one period spanning 23 May–1 June and the second 5–14 June); conducted 6:00–11:30 with two surveyors; 15 minutes per survey.
  - Method: visual and vocal identifications; weather conditions recorded.
  - Note: one mature ungrazed plot (site 15) had no survey in the first period due to logistics; other plots had two surveys.
- Data governance context:
  - Data collection roles documented (Appendix 1): experimental design, data collection, and background information by named authors.
  - Data and voucher integration: specimens archived; data linked to site IDs, plot types, and years.

## Data structure and storage
- Data products (CSV files) and key fields:
  - plant_carabid_plot_locations.csv: plot-level locations and metadata (site, plot type, year, grid reference, pitfall dates, etc.).
  - bird_plot_locations.csv: plot locations for bird surveys plus weather notes per survey.
  - plants.csv: species-level plant data per quadrat per plot, with DOMIN percent cover, presence of other species, seedling frequency.
  - carabids.csv: per-plot, per-trap time, species, and individual frequencies.
  - birds.csv: individual bird records per plot per survey, including date, time, species, how recorded, and distance from plot center.
- Metadata and standards:
  - File-level metadata explains study design, plot classifications (Forest_status and Grazing_status), and date ranges.
  - Taxonomic references noted for consistency (binomial names; some taxa identified to genus or morphospecies when necessary).
  - Spatial referencing included via 10-figure grid references, site coordinates, and plot locations.
  - Data conforms to a consistent keying scheme (Site, Plot, Quadrats/Time/Species) to enable cross-dataset joins.
- Data quality notes:
  - Some missing data: two bird surveys not conducted for one plot; some mature forest data limited due to landscape constraints.
  - Taxonomic nuance: vegetation non-vascular groups and some mosses identified to genus/morphospecies; plant identifications prioritise species where possible.
  - Voucher specimens deposited for carabids; data provenance supported by cited methods and site history.

## Data provenance, limitations, and governance
- Provenance: study designed and executed by a team with defined roles; data collection aligned with published methodologies; field methods and plotting designs well documented.
- Limitations and considerations for reuse:
  - Temporal scope limited to 2018 (plants, carabids) and 2019 (birds); future work would require ongoing updates.
  - Some plots had incomplete bird data due to logistical constraints; not all mature forest plots are equally represented.
  - Taxonomic constraints and identification levels could affect cross-dataset interoperability; ensure consistent nomenclature across releases.
- Data stewardship implications:
  - The dataset is ready for deposit in standard biodiversity data portals with clear metadata and data dictionaries.
  - Documentation supports replication and secondary analyses, including comparisons across forest statuses and grazing treatments.
  - Appendix 1 provides a transparent record of roles, supporting accountability and data lineage.

## Practical guidance for data stewards
- Ensure data are stored with stable, versioned identifiers and a persistent DOI if possible.
- Maintain a comprehensive data dictionary and metadata that reflect:
  - Plot classifications (Forest_status, Grazing_status), site metadata, coordinates, dates, and methods.
  - Field definitions, units (e.g., DOMIN scale, distances in meters, times in HH:MM), and taxonomic conventions.
  - Schema for cross-linking across plants, carabids, and birds datasets via Site, Plot, and Time identifiers.
- Verify interoperability:
  - Align site IDs and plot IDs across all files; confirm the matching between reforestation, unforested, and mature forest datasets.
  - Harmonize taxonomic names and reference sources; document any taxa identified to genus or morphospecies.
- Quality assurance and updates:
  - Implement routine checks for missing data and irregular survey periods; document any deviations or logistical constraints.
  - Plan for incremental updates to incorporate new survey years and additional sites or plots, with clear versioning.
- Access and sharing:
  - Prepare data packages with clear license terms, usage notes, and caveats (e.g., partial bird data due to logistic constraints).
  - Include links to related publications, dataset DOIs, and voucher records to facilitate traceability.
- User guidance:
  - Provide context on grazing exclusion and habitat status to support analyses comparing biodiversity across forest statuses.
  - Highlight measurement scales (DOMIN for plant cover, pitfall-trap frequencies for carabids, bird survey timing and observer methodology) to ensure proper interpretation.