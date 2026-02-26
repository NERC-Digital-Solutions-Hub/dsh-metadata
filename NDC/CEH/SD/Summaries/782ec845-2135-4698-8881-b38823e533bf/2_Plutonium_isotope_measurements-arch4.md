# Column heading explanations for 2_Plutonium_isotope_measurements.csv

- Purpose and scope
  - Defines column headings for a Plutonium isotope measurements CSV, including IDs, dates, measurement values, uncertainties, and metadata.
  - Provides explicit explanations, units, and notes for each column to support data understanding, reuse, and provenance.

- Data elements and definitions
  - Code
    - Explanation: Database serial number - unique ID
    - Units: n/a
    - Notes: .
  - Identifier
    - Explanation: UIAR unique label - chemical analysis number
    - Units: n/a
    - Notes: .
  - Date_of_Pu_measurement
    - Explanation: Date of measurement (long date format)
    - Units: dd-mm-yy
    - Notes: .
  - Terrestrial_density_of_soil_contamination_with_238Pu_kBq_m-2
    - Explanation: 238Pu contamination in soil expressed on an aerial basis
    - Units: kiloBecquerels per square meter (kBq/m^2)
    - Notes: Sample handling and radiochemical method details provided (see below)
  - Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2
    - Explanation: 239,240Pu contamination in soil expressed on an aerial basis
    - Units: kBq/m^2
    - Notes: Same sample handling and radiochemical method details as for 238Pu
  - Relative_uncertainty_238Pu_%
    - Explanation: Relative uncertainty of determination (95% CI)
    - Units: percentage
    - Notes: .
  - Relative_uncertainty_239_240Pu_%
    - Explanation: Relative uncertainty of determination (95% CI)
    - Units: percentage
    - Notes: .

- Measurement methodology and data notes
  - Notes for contamination measurements (238Pu and 239,240Pu) indicate:
    - Use of homogenized 100 cm^3 samples
    - Heating at 450 °C overnight
    - Digestion by boiling in 6M HNO3 for 4 hours
    - Plutonium radiochemical extraction by a standard method (Pavlotskaya, 1997)
    - Activity measurements with a Soloist alpha-spectrometer and Soloist-U0300 detector (EG&G ORTEC, USA)
  - These notes provide the basis for data integrity, comparability, and potential reproducibility concerns.

- Data provenance and references
  - References cited to support methods and interpretation:
    - Kashparov et al., The Science of The Total Environment, 2003 (territory contamination from Chernobyl fallout)
    - Pavlotskaya, Journal of Analytical Chemistry, 1997 (radiochemical analysis principles for environmental radionuclides)
  - Inclusion of method references aids in data lineage, auditability, and validation of measurement practices.

- Data quality and governance considerations for Data Leaders
  - Clear metadata for identifiers, date formats, and units enhances discoverability and interoperability.
  Implications:
    - Ensure consistent naming conventions and unit definitions across datasets.
    - Maintain documentation of laboratory methods and reference materials to support data quality assessments.
    - Capture uncertainty estimates (95% CI) alongside measurements to enable rigorous analysis and proper propagation of error.
  - Notes emphasize limited sample description and explicit procedural steps, highlighting the need for:
    - Versioned metadata to track methodological changes
    - Data quality controls and potential meta-annotations describing any deviations

- Practical implications for data strategy
  - This dataset demonstrates the importance of:
    - Thorough column-level explanations (data dictionary) to support reuse by different teams
    - Linking data with methodological notes and literature references to strengthen provenance
    - Recording both measured values (contaminant levels) and associated uncertainties for informed decision-making
  - To improve data assets, Data Leaders should ensure:
    - Standardized, machine-readable metadata across datasets
    - Accessibility of measurement protocols and references within data catalogs
    - mechanisms to update and verify metadata as methods evolve

- Summary of end-to-end content
  - The document provides a comprehensive data dictionary for a plutonium isotope measurement CSV, detailing field definitions, units, and method notes, along with references to foundational literature to support data quality, provenance, and usability for data-driven governance and analysis.