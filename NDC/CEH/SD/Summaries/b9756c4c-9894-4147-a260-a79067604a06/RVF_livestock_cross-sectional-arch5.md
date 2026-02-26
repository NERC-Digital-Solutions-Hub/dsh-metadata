# Experimental Design/Sampling Regime

- Purpose: Investigate effects of land use change (development of irrigation schemes in pastoral rangelands) on access to selected ecosystem services, using Rift Valley fever (RVF) as a case study. Focus on provisioning and disease regulation services; households are the primary sampling units.
- Sampling rationale: Formal power-based sample size for comparing two independent proportions (two-sided test) determined a target of 220 households per land-use type.
- Study sites: Bura and Hola irrigation schemes in Tana River County; adjacent practicing nomadic pastoralism; additional areas in Ijara and Sangailu divisions, Garissa County practicing transhumance pastoralism.
- Integration: Conducted alongside prior RVF surveys to supplement and harmonize with existing data.
- Sampling frame and approach: Compile households in target areas; clean irrigation-scheme registers to reflect movers; randomly select households and, within households, animals. Cross-sectional design with a single sampling occasion.

## Field data collection and methods

- Two-step data collection:
  - Step 1: Household-level data (identification number, geographic coordinates in decimal degrees, altitude, number of animals and species owned).
  - Step 2: Animal-level data (identify animals to sample; record characteristics such as animal ID, species, age, sex) and collect blood samples.
- Sample volumes and processing:
  - Up to 20 ml venous blood per animal from the jugular vein.
  - Whole blood collected in heparinised tubes; serum collected from clotted blood after centrifugation.
  - Samples aliquoted into 2 ml cryovials for working and long-term storage.
  - Aliquots preserved and transported on dry ice; transferred to liquid nitrogen tanks upon arrival at Nairobi laboratory.
- Linking data: Sampling forms allowed multiple entries per household; sample tubes barcoded and linked to household and animal-level data via barcodes.

## Analytical methods

- Serology: RVF virus immunoglobulin G (IgG) screened using an RVF virus inhibition ELISA suitable for humans, domestic, and wild ruminants.
- Reference: Protocol described in Paweska et al., 2005.
- Documentation: Full protocol cited and accessible via referenced publication.

## Dataset and data structure

- Data file: A single CSV named DDDAC_Kenya_livestock_rvfdata.csv.
- Variables: 18 variables with descriptions provided in Table 1.
  - Examples: hhid (household ID), animalid (animal ID), altitude (GPS altitude), goats, sheep, cattle, donkeys (animal counts by species), species, breed, sex, age, bdt (barcode for parent whole blood sample), bsr (barcode for parent serum sample), avaq (barcode for working serum aliquot), area (sampling location), pathogen (pathogen screened for), landuse (irrigated vs non-irrigated area), result (serological result).
- Data completeness: Blank cells indicate not recorded or collected; missing livestock numbers mainly due to non-disclosure by owners.

## Quality control and data governance

- Field data management: Open Data Kit (ODK) used on smartphones to collect data; supports relationship coding between datasets to minimize transcription errors.
- Data capture and workflow: Daily uploads to a central ODK Aggregate server hosted by the International Livestock Research Institute (ILRI); team included at least 2 researchers and 3 technicians; animal-level data validated in real time with interjections from team members.
- Sample handling: Preidentified tubes with barcodes; field dry ice replenished weekly; laboratory analyses performed in duplicates with re-analysis for borderline results.
- Data integrity and provenance: Clear linkage between household and animal data; samples linked through barcodes to ensure traceability; field and lab processes described to ensure reproducibility and auditability.