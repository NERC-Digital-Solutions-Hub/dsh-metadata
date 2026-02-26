# Oribatid mites 1998 [Countryside Survey], Great Britain

## Overview
- National-scale monitoring of soil biodiversity in the UK, part of Countryside Survey (CS) and CS2000, the first and only nationwide soil invertebrate baseline.
- Sampling design involves soil cores from plots within 1 km squares; five plots per square, with additional soil and vegetation data linked at the plot level.
- Oribatid mites (Acari) identified to species level for the dataset, with data linked to broader soil invertebrate surveys.
- Taxonomic identifications and updates drawn from specialist literature and ongoing revisions.

## Methods
- Soil cores collected in X-plots; five-day dry Tullgren extraction used to extract soil invertebrates.
- Specimens preserved in 70% ethanol and identified under stereomicroscope; oribatid mites identified by the specialist Frank Monson.
- Identification conducted to species level where possible, with ongoing updates to names and classifications as taxonomic work progresses.
- Taxonomic updates documented to reflect synonymies and reclassifications (examples include several genera and species reassignments within multiple families).

## Taxonomic updates and quality control
- Revisions include synonymies and reclassifications (e.g., Malaconothrus egregius → M. monodactylus; Oribatula saxicola → Scheloribates initialis; various Malaconothridae and Oppiidae updates).
- Updates also include genus transfers (e.g., Rhysotritia to Acrotritia; Lauroppia and related genera reclassified under subgenera of Oppiella).
- Taxonomic changes systematically reflected in dataset codes (e.g., MALA1 → MALA2; ORIB4 → ORIB6) to maintain consistency with current taxonomy.
- Data quality and documentation linked to established sources (Weigmann 2006; Colloff & Cameron 2013; Niedbala 2011) and data quality procedures (Black et al. 2016).

## Datasets
- ORIBATID_MITES_CS2000_PLOT_RECORDS.csv
  - Fields include: SQUARE (1 km square code), PLOT (plot code within square), COUNTRY (England, Scotland, Wales), TAXA_CODE (mite species code).
  - Link to additional taxonomy details via ORIBATID_MITES_CS2000_TAXA_DETAILS.csv.
- ORIBATID_MITES_CS2000_TAXA_DETAILS.csv
  - Fields include: TAXA_CODE, SPECIES, AUTHORITY, FAMILY.
- All CS data usage must be acknowledged with the provided acknowledgement text (see below).

## Data access, usage, and governance
- Acknowledgement and rights:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- All uses of Countryside Survey data must include the exact acknowledgement and copyright notice above.
- Data are maintained under explicit governance and rights restrictions; data sharing and reuse should respect the provenance and licensing terms.

## Relevance for monitoring frameworks
- Demonstrates a structured approach to national-scale soil biodiversity monitoring, including:
  - Clear sampling design and linkages to broader ecological and land-use data.
  - Rigorous taxonomic work with updates to reflect current taxonomy.
  - Documented data structures and metadata supporting integration, analysis, and reporting.
  - Explicit data governance, sharing constraints, and acknowledgment requirements.

## Key references (methods, taxonomy, and data quality)
- Black, H.I.J.; et al. (2016). Soil invertebrate data 1998 [Countryside Survey]. NERC Environmental Information Data Centre. https://doi.org/10.5285/f3e71ba6-bfd7-4841-9ce4fd1f0d590d2d
- Colloff, M.J.; Cameron, S.L. (2013). A phylogenetic analysis and taxonomic revision of the oribatid mite family Malaconothridae. Zootaxa 3681, 301-346.
- Emmett, B.A.; et al. (2008). Countryside Survey Technical Report No.03/07 Soils Manual. CEH.
- Niedbala, W. (2011). Ptyctimous mites of the Palaearctic Region. Fauna Mundi, Vol. 4.
- Weigmann, G. (2006). Hornmilben (Oribatida). Die Tierwelt Deutschlands, Teil 76. Goecke & Evers.