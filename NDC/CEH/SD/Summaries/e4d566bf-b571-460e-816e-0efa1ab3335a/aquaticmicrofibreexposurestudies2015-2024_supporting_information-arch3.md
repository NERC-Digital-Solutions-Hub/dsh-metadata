# AquaticMicrofibreExposurestudies2015-2024 Supporting information

## Purpose and scope
- Describes a dataset of laboratory studies on the impacts of microfibres (<5 mm) on aquatic organisms, focusing on traits such as development, fecundity, feeding, growth, hatching, health, and survival.
- Dataset compiled to support a meta-analysis comparing biological responses to non-petroleum versus petroleum-based microfibres.
- Compiled by Ben Parker, covering studies from 2015 to 2024; data accessible as of 19/06/2024.
- Data derived from published manuscripts, supplementary information, and figures, via manual extraction and a plot digitiser where needed.

## Data collection and eligibility (collection/generation)
- Source search: Web of Science on 19/06/2024 using topic terms related to microfibre/microfiber/textile effects; limited to articles.
- Screening process: three-stage filtering (Stage 1 → Stage 2 → Stage 3) to identify relevant studies.
- Inclusion criteria (Stage 3): aquatic organisms, controlled exposure to a single polymer microfibre type (>1 µm and <5 mm), study reported means with errors for exposure and control that could be extracted, and data extractable from manuscript or supplementary materials.
- Data extracted for key biological traits and only positive responses were prioritized; some negative responses were converted to positive where appropriate to maintain comparability.
- Exposures included across various life stages and conditions (starved/fed) but excluded co-contaminants and multi-polymer mixtures.
- Final timepoint/least ambiguous timepoint chosen when multiple timepoints were reported.

## Data structure and units
- Data organized in a CSV file named AquaticMicrofibreExposurestudies2015-2024.
- Key fields include:
  - IDs, Study.no, Reference, Authors, Title, Year
  - FA.country (country of first author’s affiliation), Species, Source (where the organism was sourced)
  - Environment (freshwater, marine, estuarine)
  - Taxonomic.grouping, Days.exposed, Days.cat
  - Microfibre category (petroleum-based vs other polymers), MF.category, Length.mm, Length.cat, Width.mm
  - Study.exposure, Study.exposure.units, Standard.exposure, S.cat, Standard.units
  - Time.series, Additional.variable
  - Response (development, fecundity, feeding, growth, hatching, health, survival), Converted.measure
  - Response.units, C.N, C.mean, C.SD, E.N, E.mean, E.SD, Data.source
- Data are described as either manuscript (MS) or supplementary information (SI) sources.
- Categorical classifications cover the seven traits and a standardized approach to mean and SD data across conditions.

## Data quality and governance
- Implemented multi-stage screening to ensure relevance and data quality.
- Data extraction leveraged multiple sources (MS, SI, figures) and a plot digitiser to maximize accuracy and consistency.
- Explicitly documents how negative responses were harmonized into positive categories for inclusion.

## Rationale and intended use
- Aims to enable meta-analytic comparisons of effects from different microfibre types on aquatic organisms.
- Supports evidence-informed monitoring and policy decisions by providing structured, harmonized data on microfibre exposures and organismal responses.
- Facilitates transparency and reproducibility through clear data provenance (references, sources) and explicit inclusion criteria.

## Coverage, limitations, and practical considerations for monitoring
- Coverage: studies up to 2024, limited to single-polymer exposures (no mixtures) and excluding co-contaminants.
- Limitations: potential metadata gaps; variability in primary study reporting; reliance on extracted data from MS/SI/figures; standardization choices (units, exposure metrics) may require careful interpretation when integrating with other datasets.
- Practical considerations: ongoing data governance and openness are emphasized, including sharing underlying data where appropriate and maintaining clear provenance for each data point.

## References and data availability
- The document provides an extensive list of study references used to populate the dataset (examples include Au et al. 2015; Blarer & Burkhardt-Holm 2016; Bour et al. 2022; Choi et al. 2021, 2022; Cole et al. 2020; and others).
- Data availability is described as a compiled CSV with detailed metadata and extraction notes, designed to support reproducible analyses and comparison across studies.