# WildCrickets05A-CaptureRecapture

## Overview
- A dataset describing basic information on each male adult cricket tagged in the population for capture-recapture analysis.
- Key traits captured: Year, ID, Birth, Death, and Recapture days (2-99).

## Data fields and semantics
- Year: The year the cricket was alive.
- ID: Individual identification.
- Birth: Day of birth relative to the day of birth of the first adult cricket emerging that year; zeros indicate unknown birth dates.
- Death: Date of death relative to the birth of the first adult cricket emerging that year.
- 2-99: Recapture days (days on which recaptures occurred).

## Data governance and sharing considerations
- Metadata needs: ensure clear definitions of each field, units, reference points (e.g., first adult emergence), and treatment of unknowns (birth = 0).
- Data standards: consistent field naming (Year, ID, Birth, Death, 2-99), data types, and valid value ranges.
- Provenance and versioning: track data source, collection procedures, and any transformations or cleanings applied.
- Access and sharing: define who can access the data, any embargoes, and licensing; document sharing limitations if applicable.
- Publication and cataloging: upload to relevant portals and ensure the dataset is discoverable with a descriptive description and keywords.

## Data quality and processing
- Quality assurance: verify accuracy of ID mappings, consistent reference to the first adult emergence year, and plausible Birth/Death relative to Year.
- Data cleaning: handle missing or zero Birth dates explicitly; confirm Death values are consistent with Birth references.
- Transformations: document any derived fields or recoding performed during processing.

## Accessibility and discovery
- Provide a data dictionary and metadata file alongside the dataset.
- Ensure discoverability in data catalogs with clear subject (cricket population, capture-recapture) and species notes.

## Potential challenges
- Incomplete user needs or ambiguous usage scenarios for capture-recapture analyses.
- Ensuring timely data receipt and updating across studies or years.
- Managing metadata completeness for births, deaths, and recapture days.
- Interoperability with other datasets or formats, especially across different years or study sites.
- Handling updates when birth/death data are revised or recapture patterns change.

## Recommendations for Data Stewards
- Create and maintain a comprehensive data dictionary covering all fields and their interpretations.
- Establish clear data entry standards and validation rules to minimize missing or inconsistent Birth/Death values.
- Implement version control and changelog for updates to the dataset.
- Document data provenance, collection methods, and any preprocessing steps.
- Ensure dataset is uploaded to appropriate data portals with proper metadata to support discovery and reuse.