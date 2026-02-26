# WildCrickets01-BasicTraits Description of content

- Purpose: Describes basic trait data for each adult tagged individual in the population, covering identifiers, timing of life events, and body measurements to support analysis and visualization.

- Fields included:
  - Year: Year when the cricket was alive.
  - Tag: Code used to identify the cricket in video recordings (plastic tag on pronotum).
  - Sex: Male (M) or Female (F).
  - Emerged: Date when the cricket emerged as an adult (may be empty if unknown).
  - Tagged: Date when the cricket was first caught and tagged.
  - Dead: Date when the cricket died or, if death is not recorded, the last observed date.
  - ThoraxWidth: Width of the thorax measured from a top-down image.
  - BodyMass: Mass of the cricket on the tagging date.
  - Monitored: Number of days the individual has been under observation.

- Data quality notes:
  - Emerged may be missing for some individuals.
  - Dead uses the last observation date if death is not recorded.

- Potential data transformations and derived metrics:
  - Age at tagging and time since emergence.
  - Survival indicators (alive vs. dead) and duration of monitoring.
  - Derived size metrics and growth trends (using ThoraxWidth and BodyMass over time if multiple records exist).
  - Consistency checks across Tag identifiers and video references.

- Practical data support and usage:
  - Build basic histograms and summaries of ThoraxWidth and BodyMass by Year, Sex, or status (alive/dead).
  - Create simple dashboards or pivot tables to explore size, timing, and observation duration.
  - Combine with other datasets (e.g., emergence or tagging events) to analyze life-history patterns.
  - Provide guidance on handling missing Emerged values and interpreting Dead dates.