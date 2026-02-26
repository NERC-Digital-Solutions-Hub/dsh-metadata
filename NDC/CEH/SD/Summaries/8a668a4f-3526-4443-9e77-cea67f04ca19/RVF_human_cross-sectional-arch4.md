# Rift Valley fever virus seroprevalence data from people involved in a cross-sectional survey in Tana River and Garissa counties, Kenya (December 2013 - February 2014)

## Overview
- Study investigates effects of land use change (irrigation schemes in pastoral rangelands) on access to ecosystem services, using Rift Valley fever (RVF) as a case study.
- Households are the primary sampling units; cross-sectional design profiling RVF risk across targeted sites.

## Study design and sampling regime
- Sample size: 220 households per land use type, determined by formal power calculation for comparing two independent proportions.
- Sites: Bura and Hola irrigation schemes (Tana River County) with adjacent irrigation/practice areas; Ijara and Sangailu divisions (Garissa County) with transhumance pastoralism.
- Sampling frame: Household lists from irrigation scheme registers (cleaned for duplicates/updates).
- Sampling: Random selection of households and subjects within households; cross-sectional once.
- Participants: Subjects aged 5 years and older.
- Sampling focus areas: irrigated (agricultural) and pastoral/rangeland contexts, with some riverine representation.

## Fieldwork, ethics, and data collection
- Ethics: Approved by AMREF Ethics and Scientific Review Committee; community, household, and subject-level consent obtained.
- Community engagement: Multiple meetings to review objectives and work plans.
- Data collection: Electronic forms using Open Data Kit (ODK) on smartphones; geographic coordinates captured (with ethical withholding of exact coordinates).
- Personnel: Survey team included a clinician and two medical technicians; field coordination with Ministry of Health.
- Sample collection: Blood drawn via venipuncture; sample volumes adjusted by age; serum and whole blood samples prepared and stored in duplicates.

## Laboratory analysis and data management
- Serology: Serum tested for Rift Valley fever virus IgG using a virus inhibition ELISA; protocol described in Paweska et al., 2005.
- Sample handling: Central biorepository; aliquots stored in 2 ml cryo tubes; transport with dry ice and later liquid nitrogen; duplicate testing of samples; borderline results reanalyzed.
- Data capture: Field data linked to samples via barcodes; samples and data synchronized to central ODK Aggregate server at ILRI.

## Dataset details
- File: DDDAC_Kenya_human RVF seroprevalence.csv
- Structure: 23 variables; comprehensive metadata described in Table 1.
- Variable themes:
  - Temporal and sampling identifiers: date, sampling date, sampleid, aliquotid.
  - Geographic and administrative: county, district, division, location, sublocation, villagename; altitude (GPS-derived).
  - Household and individuals: hhid, relationshiphh, hhgender, hhoccup, hhage; nmales, nfemales; gender, age; occupation.
  - Sampling site and results: area (irrigation/pastoral/riverine), result (positive/negative).
  - Livestock context: livestk_home.
- Data completeness: Blank cells indicate non-recorded or undisclosed data.

## Quality control and governance
- Data capture controls: ODK-enabled forms with relationships between datasets to minimize transcription errors.
- Data management: Daily uploads to ILRI repository; barcode-based linking of samples to household and individual data.
- Sample handling: Pre-identified tubes; barcodes read with smartphone cameras; Dry Ice replenished weekly; laboratory duplicates and reanalysis of borderline results to ensure reliability.