# Maintenance of fertility in the face of meiotic drive

## Overview
- Investigates differences in fertility (egg hatch) in Teleopsis dalmanni when females mate with SR or ST genotype males.
- Males mated with either one, five, or zero ( unmated) females over a 10-hour period.
- Post-mating, a subset of males were dissected to measure reproductive organ sizes (testes and accessory glands), which are known to correlate with fertility and mating rate.
- Data are provided to link male genotype and mating rate with fertility outcomes and morphological traits.

## Dataset and provenance
- Data source: Meade, L., Finnegan, S., Kad, R., Fowler, K., Pomiankowski, A. (2020). Maintenance of fertility in the face of meiotic drive. The American Naturalist Note. DOI: https://doi.org/10.1086/707372
- Data file: Meade2020_AmNat_data.csv
- Authors and contact: a.pomiankowski@ucl.ac.uk; lara.meade.13@ucl.ac.uk

## Experimental design and variables
- Objective: Compare fertility between SR and ST genotypes, with the effect of mating rate considered.
- Mating conditions:
  - Mated males: 1 or 5 females
  - Unmated males: 0 females (dissection data included)
- Measurements:
  - Male morphological traits: eyespan (mm), thorax length (mm)
  - Reproductive organ sizes: testis area (mm^2), accessory gland area (mm^2)
  - Female fertility outcomes: total eggs laid, fertilised (fertile) eggs
- Genotype determination: SR or ST assigned using marker data (comp162710, ms395, cnv395)

## Column headers and measurement details
- male_id: Unique identifier for each male
- females: Number of females mated with over 10 hours; values 0 (unmated), 1 (low rate), or 5 (high rate)
- batch: Experimental batch
- eyespan: Eye span in millimeters (mm)
- thorax: Thorax length in millimeters (mm)
- testis: Testis area in square millimeters (mm^2)
- accessory_gland: Accessory gland area in square millimeters (mm^2)
- total_eggs: Total eggs laid by the associated females
- fertile_eggs: Number of fertilised eggs laid
- comp162710: INDEL marker allele size in base pairs (bp)
- ms395: Microsatellite marker allele size in bp
- cnv395: INDEL marker allele size in bp
- genotype: Male genotype (SR or ST), assigned using the marker sizes

## Data management and reuse considerations
- Metadata clarity: clear definitions and units for all measurements (mm, mm^2) and explicit mating-rate coding.
- Provenance: dataset linked to a peer-reviewed note with DOI; contact information provided for clarifications.
- Discoverability and accessibility: data described with explicit column definitions; stored as a CSV file for easy reuse.
- Data quality and integrity: measurements from experimental batches; potential batch effects to consider; ensure genotype assignments are reproducible via markers.
- Governance and collaboration: transparency about experimental design supports cross-study comparisons and integration with broader data communities; encourages documentation of methods and any data updates.

## Relevance for data strategy (Data Leaders)
- Demonstrates management of a multi-faceted data asset: experimental design metadata, morphological measurements, and fertility outcomes linked to genetic markers.
- Highlights importance of comprehensive metadata to enable reuse across networks and by policy/analytical colleagues who may rely on reproducibility and data provenance.
- Emphasizes need for data standards (units, variable definitions, and genotype assignment methods) to reduce barriers to data discovery, verification, and integration with related datasets.
- Illustrates practical considerations in data access, discovery, and coordination across experimental batches, aligning with aims to support a broader data system and communities of practice.