# The purpose of the data is to compare the amount of a key pheromone between two sibling species of Drosophila

## Overview
- Study compares 7,11-heptacosadiene (7,11-HD) pheromone levels between two Drosophila species: D. simulans and D. sechellia.
- Samples: 15 female individuals of D. simulans and 15 female individuals of D. sechellia.
- Strains/Origins: D. simulans a2a2b inbred line from the Tsimbazaza strain; D. sechellia from Cousin Island, Seychelles.
- Data files: 711HDsech.csv and 711HDsim.csv.
- Data organization: amounts reported as nanograms (ng) per sample; each dataset uses sample identifiers in column 1 and ng values in column 2.
- Identification: 7,11-HD identified by retention time relative to the C26 internal standard.

## Data collection and methods
- Biological sampling: virgin females isolated and kept with other females for five days; extraction performed on the fifth day.
- Extraction: individual females placed in 150 µL of >99% hexane in a glass vial; vortexed briefly; hexane evaporated with nitrogen; vials stored at -20°C prior to shipping.
- Internal standard and resuspension: extracts resuspended in 50 µL of standard solution containing 10 ng/mL octadecane (C18) and 10 ng/mL C26 in hexane.
- Instrumentation and analysis: gas chromatography (Agilent 7890) with flame ionization detector, DB-1 column; splitless injection at 250 °C; helium carrier gas.
- GC program: 50 °C (1.5 min) to 150 °C, 10 °C/min; then to 280 °C at 4 °C/min with a 5 min hold.
- Quantification: peak areas for 7,11-HD normalized to internal standard C26; relative quantity in ng calculated using peak area ratios.
- Data processing: ChemStation software used for integration; method referenced to Krupp et al. (2008).
- Provenance and workflow: rearing/extraction conducted at University of Oxford (Stephen Goodwin lab) by Deniz Erezyilmaz; GC analysis conducted at University of Groningen by Nicolas Dubovetsky.

## Data structure and provenance
- Datasets contain two columns: sample identifier (column 1) and quantity in ng (column 2).
- 7,11-HD identified by retention time relative to C26 standard.
- Some samples excluded due to no detectable traces.
- Documentation of method and processing aligns with established pheromone quantification practices (reference to Krupp et al., 2008).

## Data governance, quality, and sharing considerations
- Data quality: presence of samples with no traces leads to incomplete datasets; transparent reporting of exclusions.
- Consistency and standards: standard internal controls (C26) and dual internal standards (C18 and C26) used to ensure comparability.
- Metadata and lineage: clear attribution of labs and personnel (Oxford for rearing/extraction; Groningen for GC analysis) to support reproducibility and provenance.
- Data stewardship implications:
  - Ensure dataset metadata include species, strain/origin, sample count, extraction/date, instrument settings, and processing workflow.
  - Maintain traceability of samples excluded due to non-detects and document reasons for exclusion.
  - Facilitate data sharing by adopting a stable, machine-readable format (CSV) with explicit units (ng) and column mappings.
  - Plan for ongoing data availability and potential future updates or corrections, including reprocessing or inclusion of additional samples if available.