# Woodlands Survey flora data 1971-2001

## Overview
- A dataset of 103 broadleaved woodlands surveyed in 1971, with detailed plot-level ecological data collected from 16 randomly placed 200 m2 plots per site.
- Re-surveys conducted in 2000, 2002, and 2003 using the same field methods to assess ecological change.
- Analyses aimed to identify principal drivers of change, including atmospheric deposition (S and N), climate, canopy changes, and woodland management.
- Key publications to consult for methods and results: Kirkby et al. (2005) and Corney et al. (2004); baseline methodological references available in the field handbook and related literature.

## Dataset scope and content
- Site-level data: 103 sites; Plot-level data: 16 plots per site.
- Recorded variables include canopy and ground flora composition, soil pH, soil organic matter, habitat management, and a wide set of plot and site descriptors.
- Related dataset linkages: Countryside Survey and earlier national woodland surveys (Steele, 1968).

## Methods and design
- Stratified sampling across the surveyed area.
- Field methods follow Bunce & Shaw (1973) standardized survey protocols.
- A field handbook accompanies the dataset to document procedures.

## Data structure and field details
- Site: numeric code (1–103).
- Plot: numeric (1–16) with descriptive plot numbers.
- BRC_number: numeric code for species (Biological Record Centre list); BRC_names provides scientific names.
- Amalgams and Amalgam_names: cross-taxa groupings created when recording was inconsistent (e.g., combining similar species groups); records may include multiple entries for a single plot.
- NEST: numeric indicator for inner 2×2 m plot nest (not always consistently filled; not present in 1971 records).
- COV: numeric percentage cover for the whole plot; special codes: -1 for bare ground/litter/wood/rock/water; 0.5 = <1% cover; null values for woody species measured differently (numbers/DBH).
- YR and Yr_2: year indicators (1971, 2000 pilot, 2002, 2003) and year-code (yr 1 vs yr 2).
- Bryo/Woody: taxonomy flags (b = bryophyte, l = lichen; w = woody).
- Field_sheet: source data sheet (e.g., “Ground flora”).
- All records include trees, shrubs, saplings, bryophytes, and herbaceous species where applicable.

## Temporal coverage and provenance
- 1971 baseline survey across 103 sites with standardized methods.
- 2000 (pilot) and 2002–2003 resurveys using identical field methods to enable long-term change assessment.
- Originators in 1971: Bunce & Shaw (Nature Conservancy, Merlewood); 2001–2003 contributors included Smart, Black, Kirby, Corney (CEH Lancaster, English Nature, University of Liverpool).

## Related resources and references
- Related datasets: Countryside Survey; Steele (1968) national woodland survey.
- Key publications for context and methods: 
  - Corney et al. (2004) on landscape-scale drivers of woodland vegetation.
  - Haines-Young et al. (2003) on landscape and vegetation diversity across Great Britain.
  - Kirby et al. (2005) Measuring Long Term Ecological Change in British woodlands (1971–2001): re-survey and analysis.
  - Avery (1973) on soil classification.
- Users should consult the cited publications for detailed field methods and analytical approaches.