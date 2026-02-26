# Forest Plantations Dataset

## Overview
- A large, multi-site dataset of plantation records identified by codes (e.g., A1, A2, A7, B3, C17, D32, E44, etc.).
- Each record includes spatial coordinates (Easting, Northing), initial planting details, soil type, and harvest/rotation history.
- Planting history often includes: first planting year and species, second planting year and species, and whether the crop is standing or felled.
- Start and end dates are provided in fragmented components (day, month, year) and sometimes span multiple lines or entries per site.
- Several entries indicate missing data (NA), placeholders (e.g., Year felled = Standing crop), or inconsistent date formats (e.g., two-digit year codes such as 95 or 97).

## Data structure and content
- Core fields per record:
  - Identifier (e.g., A1, A2, B3, C17, D32, E44)
  - Location: Easting and Northing
  - First planting: year and tree species
  - Soil type
  - Year felled and Year of second planting
  - Second planting: year and species
  - Start date and End date components (Day, Month, Year)
- Some entries include multiple planting cycles (first planting, possible second planting) and outcomes (standing crop vs. felled).
- Tree species represented include Sitka spruce, Norway spruce, Western hemlock, Japanese larch, Lodgepole pine, Scots pine, Noble fir, Douglas fir, Silver Birch, and others.
- Soils vary widely (Gley, Podzol, Brown earth, Bog) with region-specific designations (e.g., IIP, PIP, SWG, PG).
- Dates suggest activity spanning mid-20th century to late 1990s, with end dates often coded as two-digit years (e.g., 97 for 1997).

## Data quality and metadata considerations
- Widespread missing values (NA) and inconsistent formatting raise quality concerns.
- Date fields are fragmented (separate Day/Month/Year) and sometimes incomplete or repeated, complicating temporal analyses.
- Some records use placeholders like Standing crop instead of a specific felled year, requiring interpretation for lifecycle analyses.
- The dataset would benefit from a standardized schema, explicit metadata, and a data dictionary to define:
  - Meaning of Standing crop vs. numeric felled years
  - How to interpret two-digit year codes (e.g., 95 = 1995)
  - Handling of NA values and partial dates

## Patterns, examples, and potential analyses
- Geographic dispersion across multiple easting/northing coordinates implies a wide spatial coverage of plantation sites.
- Species distribution shows a mix of conifers (Sitka spruce, Norway spruce, Western hemlock, Scots pine, Lodgepole pine) and other species (Japanese larch, Noble fir, Douglas fir).
- Rotation history varies: some sites have second planting events years after first, others are marked as standing crop or NA for second planting.
- Soil type correlations with species and rotation outcomes could be explored (e.g., Sitka spruce on Gley vs. Podzol vs. Brown earth).
- Temporal patterns in planting and harvesting could be analyzed to understand succession, rotation lengths, and management practices over decades.

## Governance and data strategy recommendations for Data Leaders
- Establish a unified data model and data dictionary to standardize fields (Identifiers, location, planting events, soil types, dates, and status).
- Implement data quality rules:
  - Normalize two-digit year codes to four-digit years
  - Explicitly distinguish between felled years, standing crop, and unknowns
  - Validate and reconcile repeated or multi-line records for the same site
- Improve metadata:
  - Document provenance, data sources, collection methods, and any aggregations
  - Provide field-level definitions, acceptable values, and handling of missing data
- Enhance discoverability and usability:
  - Create a central catalog with clear schema, data types, and example queries
  - Provide data access guidance, including how to interpret partial dates and status fields
- Support analytical readiness:
  - Normalize unit formats and align coordinate systems if integrating with other geospatial datasets
  - Define canonical time granularity (e.g., annual) for temporal analyses
- Foster community and collaboration:
  - Document and share best practices for data collection across sites
  - Encourage feedback loops with data producers and users to improve data quality and utility
- Plan data stewardship:
  - Assign owners for data quality, metadata completeness, and update processes
  - Establish update cycles to incorporate new planting/harvest records and corrections

## Potential use cases for data leaders
- Tracking historical plantation rotations and harvest cycles across sites.
- Analyzing species distribution by soil type and geography to inform reforestation strategies.
- Assessing data completeness and quality gaps to prioritize data collection efforts.
- Supporting decision-making for data standards, provenance, and governance in large, multi-site datasets.