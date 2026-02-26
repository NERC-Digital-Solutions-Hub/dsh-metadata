# BSBI axiophyte scores - metadata, May 2016

- Objective: Create national (Great Britain) axiophyte scores by aggregating county-level axiophyte lists to indicate how strongly a species is associated with high-quality habitat. Plan to update the meta-list as more county lists become available.

- Data sources
  - County lists: 24 GB counties’ axiophyte lists downloaded Feb 2014 from the BSBI website; 3 Irish lists (Antrim, Fermanagh, Waterford) excluded.
  - Taxon matching and cleaning: Names checked against Stace 1997 (Second Edition); name changes aligned with Stace 2010; hybrids, microspecies, subspecies/varieties treated with specified rules; charophytes, neophytes, and counties’ known neophytes excluded.
  - County occurrence data: Vice-County Census Catalogue (VCCC; Stace et al., 2003) with records up to 1999; used to determine where taxa have ever been recorded and where they are extant (5) or extinct (4).
  - Taxon status: Exclusions and decisions recorded in exclusions_with_reason.csv; original published axiophyte data in axiophytes_as_published.csv.

- Data cleaning and standardisation
  - Taxa handling: Subspecies/varieties generally combined within species unless the subspecies was the only native/archaeophyte taxon; hybrids, microspecies, and known neophytes excluded; neophytes in specific counties noted as exclusions.
  - Name alignment: Cross-checked published lists with Stace references and updated where newer taxonomic names were published.
  - County alignment: Some county lists represented two vice-counties; these were treated accordingly during aggregation.

- Calculation of axiophyte scores
  - Score definition: For each species, axiophyte score = (number of counties where the species is listed as axiophyte) / (number of counties in which the species has ever been recorded, per VCCC), expressed as a percentage.
  - Extant vs total: Also computed as a proportion using only counties where the species is extant (excluding counties where extinct).
  - Example interpretations:
    - Acer campestre: recorded in 16 of 24 counties; axiophyte in 4 of those counties → 25%.
    - Adonis annua (archaeophyte): recorded in 14 counties; extant in 5 → 14% overall; 2 of 5 extant counties → 40% when excluding extinct counties.
  - Scope: Axiophyte scores calculated for 1420 native and archaeophyte taxa listed for the 24 included counties.

- Data outputs (CSV files and contents)
  - axiophyte_scores.csv: Calculated overall axiophyteness scores; fields include species (Stace 1997/2010 names), extant counties, extinct counties, total counties, and % extinct; size ~60 KB.
  - axiophytes_Feb_2014.csv: Raw county-level data for scoring; species vs. county axiophyte status; size ~91 KB.
  - counties_included.csv: Details of included counties (vice counties, country, total species richness, total axiophytes, % axiophyte); size ~1 KB.
  - exclusions_with_reason.csv: Taxa exclusions with actions and reasons; size ~19 KB.
  - county_occurrence.csv: Current status of taxa within counties (5 = extant; 4 = extinct), plus totals and comments; size ~101 KB.
  - axiophytes_as_published.csv: Original axiophyte data as published by counties; per-county published status and total counts; size ~103 KB.

- File and column descriptors
  - axiophyte_scores.csv: Columns include Species (Stace 1997), Species (Stace 2010), Axiophyte (yes/no), Counties extant, Counties extinct, Counties total, %counties extinct, Counties axiophyte, %counties axiophyte (extant only).
  - axiophytes_Feb_2014.csv: Columns include Species (Stace 1997/2010) and per-county yes/no flags for axiophyte status.
  - counties_included.csv: Columns include Vice county(s), Country, Total species, Total axiophytes, %axiophyte.
  - exclusions_with_reason.csv: Columns include Taxon, Action, Reason, If combined included within.
  - county_occurrence.csv: Columns include Species (Stace 1997/2010) and per-county status (5 extant, 4 extinct), plus Extant counties, Extinct counties, Total counties, %extinct, Comment.
  - axiophytes_as_published.csv: Columns include Species (Stace 1997/2010) and per-county original axiophyte status, plus Total.

- Notable considerations and limitations
  - Temporal scope: VCCC data up to 1999; may not reflect any changes after that date.
  - Geographic scope: GB-wide aggregation; Irish lists excluded from scoring.
  - Data quality and compatibility: Cleaning rules applied to align taxonomy across editions and account for changes; some counties represented multiple vice-counties.
  - Future updates: Meta-list to be updated as more county-level axiophyte lists become available and incorporated.

- References
  - Hill, M.O., Preston, C.D., and Roy, D.B. 2004. PLANTATT.
  - Lockton, A. 2008. BSBI News.
  - Stace, C.A. 1997; Stace, C.A. 2010; Stace, C.A., Ellis, R.G., Kent, D.H. & McCosh, D. 2003. Vice-county Census Catalogue.