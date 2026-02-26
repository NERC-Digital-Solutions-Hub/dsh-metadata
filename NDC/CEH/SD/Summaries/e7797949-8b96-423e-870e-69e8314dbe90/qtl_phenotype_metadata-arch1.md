# QTL_all_phenotype_data.csv

## Overview
- Dataset describing phenotype and elemental composition of threespined stickleback (Gasterosteus aculeatus) from a marine by freshwater cross.
- Fish were raised in freshwater for ~2 months, then bred in a pond for ~5 generations before sampling in autumn 2022.
- 388 individuals were collected (photos total: 419), euthanised, and measured or analysed for elemental content.

## Experimental design and sampling
- Cross design: one male freshwater fish × one female saltwater migratory fish, collected in North Uist, Spring 2016.
- Rearing: offspring reared ~2 months in freshwater aquaria at University of Nottingham; released population established in a fishless pond in Nottinghamshire.
- Generational span: pond population bred naturally for ~5 generations before sampling.
- Sampling: autumn 2022; 388 fish sampled from pond; euthanised with MS222; measurements recorded.

## Data collection and measurements
- Photographs: 419 photographs of 388 fish (files named dsc_0170.jpg to dsc_0589.jpg); collected Oct–Dec 2022.
- Measurements per fish:
  - Body length: mm to the nearest deci-millimetre.
  - Body weight: grams to the nearest milligram.
  - Wet weight of body without head: grams to the nearest milligram.
  - Sex: determined by dissection (M or F).
  - Parasite presence: Schistocephalus solidus, noted as yes if present.
  - Head: removed by dissection; body freeze-dried for elemental analysis.
  - Notes: free text field.
- Elemental analysis: Inductively coupled plasma mass spectrometry (ICP-MS) on dried tissue.

## Data structure and content
- Primary data file: QTL_all_phenotype_data.csv
  - Each row corresponds to one fish.
  - Columns include FishID, catch/processing dates (dd/mm/yyyy), length, weights, sex, Schisto flag, notes, ICP-MS run number (1 or 2), and elemental measurements by ICP-MS.
  - FishID encoding: [QTL] experiment name + year processed ('22') + three-digit ID (001 onward).
- Photographs: JPEG files corresponding to the same fish records.

## Units and measurement details
- Length: millimetres (mm) to the nearest 0.1 mm.
- Body weight and post-dissection body weight: grams (g) to the nearest milligram (mg).
- Elemental concentrations: milligrams per kilogram (mg/kg) on a dry weight basis, blank-subtracted and standardised to sample weight.
- Dates: standard British format dd/mm/yyyy.

## Quality control and instrumentation
- Balances calibrated prior to use.
- ICP-MS: Perkin Elmer NexION 2000 calibrated per manufacturer instructions prior to analysis.
- Measurements taken under standardized dissection and drying procedures prior to ICP-MS.

## Fieldwork, laboratory equipment, and workflow
- Equipment:
  - Fine balance (mg precision) and handheld calipers (deci-mm precision) for measurements.
  - Nikon digital SLR camera for photographs.
  - ICP-MS instrument for elemental analysis.
- Workflow:
  - Fish euthanised, blotted, photographed, weighed, measured.
  - Heads removed; body dissection performed; parasite presence noted.
  - Tissue freeze-dried and subjected to ICP-MS analysis.
  - Data compiled into CSV with corresponding JPEG photographs.