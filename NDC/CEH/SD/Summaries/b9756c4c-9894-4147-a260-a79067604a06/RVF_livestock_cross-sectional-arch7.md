# Experimental Design/Sampling Regime

- Purpose and scope
  - Investigates effects of land use change (development of irrigation schemes) on access to ecosystem services.
  - Case study disease: Rift Valley fever (RVF).
  - Sampling units: households; cross-sectional design with a two-sided power-based sample size for comparing two independent proportions.
  - Target sample: 220 households per land-use type.

- Study sites and context
  - Bura and Hola irrigation schemes in Tana River County and surrounding villages practicing nomadic pastoralism.
  - Additional areas in Ijara and Sangailu divisions, Garissa County practicing transhumance pastoralism.
  - Aimed to supplement and integrate with existing RVF surveys in Garissa County.

- Sampling frame and recruitment
  - Households listed in target areas; irrigation scheme registers cleaned to reflect moves.
  - Subjects identified by random selection of households and animals within households.
  - Sampling conducted once (cross-sectional).

- Field data collection (two-step process)
  - Step 1: Household-level data
    - Household identification number (hhid), geographic coordinates (decimal degrees), altitude, number of animals and species owned.
  - Step 2: Animal-level sampling
    - Animal identification number (animalid), species, age, sex.
    - Blood sampling: up to 20 ml venous blood from jugular vein.
    - Sample processing: whole blood (heparinised) and serum (non-heparinised) aliquoted into 2 ml tubes; serum extracted after clot and centrifugation.
    - Sample handling: preserved and transported on dry ice; stored in liquid nitrogen at the biorepository in Nairobi.

- Laboratory analysis
  - Serum screened for RVF immunoglobulin G (IgG) using an inhibition ELISA validated for humans, domestic, and wild ruminants.
  - Protocol referenced to Paweska et al., 2005; analyses performed in duplicates.

- Data and dataset
  - Main dataset: DDDAC_Kenya_livestock_rvfdata.csv with 18 variables.
  - Key variables include: hhid, animalid, altitude, goats, sheep, cattle, donkeys, species, breed, sex, age, bdt (parent blood bar code), bsr (parent serum bar code), avaq (working serum aliquot bar code), area (sampling location), pathogen (RVF), landuse (irrigated vs non-irrigated), result (serological outcome).
  - Some blanks indicate unrecorded or uncollected data; missing livestock numbers often due to non-disclosure.

- Data management and quality control
  - Field data collected with Open Data Kit (ODK) on smartphones; linked data via codes to minimize transcription errors.
  - Central data upload to ILRI ODK Aggregate server daily.
  - Field team: at least 2 researchers and 3 technicians; one researcher records animal-level characteristics while others verify and correct.
  - Barcodes used to link samples to households and animals; dry ice replenished weekly.
  - Lab analyses performed in duplicates; borderline results re-analysed.

- Geographic and GIS-relevant aspects
  - Georeferenced household coordinates and altitude enable spatial analyses of RVF exposure relative to irrigation schemes and pastoral practices.
  - Area variable and land-use classification (irrigated vs non-irrigated) support map-based comparisons of seroprevalence across landscapes.
  - Data structure designed for integration with other spatial datasets (e.g., existing RVF surveys, land-use maps).

- Considerations for GIS-based use
  - Enables mapping of serological results at household/animal levels.
  - Facilitates analysis of associations between RVF exposure and spatial factors like proximity to irrigation schemes, elevation, and land-use type.

- Limitations and notes
  - Cross-sectional design limits causal inferences.
  - Missing data due to non-disclosure or non-recording.
  - Geographic and sampling scope limited to specified counties and zones; integration with broader datasets recommended for comprehensive spatial analyses.