# Supporting documentation for 06-Dry_Fresh_Ratios.csv

## Purpose and scope
- Documents the structure and metadata of the 06-Dry_Fresh_Ratios.csv dataset.
- Defines five main fields: Sample_Type, Sample_Description, Mean_Value_Dry/Fresh_Ratio, Min_Value_Dry/Fresh_Ratio, Max_Value_Dry/Fresh_Ratio.
- Each field includes its Explanation, Units, and Notes.

## Data fields and metadata
- Sample_Type
  - Explanation: General description of sample (i.e. foodstuff group)
  - Units: n/a
  - Notes: n/a
- Sample_Description
  - Explanation: Part of the organism analysed (i.e. where whole organism was divided and analysed separately)
  - Units: n/a
  - Notes: n/a
- Mean_Value_Dry/Fresh_Ratio
  - Explanation: Mean value of ratio between dry mass and fresh mass
  - Units: Unitless
  - Notes: n/a
- Min_Value_Dry/Fresh_Ratio
  - Explanation: Minimum value of ratio between dry mass and fresh mass
  - Units: Unitless
  - Notes: n/a
- Max_Value_Dry/Fresh_Ratio
  - Explanation: Maximum value of ratio between dry mass and fresh mass
  - Units: Unitless
  - Notes: n/a

## Data types and units
- All ratio fields (Mean, Min, Max) are unitless.
- Descriptors for Sample_Type and Sample_Description have no specified units (n/a).

## Intended uses and value for analysis
- Provides baseline metadata to interpret dry-to-fresh mass ratios across different sample types and body parts.
- Enables computation or verification of descriptive statistics (mean, min, max) for dry/fresh mass ratios.
- Supports downstream data products such as dashboards, pivot tables, and reports that allow end users to explore these ratios by sample type and description.

## Data quality and consistency considerations
- Consistency of Sample_Type and Sample_Description is important for reliable grouping.
- Ensure that mean, min, and max values are coherent (e.g., min ≤ mean ≤ max for each group).
- Given many fields are labeled n/a in Units/Notes, additional metadata may be needed for richer context and provenance.

## How Data Support can leverage this dataset
- Create self-serve dashboards showing dry/fresh ratio statistics by Sample_Type and Sample_Description.
- Join with other datasets to enrich analyses (e.g., by organism, condition, or sample source).
- Gather user feedback and iterate on data products to improve usability and adoption.
- Promote outputs and assess reuse to maximize impact.