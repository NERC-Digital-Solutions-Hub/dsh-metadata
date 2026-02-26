# Summary (a brief description/overview of the data)

- The dataset contains outcomes from questionnaire surveys of greenspace users regarding perceptions of experimentally manipulated urban meadows with varying plant diversity and sward height, located in Bedford and Luton.
- Data were collected by the authors with informed consent and were part of the Fragments, functions and flows NERC BESS project (2014); later re-analyzed for a 2021 paper in People and Nature.
- The data resource used for public archive comprises a single CSV file (Data_Phase 2_AsUsed_ForPublicArchive.csv) with 1020 rows and 21 columns.

## Data content and scope

- Experimental design
  - Nine meadow types per site (3 diversity levels x 3 heights) at each of four sites.
  - 30 greenspace users surveyed per location.
  - Sites include three in Bedford (Chiltern Ave, Goldington Green, Brickhill Heights) and one in Luton (Bramingham Road); coordinates provided.
- Data collected
  - Questionnaire responses from greenspace users on perceived meadow characteristics and socio-economic context.
  - Variables cover perceived diversity, overall preference scores, and a range of socio-demographic and visit-related measures.
- Nature and units
  - Continuous scores (e.g., Q2_PrefScore on a 1–10 scale) and various categorical responses (diversity, height, treatment description, gender, age bands, income bands, employment, education, residency, ethnicity).
  - Includes plant/eco-knowledge and broader wellbeing-related measures (e.g., eco-centrist themes).

## Experimental design / sampling

- Each location features all nine meadow treatments (combinations of short/medium/tall height and low/medium/high diversity).
- 30 respondents per site, yielding 120 respondents across four sites.
- Data include a unique sample code per respondent and per response point.

## Data collection, processing, and quality control

- Collection method: self-administered questionnaire.
- Ethical approval: University of Sheffield Research Ethics Committee (Department of Landscape Architecture Ethics Panel).
- Data quality checks: data entry validation; responses outside categorical options excluded.
- Data lineage: data originally collected 2014; later analyses cited from 2017, 2018, and a 2021 paper.

## Data structure and variables

- File: Data_Phase 2_AsUsed_ForPublicArchive.csv
- Structure: 1020 rows, 21 columns.
- Key columns (examples)
  - SITE, Sample, SampNo, Diversity, Height, Treatment description
  - Q1_PerceivedDiversity, Q2_PrefScore
  - plantid_EcoKnowledge, totalWL_EcoCentrism
  - Visit-related: visitlength, visitfreq, othergsfreq, visitcount
  - Demographics: gender, age, income, employ, edu, ukresident, ethnic
  - Residency and geography: location/site codes, coordinates (implicit from site labels)
- Data notes
  - NA indicates no response.
  - Some fields combine multiple concept indicators (e.g., ecocentrism measures across respondent and potential garden features).

## Analytical context and reuse

- Prior analyses
  - Southon et al. (2017, 2018): multivariate analyses and mixed effects models in R to relate meadow characteristics to user responses.
  - Jones et al. (2021, in press): mixed effects models and Bayesian modelling to explore how user characteristics shape perceptions within a cultural services framework.
- Data reuse potential
  - Suitable for replication studies, meta-analyses of urban meadow perception, and modelling of cultural ecosystem services.
  - Users should note that the public archive dataset is a data resource with descriptive variables and has not itself undergone published analytical processing beyond data cleaning; analytical methods are described in related papers.

## Data governance, provenance, and stewardship notes

- Provenance
  - Data collected by named authors for a Green/urban ecology study; linked to NERC BESS project (2014) and subsequent analyses (2017–2021).
- Ethics and consent
  - Ethically approved; informed consent obtained from participants.
- Documentation and metadata
  - Dataset includes explicit variable definitions and structure; descriptive table included in the data description.
  - Related publications cited for context and analysis methods.
- Accessibility and sharing
  - Public archive format: CSV with a single data file; standard tabular structure suitable for loading into common statistical software.
- Update and maintenance
  - The dataset is a Phase 2 public archive resource; no explicit update mechanism documented in the summary. Users should consult associated publications for methodological context and potential updated datasets.
- Privacy and risk considerations
  - Anonymization is implied by the use of coded site and respondent identifiers; however, researchers should review the Sample/SampNo design to assess re-identification risk when linking with other datasets.

## Limitations and considerations for data stewards

- Temporal scope: data originate from 2014 with later analyses; consider temporal relevance for current applicability.
- Completeness: some entries may be missing (NA); ensure appropriate handling of missing data in reuse.
- Heterogeneity across sites: analysis years reference different sites and meadow treatments; harmonization may be needed for cross-site comparisons.
- Metadata depth: while variable definitions are provided, additional context (e.g., exact questionnaire wording, coding schemes, and data entry protocols) would support more robust reuse.

## References

- Southon, G.E., Jorgensen, A., Dunnett, N., Hoyle, H. and Evans, K.L. (2017). Biodiverse perennial meadows have aesthetic value and increase residents' perceptions of site quality in urban greenspace. Landscape and Urban Planning.
- Southon, G.E., Jorgensen, A., Dunnett, N., Hoyle, H. and Evans, K.L. (2018). Perceived species-richness in urban green spaces: Cues, accuracy and well-being impacts. Landscape and Urban Planning.
- Jones, L., et al. (2021, in press). Can we model cultural ecosystem services, and are we measuring the right things? People and Nature.