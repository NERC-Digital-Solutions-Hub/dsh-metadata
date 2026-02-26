# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2014.

## Overview
- Purpose: use timing of breeding in tits as an indicator of spring phenology and climate warming; first egg date is used as the timing metric.
- Context: part of a long-term study on how habitat, landscape factors, and environment influence woodland bird abundance, distribution, and breeding success.

## Scope and study design
- Study species: Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus).
- Study sites: Monks Wood, Brampton Wood, and Wennington Wood in Cambridgeshire, England.
- Nest boxes: wooden boxes (approx. 110 x 130 x 200 mm) at 1–2 m height; box accessibility varies by species and site; boxes added over time (e.g., dormouse boxes at Brampton Wood since mid-1990s affecting blue tit numbers in Brampton Wood).
- Timeframe: 1993–2014.
- Data collection approach: boxes inspected roughly weekly during the laying period (late March onward); first egg dates derived by counting back from observed eggs (one egg per day); only nests active at the time of observation are included; only first breeding attempts are recorded (no replacements or second broods).

## Data collected and variables
- Data file: GTBTfirsteggdates.CSV (Unicode), 39.4 KB; single dataset corresponding to a Minitab 16 worksheet saved as CSV.
- Columns (definitions):
  - Column 1: Species code (1 = Great Tit; 2 = Blue Tit)
  - Column 2: Site (1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood)
  - Column 3: Year number (1993 → Year 1, …, 2014 → Year 22)
  - Column 4: Nest box identifier (note: Monks Wood boxes 23–30 do not exist)
  - Column 5: First egg date (April 1 = 1; March dates appear as negative values; only 3 negative values total, in 1997)
  - Column 6: Sample size (N) for the number of clutches included per year
- Data encoding details:
  - First egg date encodes calendar timing relative to April 1
  - Negative values indicate March dates prior to April 1

## Data structure and provenance
- Data type: numerical CSV with six columns as described above
- Data provenance: field data collected by trained personnel; dates checked against original paper records
- Quality checks: line counts verified; values checked for outliers; individual egg dates validated against yearly site means

## Quality control and validation
- Verification against original paper records for date accuracy
- Consistency checks across lines and per-year site means to identify outliers
- Documentation notes ensure traceability of data handling and transformations

## Limitations and considerations for reuse
- Scope limitation: only first breeding attempts; excludes replacement clutches and second broods
- Incomplete user-needs picture possible due to site/year variations and box availability
- Box availability changed over time (e.g., certain boxes not present in some years), which may affect comparability across years/sites

## Governance and data stewardship considerations
- Metadata and standards: clear coding for species, site, year, and box IDs; ensure alignment with other related datasets
- Format and interoperability: CSV Unicode; consider providing a data dictionary and codebook for reuse
- Access and distribution: dataset suitable for upload to data portals and catalogues; define update procedures if the study continues beyond 2014
- Provenance and documentation: maintain detailed methodological notes (egg-date calculation method, active-nest inclusion criteria, annual sampling intensity)
- Reuse potential: can be linked with climate and phenology datasets; ensure consistent geographic and temporal formatting for integration with other records