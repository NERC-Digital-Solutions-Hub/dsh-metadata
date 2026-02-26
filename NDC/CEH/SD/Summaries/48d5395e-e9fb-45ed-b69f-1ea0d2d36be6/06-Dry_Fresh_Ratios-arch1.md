# Supporting documentation for 06-Dry_Fresh_Ratios.csv

- Purpose
  - Provides metadata and field definitions for the 06-Dry_Fresh_Ratios.csv data file.
  - Documents how dry-to-fresh mass ratios are represented (mean, min, max) across samples.

- Data represented
  - Mean_Value_Dry/Fresh_Ratio: mean ratio of dry mass to fresh mass (unitless).
  - Min_Value_Dry/Fresh_Ratio: minimum observed ratio (unitless).
  - Max_Value_Dry/Fresh_Ratio: maximum observed ratio (unitless).
  - Sample_Type: general description of the sample group (e.g., foodstuff group).
  - Sample_Description: part of the organism analysed (where the whole organism was divided and analysed separately).
  - All ratio fields are unitless; Sample_Type, Sample_Description have no specified units.

- Fields and Metadata
  - Sample_Type
    - Explanation: General description of sample (e.g., foodstuff group).
    - Units: n/a.
    - Notes: n/a.
  - Sample_Description
    - Explanation: Part of the organism analysed (i.e., where whole organism was divided and analysed separately).
    - Units: n/a.
    - Notes: n/a.
  - Mean_Value_Dry/Fresh_Ratio
    - Explanation: Mean value of ratio between dry mass and fresh mass.
    - Units: Unitless.
    - Notes: n/a.
  - Min_Value_Dry/Fresh_Ratio
    - Explanation: Minimum value of ratio between dry mass and fresh mass.
    - Units: Unitless.
    - Notes: n/a.
  - Max_Value_Dry/Fresh_Ratio
    - Explanation: Maximum value of ratio between dry mass and fresh mass.
    - Units: Unitless.
    - Notes: n/a.

- How to use for analysis
  - Compare mean dry-to-fresh ratios across different Sample_Types and Sample_Descriptions to identify systematic differences in tissue composition.
  - Use Min/Max values to assess the range and variability within sample groups.
  - Align interpretations with the describedSample_Description to ensure consistent grouping (e.g., specific tissues or parts).

- Data quality and reproducibility considerations
  - Metadata clarifies what each field represents, aiding interpretation and re-use.
  - Unitless ratios facilitate cross-sample comparisons but require consistent sampling and description.
  - No explicit data values are provided here; this is a metadata dictionary to accompany the CSV data.