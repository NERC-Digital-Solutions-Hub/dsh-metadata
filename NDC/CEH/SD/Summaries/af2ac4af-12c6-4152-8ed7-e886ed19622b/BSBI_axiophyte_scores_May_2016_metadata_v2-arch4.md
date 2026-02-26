# BSBI axiophyte scores - metadata, May 2016

## Overview
- Defines axiophytes as indicators of high-quality habitats and describes how county-level axiophyte lists in Great Britain are aggregated to produce national (GB) level scores.
- The information product summarizes county lists to create a meta-list of axiophytes and will be updated as more county lists become available.

## Data sources and scope
- County-level data: axiophyte lists for 24 counties in Great Britain downloaded from the BSBI website in February 2014.
  - Irish lists (Antrim, Fermanagh, Waterford) excluded.
  - Some counties represented as two vice-counties (e.g., Cornwall).
- Taxonomic standardization:
  - Raw lists checked against Stace (1997) New Flora, with changes from Stace (2010) captured in separate columns.
  - Hybrids, microspecies, charophytes, neophytes (where native status uncertain) excluded; subspecies/varieties typically treated within species.
- Occurrence data:
  - Compared against the Vice-County Census Catalogue (VCCC, Stace et al., 2003) with cleaning rules applied.
  - VCCC data up to 1999; may not reflect the most recent distributions.
- Scope of taxa:
  - 1420 native and archaeophyte taxa listed across the included counties.

## Methodology
- Data cleaning and alignment:
  - Exclusions and inconsistencies documented (exclusions_with_reason).
  - Alignment between published axiophyte lists and county occurrence data performed.
- Score computation:
  - Axiophyte score = (number of counties where a species is listed as axiophyte) / (number of counties in which it has been recorded) × 100.
  - Two scoring perspectives:
    - Proportion of counties where it has ever been recorded as axiophyte.
    - Proportion excluding counties where the species is extinct (extant counties only).
  - Example calculations provided (e.g., Acer campestre, Adonis annua).
- Output scope:
  - Axiophyte scores calculated for 1420 taxa.
  - Results summarized in CSV: axiophyte_scores.csv (overall axiophyteness).

## Data products and CSV files
- axiophyte_scores.csv — Calculated overall 'axiophyteness' scores. Size: ~60 KB.
- axiophytes_Feb_2014.csv — Raw county-level data for scoring. Size: ~91 KB.
- counties_included.csv — Details of the counties included. Size: ~1 KB.
- exclusions_with_reason.csv — Excluded taxa and reasons. Size: ~19 KB.
- county_occurrence.csv — Taxa occurrence status by county (extant/extinct). Size: ~101 KB.
- axiophytes_as_published.csv — Original axiophyte status by county as published. Size: ~103 KB.

Additional fields in the datasets (highlights):
- Species names (Stace 1997 and 2010 standards).
- County-by-county axiophyte status (yes/no) and occurrence status (extant/extinct).
- Counts per county, total counties, and percentages of axiophyte coverage.
- Status notes and comments for data adjustments.

## Data quality, provenance, and limitations
- Taxonomic alignment relies on Stace editions; changes documented to ensure traceability.
- Exclusions applied to ensure consistency across counties (e.g., hybrids, microspecies, neophytes in certain contexts).
- VCCC data is historical (up to 1999), which may not reflect current distributions.
- The meta-list is designed to be updated as additional county lists become available.

## Usage and future updates
- Intended to provide a national-level indicator of axiophyte presence and distribution across GB.
- The meta-list will be updated in the future as more county-level axiophyte lists become available.

## References
- Hill, Mark O., Preston, Christopher D., and Roy, D. B. 2004. PLANTATT.
- Lockton, A. 2008. BSBI News.
- Stace, C.A. 1997; Stace, C.A. 2010. New Flora of the British Isles.
- Stace, C.A., Ellis, R.G., Kent, D.H. & McCosh, D. 2003. Vice-county Census Catalogue.