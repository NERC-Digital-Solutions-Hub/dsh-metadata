# Data resource: Greenspace user questionnaire responses on perceptions of urban meadows in Bedford and Luton (Phase 2 public archive)

## Summary
- Dataset of questionnaire responses from greenspace users evaluating perceptions of experimentally manipulated urban meadows with varying floral diversity and sward height.
- Experimental sites: Bedford and Luton (four sites total; coordinates provided). Nine meadow types per site (3 diversity levels × 3 height levels); 30 respondents per location.
- Collected data include perception scores, diversity judgments, and extensive socio-economic and visit-related variables; data collected with informed consent and ethically approved.
- Originated from the Fragments, functions and flows NERC BESS project (2014); later re-analyzed for a 2021 paper (Jones et al., in press) in People and Nature.
- Data are stored as a single CSV for public archive: 1020 data rows and 21 columns; includes detailed schema for site, meadow treatment, respondent demographics, and visit behavior.

## Experimental design and sampling
- Layout: 9 meadow treatments (3 diversity levels × 3 height levels) at each of 4 sites.
- Sampling: 30 greenspace users surveyed per location, yielding multiple data points per respondent across meadow types.

## Data collection and processing
- Method: Questionnaires administered to greenspace users.
- Consent and ethics: Ethical approval obtained; responses checked during data entry; responses outside defined options excluded.

## Nature and units of recorded values
- Data capture includes:
  - Perceptual and preference measures: e.g., Q1_PerceivedDiversity, Q2_PrefScore (1–10 scale).
  - Plant knowledge and ecological cues: plantid_EcoKnowledge, eco-centrism measures.
  - Behavioral/usage metrics: visitlength (minutes), visitfreq, othergsfreq, visitcount (visits in 14 days).
  - Demographics and socio-economics: gender, age, income, employ, edu, ukresident, ethnic, plus location/site codes.
  - Treatment descriptor: detailed Coding for each plot’s combination of diversity and height (9 levels).

## Data structure and schema
- Data resource: single CSV file named Data_Phase 2_AsUsed_ForPublicArchive.csv.
- Size: 1020 data rows and 21 columns.
- Key columns:
  - SITE (location code), Sample (site-coded sample), SampNo (data point per respondent), Diversity (low/medium/high), Height (short/medium/tall), Treatment description (nine-level combination of diversity and height).
  - Perception and behavior metrics: Q1_PerceivedDiversity, Q2_PrefScore, visitlength, visitfreq, visitcount, etc.
  - Plant/ecometrics: plantid_EcoKnowledge, totalWL_EcoCentrism, etc.
  - Demographics: gender, age, income, employ, edu, ukresident, ethnic.
- Data handling notes: NA indicates no response to a question.

## Analytical methods (included in related analyses)
- Prior analyses on these data (Southon et al. 2017, 2018) used multivariate analysis and mixed effects models in R to link meadow characteristics with user responses.
- The 2021 Jones et al. analysis employed mixed effects models and Bayesian modelling to explore how user characteristics shape perceptions within a cultural services framework.
- The current dataset itself has not been reanalyzed in this descriptor; it supports future analyses.

## Quality control and ethics
- Ethics: Approved by University of Sheffield Research Ethics Committee (Department of Landscape Architecture Ethics Panel).
- Data integrity: Responses checked during data entry; responses outside categorical options excluded.

## Provenance and related works
- Original data collection and analyses:
  - Southon, G.E., et al. 2017; 2018. Biodiverse perennial meadows have aesthetic value and increase residents' perceptions of site quality in urban greenspace; Perceived species richness in urban green spaces: cues, accuracy and well-being impacts.
- Subsequent analysis using these data:
  - Jones, L., et al. (in press 2021). Can we model cultural ecosystem services, and are we measuring the right things? People and Nature.

## Relevance for Data Leaders (data strategy and governance)
- Demonstrates end-to-end data lifecycle: ethical collection, detailed metadata, structured data schema, and public archiving for reuse.
- Highlights importance of documenting experimental design (treatment descriptions) alongside socio-demographic context to enable robust meta-analyses across sites and conditions.
- Illustrates challenges of multi-site data: consistent coding of treatments, handling of missing responses, and integration with prior analyses.
- Provides a model for data discoverability and interoperability through clear variable descriptions and a single, well-documented data file.
- Useful for planning data governance: clear provenance, sufficient metadata, and links to related publications enhance trust, reuse, and alignment with broader data ecosystems in environmental social science.