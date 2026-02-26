# WildCrickets04_Pheromones Description of content

## Overview
- Describes pheromonal profiles of cuticular hydrocarbons (CHC) taken from the thorax of each adult cricket.
- Total: 32 CHC compounds measured.
- Structure includes columns named Year, Tag, Sex, Peak1 to Peak40.
- The Peak columns correspond to CHC peaks; each column holds the score for the cricket for that compound.
- Note: there is an inconsistency between the stated number of compounds (32) and the Peak1–Peak40 column range that should be clarified.

## Data structure and fields
- Year: year when the cricket was alive.
- Tag: two-character code identifying the cricket in video recordings; read from a plastic tag on the pronotum.
- Sex: M (male) or F (female).
- Peak1 to Peak40: columns intended to represent CHC peaks; described as the 32 compounds in the text, though the 40 peak columns are listed.

## Metadata and provenance considerations
- Missing in the current description: measurement method (e.g., GC data), units, instrument details, calibration, and data processing steps.
- Important to document:
  - Definition and meaning of each Peak column (which compound each peak corresponds to).
  - Units, scale, and any normalization or transformation applied.
  - Data collection date, sample handling, and processing workflow.
  - Version of dataset and any transformations performed.

## Data quality and governance
- Validate data types (Peak columns numeric), handle missing values, and record any imputation.
- Ensure unique and stable linkage between Year, Tag, and Sex to individual crickets.
- Implement data quality checks and a data cleaning/processing log prior to sharing.

## Sharing, accessibility, and lifecycle
- Plan for deposit in appropriate data portals and catalogues; assign a persistent identifier (e.g., DOI).
- Provide a metadata file or README with field definitions, units, methods, and data quality notes.
- Specify licensing and usage terms; note any embargoes or restrictions related to linked video data.

## Practical considerations for reuse by Data Stewards
- Ensure alignment with data governance standards: consistent naming, complete metadata, and versioning.
- Develop or adopt a metadata schema that clearly defines each field, units, and data provenance.
- Include descriptive documentation to improve dataset discoverability (title, keywords, license, and DOI).
- Establish a plan for updates and maintenance, including how new data would be integrated.

## Ambiguities and recommended actions
- Clarify the discrepancy between “32 compounds” and Peak1–Peak40 columns (confirm exact number of CHC peaks and corresponding columns).
- Add metadata detailing measurement methods, units, and processing steps to enable proper reuse and interpretation.