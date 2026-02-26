# BSBI axiophyte scores - metadata, May 2016

## Purpose and scope
- Defines axiophytes as indicators of high-quality habitat and describes how county-level axiophyte lists in Great Britain are synthesized into national (Great Britain) level axiophyte-ness scores.
- Aims to produce a meta-list of axiophytes and to update the national scores as more county-level data become available.

## Data sources and data cleaning
- County lists: 24 British counties’ axiophyte lists downloaded from the BSBI website in February 2014 (excludes 3 Irish lists).
- Taxon reconciliation: names aligned with Stace (1997) and updated to Stace (2010); changes are captured in accompanying columns.
- Exclusions: taxa excluded due to inconsistency across counties (hybrids, microspecies), subspecies/varieties generally treated within species, and natives known to be neophytes; charophytes and neophytes excluded where appropriate.
- Cross-check with occurrence data: axiophyte lists compared to county occurrence data from the Vice-County Census Catalogue (VCCC; Stace et al., 2003), noting extant (5) vs extinct (4) statuses; VCCC data up to 1999 and may not reflect latest distributions.

## Method: calculating axiophyte scores
- For each species, score = number of counties where the species is listed as axiophyte divided by the number of counties in which the species has been recorded (per VCCC).
- Two scoring variants:
  - Proportion of counties where the species is axiophyte out of all counties where it has ever been recorded.
  - Proportion excluding counties where the species is extinct (i.e., axiophyte in extant counties only).
- Example calculations:
  - Acer campestre: recorded in 16 of 24 counties; axiophyte in 4 of them → 25%.
  - Adonis annua (archaeophyte): recorded in 14 counties; extant in 5; axiophyte in 2 → 14% (2/14) overall, 40% (2/5) when excluding extinct counties.
- Final output covers 1420 native and archaeophyte taxa identified across the included counties.

## Datasets and CSV files (List and purpose)
- axiophyte_scores.csv: Calculated overall axiophyteness scores (Description: Species’ axiophyte status across counties; Size: 60 kb).
- axiophytes_Feb_2014.csv: Cleaned county-level axiophyte data (Description: Native status and county occurrences; Size: 91 kb).
- counties_included.csv: Details of included counties (Description: county information and summary metrics; Size: 1 kb).
- exclusions_with_reason.csv: Excluded taxa and reasons for exclusion (Description: Reasons for inclusion/exclusion decisions; Size: 19 kb).
- county_occurrence.csv: County-level occurrence data for species (Description: Extant vs extinct statuses; Size: 101 kb).
- axiophytes_as_published.csv: Original axiophyte data as published by counties (Description: County-level axiophyte status; Size: 103 kb).
- Species name columns and various metadata are aligned with Stace 1997 and 2010 editions where applicable; the files include detailed per-county columns (e.g., Anglesey, Banff, Berkshire, etc.) and summary columns (e.g., Counties axiophyte, Comment).

## Data governance and metadata considerations
- Name standardization across Stace editions to ensure consistent matching.
- Documentation of exclusions and the rationale to support reproducibility.
- Clear definitions of county extant vs extinct statuses and explicit references to data sources (VCCC, Stace).
- Data sharing and transparency emphasized through public availability of processed and raw-derived datasets, with explicit metadata in each CSV.

## Limitations and caveats
- VCCC data only up to 1999; may not reflect recent changes in county distributions.
- Some counties’ data may be outdated or incomplete; extrapolations are based on available records.
- Exclusion of hybrids, microspecies, and certain natives may affect comprehensive axiophyte coverage.
- The accuracy of axiophyte status depends on the consistency of original county lists and taxonomic updates.

## References
- Hill, Mark O., Christopher David Preston, and D. B. Roy. 2004. PLANTATT-attributes of British and Irish plants: status, size, life history, geography and habitats.
- Lockton, A. 2008. Coordinator's Corner. BSBI News, 107, pp. 73-74.
- Stace, C.A. 1997. New flora of the British Isles. Second edition.
- Stace, C.A. 2010. New flora of the British Isles. Third edition.
- Stace, C.A., Ellis, R.G., Kent, D.H. & McCosh, D. 2003. Vice-county Census Catalogue of the Vascular Plants of Great Britain, the Isle of Man and the Channel Islands. BSBI.