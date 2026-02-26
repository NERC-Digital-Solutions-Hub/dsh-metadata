# Woodlands Survey flora data 1971-2001

## Overview
- Long-term ecological data from 103 broadleaved woodlands in Britain, with baseline data (1971) and follow-up surveys in 2000, 2002, and 2003 using identical field methods.
- Aimed at understanding ecological change and identifying principal drivers (atmospheric deposition of sulfur and nitrogen, climate, canopy change, woodland management).
- Results linked to published analyses (e.g., Kirby et al. 2005; Corney et al. 2004).

## Study design and data collection
- Stratified sampling across the survey area; fieldwork conducted using Bunce & Shaw (1973) standardized methods; a field handbook is provided.
- Within each site, 16 plots (2 m x 2 m) sampled randomly.
- Data collected at both site level and plot level, including:
  - Plant species composition (canopy and ground flora)
  - Soil pH and Soil Organic Matter
  - Habitat management and a wide range of plot- and site-level descriptors
- Re-surveys in 2000, 2002, and 2003 used the same field methods to enable comparisons over time.

## Data structure and variables
- Core data structure:
  - Site: numeric code (1–103)
  - Plot: numeric code (1–16)
  - BRC_number: species code (Biological Record Centre)
  - BRC_names: scientific species name
  - Amalgams: grouped cross-specific taxa to reflect recording inconsistencies
  - Amalgam_names: scientific names for amalgams
  - NEST: nested plot estimate indicator (inner 2x2 m plot)
  - COV: percentage cover for the whole plot
  - YR: survey year (1971, 2000 as pilot, 2002, 2003)
  - Yr_2: year coding (yr1=1971; yr2=2000/2002/2003)
  - Bryo/Woody: flags for bryophytes/lichens or woody species
  - Field_sheet: original data sheet reference
- Data nuances and limitations:
  - In the 2000s data, bare ground/litter/water/rock/mud records were amalgamated due to inconsistent recording; multiple entries for a single code in one plot may occur.
  - Some fields have null values (e.g., woody species entries recorded as counts/DBH rather than presence/absence).
  - 0.5 in COV denotes <1% cover; -1 indicates presence of bare ground/litter/wood/rock/total bryophyte/water in certain cases.
  - The field handbook should be consulted for exact field methods and data interpretation.

## Data quality, governance, and sharing
- Metadata completeness and consistency are critical; some data recorded inconsistently across years required harmonization (e.g., amalgams).
- Standardization through field handbook and prior publications; the data structure supports reproducible analyses.
- Public dissemination of underlying data and clear documentation are emphasized; users are advised to refer to the linked publications for detailed methods and analytical context.

## Related datasets and context
- Related dataset: Countryside Survey (external data source for comparative context).
- Foundational references and analyses:
  - Corney et al. 2004; Haines-Young et al. 2003; Kirby et al. 2005
  - The 1971 baseline and subsequent re-survey analyses focus on drivers of long-term ecological change in British woodlands.

## Originators and data provenance
- 1971 originators: R.G.H. Bunce & M.W. Shaw (Nature Conservancy, Grange-over-Sands)
- 2001–2003 contributors: Simon Smart, Helaina Black, Keith Kirby, Phil Corney (CEH Lancaster, English Nature, University of Liverpool)
- Field methods and data collection were standardized and documented in the supporting field handbook.

## References
- Avery (1973); Corney et al. 2004; Haines-Young et al. 2003; Kirby et al. 2005
- The 1971–2001 study: Measuring Long Term Ecological Change in British Woodlands (English Nature Research Reports 653)