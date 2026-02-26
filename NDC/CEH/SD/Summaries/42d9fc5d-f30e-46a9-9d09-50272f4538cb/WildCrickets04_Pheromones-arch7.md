# WildCrickets04_Pheromones Description of content

## Overview
- Dataset captures pheromonal profiles (cuticular hydrocarbons, CHCs) from the thorax of adult crickets.
- Includes measurements for 32 CHC compounds per cricket.
- Each row represents an individual cricket with associated metadata.

## Data structure
- Rows: individual crickets.
- Columns:
  - Year: Year when the cricket was alive.
  - Tag: Identifier code read from a plastic tag attached to the cricket.
  - Sex: Male (M) or Female (F).
  - Peak1 to Peak40: Scores for CHC peaks; described as 32 CHC peaks, but columns span Peak1 to Peak40 (potential inconsistency to verify).

## Variables explained
- Year: Temporal attribute for cohort/tracking.
- Tag: Unique identifier linking to video recordings.
- Sex: Biological sex, relevant for comparing pheromone profiles.
- Peak1–Peak40: Quantitative measures for each CHC compound; intended to reflect the pheromonal profile.

## Geospatial considerations for GIS
- The dataset does not include explicit geographic coordinates or site data.
- Potential GIS use if location or site data from related studies are available:
  - Join with geospatial metadata to map pheromone profiles by site, year, or sex.
  - Create spatial dashboards if cricket collection locations are available.
- Immediate visualization opportunities (non-spatial): time-series or box plots of peak scores by year and sex, and per-tag visualizations.

## Data quality and processing notes
- Clarify the mismatch between “32 compounds” and “Peak1 to Peak40” columns (likely 32 CHCs described but 40 peak columns present).
- Require data cleaning: handle missing peak values, normalize peak scores across samples, and ensure consistent data types (Year numeric, Tag string, Sex categorical, Peaks numeric).

## How this data could be used in GIS projects
- Integrate with location data to map pheromonal variation across spatial units (sites, habitats).
- Visualize multi-dimensional pheromone profiles via companion charts on a GIS-enabled dashboard.
- Comparative analyses by year and sex to explore temporal and demographic patterns in CHC profiles.

## Practical considerations for GIS specialists
- Ensure data standards alignment when joining with external geospatial datasets.
- Maintain clear metadata documenting the peak-column mapping to CHC compounds and any column inconsistencies.
- Consider transforming peak data into a long format suitable for spatial-visual analytics if linking to coordinates.