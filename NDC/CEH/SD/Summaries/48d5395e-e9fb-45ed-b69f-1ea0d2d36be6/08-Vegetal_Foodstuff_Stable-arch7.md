# Supporting documentation for 08-Vegetal_Foodstuff_Stable.csv

- Purpose
  - Metadata and field definitions for the Vegetal_Foodstuff_Stable.csv dataset.
  - Documents sample-level information and multiple elemental concentration measurements relevant to plant-based foodstuffs (stable elements/markers).

- Key entities in the dataset
  - Sample identifiers and description
    - Sample_Code: unique sample identifier
    - Sample_Type: general description of the sample group
    - Location: site/name where the sample was collected
    - Sample_Description: part of the organism analyzed (e.g., tissue portion)
    - Collection_Date: date of sampling (format dd-mm-yyyy)
    - Sample_Size: amount analyzed; units vary (g fresh matter or mL for olive oil and wine)
  - Measurement variables
    - Elements measured (examples): Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th
    - Concentration fields: element_mg/kg_dm (dry mass basis) or element_mg/kg_dm, and wine/olive oil equivalents (per litre where applicable)
    - Uncertainty fields: Unc_<element>_mg/kg_dm (combined uncertainty on a dry mass basis)
    - Detection limit fields: Detection_Limit_<element>_mg/kg_dm (detection limit values)
    - Notes on values: blank entries indicate concentrations below the detection limit

- Measurement details and units
  - Concentrations are primarily on a dry mass basis (mg/kg_dm)
  - For olive oil and wine matrices, units can be mg per litre (mg/L)
  - Collection date and sample size formats are specified (dd-mm-yyyy; units specified for each sample)
  - Detection limits accompany each concentration, with blanks meaning non-detect

- Data quality and consistency considerations
  - Some fields include multiple subfields or labeled positions (e.g., Detection_Limit_K_mg/kg_dm entries with 1/2/3) due to formatting; refer to the documentation for exact field mapping
  - Blank values indicate concentrations below the detection limit
  - Data are assembled from multiple sources or measurements, potentially leading to varying standards and formats across variables

- GIS-specific considerations and use
  - Location and collection date enable spatial and temporal mapping of element concentrations
  - Concentration values, along with associated uncertainties, support thematic mapping (e.g., choropleth or graduated symbol maps) and uncertainty visualization
  - Handling non-detects is essential (treat as < Detection_Limit; consider using censored data methods)
  - Units vary by matrix (dry mass vs. per litre)—ensure unit harmonization when integrating with other geospatial datasets
  - Sample descriptions and types facilitate categorization and filtering in map applications (e.g., by foodstuff group or tissue type)

- Practical notes for GIS analysts
  - Use Location for geospatial joins and spatial analyses; align with other spatial layers as needed
  - Use Collection_Date to enable time-enabled mapping or trend analyses
  - Map concentration fields with appropriate legends; consider displaying Unc_<element> as an uncertainty halo or separate layer
  - Carefully manage non-detect values to avoid misinterpretation in visualizations
  - Be mindful of matrix-specific units (mg/kg_dm vs. mg/L) when aggregating or comparing across samples

- Limitations and cautions
  - The data dictionary reveals formatting inconsistencies in some field definitions; verify field mappings when importing
  - Consistency across samples in terms of units and detection limits may vary; harmonization may be required for cross-sample comparisons
  - The dataset focuses on stable elements; interpret results within the context of vegetal foodstuff matrices and sampling design