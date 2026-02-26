# Supporting documentation for Stable_concentration_means.csv

## Overview
- Provides metadata and field definitions for the Stable_concentration_means.csv dataset.
- Aims to support data discovery, validation, and analysis by explaining identifiers, sample context, statistical measures, and concentration fields.

## Key fields and structure
- Sample identifiers and context
  - Sample_Code: Unique sample identifier.
  - Species: Latin name of the sampled species.
  - RAP: ICRP Reference Animals and Plants (RAP) attribution for the sampled species.
  - Sample_Description: Part of the sample that was analyzed.
- Statistical and measurement context
  - Mean_Value: Indicates whether the reported mean is geometric or arithmetic.
  - Standard_Deviation_{element}_mg_kg: Standard deviation for the corresponding mean, expressed on a fresh weight basis.
- Units and basis
  - Most concentration fields are in mg_kg (milligrams per kilogram) on a fresh weight basis.
  - I-127_mg_kg explicitly denotes the mean concentration of I-127 in mg/kg.
- Data for each element
  - For each element (e.g., Li_mg_kg, Be_mg_kg, B_mg_kg, Na_mg_kg, Mg_mg_kg, Al_mg_kg, …, U_mg_kg, and others listed), the dataset provides:
    - {Element}_mg_kg: Mean concentration on a fresh weight basis.
    - Standard_Deviation_{Element}_mg_kg: Corresponding standard deviation.
    - Notes: Indicate that the mean may be geometric or arithmetic as identified by Mean_Value.
  - The table consolidates numerous elements (I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U) with their associated statistics.

## Elements included
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

(Note: The document contains formatting inconsistencies and some fields with incomplete or repeated text; the intended structure remains per-element mean and standard deviation on a fresh weight basis.)

## Data quality considerations
- Mean_Value determines whether the reported average is geometric or arithmetic for each element.
- Standard deviations accompany each mean to express variability.
- Several fields include notes clarifying that interpretations depend on the Mean_Value designation.
- Some field names and notes exhibit typographical irregularities, which may require careful parsing during data ingestion.

## Practical guidance for data use
- Ensure interpretation of concentration values uses the correct basis (fresh weight) and the correct mean type (geometric vs arithmetic) as indicated by Mean_Value.
- Use the per-sample context (Sample_Code, Species, RAP, Sample_Description) to join with broader metadata or local context.
- When building dashboards or reports, pair Mean_Value with Standard_Deviation_{element} to convey central tendency and variability for each species and RAP category.
- Validate data integrity across elements, watching for potential missing or inconsistent entries due to the document’s formatting irregularities.
- Engage subject-matter experts for RAP or species-specific considerations when integrating with other data sources.

## How this supports data products and analysis
- Enables self-serve exploration of concentration means and variability across multiple elements and samples.
- Facilitates merging with other sample metadata to support comparative analyses by species, RAP, or sample description.
- Supports creation of dashboards, pivot tables, and charts that display mean concentrations with associated uncertainty for stakeholders.