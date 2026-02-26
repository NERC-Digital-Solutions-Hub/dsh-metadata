# QTL_all_phenotype_data.csv

## Overview
- Dataset describing phenotype and elemental composition of threespined stickleback (Gasterosteus aculeatus) from a marine-by-freshwater cross raised in a freshwater pond.
- Birds-eye timeline: cross collected in 2016, raised in freshwater for ~2 months, then introduced to a pond in Nottinghamshire; natural breeding for ~5 generations; sample collected autumn 2022.
- Data supports environmental health and policy monitoring by providing standardized, comparable measurements over time.

## Experimental design and sampling regime
- Cross design: one freshwater male and one saltwater migratory female from North Uist, Scotland (spring 2016).
- Rearing: offspring raised in freshwater aquaria for ~2 months, then established in a previously fishless pond.
- Generation span: ~5 generations before sampling; typical generation time ~1 year.
- Sample size: 388 fish collected from the pond in autumn 2022; total photographs: 419.

## Data collection methods
- Photography: 419 photographs of 388 fish, taken in Aquaria at University of Nottingham; images named in dataset (dsc_0170.jpg–dsc_0589.jpg).
- Physical measurements: body length (mm, to 0.1 mm), body weight and body weight without head (g, to 0.001 g), measured with a fine balance and handheld calipers.
- Sexing and dissection: sex determined by dissection; heads removed by dissection; body freeze-dried for elemental analysis.
- Parasite data: Schistocephalus solidus presence noted (yes/no) if present.
- Euthanasia: MS-222 overdose.

## Nature and units of recorded values
- Phenotypes and elemental data stored in QTL_all_phenotype_data.csv.
- Key fields:
  - FishID: unique identifier (QTL + year + 3-digit ID, e.g., QTL22-001).
  - Date caught / Date processed: dd/mm/yyyy.
  - Body length: millimeters (mm) to 0.1 mm.
  - Body weight / Wet weight of body without head: grams to the nearest milligram.
  - Sex: M or F; Schisto column indicates parasite presence (yes/no).
  - ICP-MS run: 1 or 2 (order of machine run).
  - Elements: all measured elements listed by chemical symbol; units are mg/kg on a dry weight basis (blank-subtracted and weight-standardized).

## Data structure
- Primary data: CSV file (QTL_all_phenotype_data.csv) with one row per fish.
- Additional media: JPEG photographs corresponding to fish.

## Quality control and instrumentation
- Balance calibration prior to use.
- Perkin Elmer NexION 2000 ICP-MS machine calibrated per manufacturer instructions prior to analysis.

## Fieldwork and laboratory instrumentation
- Field/collection: accurate to the nearest milligram for weight, to the nearest deci-millimeter for length.
- Laboratory: ICP-MS analysis performed with Perkin Elmer NexION 2000.
- Imaging: Nikon digital SLR camera for photography.