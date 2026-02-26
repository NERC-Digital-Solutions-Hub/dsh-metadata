# BSBI axiophyte scores - metadata, May 2016

- Purpose: Derive national (Great Britain) axiology scores for axiophytes by aggregating county-level lists to indicate the extent a species is used as an indicator of high-quality habitat; the meta-list will be updated as more county lists become available.
- Context: Axiophytes are species indicative of high-quality habitat; BSBI has promoted this concept at county level, and this document describes the process to produce GB-wide scores and the associated data products.

## Data sources and scope

- Primary data: Published axiophyte lists for 24 Great Britain counties downloaded from the BSBI website (Feb 2014).
- Exclusions: Irish lists (Antrim, Fermanagh, Waterford) excluded; hybrids and microspecies removed; subspecies/varieties usually merged within species; charophytes, neophytes, and native taxa known to be neophytes in a county excluded.
- County representation: Some counties represented as two vice-counties; VCCC (Vice-County Census Catalogue) used for county occurrence data.
- Taxonomic alignment: Names matched to Stace 1997 (New Flora of the British Isles); notes on changes in Stace 2010; cleaning applied to ensure consistency.
- Temporal scope: VCCC data up to 1999; recognizes potential updates since then; axiophyte status and extant/ extinct status recorded accordingly.
- Data completeness: 1420 native/archaeophyte taxa listed for the included counties; meta-data files provided to document data provenance and decisions.

## Data cleaning and taxonomic alignment

- Cleaning steps: Remove taxa unlikely to be consistently treated across counties (hybrids, microspecies); subspecies/vars merged unless the subspecies is the sole native/archaeophyte taxon.
- Taxonomic checks: Align names with Stace 1997; note name changes from Stace 2010; parallel columns document updates.
- Data provenance: Cleaned axiophyte list (axiophytes_Feb_2014.csv) and the raw published list (axiophytes_as_published.csv) preserved for traceability.
- Occurrence verification: County occurrence data (county_occurrence.csv) applied the same cleaning logic; marks extant (5) or extinct since 1970 (4); acknowledges VCCC data may be dated relative to current distributions.

## Axiophyte score calculation

- Core formula: Axiophyte score = (number of counties where a species is listed as axiophyte) / (number of counties in which the species has been recorded), expressed as a percentage.
- Extant-focused alternative: Score also calculated using only counties where the species is extant (excluding extinct counties) to yield a separate percentage.
- Example (provided): Acer campestre – axiophyte in 4 of 16 counties recorded → 25%; archaeophyte Adonis annua – recorded in 14 counties, extant in 5 → 14% overall, 40% when counting only extant counties.
- Output scope: Scores calculated for 1420 native/archaeophyte taxa across the included counties.

## Data products (CSV files) and their purposes

- axiophyte_scores.csv
  - Description: Calculated overall axiophyteness scores for each taxon.
  - Size: ~60 KB.
- axiophytes_Feb_2014.csv
  - Description: Raw county-level data for scoring (axiophyte status by county).
  - Size: ~91 KB.
- counties_included.csv
  - Description: Details of counties included (vice counties, country, total species, total axiophytes, percentage axiophyte).
  - Size: ~1 KB.
- exclusions_with_reason.csv
  - Description: Taxa excluded and the reasons for exclusion.
  - Size: ~19 KB.
- county_occurrence.csv
  - Description: Status of taxa within each county (extant or extinct) and related counts/comments.
  - Size: ~101 KB.
- axiophytes_as_published.csv
  - Description: Original axiophyte data as published by counties (per county) before cleaning.
  - Size: ~103 KB.

## Notable details and interpretation

- Taxonomic alignment and data provenance are explicitly documented to enable reproducibility and audits.
- The dataset uses a standardized GB-wide framework, enabling cross-county comparisons and temporal monitoring of axiophyte indicators.
- The underlying occurrence data (VCCC) is dated (up to 1999), which may affect current applicability; the metadata acknowledges this limitation.
- The approach supports broader environmental monitoring goals by producing harmonized, shareable indicators of habitat quality across a country.

## Update plans and future work

- The meta-list of axiophytes will be updated as more county-level lists become available, allowing refinement of national scores and broader geographic coverage over time.

## References

- Hill, Mark O., Preston, Christopher D., and Roy, D. B. 2004. PLANTATT – attributes of British and Irish plants.
- Lockton, A. 2008. Coordinator's Corner. BSBI News.
- Stace, C.A. 1997; Stace, C.A. 2010. New Flora of the British Isles.
- Stace, C.A., Ellis, R.G., Kent, D.H. & McCosh, D. 2003. Vice-county Census Catalogue of the Vascular Plants of Great Britain.