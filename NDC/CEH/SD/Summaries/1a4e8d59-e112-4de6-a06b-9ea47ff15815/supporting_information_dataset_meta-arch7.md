# Survival and reproductive success of migrant and resident wildlife in published studies of partially migratory populations

- Purpose: A dataset compiled from published studies to support a meta-analysis of fitness benefits of different migratory strategies in partially migratory populations. Each data line includes a mean and variance for a fitness metric for both migrants and residents, plus population location, study species, metric type, data year, and publication details. Developed during a NERC-funded PhD project (NE/L002582/1) at the School of Environmental Sciences, University of East Anglia.

- Document scope: This document describes the methods used to construct the dataset, the data structure, and the studies from which data were extracted. Text is drawn from the methods section of a manuscript in press in the Journal of Animal Ecology.

- GIS-relevant context:
  - Geography fields: latitude, longitude, country, hemisphere, and study location enable geospatial mapping of study sites and migratory distances.
  - Taxonomic and ecological breadth: four broad taxonomic groups (herpetofauna, birds, fish, mammals) allow regional or habitat-level GIS analyses.
  - Temporal and spatial resolution: study year, year spread, and migration distance provide layers for spatiotemporal visualization and distance-based analyses of fitness outcomes.

- Literature search and data inclusion (overview for GIS planning):
  - Systematic literature search up to December 2017 using ISI Web of Science and Google Scholar; supplemented by reference lists and targeted keyword variations (e.g., diadromy).
  - Inclusion criteria focused on studies that compare residents vs. migrants (or short-distance vs. long-distance migrants) within the same species, measure fitness-related outcomes, and provide extractable data for effect sizes (Hedges' d). Direct fitness indicators prioritized; indirect metrics were excluded.
  - Included data cover direct fitness measures related to survival or breeding success; survival and breeding metrics are categorized accordingly.

- Data extraction and processing (GIS data preparation):
  - Extraction of means and standard deviations for all eligible results; SDs derived from raw data when available, or from standard errors/CI when needed. Graphically reported data digitized with WebPlotDigitizer.
  - When SDs missing, calculated from SE or CIs; bounded data logit-transformed before calculations.
  - For each effect size, recorded: study, species, location, migratory distance, year(s) of data collection, and type of fitness metric (breeding success or survival). Fitness metrics are categorized into specific measures (Table 2 in the document).
  - Data structure fields (selected highlights):
    - id, study, doi, studyyear, year, year.spread
    - taxogroup.new, species, hemisphere, country, latitude.dd, longitude.dd
    - n.mig, n.res.sdm, r.sdm.dist.km, new.ldm.distance, percent.dist, dist.saved
    - samplesize, benefit, breeding, survival
    - r.sdm.mean, r.sdm.sd, ldm.mean, ldm.sd
  - Data sources: data were drawn from a broad set of published studies across taxa (e.g., birds, fish, mammals, amphibians) and include both peer-reviewed articles and grey literature.

- Data sources and references (structure for GIS attribution):
  - Data sources comprise numerous studies on partial migration and fitness outcomes (example references include works on American dippers, brown trout, tundra swans, spoonbills, loggerhead sea turtles, moose, and many others).
  - Key methodological and data-source references support search strategy, inclusion criteria, and data extraction practices (e.g., Chapman et al. on partial migration; Stewart et al. on evidence bases; data digitization tools).

- Data usage and outputs (GIS-oriented implications):
  - The dataset enables geospatial analyses of how migratory strategy relates to fitness across species and regions.
  - Facilitates mapping of study sites, migratory distance contrasts, and regional patterns in survival or breeding success.
  - Supports meta-analytic exploration of fitness benefits by taxogroup, habitat, or geographic region, with the ability to layer coordinates, distances, and effect sizes in GIS.

- Limitations and considerations for GIS work:
  - Data cover studies published up to 2017; newer studies would not be included.
  - Heterogeneity in fitness metrics and study designs across taxa may require harmonization before spatial modeling.
  - Some data are derived from models or digitized from graphs, introducing potential uncertainty in spatial and effect-size representations.
  - Exact precision of coordinates may vary by study; metadata should be checked when aggregating at fine spatial scales.