# Supporting documentation for 08-Vegetal_Foodstuff_Stable.csv

- Purpose and scope
  - Provides metadata definitions for the dataset 08-Vegetal_Foodstuff_Stable.csv.
  - Documents sample identifiers, sample type, location, description, collection date, and sample size.
  - Details concentrations of multiple stable elements in vegetal foodstuff samples (including Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) with matrix-specific units (mg/kg dry mass or mg/L for olive oil and wine).

- Data structure and fields
  - Sample metadata fields:
    - Sample_Code: unique sample identifier.
    - Sample_Type: general description of sample (foodstuff group).
    - Location: site of sample collection.
    - Sample_Description: part of the organism analyzed.
    - Collection_Date: date of sampling (dd-mm-yyyy).
    - Sample_size: amount analyzed (g fresh matter or mL for olive oil and wine).
  - Element concentration fields (for each element, e.g., Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th):
    - Element_mg/kg_dm: concentration on a dry mass basis.
    - Unc_Element_mg/kg_dm: combined uncertainty on the concentration.
    - Detection_Limit_Element_mg/kg_dm: detection limit on a dry mass basis.
    - Notes: blanks indicate concentration below detection limit, with corresponding interpretation.
  - Units and matrix notes:
    - Primarily mg/kg_dm (dry mass) or mg per litre for olive oil and wine.
    - Some elements include additional subfields or formatting (e.g., multiple lines for certain elements), with blanks signaling below-detection values.

- Data quality, transformation and QA
  - Emphasises data verification, quality assurance, cleaning, and transformation of inputs from established sources.
  - Supports standardised analysis and consistent outputs across samples and elements.

- Outputs and presentation
  - Metadata supports clear reporting formats and the ability to categorise or compare environmental concentrations across samples and matrices.

- Storage, access, and reuse
  - Framework aligns with storing datasets and uploading to appropriate portals.
  - Enables others to access underlying data used to generate outputs, promoting data reuse and transparency.

- Practical considerations
  - Detection-limit handling: empty fields typically indicate concentrations below the detection limit.
  - Cross-matrix scope: includes olive oil and wine matrices in addition to vegetables, affecting unit representation and interpretation.