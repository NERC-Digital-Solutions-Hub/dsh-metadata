# WildCrickets04_Pheromones Description of content

## Overview
- A data file detailing the pheromonal profile of cuticular hydrocarbons (CHC) from the thorax of adult crickets.
- Covers a sample of individuals with 32 CHC compounds analyzed.

## Data structure
- Each row represents a cricket (an individual cricket).
- Columns include:
  - Year: The year when the cricket was alive.
  - Tag: A two-character code identifying the cricket in video recordings (read from a plastic tag on the cricket).
  - Sex: Male (M) or Female (F).
  - Peak1 to Peak40: Columns corresponding to CHC peaks/compounds and their recorded scores.
- Note: The description mentions 32 CHC peaks, but the columns are labeled Peak1 to Peak40, indicating a potential mismatch that needs clarification.

## Variables and data types
- Year: Numeric (year-based).
- Tag: Categorical/string identifier.
- Sex: Categorical (M/F).
- Peak1–Peak40: Numeric scores for each CHC peak (likely continuous measurement).

## Purpose and potential uses
- To enable exploration of CHC profiles across crickets and by group attributes (Year, Sex, Tag).
- To support data products that facilitate self-serve analysis, such as dashboards, pivot tables, and charts.
- To aid in identifying patterns, differences by sex or year, and significant CHC peaks.

## Data quality considerations
- Possible inconsistencies: mismatch between "32 compounds" and Peak1–Peak40 column range.
- Potential issues to verify: missing values in peak columns, mislabeling, and consistency of Year/Tag/Sex entries.
- Action needed: confirm the exact number of CHC peaks and align column naming accordingly; implement data cleaning and validation rules.

## Data support recommendations
- Clean and transform: harmonize peak count naming, handle missing values, and ensure consistent data types.
- Metadata and documentation: provide a data dictionary detailing each Peak column, units, and any preprocessing steps.
- Analytical outputs: prepare ready-to-use data products such as per-cricket profiles, summary statistics by Year/Sex, and visualization-ready datasets.
- Sharing and dissemination: develop early prototypes (dashboards, pivot tables) and gather feedback to improve reuse and uptake.
- Data quality improvements: advocate for standardized data recording practices to reduce future inconsistencies.