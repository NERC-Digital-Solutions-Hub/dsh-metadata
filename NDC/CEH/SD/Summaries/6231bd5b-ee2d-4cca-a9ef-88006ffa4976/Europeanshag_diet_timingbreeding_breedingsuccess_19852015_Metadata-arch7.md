# JAE_Keogan_Europeanshag_phenologymismatch_shagdataset

## Overview
- A set of three related datasets describing European shag phenology, diet, and their relationships with sandeel consumption across years.
- Focuses on timing of breeding events (laying, hatching/fledging), diet composition (sandeel presence), and cross-dataset comparisons between shag and sandeel.

## Datasets included

- JAE_Keogan_Europeanshag_phenologymismatch_shagdataset
  - year: Year
  - laydate: Day first egg in nest was laid; day of year from January 1
  - chicks.fledged.first: Number of chicks fledged in the first clutch
  - failedeggsfirst: Number of failed eggs (up to four) in the first clutch
  - Mean.Lay: Average lay date in each year (day of year)
  - relative.lay: Nest lay date relative to annual mean lay date (in days)
  - SST.past: Average February/March SST in year-1
  - SST.present: Average February/March SST in current year
  - pop.size: Population size in breeding pairs
  - yearcentre: Year centered around the study’s average year
  - chicks.fledged.all: Number of chicks fledged from all clutches
  - failedeggsall: Number of failed eggs from all clutches

- JAE_Keogan_Europeanshag_phenologymismatch_dietdataset
  - Year: Year
  - Date: Day of sample collection (since Jan 1)
  - Age: Whether sample was for a chick or an adult
  - SST: Average February/March SST in current year
  - yearcentre: Year centered around the study’s average year
  - meandate: Average date of sample collection in each year
  - datediff: Sample collection date centered around the average annual sample collection date
  - SE1:SE0_proportion: Proportion of 1+ sandeels relative to all sandeels in sample
  - logitSE1:SE0: Proportion above logit-transformed

- JAE_Keogan_Europeanshag_phenologymismatch_bivariatedataset
  - Year: Year
  - Species: shag or sandeel
  - chicks.fledged: Number of chicks fledged
  - failedeggs: Number of potential failed eggs
  - sandeelproportion: Proportion of 1+ sandeels relative to all sandeels in sample
  - dayofyear: Day of laying (shags) or day of sample collection (sandeels)
  - Mean.Lay: Average lay date in each year
  - Relative: Day of year centered around the average lay date

## GIS- and data-processing considerations

- Temporal alignment
  - Use year as the primary temporal unit and leverage yearcentre and relative/centred day fields to compare timing across years.
- Data fusion
  - Join datasets on Year (and, where appropriate, site identifiers if available) to produce integrated analyses of phenology, diet, and reproduction.
- Derived geospatial outputs
  - If site/location data exists, map colony-level phenology indicators (lay date, fledging counts) and diet metrics (sandeel proportion) across sites and years.
  - Create time-enabled maps or animation to show changes in phenology and diet over time.
- Data harmonization
  - Standardize date representations (DOY vs. absolute calendar dates), ensure SST variables are consistently defined (past vs present), and align units across datasets.
- Quality assurance
  - Address missing values (e.g., incomplete clutches, missing diet samples), and document any year gaps or sampling biases.
- Data standards and interoperability
  - Align field names and units with common GIS datasets; maintain metadata for reproducibility.
- Visualization targets
  - Time-series charts per metric (lay date, fledging counts, sandeel proportion) and, where possible, spatial choropleths or heatmaps by site and year.

## Practical GIS outputs and workflows

- Phenology maps (yearly):
  - Visualize lay dates and fledging counts per colony/site, with relative timing indicated.
- Diet and phenology cross-plots:
  - Explore relationships between lay timing (Mean.Lay, Relative) and sandeel consumption (sandeelproportion, SE1:SE0_proportion).
- Integrated dashboards:
  - Combine population size, lay timing, and diet metrics to assess mismatch between shag phenology and prey availability across years.
- Change detection:
  - Assess year-over-year changes in SST and their association with phenology shifts and diet composition.

## Key considerations for addressing typical GIS challenges

- Data is spread across multiple sources with varying resolutions; plan for dataset integration and resolution harmonization.
- Potential gaps in data, especially at suitable resolutions, may require interpolation or cautious interpretation.
- Establish consistent data standards and documentation to support reliable map-based visualizations and analyses.
- Engage end users early and iterate visualizations based on feedback to ensure the spatial outputs meet policy, client, or public information needs.