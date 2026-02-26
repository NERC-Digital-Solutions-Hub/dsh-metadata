# BSBI axiophyte scores - metadata, May 2016

## Overview
- Defines axiophytes as indicators of high-quality habitat.  
- Produces national (Great Britain) level axiophyte-ness scores by aggregating 24 county lists.  
- Creates a meta-list of axiophytes to be updated as more county lists become available.

## Data sources
- County data: 24 GB counties lists downloaded February 2014 from the BSBI website; excludes 3 Irish lists (Antrim, Fermanagh, Waterford). Some counties represented by two vice-counties.
- Raw and cleaned data files:
  - axiophytes_as_published.csv: original county-axiophyte data as published.
  - axiophytes_Feb_2014.csv: cleaned county axiophyte list.
  - counties_included.csv: details of counties included in the analysis.
  - exclusions_with_reason.csv: taxa excluded and reasons.
  - county_occurrence.csv: occurrence data per county (VCCC) used for scoring, with status notes up to 1999 in VCCC.
- Taxon name reconciliation: cross-checked against Stace (1997) and Stace (2010) with corresponding name-change notes.

## Cleaning and data processing
- Exclusions:
  - Hybrids, microspecies, charophytes, neophytes, and natives known to be neophytes in a county are excluded.
  - Subspecies/varieties typically collapsed within species unless the subspecies is the only native/archaeophyte taxon.
- Name standardization: align taxa with Stace editions; include changes in separate columns.
- Data cleaning applied consistently to both axiophyte lists and VCCC data prior to scoring.

## Calculation method
- Axiophyte score = (number of counties where a species is listed as axiophyte) ÷ (number of counties in which the species has been recorded in VCCC) × 100.
- Two scoring perspectives:
  - Proportion of counties where the species has ever been recorded (including extinct counties).
  - Proportion counting only counties where the species is extant (excluding extinct counties).
- Scope: scores computed for 1420 native and archaeophyte taxa across the 24 included counties.

## Data outputs and files
- axiophyte_scores.csv (60 KB): main results with per-species metrics.
  - Columns include: Species (Stace 1997), Species (Stace 2010), Axiophyte (yes/no), Counties extant, Counties extinct, Counties total, %counties extinct, Counties axiophyte, %counties axiophyte (extant only).
- Additional CSVs:
  - axiophytes_Feb_2014.csv: cleaned county axiophyte data.
  - counties_included.csv: details of counties included (Vice county, Country, Total species, Total axiophytes, %axiophyte).
  - exclusions_with_reason.csv: taxa excluded and reasons.
  - county_occurrence.csv: county-by-county occurrence statuses (extant/extinct) for each species.
  - axiophytes_as_published.csv: original published axiophyte statuses by county.

## Data lineage, limitations, and notes
- VCCC data limitations: county_occurrence uses information up to 1999; some later distribution updates are not reflected.
- Updates planned: the meta-list of axiophytes will be updated as more county-level lists become available (future work).

## References
- Hill, Mark O., Preston, C.D., Roy, D.B. 2004. PLANTATT.  
- Lockton, A. 2008. BSBI News.  
- Stace, C.A. 1997; Stace, C.A. 2010. New flora of the British Isles.  
- Stace, C.A., et al. 2003. Vice-county Census Catalogue.