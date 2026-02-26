# Plant species cover and carabid beetle species counts (2018) and bird species counts 14 5 5 in ungrazed native reforestation areas and grazed/ungrazed unforested and mature forest areas in the Scottish Highlands 14 10 5

- Scope and purpose
  - Biodiversity assessment across reforestation, unforested grazed, unforested ungrazed, and mature Caledonian pineforest habitats in the Scottish Highlands.
  - Evaluates habitat value for plants, carabid beetles, and birds, with a focus on grazing exclusion and forest establishment as restoration targets.
  - Data collected to support understanding of how deer grazing and reforestation influence biodiversity recovery.

- Study design and sites
  - 14 fenced reforestation sites established 1990–2012, located in Glen Affric and Glen Moriston.
  - Treatments represented in all combinations of forest status (reforestation, unforested, mature) and grazing status (grazed, ungrazed), excluding reforestation × grazed due to deer pressure.
  - Matched plots: each reforestation plot has counterparts in nearest unforested grazed and unforested ungrazed areas; five grazed/ungrazed mature forest plots included.
  - Plots used for plants and carabids (10 × 10 m) and birds (50 m radius); bird plots spread to maintain separation from plant/carabid plots.

- Sampling and data collection
  - Plants: survey in 2018 using three random 1 × 1 m quadrats per plot; percent cover via the DOMIN scale; full plot species list recorded.
  - Carabid beetles: six pitfall traps per plot, sampled June–August 2018; traps emptied in 2–4 week intervals; species identified to binomial level; voucher specimens deposited.
  - Birds: two surveys per plot in May–June 2019, 15 minutes per survey, conducted by two observers; identifications by sight and song; weather noted.
  - Plot matching details: reforestation plots matched to nearestforested and grazed/ungrazed comparators; mature forest plots incorporated where present to represent target habitat.

- Data structure and contents
  - Location and plot metadata
    - plant_carabid_plot_locations.csv: plot IDs, site IDs, forest status, grazing status, dates of pitfall establishment/collection, grid references.
    - bird_plot_locations.csv: plot IDs, site IDs, forest status, grazing status, weather notes, grid references.
  - Species and counts
    - plants.csv: per-plot, per-quadrat plant species list with DOMIN cover values, date, and seedling frequency where applicable.
    - carabids.csv: per-plot, per-time point counts for carabid species (binomial names) with frequencies.
    - birds.csv: per-record bird sightings with date, site, plot, time, distance from plot center, how recorded, and species.
  - File-level notes
    - Timepoints correspond to 2018 for plants and carabids; 2019 for birds.
    - Locations cover Glen Affric and Glen Moriston in the central Scottish Highlands.
    - Taxonomy aligns with binomial names; non-vascular plants identified to genus or morphospecies; certain groups (e.g., mosses) recorded as morphospecies.
    - Data include a mix of plot-level summaries and individual observation records to enable self-service analyses.

- Data quality, provenance, and limitations
  - Data collected by multiple researchers; field methods standardized but with site-specific adaptations due to landscape and fencing.
  - Patchy data for some plots/times: no bird survey in certain mature plots or during some periods; weather notes accompany bird surveys.
  - Voucher specimens and references provided for identification standards.
  - Some plots are located in contiguous or nearby positions to allow cross-comparisons between habitat treatments while maintaining separation for surveys.

- How to use the data
  - Assess biodiversity responses to native reforestation versus unforested and mature forest habitats under different grazing pressures.
  - Analyze spatial patterns and feature associations for plants, carabid beetles, and birds across treatments.
  - Combine datasets to generate multi-taxa biodiversity indicators, perform habitat restoration evaluations, and support policy or management decisions for upland woodland restoration.
  - Use the hierarchical and matched-design structure to control for site- and habitat-level confounders in analyses.

- References and context
  - Study contextualizes upland Scotland forest dynamics, deer herbivory impacts, and Caledonian Pineforest restoration priorities.
  - Data and methods align with standard vegetation and beetle survey protocols; voucher specimens deposited for reference.