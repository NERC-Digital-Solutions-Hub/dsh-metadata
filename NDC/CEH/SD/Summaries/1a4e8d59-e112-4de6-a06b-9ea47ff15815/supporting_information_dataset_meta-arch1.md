# Supporting document for dataset: Survival and reproductive success of migrant and resident wildlife in published studies of partially migratory populations

## Overview
- A dataset compiled from published studies to support a meta-analysis on fitness benefits of different migratory strategies in partially migratory populations.
- Each data line includes a mean and associated variance for a fitness metric for both migrants and residents, plus metadata on population location, study species, metric type, data collection year, and publication details.
- Funded by a NERC PhD project (NE/L002582/1) and produced by the School of Environmental Sciences, University of East Anglia.
- Documentation describes how the dataset was constructed, its structure, and the studies used; based on methods for a forthcoming Journal of Animal Ecology paper.

## Literature search and study identification
- Systematic search of studies on fitness benefits of migratory strategies published before December 2017.
- Databases: ISI Web of Science and Google Scholar; broad taxonomic scope without group restrictions.
- Supplemental validation: reference lists and narrative reviews; expanded keyword searches to capture taxonomic groups with different migration terminology (e.g., diadromy in fish).

## Data inclusion and exclusion criteria
- Included studies that compare:
  - resident vs migrant populations of the same species, or
  - short-distance vs long-distance migrants of the same species.
- Focused on outcomes considered potential consequences of migratory strategy and ecologically beneficial/detrimental to survival or reproductive success.
- Only direct indicators of fitness were included; excluded indirect metrics (e.g., body condition, growth efficiency) and non-extractable data.
- Required extractable data for calculating Hedges' d; data could be raw observations or model-predicted from raw data (experimental data and theoretical models excluded).
- Both resident-migrant and short-distance vs long-distance migrant contrasts were included.

## Data extraction and handling
- Means and standard deviations extracted for all qualifying results; SDs derived from available SDs, standard errors, or confidence intervals when needed.
- When data were only in graphs, digitized using WebPlotDigitizer (v4.1).
- Captured for each effect size: sample size, data collection years, species, study location, migratory distance, and type of fitness metric (breeding success or survival).
- Fitness metrics categorized as:
  - Survival (e.g., absolute survival, survival-related measures)
  - Breeding success (e.g., clutch size, offspring survival, breeding success metrics)
- Table 2 in the document provides the breakdown of direct fitness measures into survival vs breeding metrics.

## Data structure and fields
- Core identifiers and metadata: id, study, doi, studyyear, year, year.spread.
- Taxonomic classification: taxogroup.new (herpetofauna, bird, fish, mammal).
- Biological and geographic data: species, hemisphere, country, latitude, longitude.
- Migrant and resident sampling: n.mig, n.res.sdm; r.sdm.dist.km (distance for residents/short-distance migrants); new.ldm.distance (distance for long-distance migrants); percent.dist; dist.saved.
- Sample size and fitness context: samplesize; benefit (two-level: breeding or survival); breeding (detailed metric if applicable); survival (detailed metric if applicable).
- Effect size data: r.sdm.mean, r.sdm.sd (residents/short-distance migrants); ldm.mean, ldm.sd (long-distance migrants).
- Data sources: a comprehensive list of primary studies used.

## Data sources and references
- Includes numerous primary studies across birds, fishes, mammals, and herpetofauna (e.g., American dippers, spoonbills, white storks, loggerhead sea turtles, elk, moose, salmon/trout species, and others).
- Cited works and tools referenced (e.g., Chapman et al. 2011; Stewart et al. 2007; Data Miner; WebPlotDigitizer).

## Analytical and practical notes
- Data prepared to enable calculation of effect sizes (Hedges' d) for direct fitness measures, enabling comparative meta-analysis across taxa and studies.
- Recognizes heterogeneity due to taxon differences and varying fitness metrics; data standardization and careful interpretation needed in analyses.
- Emphasizes accessibility of data through careful documentation of study details, locations, and metrics to support reproducibility and potential data reuse.