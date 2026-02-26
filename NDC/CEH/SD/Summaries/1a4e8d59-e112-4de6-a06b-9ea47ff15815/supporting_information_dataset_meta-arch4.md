# Survival and reproductive success of migrant and resident wildlife in published studies of partially migratory populations

## Overview and purpose
- Dataset compiled to support a multi-tax meta-analysis on fitness benefits of different migratory strategies in partially migratory populations.
- Each line contains mean and variance for a fitness metric (for both migrants and residents), plus contextual data (location, species, metric, year, publication).
- Data collected as part of a NERC-funded PhD project; hosted by the School of Environmental Sciences, University of East Anglia.
- Document outlines methods, data structure, and the studies used; intended for publication in the Journal of Animal Ecology.

## Data content and scope
- Focuses on direct fitness outcomes related to survival or breeding success (excluding indirect metrics).
- Includes comparisons between residents and migrants within the same species (and short- vs long-distance migrants).
- Taxa represented include birds, fish, mammals, and herpetofauna; dataset encompasses a broad geographic range.
- Primary data items are means and standard deviations (or model-predicted equivalents) for each fitness measure, plus study and specimen details.

## Literature search and inclusion criteria
- Systematic literature search up to December 2017 using ISI Web of Science and Google Scholar.
- Search terms designed to capture partial migration and its fitness consequences; supplementary validation via reference lists and narrative reviews.
- Inclusion criteria:
  - Study compares resident and migrant (or short- vs long-distance migrant) within the same species.
  - Reported outcomes are potential fitness consequences (direct indicators of survival or breeding success).
  - Outcomes are directly interpretable as fitness; data are extractable for Hedge’s d.
  - Data are raw observations or model outputs fitted to raw data.
- Excludes studies with only indirect fitness proxies and those not meeting extractability criteria.

## Data extraction and processing
- Extracted means and standard deviations for all eligible results; SDs derived from SEs or CIs when needed.
- Graphical data digitized with WebPlotDigitizer (v4.1) when not reported numerically.
- When necessary, data transformed (e.g., logit for bounded data).
- For each effect size, captured: sample sizes, years of data collection, species, study location, migratory distance, and metric type (breeding success or survival).

## Data structure and fields
- Core data fields include:
  - ID, study, DOI, studyyear, year, year.spread
  - taxogroup.new (bird, fish, mammal, herpetofauna)
  - species, hemisphere, country
  - latitude.dd, longitude.dd
  - n.mig (migrant sample size), n.res.sdm (resident/short-distance migrant sample size)
  - r.sdm.dist.km (distance traveled by residents/short-distance migrants)
  - new.ldm.distance (distance traveled by long-distance migrants)
  - percent.dist (proportion of long-distance distance traveled by residents)
  - dist.saved (distance long-distance migrants travel beyond that of residents)
  - samplesize (total combined sample size)
  - benefit, breeding, survival (categorical detailing whether metric is breeding-related or survival-related)
  - for breeding: specific metric type; for survival: specific metric type
  - r.sdm.mean, r.sdm.sd (resident/short-distance migrant fitness measure and its SD)
  - ldm.mean, ldm.sd (long-distance migrant fitness measure and its SD)
- Data are organized to support direct comparisons of migrants vs residents across species and studies.

## Data sources and coverage
- Data sources comprise a wide set of published studies (examples include many avian, fish, and mammal system investigations).
- Each source listed with full citation; DOIs provided where available; grey literature included in the dataset.
- Table of data sources enumerates the referenced studies used for the analysis (e.g., Bai et al. 2012; Bohlin et al. 2001; Ely & Meixell 2016; etc.).

## Usage and context
- Dataset is designed to enable the calculation of effect sizes (e.g., Hedge’s d) for fitness differences between migratory strategies.
- Includes explicit metadata to support discoverability, reproducibility, and cross-study synthesis.
- Structured to support meta-analytic workflows across taxa and geographic regions, with clear separation between survival and breeding metrics.

## Notes for data governance and stewardship (Data Leaders perspective)
- Comprehensive metadata, including location, time, taxonomy, and metrics, enhances discoverability and reuse.
- Clear data model (two-level fitness outcomes: survival vs breeding) and standardized fields support consistent analyses and future updates.
- Data quality is strengthened by explicit inclusion criteria, handling of missing SDs, and digitization of graphical data.
- The dataset represents a robust, cross-study asset suitable for integration into broader data ecosystems and collaborative analyses; scope limited to data available up to 2017 (subject to future updates).