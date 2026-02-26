# Column heading explanations for 5_Fuel_particle_dissolution.csv

- Overview
  - This is a data dictionary describing the column headings, data types/units, and notes for the dataset on fuel particle dissolution, focusing on strontium isotopes (90Sr and 85Sr) in soil and related activity forms.
  - The dataset groups samples by identical identifiers (e.g., 1a, 1b) indicating samples from the same site.

- Key fields and their meanings
  - Code
    - Database serial number – unique ID
    - Units: not applicable
    - Notes: none
  - Identifier
    - UIAR unique label – chemical analysis number
    - Notes: samples with the same identifier (e.g., 1a, 1b) come from the same site
  - Date_of_90Sr_measurement
    - Date when 90Sr measurement was taken
    - Format: dd-mmm-yy
  - 90Sr_exchangeable_form_in_soil_%
    - Percentage of 90Sr present in exchangeable form in soil
    - Units: percentage
  - Relative_uncertainty_of_90Sr_exchangeable_form_portion_in_soil_%
    - Relative uncertainty of the 90Sr exchangeable form portion
    - Units: percentage
    - Confidence: 95% confidence interval
  - 85Sr_exchangeable_form_in_soil_%
    - Percentage of 85Sr present in exchangeable form in soil
    - Units: percentage
  - Relative_uncertainty_of_85Sr_exchangeable_form_portion_in_soil_%
    - Relative uncertainty of the 85Sr exchangeable form portion
    - Units: percentage
    - Confidence: 95% confidence interval
  - 90Sr_activity_in_the_FP-associated_form_%
    - Percentage activity of 90Sr in the fuel particle (FP)-associated form
    - Units: percentage
    - Notes: may contain negative values; these result from a small exchangeable fraction with high error. Users should assume these values are zero.
  - Relative_uncertainty_of_90Sr_activity_in_the_FP-associated_form_%
    - Relative uncertainty of the 90Sr activity in the FP-associated form
    - Units: percentage
    - Confidence: 95% confidence interval

- Units and data types
  - Most fields are either n/a or percentages
  - Date field uses a day-month-year format (dd-mmm-yy)

- Data quality considerations and caveats
  - Negative values in 90Sr activity for FP-associated form should be treated as zero by users
  - Relative uncertainties are provided with 95% confidence intervals; interpretations should account for measurement error
  - The data dictionary supports data cleaning and validation, including verifying consistent site grouping via Identifier

- Context and references
  - The dataset relates to kinetics of fuel particle weathering and mobility of 90Sr in the Chernobyl context
  - References include works by Kashparov et al. on dissolution kinetics and hot particle behavior (Health Physics, J Environ Rad, Environmental Science and Pollution Research)

- How this supports data work (Data Support archetype)
  - Facilitates understanding of what each column represents, enabling accurate data cleaning, transformation, and merging with related datasets
  - Supports creation of self-serve outputs (dashboards, pivot tables, reports) by clarifying definitions and units
  - Aids in communicating limitations and data quality, guiding stakeholders on appropriate interpretations and usage
  - Provides a foundation for quality assurance and reproducible analyses across sites and timepoints

- References
  - Kashparov, V. A., et al. (various works on kinetics of fuel particle weathering and 90Sr mobility in the Chernobyl zone)
  - Kashparov, V. A. (Hot Particles at Chernobyl; Environmental Science and Pollution Research)
  - Kashparov, V. A., et al. (Kinetics of dissolution of Chernobyl fuel particles in soil under natural conditions)