# The number and individual weight of bumblebees (Bombus terrestris audax) from nests containing neonicotinoids in Wester Ross, UK

- Overall purpose: Document the experimental design, sampling regime, collection methods, and data structure for a dataset on bumblebee mass from nests in field-exposed pesticide treatments in Wester Ross, Scotland.

- Experimental context
  - Bumblebees housed in setups with multiple nests per box and two Tripol units per treatment, spaced to limit cross-treatment effects.
  - Field site in Wester Ross, Highlands, Scotland: sheltered grassland/wilderness habitat with substantially lower pesticide use than intensively farmed regions.
  - Treatments delivered via sugar syrup containing pesticides; after exposure, bees forage freely and are not forced to consume treated syrup.

- Treatments and experimental design
  - Two separate experiments conducted at the same site with different pesticide combinations.
  - Experiment 1: untreated, chlorpyrifos (150 nM), and chlorpyrifos (150 nM) with imidacloprid (10 nM).
  - Experiment 2: untreated, imidacloprid (10 nM) with chlorpyrifos (150 nM), plus imidacloprid (10 nM).
  - Colony exposure durations: 28 days (Experiment 1) and 43 days (Experiment 2) depending on access to the site.
  - Final-day procedures: gate restrictions to permit entry only, followed by lab assessment after a short post-foraging interval.

- Data collected in the study
  - Colony-level observations at end of trial: mass increase, total live bees, average bee mass, healthy brood cells on nest surface, overall nest condition.
  - Individual bee data: masses recorded at the end (preparation/collection process includes CO2 anesthesia and rapid processing).
  - Pesticide exposure details: specific treatment group per colony.

- Data structure and files
  - Two CSV files:
    - Neonicotinoidsonbumblebees_Experiment1.csv
    - Neonicotinoidsonbumblebees_Experiment2.csv
  - Columns: Colony number; treatment.
  - Rows: Bee mass values in milligrams (mg), ordered from heaviest to lightest (mass-ordered list for each colony).
  - Data quality control: weights verified by two-person cross-check; recorders blinded to treatment to reduce bias.

- Spatial and GIS-related considerations
  - Site-level context provided (Wester Ross field site) but the CSV files themselves do not include explicit geographic coordinates.
  - Potential GIS use: integrate colony IDs and treatments with spatial metadata or site maps to visualize spatial distribution of treatments, colony outcomes, and mass distributions.
  - For map-based analyses, linking these data to spatial coordinates or shapefiles of nests or field plots would enable spatial visualization of treatment effects and bee mass distributions.

- Limitations and notes
  - The dataset focuses on mass data for individual bees; other colony metrics are described but not necessarily embedded in the two CSV files.
  - pollen provisioning was not provided, and bees foraged in the field, which may influence mass outcomes.
  - Environmental pesticide exposure is contextualized as relatively low in the Highlands, which is relevant when interpreting results.