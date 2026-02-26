# biodiversity in relation to fire in Sebangau National Park, Central Kalimantan, Indonesia, 2003-2019

## Overview and Purpose
- Presents methodological details for collecting, processing, and assessing ecological components in relation to fire impacts.
- Supports the study Impacts of fire and prospects for recovery in a tropical peat forest ecosystem (Harrison et al. 2024) by outlining data provenance, measurement, and analysis.
- Aims to identify environmental health measures to scrutinize policy and inform future decisions on peatland fire impacts and recovery.

## Study Site and Data Scope
- Location: Natural Laboratory of Peat-swamp Forest (NLPSF), Sebangau National Park, Central Kalimantan, Indonesia.
- Long-term context: 16 years of ecological data (ecosystem properties and biodiversity) with a history of logging and fire vulnerability.
- Fire regime: Characterized across a period (2000–2020) using MODIS thermal anomalies to identify megafire periods; six megafire events identified.
- Design approach: Combines spatial and temporal assessments to evaluate direct fire impacts and indirect landscape-level effects (e.g., haze).

## Monitoring Measures and Data Collected

### Spatial Assessment (fire treatments and controls)
- Treatments: new burn, old burn, unburned forest (controls).
- Ecosystem properties (e.g., microclimate temperature, canopy/fern/grass cover, density of key taxa, tree height, aboveground biomass).
- Biodiversity metrics across groups:
  - Trees (species identity and abundance after filtering non-identifiable samples)
  - Odonata (Anisoptera and Zygoptera)
  - Lepidoptera: Papilionoidea (butterflies)
  - Herpetofauna (amphibians and reptiles)
  - Birds: avian-focused soundscape indices (Bioacoustic Index, Acoustic Complexity Index, Acoustic Diversity Index, Normalised Difference Soundscape Index) from acoustic recorders
- Additional measures: river pH, leaf-litter productivity, leaf flush and reproductive phenology
- Data presentation: standardized mean differences (Hedges g) comparing burn treatments to unburned controls; housekeeping variables standardized across datasets; some variables summarized as proportions or densities

### Temporal Assessment (long-term time series)
- Time span: September 2003 – December 2019 (16 years), capturing variations in annual fire regimes.
- Biodiversity time series: occupancy-based detection histories for multiple taxa
- Ecosystem time series: seasonally aggregated data for variables like litterfall, river pH, and phenology (fruit/flower expression, leaf flush)
- Temporal modeling: season-based random effects; spatio-temporal covariates; two model types to parse fire regime effects (fire properties vs. proximity to megafire)

### Fire Regime Characterization
- Data source: MODIS fire detections (MCD14ML, Collection 6)
- Fire metrics: frequency, radiative power, detection confidence; megafire events defined as months exceeding 95th percentile thresholds
- Spatial scales: Central Kalimantan province and NLPSF boundary with buffer

### Data Quality, Provenance, and Metadata
- Provisions for quality control: observer training, data screening for outliers and errors, cross-checks with field staff; spectrogram checks for acoustic data to exclude disruptive recordings
- Taxonomic standardization: alignment to APG (trees), Orr (Odonata), Otsuka (butterflies), IUCN-based classifications for specialists, cross-referenced with field guides and experts
- Metadata: accompanying files document units and data columns; 24 data files plus a metadata document
- Data sharing considerations: emphasis on open data practices and transparent governance, with explicit notes on metadata and reproducibility

## Data Processing and Analytical Approaches

### Spatial Analyses
- Effect size estimation: standardized mean differences (Hedges g) with adjustments for heteroscedasticity and multiple controls
- Non-independence handling: adjust sample sizes when multiple burn treatments are compared to a single control
- Synthesis: hierarchical mixed-effects meta-analysis with random effects for data type, ecological components, and observations
- Proportional change calculations: post-hoc between burn treatments and unburned controls using GLMM-estimated means

### Temporal Analyses
- Sampling structure: discrete seasons tailored to each dataset (e.g., 3-month seasons for terrestrial vertebrates; 1-month for others)
- Occupancy modeling: multispecies occupancy models accounting for imperfect detection; random walk priors across seasons for occupancy intercepts
- Detection and effort: season-specific detection processes with survey effort covariates
- Model comparison: two candidate models per time-series (fire properties vs. spatio-temporal proximity)
- Statistical framework: Bayesian, implemented in rstan (hierarchical meta-analysis) and JAGS (GLMMs and occupancy models)

### Data Organization and Accessibility
- File structure: 24 files total (23 data files + supplementary metadata)
- Grouped data: forest specialist classifications, species groupings, inputs for spatial and temporal analyses
- Data products: includes meta-analysis inputs (both all-species and specialists-only), spatial GLMM inputs, and occupancy/detection datasets for birds, butterflies, fish, and mammals
- Citations and references: extensive methodological and taxonomic references supporting classification, sampling, and analysis methods

## Outputs and Implications for Monitoring Frameworks

- Quantifies fire impacts on peatland ecosystems through standardized effect sizes and proportional changes
- Enables policy-relevant monitoring by providing multi-taxon, multi-parameter indicators of fire impact and recovery trajectories
- Demonstrates integration of spatial and temporal monitoring, robust data governance, and transparent analytical pipelines suitable for informing future decision-making and restoration efforts

## Challenges and Considerations for Monitoring Frameworks

- Data gaps and access: occasional gaps due to fire disruption or logistical constraints; need for timely access to diverse data streams
- Data silos: coordination across taxa and datasets to avoid duplication and enable integrated analyses
- Metadata quality: ensuring complete and consistent metadata to facilitate reproducibility and reuse
- Data transformation: variable formats and units requiring standardization for cross-study comparability
- Communicating complex findings: translating diverse ecological signals into clear, policy-relevant messages
- Governance and openness: balancing data sharing with local permissions and data provenance considerations

## References and Supporting Materials

- Supplementary methodology and data references supporting methods, taxonomic classifications, and analytical approaches
- Associated with Harrison et al. (2024) and prior works on peat swamp forest biodiversity, fire regimes, and monitoring methods