# Data on clinal variation in the mimetic butterflies Heliconius erato and Heliconius melpomene in the Chocó-Darien ecoregion

## Overview
- Dataset generated as part of a study on clinal variation in Heliconius erato and Heliconius melpomene across the Chocó-Darien ecoregion (Ecuador, Colombia, Panama).
- Integrates field collection, specimen preservation, genetic sequencing, and digital wing imaging.
- Associated with a published study: Curran et al. 2020 (Molecular Ecology).

## Sampling and specimen collection
- Butterfly specimens collected over five trips:
  - May 2014 and May 2015 in Mashpi reserve, Pichincha, Ecuador.
  - January 2015 in Cauca Valley and Chocó, Colombia.
  - February 2015 in southwest Darien, Panama.
  - March 2016 in northern Chocó, Colombia.
- Sampling locations: varied sites across Ecuador, Colombia, and Panama; sampling areas within ~2 km of a single recorded point per site.
- Methods: hand nets targeting all observed Heliconius, focusing on H. melpomene and H. erato.
- Species confirmation: identities verified by at least two experts; genetic confirmation used in listed cases.
- Subspecies classification: based on wing pattern phenotype.
- Sex determination: based on genital morphology.

## Metadata and site information
- GPS coordinates collected with a Garmin etrex 10; coordinates stored as decimal degrees (lat, long) and altitude (meters).
- Altitude data incomplete for some sites; some sites are near sea level.
- A single position was recorded per sampling site; sampling occurred within ~2 km of this point.

## Specimen handling and storage
- On collection day: wings removed; bodies preserved in NaCl-saturated 20% DMSO with 0.25 M EDTA.
- All samples stored at the University of Sheffield.

## Data types and generation
- Genetic data:
  - RAD sequencing (single-digest, PstI) for 265 H. erato individuals (paired-end reads).
  - Whole-genome resequencing for 36 H. melpomene individuals.
  - Raw sequencing data deposited in the European Nucleotide Archive (ENA) under project PRJEB32848.
- Imaging data:
  - Digital wing photographs using a Nikon D7000 with standardized lighting and a colorchecker.
  - Up to two images per specimen: ventral and dorsal sides.
  - Ventral images named < specimenid >_ v _x; dorsal images named < specimenid >_ d _x.
  - Standardized imaging parameters: shutter 1/60 s, aperture f/10.

## Data files and access
- ENA project: PRJEB32848, with individual sample accessions documented in the file butterflyCollectionData2014to2016.csv.
- Data types available: genetic sequence data, sample metadata (locations, dates, sex, species, subspecies), and high-quality wing images.

## Data quality and curation
- Species identities corroborated by at least two experts; genetic data used to confirm in select cases.
- Metadata includes precise sampling locations, dates, and specimen identifiers to support traceability and reproducibility.
- Imaging and preservation standards applied to ensure consistent data quality for downstream analyses.

## Data stewardship and governance
- Data stored and managed with clear provenance (collection dates, locations, handling, storage conditions).
- Data released via ENA to support discoverability and interoperability.
- Documentation available through associated publication (Curran et al. 2020) to facilitate correct interpretation of methods and data.
- The dataset supports reuse for genetic, genomic, and phenotypic analyses of mimicry and population structure, with explicit attention to metadata completeness and standardization.

## Limitations and considerations for reuse
- Sampling was not standardized across days; varying effort and number of collectors may influence comparability.
- Altitude data missing for some sites, and there is a single position per site rather than per individual capture location.
- Some sampling sites are near sea level, which may affect habitat and population inferences.
- Researchers should account for non-uniform sampling design and potential sampling bias when reanalyzing population structure or clinal variation.

## Reference
- Curran, E.V., Stankowski, S., Pardo-Diaz, C., Salazar, C., Linares, M., Nadeau, N.J. 2020. Müllerian mimicry of a quantitative trait despite contrasting levels of genomic divergence and selection. Molecular Ecology. https://doi.org/10.1111/mec.15460