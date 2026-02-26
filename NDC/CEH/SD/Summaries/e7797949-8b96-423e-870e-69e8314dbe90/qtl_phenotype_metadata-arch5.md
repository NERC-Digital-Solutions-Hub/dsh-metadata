# Experimental design/Sampling regime

- Aim and study design
  - Investigates phenotype and elemental composition of threespined stickleback (Gasterosteus aculeatus) from a marine × freshwater cross raised in a freshwater pond for 5+ generations.
  - Final sampling comprised 388 individuals (with 419 photographs of these fish) collected from a pond in autumn 2022 after natural breeding in Nottinghamshire.

- Sampling provenance and timeline
  - 2016: One male freshwater fish and one female saltwater migratory fish collected in North Uist, Scottish Western Isles; cross established.
  - 2016–circa 2018: Offspring raised in freshwater aquaria for ~2 months before population transfer to a previously fishless pond.
  - ~5 generations (typical ~1 year per generation) bred in pond prior to sampling.
  - Oct–Dec 2022: Data collection in University of Nottingham aquaria; 388 fish sampled and euthanised for measurement.

- Data collection and processing methods
  - Measurements: photograph each fish, weigh to the nearest milligram, measure body length to the nearest 0.1 mm; heads removed by dissection; sex determined by dissection; body freeze-dried for ICP-MS elemental analysis.
  - Euthanisation: overdose of MS222.
  - Photography: Nikon digital SLR; 419 photographs recorded (files named dsc_0170.jpg to dsc_0589.jpg).

- Data content and structure
  - Phenotype and elemental data stored in a single CSV: QTL_all_phenotype_data.csv.
  - Data rows: one row per fish (388 individuals; 419 photos).
  - File pairings: JPEG photographs corresponding to the individuals.
  - Fish identification: FishID constructed as the experiment code (QTL) + year (22) + a 3-digit ID (001+).

- Variables, units, and conventions
  - Date fields: date caught and date processed in dd/mm/yyyy format (British date format).
  - Body length: millimetres to the nearest deci-millimetre.
  - Body weight and wet weight (bodyWithoutHead): grams to the nearest milligram.
  - Sex: M or F.
  - Parasite status: Schistocephalus solidus presence recorded as yes/no in the schisto column.
  - ICP-MS run: indicated as 1 or 2 depending on the run.
  - Elemental data: all measured elements identified by chemical symbol; concentrations in mg/kg on a dry weight basis after blank subtraction and normalization to sample weight.

- Quality control and provenance
  - Balance calibration prior to use; measurement accuracy aided by a fine balance and calibrated calipers.
  - ICP-MS (PerkinElmer NexION 2000) calibrated per manufacturer instructions before analysis.

- Fieldwork, instrumentation, and data capture specifics
  - Field/lab equipment: balance (mg accuracy), calipers (0.1 mm accuracy), Nikon DSLR for photography, ICP-MS (NexION 2000) for elemental analysis.
  - Data capture: data stored in a CSV with named variables corresponding to measurements; photographs stored as JPEGs with systematic naming.

- Governance, reuse, and notes for data consumers
  - Clear documentation of data structure, measurement units, and processing steps to facilitate reuse and cross-study comparability.
  - Documentation includes data provenance (collection, processing, and analysis steps) and data lineage (from field collection to ICP-MS results).
  - Notes field allows free-text annotations per individual, enabling context-specific information and potential caveats for interpretation.