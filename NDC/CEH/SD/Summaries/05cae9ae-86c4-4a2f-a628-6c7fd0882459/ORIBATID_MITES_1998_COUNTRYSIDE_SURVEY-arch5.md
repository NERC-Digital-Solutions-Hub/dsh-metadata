# Oribatid mites 1998 [Countryside Survey], Great Britain Version: 1: 27-04-2018 Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- National-scale soil biodiversity monitoring dataset from Countryside Survey (CS2000) in the UK.
- Focus on oribatid mites (Acari) identified from soil invertebrate extracts.
- Data captured in two CSV files, with taxon details in a linked reference table.
- Taxonomic updates and synonymizations applied over time; dataset versioned (Version 1, 27-04-2018).

## Data collection methods
- Soil cores collected in X-plots as part of Countryside Survey CS2000.
- Invertebrates extracted over five days using a dry Tullgren method; specimens preserved in 70% ethanol.
- Invertebrates identified to broad taxa; oribatid mites (Oribatida) isolated from Acari vials for species-level identification.
- Identification performed at ×400 magnification; specimens cleared with lactic acid as needed.
- Taxonomic references include the Monograph of oribatid mites of the British Isles and subsequent specialist publications.

## Datasets and structure
- ORIBATID_MITES_CS2000_PLOT_RECORDS.csv
  - Records of oribatid mite taxa across sampled plots.
  - Key fields: SQUARE (1 km square code), PLOT (plot within square), COUNTRY (England ENG, Scotland SCO, Wales WAL), TAXA_CODE (mite species code).
  - Links to detailed taxa data in ORIBATID_MITES_CS2000_TAXA_DETAILS.csv.
- ORIBATID_MITES_CS2000_TAXA_DETAILS.csv
  - Taxa_CODE, SPECIES, AUTHORITY, and FAMILY for recorded species.
  - TAXA_CODE in records file links to this details file.
- Both files designed to link plot-level data with species-level details and support data discovery and reuse.

## Taxonomic updates and data curation
- Regular updates to identifications based on specialist literature (e.g., Weigmann 2006; Colloff & Cameron 2013; Niedbala 2011).
- Notable synonymizations and reclassifications applied (e.g., MALA1/MALA2, ORIB4/ORIB6, updates within Malaconothridae and Oppiidae with subgenera changes, genus transfers for several species).
- Updates ensure contemporary taxonomy is reflected in the dataset; historical records may reflect prior nomenclature but are mapped to current taxa via TAXA_CODE.

## Data provenance, licensing, and usage
- All Countryside Survey data must be acknowledged in use.
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey © / Database Right or copyright retained by NERC-CEH; all rights reserved.
- Data linked to the NERC Environmental Information Data Centre (reference: Black et al. 2016; Soil invertebrate data 1998).

## Application and governance considerations for Data Stewards
- Data structure supports linking plot-level data to taxa details, enabling robust discovery and reuse across projects.
- Versioning indicates transparency about taxonomy and dataset updates; consider maintaining clear version histories and provenance in future releases.
- Taxonomic updates pose interoperability challenges; maintain a mapping between old and current nomenclature and ensure downstream users can trace changes via TAXA_CODE.
- Embargoes or data availability limitations are not explicitly stated; plan for updates to reflect any interim constraints and ensure systems allow for updates to TAXA_CODE and related metadata.
- Documentation and metadata should accompany data releases to support accuracy, consistency, and user-driven analysis across systems and formats.

## Acknowledgements and references
- Acknowledgements and dataset usage terms to be included with all copies, publications, and presentations.
- References cited include foundational CS2000 methods, taxonomic revision literature, and field manuals (e.g., Emmett et al. 2008; Black et al. 2016; Colloff & Cameron 2013; Niedbala 2011; Weigmann 2006).