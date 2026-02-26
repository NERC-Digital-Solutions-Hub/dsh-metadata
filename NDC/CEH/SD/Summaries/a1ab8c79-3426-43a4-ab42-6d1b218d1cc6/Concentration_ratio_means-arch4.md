# Sample_Code, Explanation = Unique sample identifier.

## Overview
- Defines a data schema for sample measurements, including identifiers, species, and context, plus statistical results for a wide range of analytes.
- Central metrics are mean concentration ratios and their standard deviations, with the mean type (geometric or arithmetic) indicated by Mean_Value.
- Includes taxonomic and regulatory context via RAP (ICRP Reference Animals and Plants) attribution and a description of the analyzed sample portion.

## Core fields and data structure
- Sample identification and description
  - Sample_Code: Unique sample identifier.
  - Sample_Code units/methodology: n/a.
  - Sample_Code Notes: n/a.
  - Species: Latin name of species sampled.
  - RAP: ICRP Reference Animals and Plants (RAP) attribution for the species.
  - Sample_Description: Part of the sample that was analyzed.
- measurement and statistics
  - Mean_Value: Indicates whether the reported mean is geometric or arithmetic.
  - Analyte fields (examples include I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Tl, U, etc.)
    - For each analyte, two core metrics are stored:
      - Mean concentration ratio: unitless, representing the central tendency.
      - Standard Deviation: unitless, representing dispersion.
    - Notes indicate that the mean type (geometric vs arithmetic) applies to both the mean and the associated standard deviation as identified by Mean_Value.
- metadata consistency
  - Most analyte fields are described as unitless for both mean and standard deviation.
  - Some lines show formatting irregularities (e.g., stray punctuation and field mappings like ", 1 = ., 2 = ., 3 = standard deviation as identified by Mean_Value"), which can affect automated parsing.

## Analyte fields and statistics (summary)
- A broad set of elements and isotopes are covered (e.g., I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Tl, U, etc.).
- For each analyte:
  - Mean concentration ratio: unitless.
  - Standard Deviation: unitless.
  - Both statistics may be geometric or arithmetic depending on Mean_Value.

## Metadata and provenance
- RAP linkage provides regulatory/biological context for the sampled species.
- Sample_Description offers traceability to the specific portion of the sample analyzed.
- Mean_Value governs interpretation of both the mean and its dispersion.

## Data quality and challenges (for Data Leaders)
- Potential fragmentation: fields for many analytes may be inconsistently named or partially populated.
- Parsing risk: irregular formatting in the provided schema (e.g., stray tokens and ambiguous mappings) could hinder automated ingestion or validation.
- Interpretation risk: unclear whether all analytes follow the same rule for geometric vs arithmetic means without explicit documentation of Mean_Value usage per analyte.
- Metadata gaps: explicit metadata on units for concentration (though stated as unitless here) and the exact method for calculating means/standard deviations.

## Governance implications and actions
- Data standards
  - Establish a formal data dictionary capturing: exact field names, data types, allowed values, units (clarify unitless convention), and the meaning of Mean_Value for each analyte.
  - Ensure consistent naming across all analytes and remove formatting inconsistencies.
- Data quality controls
  - Implement validation rules to ensure both mean and standard deviation exist for each analyte, and that Mean_Value is specified.
  - Validate RAP mappings and species taxonomy against authoritative references.
- Metadata and discoverability
  - Provide clear provenance: who collected data, when, and by which methodology; link to source documents or SOPs.
  - Maintain robust metadata for discoverability and reuse across networks and partners.
- Access and use
  - Document interpretation guidelines for downstream analysts (e.g., how to convert unitless concentration ratios to meaningful comparisons, when to treat means as geometric vs arithmetic).
  - Ensure data governance aligns with broader data-sharing expectations across networks of partners.
- Operational steps
  - Create a consolidated data dictionary from this schema.
  - Develop data ingestion pipelines with schema validation and anomaly reporting.
  - Establish a standard reporting template to communicate mean type and dispersion consistently for each analyte.