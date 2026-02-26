# Survival and reproductive success of migrant and resident wildlife in published studies of partially migratory populations

- Purpose and scope
  - A dataset created from information extracted from published studies to support a meta-analysis of fitness benefits of different migratory strategies in partially migratory populations.
  - Each data line includes a mean and associated variance for a given fitness metric for both migrants and residents, plus study population location, study species, type of fitness metric, data collection year, and publication details.
  - Produced as part of a NERC-funded PhD project (grant NE/L002582/1) at the School of Environmental Sciences, University of East Anglia.

- Dataset composition
  - Data lines summarize direct fitness measures for migrants and residents, enabling calculation of effect sizes (e.g., Hedges' d).
  - Includes metadata per line: study identifier, species, location, year(s) of data collection, migratory distance classification, and publication/source details.
  - Fitness metrics categorized as survival or reproductive success, with specific metric types defined (per Table 2 in the doc).

- Data collection and search strategy
  - Systematic search of studies on fitness benefits of migratory strategies in partially migratory populations up to December 2017.
  - Databases: ISI Web of Science and Google Scholar; broad taxonomic scope; supplementary searches of references and reviews to validate results.
  - Search terms designed to capture both resident–migrant and short-distance vs long-distance migrant comparisons, across multiple taxonomic groups.

- Inclusion and exclusion criteria
  - Include studies that compare resident and migrant populations (or short-distance vs long-distance migrants) within the same species.
  - Include outcomes considered direct indicators of fitness (survival or breeding success); exclude indirect proxies.
  - Require extractable data for calculating effect sizes (raw data or model-fitted predictions from raw data; SDs derivable from SEs/ CIs if missing).
  - Include studies with raw observations or model-fitted predictions; exclude purely theoretical/model-only studies.
  - Include grey literature where applicable (DOIs may be NA).

- Data extraction and processing
  - Extract means and standard deviations for all relevant results; derive SDs from SEs or CIs when needed; digitize data from graphs using WebPlotDigitizer when necessary.
  - Capture per-effect data: study, species, location, migratory distance category, year(s), metric type (breeding vs survival), sample sizes for migrants and residents.
  - Classify fitness metrics into breeding success or survival; assign specific metric types (e.g., clutch size, offspring survival, absolute survival, growth rate) as listed in Table 2.
  - For bounded data, apply logit transformations where appropriate prior to calculations.

- Data structure and fields
  - Core identifiers: id, study, doi, studyyear, year, year.spread.
  - Taxonomy and geography: taxogroup.new (bird, mammal, fish, herpetofauna), species, hemisphere, country, latitude, longitude.
  - Migratory data: n.mig, n.res.sdm, r.sdm.dist.km, new.ldm.distance, percent.dist, dist.saved.
  - Sample and design: samplesize, benefit (breeding vs survival), breeding vs survival subfields (e.g., type of measure if breeding or survival).
  - Effect data: r.sdm.mean, r.sdm.sd, ldm.mean, ldm.sd.
  - Data lineage: notes on data extraction, data sources.

- Data sources and provenance
  - Comprehensive list of studies used as data sources (e.g., Bai et al. 2012; Bohlin et al. 2001; Grayson et al. 2011; Zúñiga et al. 2017; many others).
  - Each source contributes effect-size data or raw data from which means and variances were derived.
  - References include both peer-reviewed articles and grey literature; DOIs provided where available.

- Governance, stewardship, and usage considerations
  - Transparency and reproducibility: detailed data dictionary and field definitions supporting consistent reuse and re-analysis.
  - Provenance: explicit linkage between effect sizes and source studies; documentation of data extraction and transformations (e.g., logit transforms, SD derivations from SE/CI, digitization).
  - Interoperability: standardized taxonomy for taxonomic groups and clearly defined metric categories to facilitate integration with other datasets.
  - Data availability and limitations: dataset only includes studies up to 2017; ongoing needs to update with new literature and to address potential biases due to study selection and metric heterogeneity.
  - Data quality checks: systematic extraction protocol, use of digitization tools, and explicit handling of missing SDs to enable complete effect-size calculations.

- Usage notes and limitations
  - Metrics are heterogeneous and may vary by taxon; standardization to comparable effect sizes (e.g., Hedges' d) is used to compare across studies.
  - Some data come from grey literature (DOIs NA); data completeness depends on reported statistics in source publications.
  - Bounding transformations and data exclusions (e.g., excluding indirect fitness metrics) influence the scope of the meta-analysis and should be considered when reusing the dataset.

- Publication status and contact
  - Text originates from the methods section of a manuscript in press: "Fitness consequences of different migratory strategies in partially migratory populations: a multi-tax meta-analysis" (Journal of Animal Ecology).
  - Data are prepared for meta-analytic synthesis; users should credit the University of East Anglia and the authors listed in the data sources.