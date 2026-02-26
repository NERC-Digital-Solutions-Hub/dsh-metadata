# WildCrickets04_Pheromones Description of content

## Overview
- Describes the pheromonal profile (cuticular hydrocarbons, CHCs) from the thorax of each adult cricket.
- Dataset covers 32 CHC compounds (peaks), collected from a sample of crickets.
- Each cricket entry includes identifiers and measurements for time and individual.

## Data fields and structure
- Year: The year the cricket was alive (time reference for monitoring).
- Tag: A two-character code identifying the cricket from video recordings; each cricket has a plastic tag readable in video.
- Sex: Male (M) or Female (F).
- Peak1 to Peak40: Columns representing CHC peaks; correspond to the 32 CHC compounds analyzed, with a score per compound per cricket. Note: text mentions 32 compounds but columns are labeled Peak1 to Peak40, indicating 40 peak columns in the file but 32 compounds described.

## Data quality and provenance
- Data are tied to individual crickets via the Tag, enabling traceability across video data and chemical measurements.
- Year provides a temporal axis for environmental/biological monitoring.
- CHC peak scores provide a quantitative chemical profile per cricket for monitoring changes over time.

## Applications for environmental monitoring
- Enables tracking of chemical ecology indicators (CHC profiles) across time and individuals.
- Can be used to assess population-level chemical trait variation in relation to environmental conditions or policy outcomes.
- Outputs can be combined with other datasets (e.g., behavioral observations, habitat data) to enhance environmental health assessments.

## Data management and sharing considerations
- Align with standard monitoring practices: verify, quality assure, clean, and transform data before analysis.
- Store and upload the dataset to appropriate portals to support accessibility and reuse.
- Consider integrating underlying cricket identifiers (Tag, Year, Sex) with broader datasets to maximize data reuse and value.

## Notes and clarifications
- There is a discrepancy between “32 compounds” and the columns labeled Peak1 to Peak40; the file contains 40 peak columns but describes 32 CHC compounds. Clarification may be needed during data curation.