# Oribatid mites 1998 [Countryside Survey], Great Britain

## Overview
- First national-scale monitoring of soil biodiversity in the UK, part of Countryside Survey (CS) CS2000.
- Involves soil cores processed to extract soil invertebrates over five days using a dry Tullgren method; specimens preserved in ethanol and identified to broad taxa.
- Oribatid mites (Acari) identified to species level by specialists; dataset documents presence across plots and taxonomic details.
- Data are stored as two CSV files and are intended for integration with other CS soil and vegetation data. Taxonomic updates since CS2000 are recorded to maintain traceability.

## Data assets
- ORIBATID_MITES_CS2000_PLOT_RECORDS.csv
  - Records of oribatid mite taxa across sampled plots.
  - Key fields: SQUARE (1km square code), PLOT (plot within square), COUNTRY (England, Scotland, Wales), TAXA_CODE (mite species code).
  - Links to species details via TAXA_CODE in the second file.
- ORIBATID_MITES_CS2000_TAXA_DETAILS.csv
  - Details for recorded taxa.
  - Key fields: TAXA_CODE, SPECIES, AUTHORITY, FAMILY.
- Both files are text-based; data are designed to be linked and cross-referenced with other CS2000 soil/vegetation data.

## Taxonomic updates and lineage
- Taxonomic updates and synonymisations are documented to reflect changes since CS2000, including:
  - Reassignments and consolidations within families and genera (e.g., Malaconothridae, Oppiidae, and related sub-genera changes).
  - Specific species reclassifications (e.g., Rhysotritia duplicata and R. ardua moved to Acrotritia; Ceratozella thienemanni renamed as Ceratozetes thienemanni; Zygoribatula terricola renamed as Z. excavata; Liochthonius hirtus renamed as Brachychthonius hirtus).
  - Numerous genus and species name updates affecting dataset interpretation (e.g., Lauroppia, Medioppia, Moritzoppia treated as subgenera of Oppiella; Quadroppia reorganized with some moves to Coronoquadroppia; Punctoribates quadrivertex renamed Zachvatinibates quadrivertex; Latilamellobates incisellus renamed Trichoribates incisellus; Oribatula saxicola amended to Scheloribates initialis).
- These updates are captured to support accurate downstream analysis and require careful mapping to current taxonomy.

## Collection and processing methods
- Soil cores collected in X-plots and processed over five days using a dry Tullgren extraction method.
- Invertebrates separated, counted under a stereomicroscope; 70% ethanol preserved.
- Oribatid mites identified from Acari extracts at ×400 magnification.
- Clearing with lactic acid when needed; examination on slides under a compound microscope.
- Taxonomic references used include Monograph of oribatid mites of the British Isles and Weigmann (2006), with updates from Colloff & Cameron (2013) and others.
- Quality control references include Black et al. (2016) detailing data and QC procedures; 582 of the sample vials contained Acari, with oribatids identified from those.

## Data quality, provenance and governance
- Data collected with documented methods; identifications updated according to specialist publications to reflect taxonomic revisions.
- Data quality control references and links to data quality procedures are provided (Black et al. 2016; additional taxonomic revision sources).
- Data format and structure designed to enable linking with other Countryside Survey data, supporting a broader data system for soil biodiversity.

## Access, usage and attribution
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data are associated with CEH/NERC custodianship; references available for data provenance and methods.

## References
- Black, H.I.J. et al. (2016). Soil invertebrate data 1998 [Countryside Survey]. NERC Environmental Information Data Centre. DOI link provided.
- Colloff, M.J., Cameron, S.L. (2013). Phylogenetic analysis and taxonomic revision of Malaconothridae. Zootaxa.
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07 Soils Manual. CEH.
- Niedbala, W. (2011). Ptyctimous mites. Fauna Mundi.
- Weigmann, G. (2006). Hornmilben (Oribatida). Die Tierwelt Deutschlands.

## Implications for data leaders
- The dataset demonstrates a robust national-scale approach to soil biodiversity with clearly defined data structures and taxonomic detail, suitable for integration into broader data systems and policy-oriented analyses.
- Taxonomic drift and synonymisations highlight the need for ongoing taxonomic harmonisation and clear mapping between historical and current classifications when analysing longitudinal data.
- The two-file structure (plot-level records and taxon details) enables scalable linkage to other environmental data streams but requires careful data governance to maintain consistency across updates.
- Clear data usage guidelines and required acknowledgments are essential for proper data stewardship and attribution in all outputs.