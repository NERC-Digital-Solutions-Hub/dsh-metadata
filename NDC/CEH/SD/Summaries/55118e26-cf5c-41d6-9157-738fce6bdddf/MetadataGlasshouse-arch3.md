# PhenotypeGlasshouse.txt

## Objective and Scope
- Provides phenotypic and genotypic data for Pinus species grown in a glasshouse.
- Aims to support monitoring and evaluation of environmental health indicators, genotype-phenotype associations, and climate-related responses to inform future policy and management decisions.

## Data Structure and Key Variables
- Species: MU (Pinus mugo), SY (Pinus sylvestris), UN (Pinus uncinata)
- Geographic and population metadata:
  - Country
  - Population
  - PopCode
  - PopCodeWachowiak2018 (cite Wachowiak et al. 2018)
  - Family (shared maternal lineage)
  - Latitude, Longitude
  - Block (1–25)
  - ID (unique individual tree identifier)
- Genotyping:
  - Genotyped (0 = no, 1 = yes) indicating use of the multispecies Pinus SNP array
  - snpid (SNP marker name) in GenotypeGlasshouse.txt
  - Additional genotype columns (e.g., UN18_26_16) and other SNP-related data
- Phenotypic measurements (in years):
  - BS2010: Bud set (days since first plant to set terminal bud in 2010)
  - BB2011: Budburst in 2011 (days since first plant to burst bud)
  - BB2012: Budburst in 2012
  - H2011, H2012, H2013: Height in years 2011–2013 (cm)
  - I2012: Height increment 2012 (cm; 2011→2012)
  - I2013: Height increment 2013 (cm; 2012→2013)
- Data organization:
  - Files include PhenotypeGlasshouse.txt and GenotypeGlasshouse.txt
  - All remaining columns in genotype file are tied to unique tree IDs

## Provenance, Metadata and Documentation
- Data linked to Wachowiak et al. (2018) with DOI provided
- Includes core metadata for population structure, geographic origin, and individual identifiers to support traceability and data integration

## Data Quality, Access and Governance
- Metadata completeness varies; some fields may be NA
- Precision and transformation needs:
  - Phenology measurements are expressed as days since a baseline event
  - Height values are in centimeters
- Data sharing considerations:
  - Public sharing of underlying data is a factor; ensure appropriate governance and openness standards
- Data management needs:
  - Clear linkage between phenotype and genotype data via unique IDs
  - Documentation of data sources, measurement protocols, and any transformations applied

## Relevance to Monitoring Frameworks
- Provides measurable indicators of plant phenology and growth across genetic backgrounds and populations
- Supports assessment of environmental health indicators and climate adaptation strategies in forestry
- Illustrates data governance practices: dataset provenance, standardized identifiers, and openness where feasible

## Practical Uses for Policy Evaluation
- Evaluate seed sourcing and provenance decisions under climate change scenarios
- Identify genotype-by-environment patterns to inform resilient forestry strategies
- Benchmark phenological responses and growth under controlled conditions to inform risk assessments and adaptive management

## Limitations and Considerations
- Observations derive from glasshouse experiments; generalizability to natural ecosystems may be limited
- Time frame is limited (2010–2013 for phenology; height across 2011–2013)
- Potential data gaps or inconsistencies require careful metadata review and data cleaning
- Integration with other datasets (e.g., broader field trials) may be needed for comprehensive monitoring

## Governance and Data Sharing Recommendations
- Maintain thorough metadata, including measurement protocols and data processing steps
- Use consistent identifiers across phenotype and genotype datasets
- Address data access barriers by documenting licensing and sharing permissions
- Implement data quality checks and regular updates to keep metadata and measurements current