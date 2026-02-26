# Sample_Code, Explanation = Unique sample identifier.

## Overview
- Defines a comprehensive data schema for reporting analytical results from environmental/biological samples, including radionuclide and elemental concentrations.
- Aims to support monitoring, evaluation of policy, and informing future decisions by providing structured, comparable data.

## Key data fields and structure
- Sample_Code, Explanation: Unique sample identifier.
- Sample_Code, Units/methodology: n/a.
- Sample_Code, Notes: n/a.
- Species, Explanation: Latin name of the species sampled.
- Species, Units/methodology: .
- RAP, Explanation: ICRP Reference Animals and Plant (RAP) attribution for the sampled organism.
- RAP, Units/methodology: n/a.
- Sample_Description, Explanation: Part of the sample that was analyzed.
- Sample_Description, Units/methodology: n/a.
- Mean_Value, Explanation: Indicates whether the mean is geometric or arithmetic.
- Mean_Value, Units/methodology: n/a.
- Mean_Value, Notes: .
- For each element (I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cs, Tl, Pb, U, U-related placeholders):
  - Element label (e.g., I-127, Li, Be, …).
  - 1 = Mean concentration ratio.
  - 2 = unitless.
  - 3 = Geometric or arithmetic mean as identified by Mean_Value.
  - Standard_Deviation_<Element>:
    - 1 = Standard deviation.
    - 2 = unitless.
    - 3 = Geometric or arithmetic standard deviation as identified by Mean_Value.
- Special formatting notes:
  - Occasional placeholders and dots (.) indicate where data may be absent or not yet specified.
  - For some elements, rows use generic or missing identifiers (e.g., Cr, Mn, Cs, Tl, Pb, U) with the same three-part mean specification and corresponding standard deviation fields.

## Data quality, metadata and governance implications
- Emphasizes the need to specify:
  - The type of mean used (geometric vs arithmetic) via Mean_Value.
  - The corresponding standard deviation type for each element.
  - Clear unit metadata (even when labeled as unitless) to ensure interpretability.
- Highlights that some fields may be missing or require completion, underscoring the importance of thorough metadata for data provenance and verifiability.

## Relevance to monitoring frameworks
- Provides a standardized template enabling consistent collection and reporting of contaminant concentrations across samples.
- Facilitates comparability across studies and time by uniform definitions (mean type, units, and accompanying standard deviations).
- Supports data governance goals by outlining explicit data elements, provenance (Species, RAP), and analytical descriptors.

## Practical considerations for implementation (archetype perspective)
- Data completeness: fill in all element rows with appropriate Mean_Value and Standard_Deviation where applicable; address placeholders and missing metadata.
- Metadata quality: ensure robust metadata for species, RAP attribution, sampling method, and analysis techniques to overcome barriers related to data standardization and reuse.
- Data sharing and governance: align with openness and public data-sharing expectations where possible, implementing data cleaning, transformation steps, and clear reporting dashboards to communicate results clearly.
- Addressing common challenges: plan for data gaps, inter-organisational data silos, timely data access, and clear communication of complex findings through standardized reporting formats.