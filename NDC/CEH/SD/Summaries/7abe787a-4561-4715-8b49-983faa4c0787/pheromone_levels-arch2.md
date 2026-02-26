# The purpose of the data is to compare the amount of a key pheromone between two sibling species of Drosophila.

## Overview and aims
- Objective: quantify and compare the amount of 7,11-heptacosadiene (7,11-HD) pheromone between two sibling species, Drosophila simulans and D. sechellia.
- Samples: 15 individual females from each species (D. simulans strain a2a2b; D. sechellia derived from Cousin Island, Seychelles).
- Experimental design: virgin females isolated and kept with other females for five days before extraction.

## Sample collection and preparation
- Anesthesia and handling: females anesthetised on ice for 10 minutes before processing.
- Extraction: each female extracted in 150 µL of >99% hexane in a 200 µL glass vial with a glass insert; vortexed briefly.
- Internal standard and storage: extracts were spiked with 50 µL of a standard solution containing 10 ng/mL octadecane (C18) and 10 ng/mL hexacosane (C26) in hexane; vials stored at -20°C prior to shipping.

## Analytical approach
- Instrumentation: gas chromatography with flame ionization detection (GC-FID) using an Agilent 7890, DB-1 column, splitless injector at 250 °C, helium carrier gas.
- GC method: oven programmed from 50 °C (1.5 min) to 150 °C (10 °C/min), to 280 °C (4 °C/min) with a final 5 min hold.
- Data processing: ChemStation software to integrate 7,11-HD peak areas relative to internal standard C26; identification by retention time relative to C26.
- Quantification: relative quantity expressed as ng of 7,11-HD per sample based on peak areas compared to the internal standard.

## Data organization and outputs
- Datasets: 711HDsech.csv (D. sechellia) and 711HDsim.csv (D. simulans).
- Data structure: information organized by ng (column 2) per sample (column 1); samples with no detectable traces excluded from analysis.

## Quality, provenance, and collaboration
- Quality notes: some samples failed to produce detectable traces and were excluded.
- Provenance: rearing and extraction performed at Stephen Goodwin’s lab (University of Oxford) by Deniz Erezyilmaz; samples shipped to University of Groningen for GC analysis by Nicolas Dubovetsky in J. C. Billeter’s lab.
- Data handling: outputs produced as CSV datasets with quantified 7,11-HD amounts for each sample.