# The Sampling Strategy for Countryside Survey

- This document outlines the field survey sampling strategy for Countryside Survey up to 2007 and tracks the evolution of the ITE Land Classification used to stratify the sampling framework since 1978.
- It emphasizes the need for representative sampling through stratification and the historical linkage between land classification development and survey design.

## Core purpose and approach

- Aim: To ensure field samples represent the GB countryside for robust habitats/land-use estimates and to enable national, regional, and later country-specific reporting.
- Key principle: Stratified, random sampling to minimize bias and ensure that all parts of the population (land types) are represented.
- Central technique: Use of the ITE Land Classification to define strata (land classes) that guide sample placement and sample size.

## Evolution of the ITE Land Classification and its impact on sampling

- 1978 – The Beginning
  - Indicator Species Analysis (ISA) used on environmental attributes to define 32 land classes from 1 km squares (center squares of a 15 x 15 km grid).
  - A total of 6039 km² (plus surrounding four squares per centre) were classified.
  - Sampling: 8 squares per land class, total of 256 squares surveyed.
  - National estimates calculated by combining mean habitat area per square within each land class with the area of that class.

- 1984 – Second Field Survey
  - Expanded sampling to 12 km squares per land class (total 384 squares).
  - National estimates still based on the 1978 Land Classification approach.

- 1990 – All Squares Land Classification (CS1990)
  - Land Classification revised to classify every square in GB (an extensive update), with urban/sea corrections.
  - Field survey expanded to 508 squares.
  - Introduced the Land Cover Map as part of the framework.
  - Results published in Countryside Survey 1990 main report.

- 1998–2000 – Revised Classifications and CS2000 Framework
  - To improve regional/local estimates, every GB square was reclassified using major climatic, geological, and physiographic surrogates; multiple classification attempts were tested.
  - Best match to original 1228-squares classification achieved with 62% correspondence; non-matching squares fell into neighboring classes but preserved class means.
  - Implication: The sampling framework and distributions across land classes were altered, affecting comparability and requiring careful interpretation of time-series estimates.

- 2000 – Separate Country Estimates and Upland Module
  - Recognized need for England & Wales and Scotland reporting; introduced country-unit versions of land classes and 40 strata (with aggregations where class representation was low).
  - Added 19 extra squares to ensure adequate representation of new classes; more sampling allocated to Wales for country-specific reporting.
  - Included an upland habitat module (30 additional squares) to improve upland estimates in England and Wales.

- 2007 – Wales-focused Reporting and Further Sub-divisions
  - Wales-only reporting needed, prompting Wales-specific class sub-divisions: five new country-unit classes (5w, 6w, 7w, 15w, 18w).
  - Resulted in 45 strata; 43 additional Welsh squares were added to ensure minimum representation across new Welsh classes.
  - England retained most classes but two English classes (5e, 15e) had only four squares due to Wales-focused additions; overall precision for these classes deemed acceptable for reporting purposes.
  - Revised land-class maps produced for England with Wales and for Scotland; sample squares adjusted accordingly (see Figures 6 and 7 in the document).

## Data framework, sampling, and national reporting

- Sample and class structure
  - 32 original land classes (1978), expanded to 40 (1990), then 45 (2007) with country-unit subdivisions.
  - CS2000 introduced country-specific sampling designs; CS2007 refined Wales reporting with Welsh-specific sub-classes.
- Country-level reporting
  - England & Wales and Scotland (and later Wales) require distinct reporting perspectives; the sampling frame accommodates country-unit estimates.
- Data and outputs
  - Field survey data across multiple survey years underpin national, regional, and country-specific habitat and land-use statistics.
  - National estimates are sensitive to Land Classification version; 2006 scoping notes emphasize consistency considerations when switching classifications across surveys.
- Documentation and references
  - Detailed methodological notes, figures, and tables (e.g., Tables 1–4, Figures 1–7) accompany the narrative and support reproducibility and auditability.
  - Appendix i provides a brief history of the ITE Land Classification and its development.

## Data governance and stewardship considerations for Data Stewards

- Data lineage and versioning
  - Track which Land Classification version was used for each dataset (1978, 1984, 1990, CS2000, CS2007) and note any reclassifications of squares over time.
  - Maintain crosswalks between old and new land-class labels (e.g., 32 → 40 → 45) to support time-series analyses.
- Metadata and documentation
  - Capture year, country unit, class definitions, number of sample squares, sampling rates, and spatial extents for each dataset.
  - Document upland module additions and Welsh-specific class sub-divisions, including the rationale and target reporting regime.
- Data quality and representativeness
  - Be aware of representativeness shifts due to reclassification and country-specific sampling adjustments.
  - Note the implications of unequal class representation across countries and the need for supplemental sampling to achieve adequate precision (as in CS2000/CS2007).
- Access, sharing, and publication
  - Outputs are primarily published as national and country-specific reports; ensure datasets and metadata are archived with clear versioning to support future reporting and reuse.
- Interoperability and standards
  - Adopt consistent metadata standards and documentation across survey years to facilitate interoperability between datasets from different classification eras.
  - Where possible, maintain linkage to land-class maps and sample-square inventories to support data integration and reanalysis.

## Summary

- The Sampling Strategy for Countryside Survey documents the long-running, stratified approach to ecological surveying in Great Britain, rooted in the ITE Land Classification.
- Over time, the classification system evolved from 32 to 40 to 45 land classes, with increasing emphasis on country-specific reporting (England & Wales, Scotland) and Wales-focused Wales-only estimates.
- The methodology integrates a robust sampling framework (center-square classifications, surround-square augmentation), alignment with Land Cover Mapping, and an explicit acknowledgement of changes in classification that affect trend interpretation.
- For Data Stewards, key implications include the importance of meticulous versioning, thorough metadata, careful handling of cross-era class mappings, and maintaining documentation to ensure reproducibility and reliable country-level reporting.