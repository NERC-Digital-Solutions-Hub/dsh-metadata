# Müllerian mimicry of a quantitative trait despite contrasting levels of genomic divergence and selection.

## Overview
- Describes data from a study on clinal variation in mimetic butterflies Heliconius erato and Heliconius melpomene in the Chocó-Darien ecoregion (Ecuador, Colombia, Panama).
- Sampling spanned five trips across 2014–2016, across multiple sites, with both genomic and image data collected for downstream analyses.

## Data collected and sampling design
- Sampling trips and locations:
  - May 2014 and May 2015 in Mashpi reserve, Pichincha, Ecuador.
  - January 2015 in Cauca Valley and Chocó, Colombia.
  - February 2015 in southwest Darien, Panama.
  - March 2016 in Chocó, Colombia.
- Specimens collected with hand nets, targeting Heliconius organisms with emphasis on H. melpomene and H. erato.
- Sampling effort was not standardized; variation in time and number of collectors across days.
- Species identities confirmed by at least two experts; genetic confirmation used in listed cases.
- Subspecies identities based on wing pattern phenotype; sex determined by genital morphology.

## Metadata, data types, and data standards
- Geolocation and site data:
  - GPS coordinates recorded with Garmin etrex 10; stored as decimal degrees (lat, long) and altitude (m).
  - One sampling position per site; samples collected within ~2 km of the recorded point.
  - Some sites lacked altitude data; many near sea level.
- Biological samples:
  - Wings removed on day of collection; bodies preserved in NaCl-saturated 20% DMSO with 0.25 M EDTA.
  - Specimens stored at the University of Sheffield.
- Genomic data:
  - Heliconius erato: single-digest, paired-end RAD sequencing (PstI) on 265 individuals.
  - Heliconius melpomene: whole-genome re-sequencing on 36 individuals.
  - Data deposited in European Nucleotide Archive under project PRJEB32848.
  - Individual sample accessions listed in butterflyCollectionData2014to2016.csv.
- Imaging data:
  - Digital wing photographs using Nikon D7000 with 40 mm macro lens; standardized lighting with two daylight fluorescent lights.
  - Shutter 1/60 s, aperture f/10; included X-Rite color checker in every shot.
  - Up to two images per specimen: dorsal and ventral wings.
  - File naming: ventral <specimenid>_v_x; dorsal <specimenid>_d_x.

## Data storage, provenance, and access
- Physical samples stored at the University of Sheffield.
- Genomic data available via European Nucleotide Archive (PRJEB32848).
- Metadata and accession details provided in butterflyCollectionData2014to2016.csv.

## Data quality, limitations, and considerations for reuse
- Non-standardized sampling effort may affect comparability across sites/time.
- Identity verification relied on expert assessment and selective genetic confirmation.
- Some site metadata (e.g., altitude) incomplete.
- Comprehensive documentation of procedures supports reuse for population genetics, landscape genetics, and phenotype-genotype association analyses.

## Potential uses and governance for data leadership
- Enables cross-site comparisons of clinal variation in mimicry phenotypes with genomic divergence.
- Supports integration with broader data networks through standardized metadata (GPS, site, sampling context) and deposited genomic and image data.
- Encourages reproducibility via explicit specimen identifiers, CSV with accession data, and detailed methodological notes.
- Highlights importance of data accessibility (ENA deposition, accession CSV) and clear data stewardship (storage at a single institution with defined custody).