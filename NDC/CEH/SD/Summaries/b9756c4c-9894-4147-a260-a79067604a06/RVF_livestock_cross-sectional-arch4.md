# Experimental Design/Sampling Regime

- Context and aim
  - Part of a study on land use change (irrigation development in pastoral rangelands) and access to ecosystem services, using Rift Valley fever (RVF) as a case study.
  - Cross-sectional survey intended to integrate new irrigated-area data with pre-existing RVF survey data in Garissa County, Kenya.

- Sampling design
  - Primary sampling units: households.
  - Sample size: 220 households per land use type, determined by formal power calculations for comparing two independent proportions (two-sided test).
  - Sites: Bura and Hola irrigation schemes (Tana River County) and nearby pastoral villages; additional areas in Ijara and Sangailu divisions (Garissa County) practicing transhumance.
  - Frame and selection: households listed in target areas; irrigation scheme registers cleaned for in/out movement; random selection of households and, within households, animals.
  - Design: cross-sectional, single survey.

- Field data collection (two-step process)
  - Step 1: household-level data
    - Variables collected: household identification, geographic coordinates (decimal degrees), altitude, and number of animals by species.
  - Step 2: animal-level data
    - For selected animals: animal identification, species, age, sex.
    - Biological sampling: up to 20 ml venous blood per animal (jugular vein).
    - Sample processing: whole blood in heparinised tubes; serum in non-heparinised tubes after clotting; serum aliquoted and stored as working and long-term duplicates.

- Sample storage and transport
  - Serum and blood aliquots preserved in 2 ml cryo tubes; samples shipped on dry ice and transferred to liquid nitrogen tanks at the Nairobi biorepository.

- Analytical methods
  - Serology: RVF IgG antibodies screened using an RVF virus inhibition ELISA (protocol described in Paweska et al., 2005).

- Dataset and metadata
  - Data file: a single CSV named DDDAC_Kenya_livestock_rvfdata.csv.
  - Variables: 18 fields including household ID (hhid), animal ID (animalid), altitude (GPS), counts of goats/sheep/cattle/donkeys, species, breed (not reliable), sex, age, barcodes for samples (bdt, bsr, avaq), area (sampling location), pathogen tested, land use (irrigated vs. non-irrigated), and serological result.
  - Table 1 (dataset descriptor) provides detailed variable descriptions; notes that some fields may be blank due to non-recording or non-disclosure (e.g., livestock numbers).

- Quality control and data management
  - Field data capture: Open Data Kit (ODK) on smartphones to reduce transcription errors; daily uploads to a central ODK Aggregate server at the International Livestock Research Institute (ILRI).
  - Data linkage: barcodes used to link household, animal, and sample data; sampling tubes pre-labeled with barcodes; sample-to-field data connections established via barcode scanning.
  - Team structure and procedures: at least 2 researchers and 3 technicians; dedicated roles for recording animal-level data and verifying entries; dry ice replenished weekly.
  - Laboratory QA/QC: analyses performed in duplicates; borderline results re-run.

- Data provenance and governance
  - Links between field data, serology results, and laboratory processing are maintained through household and animal identifiers and barcodes.
  - Centralized storage and governance through ILRI facilities; the dataset is designed for integration with existing RVF survey data in the region.