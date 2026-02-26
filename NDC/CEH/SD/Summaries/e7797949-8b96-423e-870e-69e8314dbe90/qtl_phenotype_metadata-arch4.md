# Experimental design/Sampling regime

- Summary of purpose and origin
  - Investigates the phenotype and elemental composition of threespined stickleback (Gasterosteus aculeatus) from a marine by freshwater cross, raised in a freshwater pond for 5+ generations.
  - Cross between a single male freshwater fish and a single female saltwater migratory fish collected in North Uist, spring 2016; offspring raised in freshwater tanks at the University of Nottingham for ~2 months before establishing a population in a pond in Nottinghamshire.
  - Population bred naturally for ~5 generations; a sample of 388 individuals was collected from the pond in autumn 2022.

- Data collection and processing workflow
  - Fish were euthanised with MS222 and measured.
  - 419 photographs of 388 fish were taken between October and December 2022 in Aquaria at the University Park campus.
  - Each fish was blotted, weighed to the nearest milligram, and measured for body length to the nearest 0.1 mm.
  - Heads were removed by dissection; sex determined by dissection; body freeze-dried for elemental analysis via ICP-MS.

- Data recorded and formats
  - Phenotype and elemental data stored in QTL_all_phenotype_data.csv.
  - Data fields include: FishID (experiment code + year '22 + 3-digit ID), collection and processing dates (dd/mm/yyyy), body length (mm to 0.1 mm), body weight and wet weight (g to mg), sex (M/F), parasite presence (Schistocephalus solidus) as yes/no, notes (free text), ICP-MS run (1 or 2), and elemental measurements.
  - Elemental concentrations reported as mg/kg on a dry weight basis after blank subtraction and standardization.

- Data structure and file organization
  - CSV file: QTL_all_phenotype_data.csv with one row per fish.
  - Photographs: JPEG files (dsc_0170.jpg to dsc_0589.jpg), corresponding to the 419 images.

- Measurement and quality control
  - Balances calibrated prior to use.
  - ICP-MS (PerkinElmer NexION 2000) calibrated per manufacturer instructions prior to analysis.

- Fieldwork and instrumentation
  - Equipment: fine balance (milligram precision), handheld calipers (deci-millimetre precision), Nikon digital SLR for photographs, ICP-MS instrument (PerkinElmer NexION 2000).
  - Data capture occurred in aquaria facilities and involved dissection, weighing, length measurement, and ICP-MS analyses.

- Units, standards, and provenance
  - Length: millimetres (to 0.1 mm precision).
  - Weight: grams to the nearest milligram.
  - Elemental concentrations: mg/kg (dry weight).
  - Dates in British format (dd/mm/yyyy).
  - Data provenance includes the generation of a cross, rearing history, and the generation of a pond population, with explicit detailing of processing and measurement steps.