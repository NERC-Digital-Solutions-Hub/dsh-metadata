# Supporting documentation for 12-Feedstuff_Stable.csv

- The document provides the data dictionary and column explanations for the 12-Feedstuff_Stable.csv dataset, focusing on stable element concentrations in feedstuffs and related metadata.

## Overview of the dataset

- Purpose: Describe sample-level and analyte-level data for stable elements measured in feedstuff samples.
- Core content: 
  - Sample identifiers and descriptors (Sample_Code, Sample_Type, Location, Sample_Description, Collection_Date, Sample_size).
  - Concentrations of multiple elements on a dry mass basis (e.g., Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) with associated metadata.
- Measurement conventions:
  - Concentrations reported as mg per kg of dry matter (mg/kg_dm).
  - Each analyte includes a corresponding uncertainty (Unc_…_mg/kg_dm) and a detection limit (Detection_Limit_…_mg/kg_dm).
  - Many fields include notes such as “Where blank, then concentration was below the detection limit.”

## Data model and key fields

- Sample-related fields:
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (foodstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analysed (e.g., tissues or components).
  - Collection_Date: Date of collection (format: dd-mm-yyyy).
  - Sample_size: Amount of sample analysed (units: g fresh matter).
- Analyte-related fields (example structure repeated for each element):
  - Element_concentration (e.g., Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm): Concentration on a dry mass basis (mg/kg_dm).
  - Unc_Element_mg/kg_dm: Combined uncertainty of the element concentration (mg/kg_dm).
  - Detection_Limit_Element_mg/kg_dm: Detection limit for the element (mg/kg_dm).
  - Notes: Indicate when a value is below the detection limit, or other caveats.
- Formatting inconsistencies are present in the notes (e.g., occasional capitalization or spacing differences in Unc_K_Mg/kg_dm, Mg/kg_dm, etc.), but the intended meaning is the concentration, uncertainty, and detection limit per element.

## Metadata and data quality

- For every analyte, the dataset provides:
  - Concentration on a dry mass basis (mg/kg_dm).
  - Combined uncertainty (Unc_…_mg/kg_dm).
  - Detection limit (Detection_Limit_…_mg/kg_dm).
  - Notes clarifying when values are below detection limits.
- Metadata organization:
  - Each column has an Explanation, Units, and Notes, enabling interpretation and data quality checks.
  - Collection_Date format and Sample_size units are defined to support consistency and comparability.

## Data collection and processing context

- Concentrations are given on a dry mass basis, improving comparability across samples with varying moisture.
- Date format is explicit (dd-mm-yyyy) to support temporal analyses.
- Sample_size is specified as grams of fresh matter, aiding interpretation of sample representativeness.

## Implications for Data Leaders (data governance and strategy)

- Data quality and standards
  - Standardize column names and units across datasets to avoid ambiguity (e.g., harmonize Unc_K_Mg/kg_dm vs Unc_K_mg/kg_dm).
  - Ensure consistent handling of “below detection limit” values across all analytes.
  - Maintain complete metadata for each variable (explanation, units, notes) to support discoverability and reuse.
- Metadata and discoverability
  - Preserve the explicit Explanation/Units/Notes structure to facilitate data discovery and reuse by policy colleagues and other stakeholders.
  - Consider creating a data dictionary governance document to enforce consistent naming and formatting.
- Data usage and user needs
  - The dataset supports assessment of element concentrations in feedstuffs and can underpin risk assessments, dietary exposure analyses, and regulatory reporting.
  - Co-ownership of data products by data users (e.g., policy colleagues) can be encouraged by maintaining clear metadata and user-friendly documentation.
- Data quality processes
  - Implement validation rules for collection dates, units, and detection-limit handling.
  - Flag and curate any inconsistent field names or units to prevent downstream misinterpretation.
- Collaboration and governance
  - Given the potential for scattered data sources, maintain a centralized, well-documented data dictionary to reduce duplication and enhance coordination across teams and partners.

## Challenges and considerations highlighted by the document

- Ensuring consistent understanding of user needs and data scope across stakeholders.
- Achieving an overview of available data given the breadth of analytes and metadata.
- Handling data gaps or limits in granularity for certain elements.
- Managing data standards, quality, and metadata clarity to prevent misinterpretation.
- Coordinating across teams to avoid duplicated effort and to foster a broader data-sharing community.

## Recommendations for action

- Align and standardize column naming, especially for uncertainty and detection-limit fields.
- Maintain and enforce a complete, structured metadata schema (Explanation, Units, Notes) for all fields.
- Implement data quality checks for date formats, units, and detection-limit treatment.
- Develop a data product that supports co-ownership with policy colleagues, including clear documentation and accessible metadata.
- Foster cross-team collaboration to advance consistency, reduce duplication, and build a stronger data community around stable element data in feedstuffs.