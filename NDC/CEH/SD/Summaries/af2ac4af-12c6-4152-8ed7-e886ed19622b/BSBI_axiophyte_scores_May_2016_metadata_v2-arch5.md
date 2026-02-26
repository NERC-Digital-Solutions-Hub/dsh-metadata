# BSBI axiophyte scores - metadata, May 2016

## Overview
- Defines axiophytes as indicators of high-quality habitat and describes a national (Great Britain) level aggregation of county lists to assess “axiophyte-ness.”
- Purpose: produce a meta-list of axiophytes and their scorings, with plans to update as more county-level lists become available.
- Produces quantitative scores for 1420 native and archaeophyte taxa across 24 GB counties.

## Data provenance and scope
- Primary data sources: published county axiophyte lists for 24 Great Britain counties, downloaded February 2014 from the BSBI website.
- Exclusions: 3 Irish lists (Antrim, Fermanagh, Waterford) removed; some multi-county listings treated as vice-counties; hybrids, microspecies largely excluded; subspecies/varieties generally merged within species; charophytes, neophytes, and known native neophytes excluded per county.
- Taxonomic verification: names harmonized with Stace (1997) New Flora of the British Isles; name changes aligned with Stace (2010).
- Occurrence data: county occurrence derived from the Vice-County Census Catalogue (VCCC; Stace et al., 2003), with cleaning similar to axiophyte data; VCCC records up to 1999 (may not reflect latest distributions).

## Methods and data processing
- Cleaning and standardization:
  - remove inconsistent taxa; harmonize taxa names; document exclusions with reasons.
  - align native status codes and county occurrences with cleaned data.
- Scoring approach:
  - axiophyte score = number of counties where a taxon is listed as axiophyte divided by the number of counties where it has ever been recorded (per VCCC).
  - also calculate a variant using only counties where the taxon is extant (excluding extinct occurrences from the denominator).
- Output scope:
  - computed scores for 1,420 taxa across 24 counties.
  - provides both “ever recorded” and “extant only” denominators for scoring.

## Data products (CSV files)
- axiophyte_scores.csv — Calculated overall axiophyteness scores (description, counts, percentages; 60 KB).
  - Includes: species names (Stace 1997/2010), axiophyte yes/no, counties extant/extinct/total, % extant, axiophyte counts, %axiophyte (extant).
- axiophytes_Feb_2014.csv — Raw county-level axiophyte data as published (91 KB).
- counties_included.csv — Details of the 24 counties included (1 KB).
- exclusions_with_reason.csv — Taxa excluded and reasons (19 KB).
- county_occurrence.csv — Current status of taxa by county (5 extant seasons, 101 KB).
- axiophytes_as_published.csv — Original axiophyte status by county as published (103 KB).
- Additional metadata fields describe native status, per-county axiophyte flags, and counting aggregates.

## Data quality, limitations, and governance
- Temporal limitations: VCCC data only up to 1999; may not reflect recent changes or redistributions.
- Taxonomic and naming uncertainty: reliance on Stace editions with explicit reconciliation to newer names; some changes require interpretation.
- Coverage and completeness: only 24 GB counties included; Irish lists excluded; vice-county aggregations introduced for some counties.
- Data provenance and transparency: explicit documentation of cleaning steps, exclusions, and decision rules; multiple CSVs document the lineage and transformations.
- Reproducibility: clearly defined scoring formula and denominators enable replication, given access to the same source lists and VCCC data.

## Implications for data stewardship and reuse
- Enables standardized, auditable aggregation of county-level axiophyte data into a national metric.
- Supports metadata-driven governance by documenting sources, cleaning rules, and scoring methodology.
- Facilitates future updates as additional county lists become available; the meta-list is designed to be refreshed.
- Useful for researchers and land management partners evaluating habitat quality indicators across Great Britain.

## Update and maintenance notes
- The meta-list will be updated in the future when more county-level axiophyte lists are available.
- Users should reference the original Stace nomenclature and Hill et al. (2004) annotations for interpretation of native status and habitat associations.

## References
- Hill, M.O., Preston, C.D., and Roy, D.B. 2004. PLANTATT—attributes of British and Irish plants.
- Lockton, A. 2008. BSBI News, coordinator’s corner.
- Stace, C.A. 1997, 2010. New Flora of the British Isles (editions 2 and 3).
- Stace, C.A., Ellis, R.G., Kent, D.H., & McCosh, D. 2003. Vice-county Census Catalogue.