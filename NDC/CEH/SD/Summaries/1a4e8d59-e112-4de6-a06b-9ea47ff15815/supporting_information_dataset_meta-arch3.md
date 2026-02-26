# Survival and reproductive success of migrant and resident wildlife in published studies of partially migratory populations

- Purpose and scope
  - A dataset generated from information extracted from published studies to support a meta-analysis on fitness benefits of different migratory strategies in partially migratory populations.
  - Aims to compare migrants and residents (and also short-distance vs long-distance migrants) across species to assess direct fitness consequences (survival and reproductive success).

- Dataset content
  - Each data line includes a mean and associated variance for a given fitness metric for both migrants and residents, plus metadata on population location, study species, metric type, data collection year, and publication details.
  - Data collected as part of a NERC-funded PhD project (grant NE/L002582/1) at the School of Environmental Sciences, University of East Anglia.

- Data structure and metadata
  - Comprehensive schema with fields such as:
    - id, study, doi, studyyear, year, year.spread, taxogroup.new (herpetofauna, bird, fish, mammal), species, hemisphere, country, latitude/longitude
    - n.mig (migrant sample size), n.res.sdm (resident/short-distance migrant sample size)
    - r.sdm.mean/sd (resident/short-distance migrant fitness mean and SD), ldm.mean/sd (long-distance migrant fitness mean and SD)
    - dist parameters (new.ldm.distance, percent.dist, dist.saved)
    - benefit (breeding vs survival), and subcategories (breeding or survival detail)
  - Data sources listed and linked to the corresponding study for traceability.

- Data sources and literature coverage
  - Data drawn from a broad literature base, with a detailed list of data sources (e.g., multiple bird, fish, mammal, and amphibian studies) provided in the dataset.
  - Literature search spanned studies published prior to December 2017.

- Literature search and study inclusion
  - Systematic search of ISI Web of Science and Google Scholar using predefined terms (with supplementary searches of references and reviews) to identify relevant studies on partial migration and fitness outcomes.
  - Inclusion/exclusion criteria applied in two stages:
    - Abstract screening followed by full-text screening.
    - Included studies: comparisons of resident vs migrant or short-distance vs long-distance migrants within the same species; reported outcomes linked to potential fitness consequences; direct indicators of fitness; extractable data to compute effect sizes (Hedges' d); data either raw or model-predicted.
  - Included both resident-migrant and short-distance/long-distance migrant comparisons to capture the spectrum of migratory differences.

- Data extraction and handling of effect sizes
  - Extracted means and standard deviations for all eligible results; when only model outputs or predicted values were available, these were used.
  - When SDs were missing, derived from SEs or confidence intervals; bounded data logit-transformed as needed.
  - For results reported graphically, data were digitized using WebPlotDigitizer.
  - For each effect size, recorded study year(s), species, location, migratory distance, and the specific fitness metric (breeding success or survival).

- Fitness metrics and categorization
  - Direct fitness measures categorized into two main groups:
    - Survival-related metrics (e.g., absolute survival, survival-related measures)
    - Breeding-related metrics (e.g., clutch size, offspring survival, breeding success)
  - A structured table (Table 2) documents the specific metric types encountered and their classification as survival or breeding related.

- Data quality and governance considerations
  - Emphasizes transparent metadata for traceability of each data point (study, location, species, year).
  - Metadata-rich structure facilitates verification, replication, and potential future updates or re-analyses.
  - Data extraction and digitization methods are documented to support data provenance and reuse.

- Documentation and provenance
  - Text derived from the methods section of a manuscript to be published in the Journal of Animal Ecology (in press): "Fitness consequences of different migratory strategies in partially migratory populations: a multi-tax meta-analysis."
  - Provides a formal data appendix describing data structure, sources, and extraction procedures to support reproducibility.