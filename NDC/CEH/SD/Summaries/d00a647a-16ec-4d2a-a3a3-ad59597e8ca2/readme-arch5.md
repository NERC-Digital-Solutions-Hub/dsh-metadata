# Identifying priorities, targets, and actions for the long-term social and ecological management of invasive alien species

## Overview
- A study using expert elicitation to identify and rank impacts of invasive alien species (IAS) across multiple case studies.
- Final impact scores and supporting data are prepared for sharing and reuse to inform long-term IAS management.

## Data assets (files)
- Compiled-Impact.csv: contains aggregated expert-elicitated impact outcomes with fields including:
  - Impact.outcome, Impact.mechanism
  - Maximum.impact..EICAT.classification.level.
  - Level.of.confidence
  - Type (plant or animal), Country
  - References.and.supporting.information
- Unique-Impact.csv: deduplicated version of impacts by species and country with additional fields:
  - Species.or.asset.impacted
  - Direction.of.the.impact
  - Area (km2)
  - Species, Type, Country
- CONTAIN-ImpactScoringInstructions.pdf: instructions, lists, and guidance for completing the Impact Score Spreadsheets.
- ImpactBrief-CONTAIN(English).pdf and ImpactBrief-CONTAIN(Español).pdf: briefs circulated to collaborators to gather feedback on procedures and questions.
  
## Data collection and curation process
- Participants: Seventeen experts across seven case studies.
- Method: Independent completion of Impact Score spreadsheets following standardized instructions.
- Rounds: Two rounds of scoring, followed by a facilitated workshop in San Carlos de Bariloche, Argentina (December 2019).
- Output: Final agreed impact scores documented in Unique-Impact.csv.
- Validation: Preliminary evaluation of methods via dissemination of ImpactBriefs to Latin American collaborators.

## Data content and schema
- Compiled-Impact.csv:
  - Columns reflect individual impact outcomes and their assessed mechanisms, with EICAT classifications and confidence levels.
  - Includes who (Type: plant or animal) and where (Country), plus supporting references.
- Unique-Impact.csv:
  - Similar core fields as Compiled-Impact.csv but deduplicated (same impact outcome for a given species and country appears only once).
  - Additional fields:
    - Direction.of.the.impact (positive/negative)
    - Area (km2)
    - Species (identity of invasive species)
    - Species.or.asset.impacted (the affected asset or species)
- Both datasets anchored to expert consensus on species and country-level impacts, with a documented scoring basis in CONTAIN-ImpactScoringInstructions.pdf.

## Provenance and documentation
- Data and methods are documented in a set of accompanying files (scoring instructions and briefings).
- Final data reflect consensus after two scoring rounds and a collaborative workshop.
- English and Spanish briefing materials provided to support wider understanding and uptake.

## Access, sharing, and reuse
- Data are described as freely available data, with clearly defined files and documentation to support reuse.
- Documentation enables reproducibility and auditability of the expert elicitation process and classifications.

## Data governance considerations for Data Stewards
- Standards and metadata:
  - Ensure consistent field definitions (e.g., Impact.outcome, Impact.mechanism, EICAT level, confidence, type, country).
  - Maintain consistent units (Area in km2) and clear taxonomy for species identification.
- Data quality and provenance:
  - Document the scoring process, rounds, and workshop to support reproducibility.
  - Preserve references and supporting information for each impact evaluation.
- Access and licensing:
  - Freely available data should be tracked for versioning and licensing to support open sharing.
- Updates and maintenance:
  - Clear process for updating impact scores or adding new case studies; consider versioning to capture changes.
- Interoperability and reuse:
  - Ensure data formats (CSV, PDFs) are accessible and supplemented with machine-readable metadata for cross-platform use.
- Challenges relevant to data stewardship:
  - Aligning user needs with dataset scope (e.g., if new stakeholders require different granularity).
  - Managing timely updates from collaborating experts and expanding to additional case studies.
  - Handling potential complexity in cross-country, cross-species datasets and ensuring consistent interpretation of outcomes.

## Use and relevance
- The datasets support prioritization and action planning for long-term IAS management by providing structured, expert-validated impact data across multiple contexts.
- Documentation and open access aim to facilitate discovery, reuse, and integration into broader governance and policy-making activities.