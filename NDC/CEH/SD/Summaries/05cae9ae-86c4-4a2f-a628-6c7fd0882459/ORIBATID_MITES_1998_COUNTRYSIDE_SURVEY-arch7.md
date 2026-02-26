# Oribatid mites 1998 [Countryside Survey], Great Britain

## Overview
- First national-scale monitoring of soil biodiversity in the UK via Countryside Survey (CS2000).
- Focus on oribatid mites within soil invertebrate diversity data; spatially structured across 1 km squares.

## Methods
- Soil cores collected in X-plots; five-day dry Tullgren extraction to recover soil invertebrates.
- Specimens preserved in 70% ethanol; sorted to broad taxonomic groups under a stereomicroscope.
- Acari specimens sent for specialist identification; oribatid mites identified to species level.
- Identification at ×400 magnification; clearing with lactic acid when needed.
- Taxonomic updates incorporated from specialist publications (Weigmann 2006; Colloff & Cameron 2013; others).

## Datasets
- ORIBATID_MITES_CS2000_PLOT_RECORDS.csv
  - SQUARE: 1 km square code.
  - PLOT: plot code within the square (one of 5 plots per square).
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL).
  - TAXA_CODE: code for oribatid mite species; links to taxa details file.
- ORIBATID_MITES_CS2000_TAXA_DETAILS.csv
  - TAXA_CODE: code for species.
  - SPECIES: species name.
  - AUTHORITY: taxonomic authority.
  - FAMILY: taxonomic family.
- Data use requires acknowledgement of Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.

## Taxonomic updates and nomenclature changes
- Synonymies and reclassifications affecting dataset codes (e.g., MALA1 = MALA2; ORIB4 = ORIB6).
- Key updates include:
  - Malaconothrus egregius → M. monodactylus; Oribatula venusta → O. tibialis.
  - Malaconothridae revisions: MALA4, MALA5, MALA6, MALA7, MALA8.
  - Rhysotritia duplicata/ardua moved to Acrotritia (EUPH1, EUPH2).
  - Ceratozella thienemanni now Ceratozetes thienemanni (CERA2).
  - Zygoribatula terricola → Z. excavata (ORIB5).
  - Liochthonius hirtus → Brachychthonius hirtus (BRAC3).
  - Oppiidae genera updated as subgenera of Oppiella (OPPI3, OPPI4, OPPI5, OPPI7, OPPI8, OPPI10); Quadroppia split with some species moved to Coronoquadroppia (OPPI13, OPPI15, OPPI17, OPPI20).
  - Punctoribates quadrivertex → Zachvatinibates quadrivertex (MYCO3).
  - Latilamellobates incisellus → Trichoribates incisellus (CERA8).
  - Oribatula saxicola → Scheloribates (Hemileus) initialis (ORIB3).

## Data fields and linking
- Plot-level spatial linkage enables integration with other soil and vegetation data collected in each plot.
- TAXA_CODE in plot records links to detailed species information in the TAXA_DETAILS file.

## Usage, attribution and rights
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement requirement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © database rights.

## References
- Black et al. (2016). Soil invertebrate data 1998 [Countryside Survey]. NERC Environmental Information Data Centre.
- Colloff & Cameron (2013). Phylogenetic analysis and taxonomic revision of Malaconothridae (Acari: Oribatida).
- Emmett et al. (2008). Countryside Survey Technical Report No. 03/07 Soils Manual.
- Niedbala (2011). Ptyctimous mites (Acari: Oribatida) of the Palaearctic.
- Weigmann (2006). Hornmilben (Oribatida).