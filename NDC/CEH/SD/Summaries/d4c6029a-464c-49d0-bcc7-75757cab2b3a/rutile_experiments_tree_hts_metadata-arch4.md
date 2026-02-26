# Materials and methods for the dataset: Growth of five species of trees on experimental plots on sand tailings left after mining for rutile in Sierra Leone

- Overview
  - Study investigates growth of five tree species on sand tailings resulting from rutile mining in Sierra Leone.
  - Primary data: tree height after 2.5 years (June 2007 – November 2009) across eight rehabilitation plots, with additional soil, heavy metals, and biodiversity measurements collected in 2009.
  - Contextful data include site description, experimental design, planting and surface treatments, and data collection/quality procedures.

- Site and environmental context
  - Location: Lanti South, near SRL rutile concession in Sierra Leone; proximity to active dredge ponds and mangrove forest.
  - Substrate: coarse quartz sand tailings with very low nitrogen (~0.0027%) and carbon (~0.073%), high rainfall (~3 m/yr), limited natural regeneration.
  - Plot layout: eight plots (1–8), each 4 compartments of 25 m x 25 m; square plots (1–4) and rectangular plots (5–8).
  - Climate and hydrology: tropical wet climate with heavy rainfall in August; drainage toward ponds; some seasonally flooded depressions.
  - History: mining since 1970s; restoration activities limited; plots planted in June 2007; some weed issues from locally produced compost.

- Experimental design
  - Species planted (one per row per compartment): Gmelina arborea, Mangifera indica (mango), Anacardium occidentale (cashew), Citrus sinensis (sweet orange), Anisophyllea laurina (monkey apple).
  - Planting arrangement: five rows per compartment, 5 m x 5 m spacing; same planting treatment applied within a compartment.
  - Planting treatments (per tree): 17 liters of compost, 17 liters of topsoil, 17 liters of 50:50 compost/topsoil mix, or control (no additive).
  - Surface treatments (applied to all compartments in a plot): ~2 cm compost, ~2 cm topsoil, ~5 cm mulch (from mattress grass), or nothing.
  - Plot and compartment structure: eight plots, each with four compartments; trees planted with standardized hole dimensions and spacing; some taxa started as seedlings in bags, others as wildings.

- Data collection and scope
  - Primary measurement: height of each tree in centimeters (id 1–800 across eight plots x four compartments x five species, with position data).
  - Additional measurements: invertebrates, birds, ground flora; soil carbon and nitrogen measured in January 2009; heavy metals and additional soil metrics measured in 2009.
  - Timing: growth measured over at least two field visits per year; initial soil samples collected before planting (June 2007) and again in January 2009.
  - Documentation: field data recorded on paper, transcribed to Excel, then double-punched for QA.

- Data file and metadata
  - Data file: rutile_experiements_tree_hts.csv (42 KB; 8 columns; 801 rows; 800 trees recorded; height is the final variable of interest in this dataset).
  - Key variables (with descriptions):
    - id: unique tree identifier (1–800).
    - Plot: plot number (1–8).
    - Planting: planting treatment in hole (compost, topsoil, ts_and_c, or control).
    - Surface: surface treatment applied to plot (topsoil_surf, compost_surf, mulch_surf, nothing_surf).
    - position: position along the row (1–5).
    - Species: tree species (Mangifera, Gmelina, Anisophyllea, Anacardium, Citrus).
    - Height: tree height in centimeters (0 indicates dead or missing).
  - Data types and units are specified; header row includes variable names; descriptive metadata is provided in associated documentation (e.g., Tables 1 and 3 for variables and values).

- Data quality assurance and governance
  - QA processes: two-person teams (measurer and recorder); measurements checked for accuracy and completeness; attempts to verify correct plot and treatment assignments against maps.
  - Measurement notes: height measured from ground to apex; tall trees posed measurement challenges; some signage and plot markers were lost or relocated.
  - Data integrity: no missing data for the id/Plot/Planting/Surface/position/Species columns; zero height used to denote dead/missing trees; cross-checks performed between field maps and plot locations.

- Considerations for data users (opportunities and limitations)
  - Opportunities: analyze growth response to different planting and surface treatments; compare across five species; integrate height data with soil chemistry and biodiversity observations for holistic rehabilitation assessments.
  - Limitations: variability in citrus variety; weed encroachment from local compost; limited maintenance/record of irrigation events; data focuses on height over a 2.5-year window with supplementary soil and biodiversity data available separately.