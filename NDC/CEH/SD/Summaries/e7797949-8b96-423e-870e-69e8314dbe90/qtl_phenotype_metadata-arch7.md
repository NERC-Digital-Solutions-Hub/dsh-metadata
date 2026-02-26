# Experimental design/Sampling regime

- Study aim and setup
  - Investigates phenotype and elemental composition of threespined stickleback (Gasterosteus aculeatus) from a marine-by-freshwater cross, raised in a freshwater pond for 5+ generations.
  - Cross between a single male freshwater fish and a single female saltwater migratory fish conducted in spring 2016 on North Uist, Scottish Western Isles.
  - Offspring raised ~2 months in freshwater aquaria at University of Nottingham before establishing a population in a previously fishless pond in Nottinghamshire.
  - Population bred naturally for ~5 generations; a sample of 388 individuals collected from the pond in autumn 2022; fish euthanised for measurement.

- Collection and generation timeline
  - Initial cross in 2016; pond population established subsequently; data collection and sampling conducted October–December 2022.
  - Measurements performed on euthanised individuals.

- Data and measurements collected
  - Photographic data: 419 photographs of 388 fish (files dsc_0170.jpg–dsc_0589.jpg) captured in aquaria.
  - Physical measurements: weight to the nearest milligram; body length from snout tip to caudal peduncle to the nearest deci-millimetre.
  - Morphology: sex determined by dissection; heads removed by dissection.
  - Chemical analysis: body freeze-dried for elemental composition via Inductively Coupled Plasma Mass Spectrometry (ICP-MS).

- Data files and naming
  - Phenotype and elemental data stored in QTL_all_phenotype_data.csv.
  - FishID encoding: QTL experiment name + year code ('22') + three-digit ID (001–).
  - Dates recorded in dd/mm/yyyy format for catch and processing.

- Variables, units, and coding
  - Body length: millimetres (mm) to the nearest 0.1 mm.
  - Body weight and wet weight (body without head): grams (g) to the nearest milligram (mg).
  - Sex: M or F.
  - Parasite presence: schisto column recorded as yes if Schistocephalus solidus present.
  - Notes: free-text field.
  - ICP-MS run: 1 or 2 (which analytical run).
  - Elemental measurements: all elements represented by chemical symbols; units are mg/kg on a dry weight basis after blank subtraction and standardisation to sample weight.

- Data structure and accessibility
  - Data delivered as a CSV file (QTL_all_phenotype_data.csv) with one row per fish.
  - Photographs provided as JPEG files corresponding to the sampled individuals.

- Quality control and instrumentation
  - Balance calibration performed prior to use.
  - ICP-MS calibrated according to manufacturer guidelines.
  - Instruments used: fine balance (milligram precision), calipers (deci-millimetre precision), Perkin Elmer NexION 2000 ICP-MS.
  - Laboratory workflow: blotted fish, photographed, weighed, measured, dissected for sex, body dried for ICP-MS analysis.

- Fieldwork and laboratory workflow
  - Specimens photographed in aquaria; euthanised via MS-222 overdose.
  - Post-math handling included dissection for sex determination and removal of heads.
  - ICP-MS analysis conducted on dry-weight samples; blank subtraction and standardisation applied before reporting mg/kg values.

- GIS-relevant notes for data products
  - Spatial context: origin of the cross (North Uist) and pond location (Nottinghamshire) provide geospatial anchors for mapping life-history origin versus laboratory-reared generations.
  - Temporal context: distinct dates for collection (autumn 2022) and processing; potential time-series linkage across generations.
  - Data integration: single CSV with structured phenotypic and elemental data plus a separate set of photographic images enables tied spatial and visual mapping of individuals.
  - Data standards: explicit encoding for FishID, consistent date format, and clearly defined units support reliable GIS attribute joins and unit conversions.
  - Considerations for GIS use: handling of missing or free-text Notes field; ensuring consistent parasite coding; linking photographs to corresponding CSV rows for rich map-based visualization.