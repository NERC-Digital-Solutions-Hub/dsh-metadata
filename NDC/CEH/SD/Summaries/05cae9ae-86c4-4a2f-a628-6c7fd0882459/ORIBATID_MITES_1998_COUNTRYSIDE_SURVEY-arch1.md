# Oribatid mites 1998 [Countryside Survey], Great Britain

## Overview
- National-scale soil biodiversity monitoring for the UK (Countryside Survey, CS), with data from CS2000.
- Soil cores from X-plots used to extract soil invertebrates over five days via dry Tullgren method; specimens preserved in 70% ethanol.
- Invertebrates identified to broad taxa; oribatid mites (Acari) identified from each Acari extract and recorded across samples.
- Taxonomic identifications updated over time using specialist publications; dataset links to a taxon details file and documents taxonomic changes and synonymies.

## Methods
- Sampling and extraction
  - Soil cores collected in 1 km squares; five plots per square.
  - Dry Tullgren extraction performed over five days; invertebrates preserved in ethanol.
- Identification
  - Invertebrates identified to broad taxa; Acari kept separate for mite processing.
  - Oribatid mites identified at ×400 magnification using a Watson Service 2 microscope.
  - Clearing with lactic acid when needed; slides prepared for examination.
- Taxonomic references and updates
  - Initial identifications based on Luxton (unpublished) and related primary literature.
  - Updates incorporated from Weigmann (2006) and Colloff & Cameron (2013), among others.
  - Numerous synonymies and reclassifications applied (examples below).

## Taxonomic updates (highlights)
- Malaconothridae: revisions with new species; several species reclassified (e.g., MALA1 = MALA2).
- Oribatid genera/ species updated (e.g., Rhysotritia duplicata and R. ardua moved to Acrotritia; Ceratozetes thienemanni renamed Ceratozetes thienemanni; Zygoribatula terricola renamed as Z. excavata).
- Oppiidae group updated with sub-genera reclassifications (Lauroppia, Medioppia, Moritzoppia as sub-genera of Oppiella; Quadroppia with some species moving to Coronoquadroppia).
- Punctoribates quadrivertex renamed Zachvatinibates quadrivertex; Latilamellobates incisellus renamed Trichoribates incisellus.
- Oribatula saxicola amended to Scheloribates (Hemileus) initialis.
- Ongoing revisions emphasize changes in genus/species placement and synonymies.

## Datasets
- ORIBATID_MITES_CS2000_PLOT_RECORDS.csv
  - SQUARE: 1 km square code where sample was taken.
  - PLOT: plot code within the square (one of five plots per square).
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL).
  - TAXA_CODE: code for oribatid mite species (links to details file).
  - Relationship: links to ORIBATID_MITES_CS2000_TAXA_DETAILS.csv for taxon details.
- ORIBATID_MITES_CS2000_TAXA_DETAILS.csv
  - TAXA_CODE: code for oribatid mite species.
  - SPECIES: species name.
  - AUTHORITY: taxonomic authority for the recorded species.
  - FAMILY: taxonomic family.

## Data quality, access, and use
- All CS data require acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
- Taxonomic updates mean users should align with current oribatid taxonomy where possible; note that nomenclature in the CS2000 dataset reflects revisions listed in the updates.

## Usage notes and potential analyses
- The dataset enables analysis of oribatid mite diversity and distribution across 1 km squares and plots in England, Scotland, and Wales.
- Potential to correlate oribatid taxa with soil properties and vegetation data collected at the plot level.
- Consider taxonomic revision context when comparing to other datasets or historical records; use TAXA_CODE with the TAXA_DETAILS file for current species naming and family classification.

## References
- Black, H.I.J.; et al. (2016). Soil invertebrate data 1998 [Countryside Survey]. NERC Environmental Information Data Centre. https://doi.org/10.5285/f3e71ba6-bfd7-4841-9ce4fd1f0d590d2d
- Colloff, M.J.; Cameron, S.L. (2013). A phylogenetic analysis and taxonomic revision of the oribatid mite family Malaconothridae (Acari: Oribatida). Zootaxa 3681, 301-346.
- Emmett, B.A.; et al. (2008). Countryside Survey Technical Report No.03/07 Soils Manual. CEH.
- Niedbala, W. (2011). Ptyctimous mites (Acari: Oribatida) of the Palaearctic Region. Fauna Mundi, 4, 472 pp.
- Weigmann, G. (2006). Hornmilben (Oribatida). Die Tierwelt Deutschlands, 76. Teil. Goecke & Evers.