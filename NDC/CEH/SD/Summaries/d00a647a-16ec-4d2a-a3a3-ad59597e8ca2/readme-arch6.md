# Data from: García-Díaz, P., et al. Identifying priorities, targets, and actions for the long-term social and ecological management of invasive alien species.

## Overview
- Study engages 17 experts across seven case studies to identify priorities, targets, and actions for long-term management of invasive alien species.
- Objective: produce data-driven insights to inform policy, management, and public understanding.
- Outputs are designed as open, reusable data products to enable further analysis and self-service use.

## Data collection and process
- Experts completed Impact Score Spreadsheets independently following guidance in CONTAIN-ImpactScoringInstructions.pdf.
- Two rounds of scoring were conducted, followed by a facilitated workshop in Bariloche, Argentina (Dec 2019) to reach final consensus.
- Preliminary evaluation of methods was shared with collaborators in Latin America via ImpactBrief-CONTAIN English and Spanish documents.
- Data were compiled, cleaned, and prepared for sharing in structured CSV formats.

## Data files and structure
- Compiled-Impact.csv
  - Contains the results of expert elicitation for each impact outcome.
  - Columns include: Impact.outcome, Impact.mechanism, Maximum.impact..EICAT.classification.level., Level.of.confidence, Type (plant or animal), Country, References and supporting information.
  - Represents all impact outcomes as identified by experts (includes duplicates at the outcome level).
- Unique-Impact.csv
  - A deduplicated version of the impact data (one impact outcome per species and country).
  - Additional fields include: Species.or.asset.impacted, Direction.of.the.impact (positive/negative), Area (km2), Species, Type, Country.
  - Columns mirror the core fields from Compiled-Impact.csv with species- and country-specific aggregation.
- CONTAIN-ImpactScoringInstructions.pdf
  - Documentation and guidance used by experts to complete scoring.
- ImpactBrief-CONTAIN(English).pdf and ImpactBrief-CONTAIN(Español).pdf
  - Briefs circulated to collaborators to explain procedures, examples, and questions, and to gather feedback.

## Data usage and dissemination
- The datasets are designed to support broad data exploration and self-service analyses related to invasive alien species impacts.
- Data include geographic (Country), taxonomic (Plant/Animal), impact type and mechanism, and estimated impact severity (EICAT classification) with confidence levels.
- References and supporting information are provided to document evidence behind impact evaluations.
- Outputs were shared with networks in Latin America for usability testing and feedback to improve the data products.

## Documentation and supporting materials
- The project provides a comprehensive suite of documents to guide data use:
  - CONTAIN-ImpactScoringInstructions.pdf (scoring workflow and data fields)
  - ImpactBrief-CONTAIN(English).pdf and ImpactBrief-CONTAIN(Español).pdf (procedural briefs for collaborators)
- All materials accompany the data to facilitate understanding, replication, and extension of the work.