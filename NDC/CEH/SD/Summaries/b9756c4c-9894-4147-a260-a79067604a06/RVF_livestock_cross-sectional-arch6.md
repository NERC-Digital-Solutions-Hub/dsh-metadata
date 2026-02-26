# Experimental Design/Sampling Regime

- Purpose: Investigate the effects of land use change (development of irrigation schemes in pastoral rangelands) on access to selected ecosystem services, using Rift Valley fever (RVF) as a case study. Data collected to integrate with existing RVF surveys.

- Study design: Cross-sectional survey with formal power-based sample size determination for comparing two independent proportions; 220 households per land use type.

- Study sites:
  - Bura and Hola irrigation schemes in Tana River County, Kenya.
  - Villages surrounding these schemes that practice nomadic pastoralism.
  - Additional areas in Ijara and Sangailu divisions, Garissa County, practicing transhumance pastoralism.

- Sampling frame and method:
  - Households listed in target areas; irrigation scheme registers cleaned for in-move/out-move.
  - Random selection of households and, within households, animals.

- Fieldwork and data collection:
  - Two-step data collection:
    - Step 1: Household characteristics (household ID, geographic coordinates, altitude, number of animals and species).
    - Step 2: Animal identification, characteristics (ID, species, age, sex) and blood sampling.
  - Sampling unit: Households and individual animals; up to 20 ml venous blood per animal (jugular vein).

- Sample handling and storage:
  - Blood processed into whole blood (heparinised) and serum; serum separated after clotting and centrifugation.
  - Aliquots prepared (duplicates) and preserved in dry ice; later stored in liquid nitrogen at the lab in Nairobi.

- Laboratory analysis:
  - Serum screened for Rift Valley fever virus IgG using a virus inhibition ELISA (protocol described by Paweska et al., 2005).

- Dataset and variables:
  - File: DDDAC_Kenya_livestock_rvfdata.csv (one CSV with 18 variables).
  - Key variables and descriptions:
    - hhID: Household identification number
    - animalID: Animal identification number
    - altitude: Altitude in meters (GPS)
    - goats: Number of goats in the household
    - sheep: Number of sheep in the household
    - cattle: Number of cattle in the household
    - donkeys: Number of donkeys in the household
    - species: Species of the sampled animal
    - breed: Breed of the sampled animal (not reliable)
    - sex: Sex of the animal
    - age: Estimated age group (Adult, Weaner, Kid/Lamb/Calf)
    - bdt: Bar code for the parent whole blood sample
    - bsr: Bar code for the parent serum sample
    - avaq: Bar code for the working serum aliquot
    - area: Location of sampling
    - pathogen: Pathogen screened for (serological testing)
    - landuse: Whether the animal was in the irrigated area or not
    - result: Serological analysis result
  - Note: Blank cells indicate data not recorded or collected; missing livestock numbers often due to owner non-disclosure.

- Data quality control and management:
  - Data collected with Open Data Kit (ODK) on smartphones; linkage codes to avoid transcription errors.
  - Centralized data uploads to an ODK Aggregate server at the International Livestock Research Institute (ILRI) daily.
  - Field team: at least 2 researchers and 3 technicians; verification by team members; barcodes used to link samples to households and animals.
  - Samples: duplicate laboratory analyses; borderline results re-analyzed.
  - Sample preservation: dry ice replenished weekly in the field; samples transported to Nairobi for storage and analysis.

- Notes on data use:
  - Data are structured to enable integration with other RVF datasets and to support self-service analysis (e.g., combining household and animal-level data with serology results).
  - Some data gaps may exist due to non-disclosure or recording omissions.