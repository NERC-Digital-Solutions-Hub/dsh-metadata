# Plant cover in a Floridian foredune following hurricane Irma: effect of experimental wrack removal

- Overview
  - Dataset records plant cover by species in a Floridian foredune following Hurricane Irma, assessing the effect of experimental wrack removal.
  - Study site: Anastasia State Park, coastal foredune near St. Augustine, Florida; site experienced hurricane Irma in October 2017 with storm wrack deposition.
  - Sampling framework: five experimental blocks, each containing three 10 x 10 m plots assigned to control, procedural control, or wrack removal treatments.
  - Time points: data collected immediately after setup (March 2018) and subsequently in August 2018, October 2018, and January 2019.

- Experimental design and procedures
  - Treatments per block: 
    - Control — undisturbed
    - Procedural control — wrack removed and replaced
    - Removal — wrack removed without replacement
  - Plot structure: nine 0.5 x 0.5 m quadrats per plot for surveying plant cover.
  - Observation timing: four survey rounds spanning March 2018 to January 2019.

- Data collected
  - Primary variables: 
    - Plant percentage cover by species
    - Total plant cover per quadrat
  - Observational methods: visual estimation of species cover within each quadrat; total cover is the sum of all species covers in a quadrat.
  - Spatial and temporal identifiers: 
    - block, plot (within block), plot_id, quadrat_number
    - sampling_period (month and year)
    - treatment_type for each plot
  - Species format: cover data provided for Uniola paniculata and 19 additional species (reported as separate columns).

- Data structure and documentation
  - Data formats: Excel and CSV
  - Dataset field descriptions include header descriptions and a description field for context (e.g., sampling_period, plot_id, block, plot, treatment_type, quadrat_number, plant_cover, uniola_paniculata, etc.).
  - Figures referenced for site/location context:
    - Fig. 1A: Google Earth image showing replication layout
    - Fig. 1B: schematic of plots and data collection points

- Data quality and governance
  - Quality checks: distributions of variables screened for unusual values; cross-checked against field notebooks.
  - Custodianship: staff responsible for the dataset are Matthew Joyce and John Griffin.
  - Location details provided to support discoverability and reuse, with explicit site description and context of hurricane Irma impacts.

- Relevance for reuse and stewardship considerations
  - Provides a time-series dataset of species- and plot-level plant cover under different wrack-management treatments, useful for habitat recovery, plant community dynamics, and coastal resilience studies.
  - Clear documentation of experimental design and observation methodology aids reproducibility and data interoperability.
  - Metadata completeness supports discovery and understanding of methods, units (percent cover), and structure across multiple survey waves.

- Notes for future data governance
  - Consider adding or confirming an official metadata standard (variables, units, and taxonomic references) to enhance interoperability across datasets.
  - If ongoing updates or additional time points are planned, establish a clear update protocol and versioning.
  - Ensure a public data dictionary and readme accompany the CSV/Excel files to facilitiate reuse by data users and other stewards.