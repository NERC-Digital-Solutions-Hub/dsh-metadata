# Identifying priorities, targets, and actions for the long-term social and ecological management of invasive alien species

- A study aiming to identify priorities, targets, and actions for the long-term social and ecological management of invasive alien species (IAS) by combining expert judgment with a standardized scoring framework.
- Emphasizes the use of data-driven insights to inform practical decisions in management and policy contexts.

## Data collection and governance

- Seventeen experts across seven case studies independently scored impact outcomes using the CONTAIN-ImpactScoringInstructions framework.
- Two rounds of scoring were conducted, followed by a facilitated workshop in San Carlos de Bariloche, Argentina (December 2019).
- Final agreed impact scores are presented in Unique-Impact.csv; preliminary usefulness evaluated by sharing ImpactBrief documents with Latin American collaborators.
- The data reflect an elicitation process rather than solely published field measurements, and are intended to support comparative analyses and decision making.

## Datasets and file contents

- Compiled-Impact.csv
  - Contains results of expert elicitation for IAS impacts.
  - Each row corresponds to a single expert-listed impact outcome.
  - Key columns include:
    - Impact.outcome
    - Impact.mechanism
    - Maximum.impact..EICAT.classification.level.
    - Level.of.confidence
    - Type (plant or animal)
    - Country
    - References.and.supporting.information

- Unique-Impact.csv
  - Similar to Compiled-Impact.csv but removes duplicates (same impact outcome for a given species and country appears only once).
  - Key columns include:
    - Impact.outcome
    - Impact.mechanim (mechanism)
    - Maximum.impact..EICAT.classification.level.
    - Level.of.confidence
    - Species.or.asset.impacted
    - Direction.of.the.impact (positive or negative)
    - Area (km2)
    - Species
    - Type (plant or animal)
    - Country

- CONTAIN-ImpactScoringInstructions.pdf
  - Instructions, lists, and guidance used by experts to complete the Impact Score Spreadsheets.

- ImpactBrief-CONTAIN(English).pdf and ImpactBrief-CONTAIN(Español).pdf
  - Briefings circulated to collaborators with procedures, examples, and questions to answer.

## Data scope and semantics

- Based on expert elicitation across seven IAS case studies, with involvement from Latin American collaborators.
- Includes both negative and positive impacts, classified using the EICAT framework for impact severity.
- Captures who or what is affected (Species.or.asset.impacted or impacted assets) and the geographic scope (Country, Area in km2).

## Data provenance and accessibility

- Freely available data (CSV files and PDFs) with metadata and described fields.
- Datasets are designed to enable cross-case comparisons and downstream analyses, with clear documentation of scoring procedures.

## Analyses and uses for data-driven questions

- Potential analyses for answering data-driven questions:
  - Correlations between EICAT severity levels and impact outcomes, mechanisms, species type (plant vs. animal), and country.
  - Cross-country and cross-case comparisons of impact types and magnitudes.
  - Prioritization of targets and actions based on frequency, severity, and affected assets.
  - Scenario or predictive analyses to anticipate effects of management actions on IAS impacts.
  - Meta-analysis combining multiple datasets with consistent fields to identify patterns in IAS impacts across scales.

## Limitations and caveats

- Small number of case studies and expert participants may limit generalizability.
- Expert elicitation introduces subjectivity and potential biases; results depend on the quality and scope of included literature and expert perspectives.
- Data are not time-series; lack explicit temporal resolution and dynamic change.
- Some fields rely on the quality and completeness of supporting publications and information cited for each impact.

## Practical notes for analysts

- When using Unique-Impact.csv for analyses, account for the removal of duplicates to avoid overweighting repeated assessments for the same species-country pair.
- Leverage the Direction.of.the.impact to separate positive from negative effects when profiling IAS consequences.
- Use Area (km2) and Country to contextualize impacts spatially and to explore regional patterns.
- Consult CONTAIN-ImpactScoringInstructions.pdf to understand the scoring rationale behind Maximum.impact..EICAT.classification.level. and Level.of.confidence.
- Reference the ImpactBrief documents for methodological context and potential pitfalls identified by the researchers.