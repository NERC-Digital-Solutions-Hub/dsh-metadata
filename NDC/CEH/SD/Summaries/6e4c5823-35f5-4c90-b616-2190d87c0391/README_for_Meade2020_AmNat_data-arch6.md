# Maintenance of fertility in the face of meiotic drive

## Overview
- Investigates differences in fertility (egg hatch) when Teleopsis dalmanni females mate with SR or ST genotype males.
- Experimental setup: males mated to one (low mating rate) or five (high mating rate) females; mated and unmated males dissected to measure testes and accessory gland sizes.
- Organ sizes are linked to fertility and/or mating rate in wild-type males.
- Data provided as a single CSV file: Meade2020_AmNat_data.csv, with column explanations below.

## Dataset origin and access
- Source: Meade, L.; Finnegan, S.; Kad, R.; Fowler, K.; Pomiankowski, A. 2020. Maintenance of fertility in the face of meiotic drive. The American Naturalist (Note).
- DOI: https://doi.org/10.1086/707372
- Contact: a.pomiankowski@ucl.ac.uk; lara.meade.13@ucl.ac.uk
- File: Meade2020_AmNat_data.csv

## Experimental design
- Subject: Teleopsis dalmanni (flies).
- Genotype comparison: SR vs ST male genotypes.
- Mating treatments: 1 mate (low rate) or 5 mates (high rate); includes unmated males.
- Measurements per male: male morphology, reproductive organ sizes, and female fecundity/fertility outcomes.
- Outcome measures: total eggs laid by females (total_eggs) and fertilised eggs (fertile_eggs).

## Variables and column headers (with brief descriptions)
- male_id: Unique identifier for each male.
- females: Number of females the male was allowed to mate with over a 10-hour period (0 = unmated, 1 = low rate, 5 = high rate).
- batch: Experimental batch.
- eyespan: Male eyespan (mm).
- thorax: Male thorax length (mm).
- testis: Testis area (mm^2).
- accessory_gland: Accessory gland area (mm^2).
- total_eggs: Total number of eggs laid by female(s) (fecundity).
- fertile_eggs: Total number of fertilised eggs laid by female(s) (fertility).
- comp162710: INDEL marker allele size (bp).
- ms395: Microsatellite marker allele size (bp).
- cnv395: INDEL marker allele size (bp).
- genotype: Male genotype (SR or ST) assigned using comp162710, ms395 and/or cnv395 allele sizes.

## Data preparation and interpretation notes
- Units:
  - Eyespan and thorax are in millimeters (mm).
  - Testis and accessory_gland are in square millimeters (mm^2).
  - Allele sizes are in base pairs (bp).
- Genotype assignment relies on allele sizes from multiple markers (comp162710, ms395, cnv395).
- Data can be used to explore relationships between genotype, mating rate, morphology, and fertility outcomes.

## Potential analyses and data products
- Explore associations between SR vs ST genotype and fertility outcomes (fertile_eggs) controlling for mating rate and morphology (eyespan, thorax, organ sizes).
- Assess how morphometrics and gonad sizes relate to fecundity (total_eggs) and fertility (fertile_eggs).
- Compare unmated, low-rate, and high-rate treatments to understand mating effects on reproductive metrics.
- Create self-serve data products (dashboards/pivot tables) to examine genotype effects across batches and on organ sizes.
- Document and promote data reuse by sharing code or prototypes for calculating fertility indices from the provided variables.