# Maintenance of fertility in the face of meiotic drive

## Overview
- Investigates differences in fertility, measured by egg hatch, when Teleopsis dalmanni females are mated to SR vs ST genotype males.
- Males mated with either one (low mating rate) or five (high mating rate) females; unmated males were also dissected.
- Dissections targeted testes and accessory glands sizes, which are correlated with fertility and/or mating rate in wild-type males.

## Experimental design
- Species: Teleopsis dalmanni (stalk-eyed fly).
- Genotype determination: SR or ST assigned using markers comp162710, ms395, and/or cnv395.
- Mating treatments: mated with 1 or 5 females; includes unmated males.
- Measurements:
  - Morphometrics: eyespan, thorax length.
  - Reproductive organs: testis area, accessory gland area.
  - Reproductive output: total eggs laid by females, fertilised (fertile) eggs.

## Data structure / dataset
- Data file: Meade2020_AmNat_data.csv.
- Authors and publication: Meade, Finnegan, Kad, Fowler, Pomiankowski (2020); The American Naturalist.
- Contact emails: a.pomiankowski@ucl.ac.uk, lara.meade.13@ucl.ac.uk.
- Columns:
  - male_id: unique identifier for each male.
  - females: number of females the male mated with (0 = unmated; 1 or 5 = mated).
  - batch: experimental batch.
  - eyespan: male eyespan (mm).
  - thorax: male thorax length (mm).
  - testis: testis area (mm^2).
  - accessory_gland: accessory gland area (mm^2).
  - total_eggs: total eggs laid by female(s).
  - fertile_eggs: fertilised eggs laid by female(s).
  - comp162710: INDEL marker allele size (bp).
  - ms395: Microsatellite marker allele size (bp).
  - cnv395: INDEL marker allele size (bp).
  - genotype: male genotype (SR or ST) inferred from marker sizes.