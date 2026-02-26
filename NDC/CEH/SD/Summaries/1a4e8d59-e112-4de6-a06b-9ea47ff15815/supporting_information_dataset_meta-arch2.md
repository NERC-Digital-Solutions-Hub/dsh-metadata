# Survival and reproductive success of migrant and resident wildlife in published studies of partially migratory populations

## Overview
- Purpose: A dataset generated from published studies to support a meta-analysis on fitness benefits of different migratory strategies in partially migratory populations.
- Content per line: mean and variance for a fitness metric for both migrants and residents, plus population location, study species, metric type, data year, and publication details.
- Project and funding: part of a NERC-funded PhD project (NE/L002582/1) at the School of Environmental Sciences, University of East Anglia, Norwich, UK.
- Scope: Methods, dataset structure, and list of data sources are documented; text drawn from the methods section of an in-press Journal of Animal Ecology manuscript.

## Data collection and sources
- Literature search: systematic search up to December 2017 using ISI Web of Science and Google Scholar; broad taxonomic coverage; supplementary searches of references and reviews; terminology extended to alternative migration terms (e.g., diadromy).
- Inclusion of studies: screened abstracts and full texts to identify those potentially meeting criteria; supplementary searches to validate results.
- Data sources: extensive list of studies used for data extraction (detailed in the document).

## Inclusion criteria
- Comparisons: resident vs migrant populations of the same species, or short- vs long-distance migrants of the same species.
- Outcomes: measures identified as potential fitness consequences (direct indicators of survival or breeding success).
- Data requirements: extractable data for calculating Hedge’s d; data must be raw observations or model predictions based on raw data (not purely theoretical models).
- Metrics: focus on direct fitness measures; survival and breeding metrics are prioritized, with explicit exclusions for indirect metrics (e.g., body condition, egg size, etc.).
- Scope: includes both resident–migrant and short–long distance comparisons; rates are interpreted as direct fitness indicators.

## Data extraction and structure
- Extraction methods: means and standard deviations extracted; SDs derived from SEs or CIs when missing; graphical data digitized using WebPlotDigitizer.
- Metadata captured for each effect size: study year(s), species, study location, migratory distance, sample sizes, and type of fitness metric (breeding success or survival).
- Fitness metric categorization (Table 2): 
  - Survival metrics (e.g., absolute survival, survival-related measures)
  - Breeding metrics (e.g., clutch size, surviving offspring, breeding success)
- Data structure and fields: 
  - ID, study, DOI, studyyear, year, year.spread
  - taxogroup.new (bird, mammal, fish, herpetofauna)
  - species, hemisphere, country, latitude.dd, longitude.dd
  - n.mig, n.res.sdm, r.sdm.dist.km, new.ldm.distance, percent.dist, dist.saved
  - samplesize
  - benefit (breeding vs survival), breeding (sub-metric type) or survival (sub-metric type)
  - r.sdm.mean, r.sdm.sd, ldm.mean, ldm.sd
- Intended outputs: dataset structured to support a multi-taxonomic meta-analysis of fitness consequences across studies.

## Data sources and references
- Primary data sources: numerous studies across birds, mammals, fish, and other taxa (examples include Bai et al. 2012; Bohlin et al. 2001; Ely & Meixell 2016; Grayson et al. 2011; Lok et al. 2011, 2015; Zúñiga et al. 2017, among many others).
- Key cited works and methodological references: Chapman et al. 2011; Reid et al. 2018; Stewart et al. 2007; Rohatgi 2018; Data Miner 2017; Google 2018.
- Data provenance: the document lists a comprehensive set of data sources used for extraction and subsequent meta-analysis.

## Data use and outputs
- Purpose of the dataset: to enable a multi-taxonomic meta-analysis of fitness consequences associated with migratory strategies in partially migratory populations.
- Documentation basis: the methods section of the manuscript “Fitness consequences of different migratory strategies in partially migratory populations: a multi-tax meta-analysis” (in press in Journal of Animal Ecology).
- Data management: structured data with explicit metadata fields and standardized fitness metrics to facilitate cross-study comparisons and synthesis.