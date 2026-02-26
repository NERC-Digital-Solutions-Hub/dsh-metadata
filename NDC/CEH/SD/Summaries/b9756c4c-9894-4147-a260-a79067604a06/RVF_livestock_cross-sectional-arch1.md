# Experimental Design/Sampling Regime

- Context and aim: A cross-sectional study to investigate the effects of land use change (irrigation schemes) on access to selected ecosystem services, using Rift Valley fever (RVF) as a case study. Focus on provisioning and disease-regulation services; households are the primary sampling units.

- Study sites and sampling frame:
  - Locations: Bura and Hola irrigation schemes in Tana River County; villages bordering these schemes practicing nomadic pastoralism; additional areas in Ijara and Sangailu divisions, Garissa County practicing transhumance pastoralism.
  - Sample size: 220 households per land use type, determined by formal power analysis for comparing two independent proportions (two-sided test).
  - Design: Cross-sectional; integration with prior RVF surveys in Garissa County.
  - Frame construction: Household lists; irrigation scheme registers cleaned for in/out movers.

- Sampling approach:
  - Random selection of households.
  - Random selection of animals within selected households.

- Field data collection (two-step process):
  - Step 1 – Household data: household identification, GPS coordinates (decimal degrees), altitude, and the number of animals by species.
  - Step 2 – Animal data: animal identification, species, age, sex; recording of animal-level characteristics.
  - Biological sampling: up to 20 ml venous blood per animal (jugular vein). Blood divided into whole blood (heparinized) and serum (non-heparinized). Serum separated after clotting and centrifugation.

- Sample processing and storage:
  - Aliquoting: Both whole blood and serum aliquoted to 2 ml cryovials in duplicates (working and long-term storage).
  - Preservation: Samples transported in dry ice, then stored in liquid nitrogen at the biorepository in Nairobi.

- Laboratory analysis:
  - Serology: RVF virus immunoglobulin G (IgG) tested in working serum aliquots using an RVF virus inhibition ELISA (validated for humans, domestic, and wild ruminants).
  - Reference method: Paweska et al., 2005.
  - Quality checks: Analyses performed in duplicates; borderline results re-analysed.

- Dataset and data management:
  - Data file: DDDAC_Kenya_livestock_rvfdata.csv with 18 variables (Table 1 describes each variable).
  - Variables include household ID (hhid), animal ID (animalid), altitude, counts of goats/sheep/cattle/donkeys, species, breed (unreliable), sex, age, barcodes for samples (bdt, bsr, avaq), area, pathogen, land use (irrigated vs non-irrigated), and test result.
  - Data collection tool: Open Data Kit (ODK) on smartphones; barcoded tubes linked to household and animal data; daily uploads to a central ODK Aggregate server at the International Livestock Research Institute.

- Data integrity and quality control:
  - Field team: at least 2 researchers and 3 technicians; roles include real-time verification of animal-level data.
  - Barcoding and data linkage: Barcodes scanned with smartphone cameras to minimize transcription errors; dry ice replenishment weekly for sample preservation.
  - Laboratory QA: Duplicate testing; re-analysis of borderline results.
  - Data completeness: Blank cells indicate not recorded or not collected; missing counts often due to owner non-disclosure.
  - Integration: Data collected alongside and integrated with previous RVF surveys in Garissa County.

- Additional notes:
  - Breed information is not considered reliable.
  - The study acknowledges potential data gaps and ongoing data integration with existing surveys.