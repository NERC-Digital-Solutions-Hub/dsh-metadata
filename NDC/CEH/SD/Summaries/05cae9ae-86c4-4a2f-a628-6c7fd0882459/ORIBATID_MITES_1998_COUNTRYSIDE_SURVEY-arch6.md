# Oribatid mites 1998 [Countryside Survey], Great Britain

## Overview
- Documentation of oribatid mite data from Countryside Survey (CS) 2000 baseline—UK national soil biodiversity monitoring.
- Two CSV datasets document taxa records and taxon details across sampled plots in England, Scotland, and Wales.
- Emphasizes data provenance, taxonomic updates, and required acknowledgement for data reuse.

## Methods and Identification
- Soil cores from Countryside Survey (CS) were collected in plots within 1 km squares and processed using a dry Tullgren extraction over five days.
- Invertebrates identified to broad taxa; specimens preserved in 70% ethanol.
- Oribatid mites identified from Acari extracts by Frank Monson to species level when possible.
- Identification performed at ×400 magnification; necessary clearing with lactic acid before slide examination.
- Taxonomic references and ongoing updates used, including the Monograph of oribatid mites of the British Isles and Weigmann (2006), with several synonymies and reclassifications applied.

## Taxonomic Updates (selected changes)
- Synonymies and reclassifications for multiple species (e.g., Malaconothrus egregius → M. monodactylus; Oribatula venusta → O. tibialis).
- Updates within Malaconothridae (MALA4–MALA8) based on Colloff & Cameron (2013).
- Genus transfers: Rhysotritia duplicata/ardua → Acrotritia; Ceratozella thienemanni → Ceratozetes thienemanni; Zygoribatula terricola → Z. excavata; Liochthonius hirtus → Brachychthonius hirtus.
- Oppiidae revision: Lauroppia, Medioppia, Moritzoppia reclassified as subgenera of Oppiella; Quadroppia split, with some species moved to Coronoquadroppia.
- Punctoribates quadrivertex → Zachvatinibates quadrivertex; Latilamellobates incisellus → Trichoribates incisellus; Oribatula saxicola → Scheloribates initialis.

## Datasets and File Structure
- ORIBATID_MITES_CS2000_PLOT_RECORDS.csv
  - Records of oribatid mite taxa across sampled plots.
  - Key fields: SQUARE (1 km square code), PLOT (plot within square), COUNTRY (England ENG, Scotland SCO, Wales WAL), TAXA_CODE (mite species code).
  - Links to detailed taxa in ORIBATID_MITES_CS2000_TAXA_DETAILS.
- ORIBATID_MITES_CS2000_TAXA_DETAILS.csv
  - Taxon details for recorded mites.
  - Key fields: TAXA_CODE, SPECIES (species name), AUTHORITY (taxonomic authority), FAMILY (taxonomic family).

## Data Usage and Acknowledgement
- All use of Countryside Survey data must include acknowledgement:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## References
- Black, H.I.J. et al. (2016). Soil invertebrate data 1998 [Countryside Survey]. NERC Environmental Information Data Centre. https://doi.org/10.5285/f3e71ba6-bfd7-4841-9ce4fd1f0d590d2d
- Colloff, M.J., Cameron, S.L. (2013). A phylogenetic analysis and taxonomic revision of the oribatid mite family Malaconothridae. Zootaxa 3681, 301-346.
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07 Soils Manual. CEH.
- Niedbala, W. (2011). Ptyctimous mites (Acari: Oribatida) of the Palaearctic Region. Fauna Mundi.
- Weigmann, G. (2006). Hornmilben (Oribatida). Die Tierwelt Deutschlands, 76. Teil. Goecke & Evers.