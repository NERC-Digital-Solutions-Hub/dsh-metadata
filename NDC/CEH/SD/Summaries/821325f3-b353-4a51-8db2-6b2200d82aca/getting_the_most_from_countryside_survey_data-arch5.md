# Notes on the downloadable data

- Overview
  - Explains how Countryside Survey (CS) field data are collected, how sampling design affects use and analyses, and how precise locations are withheld to preserve representativeness.

- Privacy and representativeness of locations
  - Exact square locations are kept confidential.
  - External users cannot identify survey squares with precision better than 100 square km to protect representativeness of the broader countryside.

- Sampling design and scope
  - Field data come from a sample of 1-km squares across Great Britain.
  - Two sampling levels: whole square and within-square measurements (e.g., quadrats for vegetation, soils).
  - Not a random subset; the sample is stratified by the ITE Land Classification.
  - Country-specific classifications: 21 classes in England, 8 in Wales, 16 in Scotland; historically, country-level adaptations yielded 42–45 total classes.
  - Not all squares are surveyed: excluded if >90% sea or >75% urban (per 1:250,000 OS maps). This means CS field data represent only eligible squares; extrapolations to GB or regions assume similar vegetative land composition in excluded squares, which may introduce bias if regions have high sea/urban coverage.

- Implications for analysis and interpretation
  - Estimates are ratio estimates, weighted by vegetative land area within each land class.
  - Proper use requires accounting for stratification; ignoring it can lead to biased variation estimates.
  - Standard errors and confidence intervals are computed via bootstrap methods since 1998, addressing skewness in some features.
  - Extrapolations to broader areas rely on assumptions about the vegetation composition of excluded squares.

- Methods and key references
  - Methodology aligned with ratio estimation (Cochran, 1963) and bootstrap-based SEs (Efron & Tibshirani, 1993).
  - Core reporting and sampling details are documented in related works (e.g., Barr et al., 1993).

- Data stewardship considerations for users
  - Metadata should clearly document sampling design, stratification, exclusion criteria, weighting, and bootstrap SEs.
  - Users must consider the representativeness limitations when conducting region- or GB-scale analyses.
  - When reusing data, reproduce the weighting and SE methodology to ensure comparable uncertainty estimates.
  - Maintain confidentiality constraints around precise square locations in any shared derivatives.