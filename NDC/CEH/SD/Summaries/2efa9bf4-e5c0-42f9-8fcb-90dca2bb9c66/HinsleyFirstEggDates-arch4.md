# Dataset Title

- Dataset documenting the first egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England, from 1993 to 2015.

## Overview

- Purpose: Part of a long-term study on habitat, landscape factors, and breeding success of woodland birds; also serves as an indicator of spring phenology and climate warming.
- Species: Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus)
- Study sites: Monks Wood, Brampton Wood, and Wennington Wood in Cambridgeshire
- Data format: CSV (Unicode), GTBTfirsteggdates.CSV, ~42 KB

## What’s in the dataset

- Columns and coding:
  - Species code: 1 = Great Tit; 2 = Blue Tit
  - Site: 1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood
  - Year number: 1993 = Year 1 through 2015 = Year 23
  - Nest box identifier: box IDs per site (note: some boxes do not exist in certain years)
  - First egg date: coded with April 1 = 1; March dates appear as negative values (3 negatives observed, all in 1997)
  - Sample size: N for clutches included per year
- Data scope:
  - 1993–2015 across three woods
  - Box coverage varies by site/year (e.g., Monks Wood box range changes by period)
- Data structure:
  - Observations come from breeding in wooden nest boxes; box height 1–2 m; hole sizes determine accessibility (Blue Tits vs both species)

## Data collection and provenance

- Monitoring protocol:
  - Boxes inspected approximately weekly during the laying period (start ~late March)
  - First egg date inferred by counting backwards from observed egg count (one egg per day)
  - Only nests active at observation included; only first breeding attempts are recorded (replacements and second broods excluded)
- Box and habitat context:
  - Boxes set with controlled hole sizes; Brampton Wood includes dormouse boxes that may influence Blue Tit abundance
  - Boxes located in deciduous woodland areas with variable surrounding habitat (ash, oak, maple, hawthorn, hazel, blackthorn)

## Data structure and format

- File format: CSV (Unicode)
- File name: GTBTfirsteggdates.CSV
- Data validation:
  - Data collected by trained personnel
  - Egg dates checked against original paper records
  - Consistency checks across lines and against yearly means

## Quality control and reliability

- Multiple layers of QA:
  - Field data verified by experienced staff
  - Dates validated against primary records
  - Line counts checked; outliers reviewed
  - Individual egg dates cross-checked with yearly means per site
- Reliability notes:
  - Rare negative dates (March occurrences) and a small number of March dates observed
  - Data coverage varies by site and year due to box availability and management of sites

## Context, use cases, and governance

- Use cases for data leaders:
  - Track phenology and climate-related shifts in breeding timing across multiple sites and years
  - Integrate with habitat/landscape datasets to assess factors influencing breeding success
  - Support data quality, provenance, and metadata standards for long-term ecological studies
- Governance considerations:
  - Clear documentation of box configurations, site changes, and year-by-year box counts
  - Maintain consistent encoding for species, sites, and year numbering
  - Ensure metadata includes data origin (field protocols, QA steps) and any deviations across years

## Access, limitations, and caveats

- Limitations:
  - Box numbers and availability change by site and year, affecting comparability at fine scale
  - Some gaps in data due to box availability or field conditions
- Important caveats for interpretation:
  - First egg date encoding requires careful handling of March dates (negative values)
  - Data represent first breeding attempts only; not suitable for analyses of second clutches without additional data
- Metadata and lineage:
  - Dataset is part of a broader long-term study; consider linking to habitat and landscape factor data for comprehensive analyses