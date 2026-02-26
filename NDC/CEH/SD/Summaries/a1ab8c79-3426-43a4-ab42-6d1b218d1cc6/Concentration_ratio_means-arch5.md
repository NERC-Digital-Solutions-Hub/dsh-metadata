# Sample_Code, Explanation = Unique sample identifier.

- Purpose of the document
  - A data dictionary / metadata schema for sample analysis results, focusing on concentration ratios (mean values) and associated statistics across a wide range of elements.
  - Supports data sharing, discovery, and reuse by enabling consistent description of samples, species context, and analytical results.

- Key fields and structure
  - Core identifiers and context
    - Sample_Code: Unique sample identifier.
    - Species: Latin name of the sampled species.
    - RAP: Reference Animals and Plants (ICRP) classification to which the species can be attributed.
    - Sample_Description: Part of the sample that was analysed.
    - Mean_Value: Indicates whether the mean is geometric or arithmetic.
  - Concentration ratio fields (per element)
    - For each element (e.g., I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cs, Tl, U, Pb, U, etc. including U and Pb)
      - <Element>, 1: Mean concentration ratio.
      - <Element>, 2: Unit (described as unitless for concentration ratios).
      - <Element>, 3: Geometric or arithmetic mean as identified by Mean_Value.
      - Standard_Deviation_<Element>, 1: Standard deviation.
      - Standard_Deviation_<Element>, 2: Unit (unitless).
      - Standard_Deviation_<Element>, 3: Geometric or arithmetic standard deviation as identified by Mean_Value.
  - Notes on field values
    - Many fields use placeholders or n/a for Units/methodology or Notes (e.g., RAP, Units/methodology = n/a; Notes = n/a).
    - Several entries include formatting remnants (e.g., lines like “, 1 = . , 2 = . , 3 = standard deviation as identified by Mean_Value”) indicating partially populated schema or data extraction artifacts.

- Data standards and semantics
  - Concentration data are stored as mean concentration ratios and associated standard deviations for each element.
  - Units for concentration ratios are generally unitless.
  - Mean_Value governs whether means are geometric or arithmetic and how standard deviations are interpreted.
  - RAP links data to established reference organisms, enabling cross-study comparability within an ICRP framework.
  - Metadata fields like Sample_Description and Species provide necessary biological and sample-context for reuse.

- Data governance considerations for Data Stewards
  - Ensure completeness and consistency of core contextual fields (Sample_Code, Species, RAP, Sample_Description, Mean_Value).
  - Enforce standardized formatting across all element blocks (consistency in element names, the triplet for means, and the triplet for standard deviations).
  - Validate that Mean_Value correctly aligns with the corresponding Standard_Deviation fields (geometric vs arithmetic interpretation).
  - Maintain unit consistency (prefer unitless for concentration ratios) and document any deviations or exceptions.
  - Preserve provenance and versioning when datasets are updated or extended with new elements or samples.
  - Support data discovery by keeping the RAP classification and element-wise statistics machine-readable for portal/catalogue indexing.

- Practical challenges and considerations
  - Incomplete or partially populated fields (n/a, dots, or missing units) may impede interoperability and discovery.
  - Large, multi-element datasets with many similar field patterns require robust validation rules to prevent misalignment between means and standard deviations.
  - Diverse data sources and formats may necessitate normalization to the standardized element set and field naming conventions.

- Implications for data sharing and reuse
  - The structured, element-centered schema supports cross-dataset comparisons of concentration ratios and uncertainty.
  - Clear metadata around sample context (Species, RAP, Sample_Description) enables meaningful reuse in risk assessment, environmental monitoring, and radiological studies.
  - Adherence to the described data standards improves discoverability in portals and catalogues used by researchers and data managers.