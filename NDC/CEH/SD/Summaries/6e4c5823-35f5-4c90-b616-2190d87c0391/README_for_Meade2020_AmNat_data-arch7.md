# Maintenance of fertility in the face of meiotic drive.

## Overview
- Investigates differences in fertility (egg hatch) between Teleopsis dalmanni females mated to SR vs ST males.
- Experimental design includes two mating-rate conditions (low: 1 female; high: 5 females) and unmated males as controls.
- Males (mated and unmated) were dissected to measure organ sizes; organ sizes are linked to fertility and/or mating rate in wild-type males.
- Data available as a CSV: Meade2020_AmNat_data.csv.
- Source: Meade et al., 2020, The American Naturalist (Note). Authors and contact emails provided.

## Data structure and variables
- male_id: Unique male identifier.
- females: Number of females the male mated with (0 = unmated, 1 = low rate, 5 = high rate).
- batch: Experimental batch identifier.
- eyespan: Male eyespan (mm).
- thorax: Thorax length (mm).
- testis: Testis area (mm^2).
- accessory_gland: Accessory gland area (mm^2).
- total_eggs: Total eggs laid by female(s) (fecundity).
- fertile_eggs: Total fertilised eggs laid by female(s) (fertility).
- comp162710: INDEL marker allele size (bp).
- ms395: Microsatellite marker allele size (bp).
- cnv395: INDEL marker allele size (bp).
- genotype: Male genotype (SR or ST), inferred from marker sizes (comp162710, ms395, cnv395).

## Experimental design details
- Males mated with 0, 1, or 5 females across 10 hours.
- Post-mate dissections conducted to obtain organ measurements.
- Outcomes include fecundity (total eggs) and fertility (fertilized eggs), with genotype context (SR vs ST) and mating-rate context.

## GIS-focused interpretation and applications
- Dataset is tabular with metadata suitable for GIS-style dashboards, even though it is not inherently geospatial.
- Mapping opportunities in GIS-like visuals:
  - Group comparisons by genotype (SR vs ST) across batches.
  - Visualize organ sizes, fecundity, and fertility distributions by mating-rate category.
  - Correlation maps or charts (e.g., organ size vs fertility) colored by genotype or batch.
- Potential to enrich with spatial or population-location data if integrated with geographic provenance (not present in current data).

## Data quality, cleaning and transformation
- Important steps for GIS workflows:
  - Ensure numeric data types for all measurement columns (eyespan, thorax, testis, accessory_gland, total_eggs, fertile_eggs, marker sizes).
  - Validate genotype assignment against marker sizes; document any uncertain classifications.
  - Handle missing values appropriately for analyses (e.g., imputation or removal).
  - Standardize units and scale (mm for measurements; ensure consistent column formats).
- Data originates from multiple experimental batches; account for batch effects in analyses.

## Provenance and access
- Source publication: Meade, Finnegan, Kad, Fowler, Pomiankowski (2020) Maintenance of fertility in the face of meiotic drive.
- DOI: https://doi.org/10.1086/707372
- Contact emails: a.pomiankowski@ucl.ac.uk, lara.meade.13@ucl.ac.uk.
- Data file: Meade2020_AmNat_data.csv.

## Usage notes and caveats
- The dataset captures fertility through egg hatch and fertilized eggs, with multiple biological and experimental factors (genotype, mating rate, batch).
- No explicit geographic locations are included; additional spatial context would require integration with external location data.
- When reusing, cite the original publication and dataset accordingly.