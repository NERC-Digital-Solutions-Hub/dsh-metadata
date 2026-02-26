# Code_of_the_sample, Explanation = Database serial number - unique ID.

## Overview
- Dataset describes sampling metadata and radionuclide activity concentrations in soil cores, including per-layer measurements and associated uncertainties.
- Focuses on data governance-ready elements: identifiers, date of measurement, sampling area, layer geometry, sample mass, and activity concentrations for multiple radionuclides.

## Key data elements
- Identifiers
  - Code_of_the_sample: database serial number – unique ID
  - Identifier_of_the_sample: UIAR unique label – chemical analysis number
- Measurements and timing
  - Dates_of_the_activity_measurements: date of measurement (long date format; intended as dd-mmm-yy)
- Sampling context
  - Sampling_area_m2: size of the area sampled (square metres)
  - The_top_border_of_a_layer_cm and The_bottom_border_of_a_layer_cm: layer boundaries (cm) with example ranges and slicing details (e.g., 0-2, 2-4, …, 25-30 cm; one site to 110 cm)
  - Mass_of_the_layer_kg: sample mass per layer (kilogram) for a 37 mm diameter core
- Measurements by radionuclide (per kg dry soil)
  - Activity_concentration_137Cs_Bqkg: 137Cs activity (Bq/kg)
  - Relative_uncertainty_of_specific_activity_of_137Cs_%: 95% confidence interval uncertainty (percent)
  - Activity_concentration_90Sr_Bqkg: 90Sr activity (Bq/kg)
  - Relative_uncertainty_of_specific_activity_of_90Sr_%: 95% confidence interval uncertainty (percent)
  - Activity_concentration_238Pu_Bqkg: 238Pu activity (Bq/kg)
  - Relative_uncertainty_of_specific_activity_of_238Pu_%: 95% confidence interval uncertainty (percent)
  - Activity_concentration_239_240Pu_Bqkg: combined 239/240Pu activity (Bq/kg)
  - Relative_uncertainty_of_specific_activity_of_239_240Pu_%: 95% confidence interval uncertainty (percent)
- Explanations, units, and notes
  - Each field includes a short Explanation and Units; Notes often provide methodological context (e.g., core diameter, slicing scheme)

## Metadata quality and consistency considerations
- Observed inconsistencies
  - Some units fields are blank (e.g., Code_of_the_sample units); minor typographical issues (e.g., “bequerel” instead of “becquerel”)
  - Field names include spaces/formatting variants and multi-line notes, which may affect interoperability
- Opportunities for standardization
  - Normalize units across radionuclide measurements (ensure consistent Bq/kg)
  - Correct typos and harmonize field naming for machine readability
  - Consolidate date formats to a single standard (dd-mmm-yy) and provide clear provenance

## Data governance implications
- Data provenance and lineage
  - Clear identifiers and measurement dates support traceability to original data creators and laboratories
  - Notes describe sampling scheme (30 cm cores, layering into depth intervals, 37 mm cores), aiding reproducibility
- Data quality and stewardship actions
  - Validate and harmonize units, correct typos, and ensure consistent naming
  - Implement data quality checks for layer boundaries, core dimensions, and mass consistency
  - Capture and store formal metadata: measurement methods, calibration details, laboratory (origin), and data processing steps
- Accessibility and sharing
  - Dataset is structured for cataloging and portal upload; ensure versioning and documentation accompany the dataset
  - Document any sharing restrictions or embargoes and clarify data availability limits

## Practical actions for Data Stewards
- Standardize and enforce metadata schema: consistent field names, units, and date formats
- Address data quality issues:
  - Fill or flag missing units
  - Correct typographical errors (e.g., “bequerel”)
  - Verify layer border definitions and slicing scheme align with the stated core geometry
- Enhance documentation
  - Add a data collection methods section detailing core diameter, depth intervals, sampling locations, and lab analysis methods
  - Record data lineage, calibration and QA procedures, and any transformations performed
- Catalog and publish
  - Upload to appropriate data portals and data catalogs with a complete metadata record
  - Implement version control and provide downstream users with guidance on interpretation of per-layer radionuclide concentrations and uncertainties
- Plan for updates and data availability
  - Establish processes to obtain updated measurements or corrections from data creators; note any embargoes or access constraints

## Context and utility
- Enables assessment of radionuclide distribution with depth in soil layers, supporting environmental monitoring, radiological risk assessment, and historical contamination studies.