# Experimental Design/Sampling Regime

- Objective and context
  - Investigates the effects of land use change (development of irrigation schemes in pastoral rangelands) on access to selected ecosystem services, using Rift Valley fever (RVF) as a case study disease.
  - Aimed to integrate newly collected data with existing RVF surveys conducted in Garissa County.

- Study area and sampling units
  - Locations: Bura and Hola irrigation schemes in Tana River County; villages surrounding these schemes with nomadic pastoralism; additional areas in Ijara and Sangailu divisions, Garissa County with transhumance pastoralism.
  - Sampling units: households as the primary units; animals within households.

- Sampling design and sample size
  - Sample size determined by formal power analysis for comparing two independent proportions (two-sided test).
  - Required sample: 220 households per land use type.
  - Design: cross-sectional survey conducted at a single point in time.

- Sampling frame and recruitment
  - Frame created by listing all households in target areas; irrigation scheme registers cleaned to reflect in/out movements.
  - Subjects identified by randomly selecting households and then randomly selecting animals within those households.
  
- Field data collection (two-step process)
  - Step 1: Household-level data
    - Variables collected: household identification number, geographic coordinates (decimal degrees), altitude, number of animals and species owned.
  - Step 2: Animal-level data and biospecimens
    - Variables collected: animal identification number, species, age, sex.
    - Blood sampling: up to 20 ml per animal from the jugular vein; whole blood and serum aliquots prepared (2 ml per aliquot) for storage.

- Sample handling and storage
  - Serum and whole blood aliquots preserved and transported on dry ice; later transferred to liquid nitrogen in the Nairobi lab biorepository.

- Analytical methods
  - Serology: RVF virus immunoglobulin G (IgG) screening using a virus inhibition ELISA validated for humans, domestic and wild ruminants.
  - Protocol reference: Paweska et al., 2005 (linked in the document).

- Dataset and variables
  - Single dataset: DDDAC_Kenya_livestock_rvfdata.csv.
  - Contains 18 variables; key ones include:
    - hhID (household ID), animalID (animal ID)
    - altitude (GPS-based altitude), goats, sheep, cattle, donkeys (livestock counts)
    - species, breed (not reliable), sex, age
    - bdt (barcode for parent whole blood sample), bsr (barcode for parent serum sample), avaq (barcode for working serum aliquot)
    - area (sampling location), pathogen (pathogen screened for), landuse (irrigated vs non-irrigated), result (serology result)
  - Blank cells indicate data not recorded or collected; missing livestock numbers often due to owner non-disclosure.
  
- Quality control and data management
  - Field data collection with Open Data Kit (ODK) on smartphones; data linked via codes to minimize transcription errors.
  - Central data repository: daily uploads to an ODK aggregate server at the International Livestock Research Institute (ILRI).
  - Team composition: at least 2 researchers and 3 technicians; one researcher validates animal-level observations in real time.
  - Sampling tubes barcoded; sample–data linkage achieved via barcode scanning with smartphone cameras.
  - In-field preservation: dry ice replenished weekly; laboratory analyses performed in duplicates; borderline results re-tested.

- Data governance and reproducibility notes
  - The design emphasizes end-to-end data handling: field collection, unique household/animal identifiers, barcoded samples, centralized storage, and duplicate lab analyses to ensure data quality and traceability.
  - Data were integrated with existing RVF survey data to enhance comparability and breadth of analysis.

- Limitations and challenges
  - Missing or undisclosed data (e.g., livestock numbers) and reliance on owner reporting.
  - Breed information deemed unreliable for analysis.