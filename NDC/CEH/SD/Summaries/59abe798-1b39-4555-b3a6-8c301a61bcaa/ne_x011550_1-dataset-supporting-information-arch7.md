# A systematic map of studies testing the relationship between temperature and animal reproduction

## Overview
- A dataset collection for meta-analyses of how temperature affects animal reproduction.
- Contains data needed to replicate analyses and to create map-based data products for viewing spatial and taxonomic patterns.
- Based on a systematic literature search covering 339 studies across 308 invertebrate species, with data contributed by 30 researchers.

## What is in the dataset
- all_data.csv: Univariate effect sizes for reproductive or longevity outcomes; one row per study comparison; key metric is the standardized mean difference between a reference temperature and an experimental temperature.
- multivariate_data.csv: Subset where both reproduction and longevity were recorded in the same individuals; each row includes two effect sizes (one for reproduction, one for longevity) for multivariate analyses.
- reproduction_tree.nex: Phylogenetic tree for species with reproduction data.
- longevity_tree.nex: Phylogenetic tree for species with longevity data.

## Data collection and scope
- Systematic literature search identified studies reporting temperature effects on reproduction and longevity for the same species.
- Data extracted from 339 studies covering 308 invertebrate species.
- Involvement: ~30 researchers contributed to data extraction.
- For each study, means and associated variances for life-history traits at each reported temperature treatment were captured.

## Data structure and key fields
- Core dataset columns (examples):
  - Paper.code, Paper.number, Paper, Publication.year, Title, DOI
  - Species.latin, Family, Class, Phylum
  - Sex.exposed, Fertilisation.mode, reproductive.mode
  - Lab.or.field, Animal.origin, Habitat, Habitat2, Mobility, Thermoregulation
  - Country.of.origin, Continent.of.origin, Ocean.sea.of.origin
  - Exposure.duration, Life.stage.of.animal, Rearing.temperature
  - Lowest.temp.below.10.C, Constant.or.fluctuating, Acclimated
  - Treatment details: diff, reftemp, treattemp, warm.cool, c_treattemp
  - Effect sizes: es_reproduction, v_reproduction, es_longevity, v_longevity
  - es (overall), v (variance for overall)
  - es_reproduction/v_reproduction and es_longevity/v_longevity as applicable
- Data are structured to support both univariate and multivariate meta-analyses; allow linking to geographic and ecological characteristics for GIS mapping.
- Geographic and ecological fields enable mapping by origin, habitat type, and potential exposure contexts.

## Quality control and provenance
- Data checked for accuracy by Fay Frost (FF) or LRD prior to analyses.
- Quality relies on the original study authors for data transcription; cross-checks performed during cleaning.

## GIS-relevant considerations and usage
- Mapping opportunities
  - Visualize study origins by country/continent and aquatic vs. terrestrial habitats.
  - Map species distributions and origins alongside temperature treatment ranges.
  - Display multivariate results (reproduction vs. longevity) for species where both were measured.
  - Overlay study data with climate datasets to explore temperature exposure contexts.
- Data integration challenges
  - Data are drawn from many sources with varying resolutions and standards.
  - Large, complex datasets require careful cleaning and transformation for GIS workflows.
  - Some fields are study- or species-specific; missing values are common.
- Phylogenetic context
  - Reproduction and longevity trees provide evolutionary context that can enrich spatial analyses when combined with GIS layers.

## Access and usage notes
- Files available:
  - all_data.csv
  - multivariate_data.csv
  - reproduction_tree.nex
  - longevity_tree.nex
- Reference for the dataset: Dougherty, L. R., Frost, F., Maenpaa, M. I., Rowe, M., Cole, B. J., et al. (2024). A systematic map of studies testing the relationship between temperature and animal reproduction. Ecological Solutions and Evidence, 5(1), e12303.

## Authors
- Fay Frost; Daniel W. A. Noble; Mads Schou; Melissah Rowe; Jasper Rees; Stefan Lüpold; Amber Chatten; Claire Smithson; Benjamin J. Cole; Pedro Simões; Ina Lindenbaum; Mareike Koppik; Hester Weaving; Berta Canal Domenech; Emily Churchill; Z. Valentina Zizzari; Jacintha Ellers; Sofia Gigliotti; Marco Graziano; Graziella Iossa; Alessio N. De Nardo; Natalie Pilakouta; Abhishek Meena; Steven A. Ramm; Shinichi Nakagawa; Amanda Bretman; Claudia Fricke; Rhonda R. Snook; Tom A.R. Price; Liam R. Dougherty.