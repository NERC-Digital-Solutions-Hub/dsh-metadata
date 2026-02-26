# Maintenance of fertility in the face of meiotic drive

## Overview
- Investigates the difference in fertility, measured as egg hatch, between Teleopsis dalmanni females mated to SR or ST genotype males.
- Experimental design included males mated with one (low mating rate) or five (high mating rate) females; unmated males were also dissected.
- Dissections measured testes and accessory glands; organ sizes are linked to fertility and mating rate in wildtype males.
- Dataset supports understanding how genotype and mating rate influence fertility and related anatomical traits.

## Dataset details

- Source and publication context
  - Authors: Meade, L.; Finnegan, S.; Kad, R.; Fowler, K.; Pomiankowski, A.
  - Year: 2020
  - Title: Maintenance of fertility in the face of meiotic drive
  - Publication: The American Naturalist (Note)
  - DOI: https://doi.org/10.1086/707372
  - Contact emails: a.pomiankowski@ucl.ac.uk, lara.meade.13@ucl.ac.uk

- Data file
  - File name: Meade2020_AmNat_data.csv
  - Format: CSV

- Study design and variables
  - mated vs unmated status: females permitted to mate with 0, 1, or 5 males (column: females)
  - Batch: experimental batch identifier
  - Morphometrics: 
    - eyespan (mm)
    - thorax (mm)
  - Reproductive organs (area in mm^2):
    - testis
    - accessory_gland
  - Reproductive output:
    - total_eggs (fecundity)
    - fertile_eggs (fertility)
  - Genotype determination (marker-based):
    - comp162710 (INDEL, bp)
    - ms395 (Microsatellite, bp)
    - cnv395 (INDEL, bp)
    - genotype (SR or ST) determined from the above allele sizes

## Data contents and metadata guidance

- Key identifiers
  - male_id: unique identifier for each male

- Experiment conditions
  - batch: experimental batch
  - females: number of females allowed to mate (0 = unmated, 1 = low mating rate, 5 = high mating rate)

- Measurements and units
  - eyespan: mm
  - thorax: mm
  - testis: mm^2
  - accessory_gland: mm^2
  - total_eggs: count of eggs laid by females
  - fertile_eggs: count of fertilised eggs

- Genotyping
  - genotype is SR or ST, assigned using allele sizes from comp162710, ms395, and/or cnv395

## Data governance and stewardship notes

- Provenance and documentation
  - Data are tied to a published note with explicit study design and measurement context.
  - Clear data file naming and in-line metadata for columns support discoverability and reuse.

- Standards and interoperability
  - Uses explicit units and clearly defined headers (e.g., mm, mm^2, bp) to support interoperability.
  - Genotype assignment relies on multiple molecular markers, providing a reproducible method for determining SR vs ST.

- Accessibility and reuse
  - CSV format facilitates reuse in common data analysis environments.
  - Contact authors provided for data questions or clarification.

- Considerations for ongoing data management
  - Ensure metadata remains aligned with any future updates or re-releases.
  - If adding-derived or updated data, maintain linkage to the original study and dataset file.
  - Consider cataloguing in a central data portal with the DOI to enhance discoverability and proper attribution.

## Usage guidance for researchers and data stewards

- Suitable for reanalysis of fertility differences by genotype and mating rate, and for correlating organ sizes with reproductive outcomes.
- Use the detailed column definitions and units to ensure consistent interpretation across studies.
- When integrating with other datasets, align genotype determination methods and ensure consistent measurement scales (mm, mm^2, bp).
- If disseminating derivatives, retain original identifiers (male_id, batch, genotype) to preserve traceability to the source data.