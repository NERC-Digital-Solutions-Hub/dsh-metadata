# The purpose of the data is to compare the amount of a key pheromone between two sibling species of Drosophila

## Scope and aim
- Compare the amount of 7,11-heptacosadiene (7,11-HD) between two sibling Drosophila species: D. simulans and D. sechellia
- Species lines: D. simulans a2a2b (inbred; Tsimbazaza origin) and D. sechellia from Cousin Island, Seychelles
- Samples: 15 virgin females per species, kept with other females for five days before extraction

## Data collection and analytical methods
- Extraction: individual females anaesthetised, hexane extraction, internal standards added (50 µL of standard solution with 10 ng/mL C18 and 10 ng/mL C26)
- Instrumental analysis: GC-FID (Agilent 7890) with DB-1 column; splitless injector at 250 °C; helium as carrier gas
- GC program: 50 °C (1.5 min) → 150 °C (10 °C/min) → 280 °C (4 °C/min) with 5 min hold
- Quantification: peak areas relative to internal standard (C26); 7,11-HD identified by retention time relative to C26
- Data files: 711HDsech.csv (D. sechellia) and 711HDsim.csv (D. simulans); data organized by ng per sample

## Data processing and provenance
- Data processing: relative quantities expressed in ng
- Sample exclusion: some samples produced no traces and were excluded
- Provenance: rearing and extractions at University of Oxford (Stephen Goodwin lab) by Deniz Erezyilmaz; GC analysis at University of Groningen by Nicolas Dubovetsky

## Metadata, standards, and references
- Internal standards: C18 and C26 used for quantification
- Identification method: retention time relative to C26
- Reference framework: method described in Krupp et al. (2008)

## Data quality, limitations, and governance
- Data quality notes: some samples lacked traces; quantification relies on consistent internal standard
- Cross-lab collaboration demonstrates reproducibility challenges and the importance of standardized protocols
- Documentation enables traceability from rearing through extraction to GC analysis

## Implications for data strategy for Data Leaders
- Emphasizes end-to-end data lineage and clear metadata (species, line, sex, sample ID, processing steps)
- Highlights need for data standardization and disclosure of analytical methods for reproducibility
- Demonstrates value of sharing datasets across labs to enable cross-study comparisons and meta-analyses

## Practical takeaways for future data projects
- Maintain both raw and processed data with explicit mapping to methods
- Capture complete metadata: strain origins, rearing conditions, sample handling, and instrument settings
- Plan for data quality checks and explicit handling of missing or unusable samples
- Foster collaboration and transparent data sharing across contributing labs to enhance system-wide data effectiveness