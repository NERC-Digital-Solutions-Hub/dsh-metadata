# Procedure for enumeration, isolation, preservation and identification of E. coli isolates NERC project NE/N019555/1

## Overview
- Describes enumeration, isolation, preservation and confirmation of E. coli isolates resistant to third generation cephalosporins or carbapenems from fecal, soil, solid waste, water, and wastewater samples.
- Supports downstream genetic analysis by preserving isolates and providing standardized data on sample provenance and results.

## Data Generated and Key Data Objects
- Sample-level data:
  - Sample ID, sample type (fecal, soil, poultry waste, tap/tubewell water, wastewater), collection method
  - Volume/weight used for processing, dilution factors, and plating details
- Plate- and colony-level data:
  - Plate type (CHROMagar ESBL, CHROMagar KPC, TBX, MacConkey with antibiotics)
  - Antibiotics used (cefotaxime, meropenem) and concentrations
  - Colony counts and morphology (typical E. coli colonies: dark pink/reddish on ESBL and KPC plates)
  - Isolates selected for subculture (min. 3 colonies from ESBL, min. 3 from KPC)
  - Stock preservation identifiers (TSB with 30% glycerol, stored at -80°C)
  - Culture sweeps and corresponding glycerol stocks
- Confirmation and identification data:
  - API 20E confirmation results for one E. coli isolate per sample (and a second isolate if initial test is negative)
  - Oxidase test results and other API-20E reaction data
  - API-20E interpretation and identification status (via APIweb) with any follow-up tests if unidentifiable
- Data quality and provenance:
  - Date/time of processing, operator IDs, plate/lab identifiers, and storage conditions
  - Documentation of media preparation steps and supplement handling (including batch/lot where applicable)

## Data Collection Workflow and Provenance
- Sample processing:
  - For various sample types, create 1× PBS and perform serial dilutions; inoculate onto CHROMagar ESBL, CHROMagar KPC, and TBX plates
  - Incubate at 37°C for 18–24 h; identify presumptive E. coli by colony color
- Isolation and preservation:
  - Subculture at least 3 colonies from ESBL and 3 from KPC onto MacConkey with corresponding antibiotics
  - Create culture sweeps, suspend in TSB with 30% glycerol, and store at -80°C
- Water and waste handling:
  - Filter water samples and inoculate onto mTEC agar with antibiotics; perform starter incubations (2 h at 37°C, then 18 h at 44°C)
  - Count colonies; select isolates and preserve as above
  - For wastewater, apply dilutions and similar filtration/incubation steps; preserve selected isolates
- Confirmation and identification:
  - Perform API 20E on one isolate per sample; if necessary, test a second isolate
  - Oxidase test and API strip inoculation per kit instructions; incubate 36 ± 2°C for 18–24 h
  - Interpret results using Reading Table and APIweb; perform additional tests if unidentifiable
- Documentation and traceability:
  - Record all results, plate IDs, sample IDs, and isolate IDs; maintain chain of custody and storage records

## Metadata, Standards and Documentation
- Media preparation and antibiotic concentrations are standardized (CHROMagar ESBL/KPC supplements, MacConkey with cefotaxime/meropenem; TBX)
- Clear labeling requirements: agar type, date, sample ID; plate/dish labeling for traceability
- API 20E workflow documented (oxidase step, incubation, reading, and interpretation rules)
- Supplement handling notes emphasize same-day use and non-reuse to ensure data integrity

## Data Storage, Preservation and Access
- Biological preservation:
  - Culture sweeps stored in TSB with 30% glycerol at -80°C
- Physical storage:
  - TBX plates stored 4°C for up to 4 weeks; ESBL plates up to 4 weeks (refrigerated and light-protected)
  - CHROMagar KPC plates stored up to 2 months under refrigeration (2–8°C) in the dark
- Data localization and accessibility:
  - Results and metadata should be linked to unique sample IDs, plate IDs, and isolate IDs for discoverability and reuse

## Quality Assurance, Validation and Uncertainty
- Confirmation pathway:
  - API 20E used to confirm E. coli identity; if initial API result is inconclusive, a second isolate is tested
- Reproducibility checks:
  - If fewer than 3 positive API tests, incubation extended by ~24 hours before re-reading
- Documentation and references:
  - API 20E interpretation guided by Reading Table and APIweb; cross-referenced with Chromogenic media manuals

## Governance, Compliance and Documentation
- Procedures are aligned with established manuals (CHROMagar ESBL/KPC, API 20E)
- Ensures traceability from sample collection to isolate preservation and identification
- Data should be organized to enable discovery, reuse, and potential sharing, with clear metadata, stable storage, and ongoing documentation

## References
- CHROMagar ESBL and CHROMagar KPC media manuals
- API 20E identification kit manual
- APIweb online identification resource