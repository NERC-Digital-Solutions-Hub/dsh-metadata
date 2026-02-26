# Identifying priorities, targets, and actions for the long-term social and ecological management of invasive alien species

## Aim and scope
- Identify priorities, targets, and actions for long-term social and ecological management of invasive alien species (IAS).
- Build a data-supported basis for monitoring environmental health and policy performance related to IAS management.

## Methods

- Expert elicitation
  - Seventeen experts across seven case studies participated.
  - Each expert completed impact scoring independently using the provided guidance.
- Scoring process
  - Two rounds of scoring.
  - Results discussed in a facilitated workshop in San Carlos de Bariloche, Argentina (December 2019).
- Guidance and validation
  - Used the CONTAIN-ImpactScoringInstructions.pdf to standardize scoring.
  - Preliminary evaluation of usefulness via ImpactBriefs shared with collaborators in Latin America.
  - Final consensus reflected in the datasets.

## Data and outputs

- Compiled-Impact.csv
  - Contains results of the expert elicitation for IAS impacts.
  - Each row corresponds to one impact outcome listed by an expert.
  - Key columns include: Impact.outcome, Impact.mechanism, Maximum.impact..EICAT.classification.level., Level.of.confidence, Type (plant or animal), Country, References and supporting information.
- Unique-Impact.csv
  - Deduplicated version of impact outcomes (one impact outcome per species and country).
  - Includes: Impact.outcome, Impact.mechanim, Maximum.impact..EICAT.classification.level., Level.of.confidence, Species.or.asset.impacted, Direction.of.the.impact, Area (km2), Species, Type, Country, etc.
  - Represents the final agreed evaluations after expert discussions.
- Data structure notes
  - Both datasets reflect standardized EICAT classifications and reported confidence levels.
  - Distinguishes plant vs. animal IAS and captures country-level impacts.

## Supporting materials

- CONTAIN-ImpactScoringInstructions.pdf
  - Instructions, lists, and guidance for completing the Impact Score Spreadsheets.
- ImpactBrief-CONTAIN(English).pdf
  - English briefing document with procedures, examples, and questions.
- ImpactBrief-CONTAIN(Español).pdf
  - Spanish version of the briefing document.

## Data accessibility and use

- Freely available data.
- Intended to support prioritization, target-setting, and action planning for long-term IAS management.
- Outputs are designed to facilitate cross-study comparability and inform monitoring of environmental health and policy performance.

## Relevance for Analysts Monitoring the Environment

- Provides standardized, transparent datasets suitable for long-term environmental monitoring and policy evaluation related to invasive species.
- Enables data quality assurance, transformation, and storage into appropriate data portals.
- Supports data-driven decisions by allowing comparison of impact outcomes across species, mechanisms, countries, and study areas.
- Highlights the importance of deduplication (Unique-Impact.csv) to avoid counting the same impact multiple times and to improve data usability across analyses.