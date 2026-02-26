# Supporting documentation for Biota_CR.csv

- Purpose and scope
  - Defines CR (concentration ratio) as CR = biota stable element concentration / soil stable element concentration.
  - Supports environmental health monitoring by enabling assessment of transfer of elements from soil to biota and informing future decisions.
  - Provides metadata and guidance to ensure data quality, openness, and traceability.

- Dataset structure and key fields
  - Sample identity and context
    - Sample_Code: Unique sample identifier.
    - RAP: Sample type based on ICRP Reference Animals and Plants (RAPs).
    - Sample_Description: Additional description of the sample.
    - Collection_Date: Date of soil sample collection (format: dd month yyyy).
    - Soil_used_for_CR_Calculations: Identifies the soil sample(s) used to estimate the CR for the given Sample_Code.
  - Data content and coverage
    - CR fields: For each element (I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U), a concentration ratio value (unitless) is recorded. For animals, this is the whole-organism CR and is on a fresh mass basis where noted.
    - Detection_Limit_* fields: Corresponding detection-limit-based values and semantics for each element (e.g., Detection_Limit_I-127, Detection_Limit_Li, etc.), described as the likely maximum CR value estimated using the biota concentration for which the detection limit was quoted.
    - Notes: Notes on analyses or how samples were used in estimating the whole-organism CR.
  - Data interpretation and handling of non-detects
    - Where a CR value is blank, the concentration was below the detection limit (as indicated in the adjoining Detection_Limit_* field or in the element’s notes).
    - Detection_Limit_* fields provide the upper bound used to interpret non-detects for each element.
  - Units and conventions
    - CR values are unitless.
    - Many elements’ CR values for animals reflect whole-organism concentrations on a fresh mass basis.
    - Some elements’ detection-limit fields explicitly indicate the maximum CR value estimated from the quoted detection limit.

- Calculation, interpretation, and data context
  - CR calculation relies on paired soil and biota stable element concentrations derived from the dataset; the biota value is divided by the soil value for the same Sample_Code (and soil used for calculations is identified).
  - For non-detects, the reported CR is replaced or bounded by the detection-limit-derived maximum CR, with Notes clarifying the estimation approach.
  - RAP classification and sample metadata enable grouping and stratification by reference organisms and sampling context.

- Data quality, metadata, and governance considerations
  - Emphasizes the need for complete metadata to verify data suitability (e.g., detection limits, sample provenance, and how CRs were estimated).
  - Highlights potential barriers for data sharing, but the structure here supports transparency through explicit definitions, units, and detection-limit semantics.
  - Notes field provides context on analyses and processing steps to support reproducibility and governance.

- Practical use for monitoring frameworks
  - Facilitates assessment of environmental transfer patterns across elements and samples.
  - Supports comparisons by RAP category and sampling context via RAP and collection date metadata.
  - Provides clear handling rules for non-detects to maintain defensible interpretation of low-concentration data.
  - Aids in documenting data provenance and methodological decisions for future monitoring decisions and policy evaluation.