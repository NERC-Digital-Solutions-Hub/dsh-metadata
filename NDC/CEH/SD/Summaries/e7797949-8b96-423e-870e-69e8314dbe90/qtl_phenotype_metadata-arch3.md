# Experimental design/Sampling regime

- Purpose and scope
  - Investigates phenotype and elemental composition of threespined stickleback (Gasterosteus aculeatus) from a marine by freshwater cross, raised in a freshwater pond for 5+ generations.
  - Aims to support understanding of phenotypic and elemental variation across generations, with data collected in autumn 2022.

- Study design and sampling
  - Founders: one male freshwater fish and one female saltwater migratory fish collected in North Uist, Scottish Western Isles (spring 2016).
  - Rearing: offspring raised for ~2 months in freshwater aquaria at University of Nottingham; population established in a previously fishless pond in Nottinghamshire.
  - Generations: maintained in pond for ~5 generations (typical stickleback generation time ~1 year).
  - Sample: 388 individuals collected from the pond in autumn 2022; 419 photographs produced for 388 fish.
  - Ethics: fish euthanised with overdose of MS222 before measurements.

- Data collected and measurements
  - Photographs: 419 JPEG images of fish captured in aquaria.
  - Morphometrics: body length measured to nearest 0.1 mm; body weight and wet weight after dissection measured to nearest mg.
  - Biological data: sex determined by dissection; presence of Schistocephalus solidus recorded (yes/no in a dedicated column).
  - Dissection: heads removed; body freeze-dried for elemental analysis.
  - Additional notes: free-text notes field for observations.

- Data file structure and variables
  - Primary dataset: QTL_all_phenotype_data.csv containing fish phenotypes and elemental data.
  - Key identifiers: FishID (experiment-specific ID with year suffix '22' and a 3-digit fish number).
  - Dates: date caught and date processed recorded in British date format (dd/mm/yyyy).
  - Measurements and units:
    - Body length: millimetres to the nearest deci-millimetre.
    - Body weight and wet weight of body without head: grams to the nearest milligram.
    - Sex: M or F.
    - Parasite status: yes/no in the schisto column.
    - ICP-MS run: 1 or 2, indicating the analytical batch.
    - Elemental data: all measured elements named by chemical symbol; concentrations reported in mg/kg on a dry weight basis after blank subtraction and normalization to sample weight.
  - Data and imagery: accompanying photographs provided as JPEG files.

- Quality control and instrumentation
  - Calibration and equipment:
    - Balances calibrated prior to use.
    - PerkinElmer NexION 2000 ICP-MS instrument calibrated per manufacturer instructions.
  - Field and lab tools:
    - Nikon DSLR camera for photographs.
    - Fine balance for weight (mg precision) and calipers for length (0.1 mm precision).
    - ICP-MS analysis for elemental composition.

- Data provenance and metadata
  - Fieldwork and lab processes documented, including sample origin (North Uist to Nottinghamshire), generation timeline, and processing dates.
  - Notes field allows free-text metadata to capture observations not captured by structured columns.
  - Data structure supports one fish per row in the CSV, with photographs stored separately, enabling linkage via FishID.

- Reproducibility and data use considerations
  - Two ICP-MS runs (1 or 2) indicate replication or batch processing for elemental data.
  - Clear unit definitions and data formats facilitate cross-study comparability and monitoring workflows.
  - Public availability of both phenotypic data and corresponding images supports transparency and external validation.