# Maintenance of fertility in the face of meiotic drive

## Objective
- Investigates differences in fertility (egg hatch) between Teleopsis dalmanni females mated to SR or ST genotype males.
- Assesses how mating rate (one vs five females) and male morphology/organ sizes relate to fertility outcomes.

## Dataset and provenance
- Source: Meade, L.; Finnegan, S.; Kad, R.; Fowler, K.; Pomiankowski, A. 2020. Maintenance of fertility in the face of meiotic drive. The American Naturalist.
- Dataset file: Meade2020_AmNat_data.csv
- DOI: https://doi.org/10.1086/707372
- Contact emails: a.pomiankowski@ucl.ac.uk; lara.meade.13@ucl.ac.uk

## Experimental design
- Males mated with either:
  - One female (low mating rate) or five females (high mating rate)
  - Unmated males included as controls
- Post-mating dissections to measure reproductive organ sizes (testes and accessory glands)

## Variables and measurements
- male_id: Unique male identifier
- females: Number of females mated with (0 = unmated, 1 = low, 5 = high)
- batch: Experimental batch
- eyespan: Eye span length (mm)
- thorax: Thorax length (mm)
- testis: Testis area (mm²)
- accessory_gland: Accessory gland area (mm²)
- total_eggs: Total eggs laid by female(s)
- fertile_eggs: Fertilised eggs laid by female(s)
- comp162710: INDEL marker allele size (bp)
- ms395: Microsatellite marker allele size (bp)
- cnv395: INDEL marker allele size (bp)
- genotype: Male genotype (SR or ST), assigned from the marker sizes

## Genotype determination and markers
- Genotype (SR vs ST) assigned using combinations of comp162710, ms395, and/or cnv395 allele sizes

## Potential analyses and outputs
- Assess effects of male genotype (SR vs ST) and mating rate on fertility outcomes and organ sizes
- Explore associations between morphological measures (eyespan, thorax) and reproductive metrics (testis/ampulla sizes, egg counts)
- Link molecular marker data to genotype validation and analytic categorization

## Data availability and usage notes
- Data comprise a standardised CSV with both phenotypic and genotypic measurements
- Suitable for integrative analyses and cross-study comparisons; reflect transparent data provenance
- For details, refer to the cited publication and contact authors via provided emails