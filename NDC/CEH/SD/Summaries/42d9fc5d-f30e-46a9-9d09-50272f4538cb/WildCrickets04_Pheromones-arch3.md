# WildCrickets04_Pheromones Description of content

- Overview: Describes the pheromonal profile of cuticular hydrocarbons (CHCs) taken from the thorax of each adult cricket, totaling 32 compounds analyzed per cricket.

- Dataset structure: Each record represents an individual cricket with associated metadata and chemical measurements.

- Data fields:
  - Year: The year when the cricket was alive.
  - Tag: A two-character code used to identify the cricket in video recordings (plastic tag read from the cricket’s pronotum).
  - Sex: Male (M) or Female (F).
  - Peak1 to Peak40: Columns corresponding to CHC peaks; these contain the score for each compound. The description notes 32 CHC peaks but includes 40 peak columns, indicating a potential inconsistency between the stated number of compounds (32) and the number of peak columns (Peak1–Peak40).

- Linkages and provenance:
  - Each cricket is tracked by the Tag, enabling alignment between chemical data and video observations.
  - The dataset integrates chemical analysis results with individual identifiers and life-history year.

- Potential inconsistencies to note:
  - Mismatch between the stated number of CHC compounds (32) and the presence of Peak1–Peak40 (40 columns). Clarification needed on the actual number of peaks and corresponding metadata.

- Implications for monitoring frameworks:
  - Demonstrates how biological/chemical indicators can be structured for policy-relevant monitoring (individual-level data linked to time and observational context).
  - Highlights the importance of robust metadata, clear naming conventions, and data provenance when aggregating biological monitoring data for decision-making.

- Data governance considerations:
  - Ensure metadata completeness (units, methods, instrument details, data processing steps).
  - Address potential data quality issues (inconsistencies in peak counts, missing values, standardization across datasets).
  - Maintain clear data sharing and linkage between primary observations (video) and analytical results (CHC peaks) to support transparency and reproducibility.