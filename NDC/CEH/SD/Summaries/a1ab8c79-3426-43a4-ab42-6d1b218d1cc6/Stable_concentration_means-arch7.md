# Supporting documentation for Stable_concentration_means.csv

## Overview
- Documentation describing the structure, fields, and semantics of the Stable_concentration_means.csv dataset.
- Focuses on sample metadata, taxonomic identification, reference attribution, sample description, and a comprehensive set of element concentrations expressed in mg/kg on a fresh weight basis.
- Indicates how central values are derived (Geometric or Arithmetic mean) and how variability is represented (Standard Deviation).

## Core metadata fields
- Sample_Code: Unique sample identifier.
- Species: Latin name of the sampled species.
- RAP: ICRP Reference Animals and Plants attribution for the sampled species.
- Sample_Description: Part of the sample that was analysed.
- Mean_Value: Indicates whether the reported central tendency is a Geometric mean or Arithmetic mean.
- Standard_Deviation_<element>_mg_kg: Standard deviation (fresh weight basis) for each element, aligned with the corresponding Mean_Value type.

## Concentration measurements included
- I-127_mg_kg
- Li_mg_kg
- Be_mg_kg
- B_mg_kg
- Na_mg_kg
- Mg_mg_kg
- Al_mg_kg
- P_mg_kg
- S_mg_kg
- K_mg_kg
- Ca_mg_kg
- Ti_mg_kg
- Mn_mg_kg
- Fe_mg_kg
- Co_mg_kg
- Ni_mg_kg
- Cu_mg_kg
- Zn_mg_kg
- As_mg_kg
- Se_mg_kg
- Rb_mg_kg
- Sr_mg_kg
- Mo_mg_kg
- Ag_mg_kg
- Cd_mg_kg
- Cs_mg_kg
- Ba_mg_kg
- Pb_mg_kg
- U_mg_kg
- (Each listed with corresponding Units = Milligrams per kilogram and Notes aligning with Mean_Value usage)

Note: The document presents a large, repeating set of element-specific fields with similar structure (element_mg_kg, Standard_Deviation_<element>_mg_kg), all tied to the Mean_Value interpretation.

## Units, interpretation, and notes
- Units: Milligrams per kilogram (mg/kg) on a fresh weight basis for concentration fields and standard deviations.
- Mean_Value: Specifies whether the central tendency is a Geometric mean or Arithmetic mean for the corresponding concentration value.
- Standard_Deviation_<element>_mg_kg: Describes the dispersion around the Mean_Value, corresponding to the chosen Mean_Value type (geometric or arithmetic).

## GIS and data integration considerations
- Use Sample_Code as the primary key to join with spatial data (e.g., sampling locations) or attribute data in GIS projects.
- RAP provides a crosswalk to reference animal/plant categories, useful for thematic mapping by RAP group or ecological category.
- Species and RAP enable stratification by taxa or reference groups when creating map visualizations of concentration patterns.
- Concentration fields enable choropleth or graduated-symbol maps to depict mean concentrations and potentially separate visualizations for different elements.
- Ensure consistent unit application (fresh weight mg/kg) when merging with other datasets or performing spatial analyses.

## Data quality, caveats, and preparation
- The documentation contains extensive field definitions but exhibits formatting inconsistencies and garbled lines in places, which may affect parsing or automated ingestion.
- Several fields are repeated or partially truncated (e.g., some lines show incomplete metadata for elements or standardized naming).
- Before GIS use, verify:
  - Consistency of field names and alignment with actual CSV headers.
  - Completeness of Mean_Value and corresponding Standard_Deviation fields for each element.
  - Uniform application of mg/kg on a fresh weight basis across all records.
  - Accurate linkage between Sample_Code, Species, RAP, and Sample_Description for proper contextual mapping.
- Consider data cleaning to consolidate field names (e.g., standardizing to <Element>_mg_kg and Standard_Deviation_<Element>_mg_kg) and to remove garbled entries.

## Practical guidance for map-based products
- Map design ideas:
  - Show mean concentrations by sample or RAP category using choropleth or proportional symbol maps.
  - Create per-element or composite hazard/trace-element layers by aggregating relevant mean values.
  - Include uncertainty visuals using standard deviation fields alongside mean values.
- Workflow steps:
  - Join Stable_concentration_means.csv to spatial features via Sample_Code.
  - Validate data: check for missing values and field name consistency.
  - Choose appropriate elements based on policy or project needs; render visuals with clear legends indicating mean values and units.
  - Use RAP and Species attributes to enable audience-specific views (e.g., policy colleagues vs. public).

## Endnotes
- The document serves as a comprehensive attribute dictionary for a multi-element concentration dataset, with emphasis on how means and variability are expressed and how samples are taxonomically and reference-attribution tagged for GIS-enabled interpretation.