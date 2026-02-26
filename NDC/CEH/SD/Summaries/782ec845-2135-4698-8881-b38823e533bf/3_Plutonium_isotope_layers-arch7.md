# Dataset column definitions for soil core sampling radiometric measurements

## Overview
- Defines the data schema for soil core samples including identifiers, sampling details, layer depth boundaries, mass per layer, and radiometric activity concentrations with uncertainties.
- Focuses on 137Cs, 90Sr, 238Pu, and 239/240Pu measured in soil dry matter.

## Key fields and data types
- Code_of_the_sample
  - Explanation: Database serial number - unique ID
  - Units: none
- Identifier_of_the_sample
  - Explanation: UIAR unique label - chemical analysis number
  - Units: none
- Dates_of_the_activity_measurements
  - Explanation: Date of measurement (long date format)
  - Units: dd-mmm-yy
- Sampling_area_m2
  - Explanation: Size of the area sampled
  - Units: square metres
- The_top_border_of_a_layer_cm
  - Explanation: Top depth border of layer (cm); description indicates 30 cm cores with layers such as 0-2, 2-4, ..., up to 25-30 cm; one site sampled to 110 cm with 10 cm slices
  - Units: cm
- The_bottom_border_of_a_layer_cm
  - Explanation: Bottom depth border of layer (cm); same layering description
  - Units: cm
- Mass_of_the_layer_kg
  - Explanation: Sample mass of each layer of 37 mm diameter core
  - Units: kilogram
- Activity_concentration_137Cs_Bqkg
  - Explanation: Activity concentration in soil dry matter for 137Cs
  - Units: bequerel (Bq) per kilogram
- Relative_uncertainty_of_specific_activity_of_137Cs_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percent
- Activity_concentration_90Sr_Bqkg
  - Explanation: Activity concentration in soil dry matter for 90Sr
  - Units: Bq/kg
- Relative_uncertainty_of_specific_activity_of_90Sr_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percent
- Activity_concentration_238Pu_Bqkg
  - Explanation: Activity concentration in soil dry matter for 238Pu
  - Units: Bq/kg
- Relative_uncertainty_of_specific_activity_of_238Pu_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percent
- Activity_concentration_239_240Pu_Bqkg
  - Explanation: Activity concentration in soil dry matter for 239/240Pu
  - Units: Bq/kg
- Relative_uncertainty_of_specific_activity_of_239_240Pu_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percent

## Data quality and structure notes
- Many fields include empty or placeholder Notes, indicating potential gaps in metadata.
- Units vary across fields (e.g., Bq/kg, kg, m2); ensure consistent unit usage across the dataset.
- Some typographical inconsistencies (e.g., “bequerel” vs. “Bq”) may require standardization.
- Depth layer definitions are described in natural language within the explanations; consider formalizing layer boundaries as explicit numeric ranges for GIS usage.

## GIS relevance and use cases
- Spatial relevance:
  - Sampling_area_m2 provides a spatial footprint that can be linked to site polygons or raster representations.
  - Layer depth borders (top and bottom of each layer) offer depth dimension data for 3D visualization or multi-layer mapping.
- Potential representations:
  - Point features per sample site with per-layer records to capture depth-resolved radiometric data.
  - 3D or multi-attribute layers showing activity concentrations by depth slices.
- Use cases:
  - Map radiometric contamination by layer across sites.
  - Visualize depth profiles of 137Cs, 90Sr, and Pu isotopes for site-specific assessments.

## Recommendations for GIS workflows
- Normalize identifiers:
  - Ensure Code_of_the_sample and Identifier_of_the_sample are consistently linked to geolocated site records.
- Structure depth data:
  - Convert The_top_border_of_a_layer_cm and The_bottom_border_of_a_layer_cm into explicit numeric depth intervals per layer (e.g., 0–2 cm, 2–4 cm, etc.) for reliable querying and visualization.
- Ensure unit consistency:
  - Standardize units across all records (e.g., Bq/kg for activity, kg for mass, m2 for area) and correct any spelling inconsistencies (e.g., “bequerel” → “Bq”).
- Handle missing metadata:
  - Populate or document Notes and missing explanations to improve data discoverability and quality assurance.
- Data integration:
  - Prepare a relational schema or a linked dataset so radiometric measurements (per isotope) can be joined to site-level attributes and spatial geometry.
- Quality checks:
  - Validate 95% confidence interval uncertainties and ensure they align with recorded activity concentrations.