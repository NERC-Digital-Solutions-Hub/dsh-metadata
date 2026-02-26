# Survival and reproductive success of migrant and resident wildlife in published studies of partially migratory populations

- Purpose and scope
  - A dataset generated from information extracted from published studies to investigate fitness benefits of different migratory strategies in partially migratory populations.
  - Each data line includes a mean and associated variance for a fitness metric for both migrants and residents, plus study metadata (location, species, metric type, year collected, publication details).
  - Created as part of a NERC-funded PhD project (grant NE/L002582/1) by the School of Environmental Sciences, University of East Anglia.
  - Text is derived from the methods section of a manuscript to be published in the Journal of Animal Ecology (in press: “Fitness consequences of different migratory strategies in partially migratory populations: a multi-tax meta-analysis”).

- What the dataset contains
  - Fitness metrics directly tied to survival or reproductive success (direct fitness metrics); metrics considered indirect (e.g., body condition, egg size, etc.) are excluded.
  - For each study, extract means and standard deviations for both long-distance migrants and residents/short-distance migrants; where necessary, SDs are derived from SE or CIs, or digitized from graphs.
  - Metadata captured for each effect size: study/year, species, geographic location, migratory distance, and the specific fitness metric (classified as breeding success or survival; detailed subtypes provided for each category).
  - Structure supports a meta-analytic comparison of migrants versus residents (and short- versus long-distance migrants) across taxa.

- Literature search and inclusion criteria
  - Systematic search of studies (published before December 2017) using ISI Web of Science and Google Scholar; broad taxonomic scope.
  - Use a wide set of search terms related to partial migration, migration strategy, and fitness outcomes; supplemented by reference list checks and narrative reviews.
  - Inclusion criteria:
    - Comparisons between resident and migrant populations of the same species or between short- and long-distance migrants of the same species.
    - Outcomes are potential consequences of migratory strategy and ecologically tied to survival or reproductive success.
    - Direct fitness indicators; data must be extractable for calculating Hedges' d; raw data or model-predicted data allowed (experimental/theoretical models excluded).
    - Both direct data and model-predicted data are used; non-extractable or unsuitable data excluded.
  - To broaden scope, included short-distance versus long-distance comparisons in addition to resident versus migrant.

- Data extraction and handling
  - Means and standard deviations extracted for all qualifying results; when SDs were missing, calculated from SEs or CIs; logit transformations applied to bounded data as needed.
  - When data appeared only in graphical form, digitization software (WebPlotDigitizer) used to extract values.
  - For each effect size, capture: sample size, year(s) of data collection, species, study location, migratory distance, and fitness metric type (breeding success or survival).
  - Fitness metrics classified as:
    - Breeding metrics (e.g., clutch size, offspring survival, breeding success)
    - Survival metrics (e.g., absolute survival, growth rate)
  - Table 2 in the dataset documents the breakdown of direct fitness measures encountered.

- Data structure and schema
  - Key fields include:
    - ID, study, doi, studyyear, year, year.spread
    - taxogroup.new (bird, fish, mammal, herpetofauna)
    - species, hemisphere, country, latitude.dd, longitude.dd
    - n.mig (migrant sample size), n.res.sdm (resident/short-distance migrant sample size)
    - r.sdm.dist.km (distance traveled by residents/short-distance migrants)
    - new.ldm.distance (distance traveled by long-distance migrants)
    - percent.dist (distance proportion traveled by residents or short-distance migrants)
    - dist.saved (distance not traveled by short-distance migrants)
    - samplesize (total sample size for migrants and residents)
    - benefit (breeding or survival)
    - breeding / survival subtypes (e.g., for breeding: clutch size, offspring survival; for survival: absolute survival, growth rate, etc.)
    - r.sdm.mean / r.sdm.sd (mean and SD for residents/short-distance migrants)
    - ldm.mean / ldm.sd (mean and SD for long-distance migrants)

- Data sources and coverage
  - Dataset draws from a broad set of studies across taxa, including birds, fish, mammals, and amphibians; example sources include papers on: partial migration and life-history tradeoffs, survival benefits, and reproductive outcomes.
  - Representative cited studies and topics include: altitudinal migration effects, life-history correlates of migratory strategies, reproductive performance of migrants vs residents, and survival benefits in various partially migratory species.
  - The data compilation references a comprehensive bibliography (Data sources section) with numerous studies such as Bai et al. (2012), Bohlin et al. (2001), Grayson et al. (2011), Lok et al. (2011, 2015), Zúñiga et al. (2017), and many others.
  - Data collection involved both published articles and grey literature, with DOIs provided where available.

- Provenance, tools, and reproducibility
  - Data extraction and digitization relied on multiple tools to maximize coverage and accuracy:
    - WebPlotDigitizer (for graphs)
    - Data Miner (for Google Scholar harvesting)
  - The methodology includes supplementary searches of references and reviews to validate and extend results.
  - The dataset aims to support a multi-tax meta-analysis and facilitate future data products and public-facing insights into migratory strategies and fitness.

- Potential uses for Data Support archetype
  - Build dashboards or reports summarizing the fitness consequences of migratory strategies across taxa and regions.
  - Provide self-serve insights for policy makers or conservation planning by showing where migratory behavior correlates with survival or reproductive success.
  - Facilitate data quality assurance, cleaning, and integration with other datasets on wildlife migration and fitness.
  - Support replication or extension studies, meta-analyses, or comparative reviews across additional years or newly published studies.