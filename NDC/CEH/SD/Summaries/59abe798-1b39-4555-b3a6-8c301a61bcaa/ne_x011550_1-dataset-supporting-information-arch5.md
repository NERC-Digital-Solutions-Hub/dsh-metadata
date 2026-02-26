# A systematic map of studies testing the relationship between temperature and animal reproduction

- This dataset-compilation presents the results of a meta-analysis examining how temperature affects animal reproduction, including data and tools to reproduce the analyses.

## Overview
- Scope: Systematic collection of studies linking temperature to reproduction (and related longevity) across species.
- Content: Two CSV data files containing effect size data and two phylogenetic trees showing species relationships.
- Scale: Data from 339 studies covering 308 invertebrate species.
- Collaboration: Involvement of 30 researchers in data extraction.
- Purpose: Enables univariate and multivariate meta-analyses of temperature effects on life-history traits.

## Files and what they contain
- all_data.csv
  - Univariate meta-analysis data; each row represents a single comparison of a reference temperature vs. a treatment temperature.
  - Key metric: standardized mean difference in reproduction or longevity between reference and treatment temperatures.
- multivariate_data.csv
  - Subset of data where both reproduction and longevity were measured in the same individuals.
  - Each row includes two effect sizes (one for reproduction, one for longevity) and corresponding variances.
- reproduction_tree.nexus
  - Phylogenetic tree for species with reproduction data.
- longevity_tree.nexus
  - Phylogenetic tree for species with longevity data.

## Data structure and metadata (highlights)
- Core columns (examples of many included):
  - Paper.code, Paper.number, Paper, Publication.year, Title, DOI
  - Species.latin, Family, Class, Phylum
  - Sex.exposed, Fertilisation.mode, reproductive.mode
  - Lab.or.field, Animal.origin, Stressor.variation, Habitat, Habitat2, Mobility, Thermoregulation
  - Country.of.origin, Continent.of.origin, Ocean.sea.of.origin
  - Exposure.duration, Life.stage.of.animal, Lowest.temp.below.10.C, Constant.or.fluctuating, Acclimated
  - reftemp, treattemp, diff, warm.cool, c_treattemp
  - Trait.category, Trait, Sex, Rearing.temperature
  - es, v (overall effect size and variance)
  - es_reproduction, v_reproduction, es_longevity, v_longevity (for multivariate data)
- Purpose of fields: document study identity, taxonomic details, experimental design, temperature treatment details, life-history traits measured, and statistical results.

## Collection and quality control
- Method: Systematic literature search identifying studies that report temperature effects on both reproduction and longevity/survival for the same species where possible; data extraction performed from published papers.
- Scope of data collection: 339 studies; 308 invertebrate species.
- Data extraction collaborators: 30 researchers including Fay Frost and colleagues.
- Quality control: Data recorded and presented by study authors; extracted data checked prior to analysis by designated researchers (FF or LRD).

## Access, reuse, and governance considerations for Data Stewards
- Data formats: CSV files for data, NEXUS files for phylogenetic trees, suitable for ingestion into standard data portals and analysis pipelines.
- Provenance: Strong linkage between data rows and primary studies via Paper.code/Experiment.code; explicit trial-level details (reftemp, treattemp, diff) support reproducibility of meta-analyses.
- Metadata richness: Extensive column-level metadata enables accurate interpretation, filtering, and interoperability across platforms.
- Updates and versioning: Dataset represents a comprehensive map up to the cited compilation; future updates would require maintaining version history (e.g., new studies, updated metadata, revised effect sizes).
- Sharing considerations: Data can be uploaded to data portals and catalogues; clear documentation of column semantics and units will aid discoverability and reuse.
- Interoperability challenges: Heterogeneous study designs and temperature treatments; large data volume from many studies necessitates robust data governance and standardization of key fields (e.g., temperature units, trait definitions).

## End notes
- Reference: Dougherty, L. R. et al. (2024). A systematic map of studies testing the relationship between temperature and animal reproduction. Ecological Solutions and Evidence, 5(1), e12303. DOI: 10.1002/26888319.12303.