# TREE_Northumbria_ICPMS_Vole_FM_Concentration_Ratio

- Purpose and scope
  - Metadata/schema for concentration ratios of various elements in vole tissue (fresh mass) relative to soil dry mass, used to analyze uptake and environmental transfer.
  - Includes specimen and sampling details to support correlation and predictive analyses.

- Key metadata fields
  - Taxonomic and sample identifiers: Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Code, CEH_Sample_Description, Notes.
  - Sampling context: Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (soil location tied to the vole collection).
  - Concentration ratio measurements (Fresh Mass Vole divided by Dry Mass Soil) for numerous elements/metals.

- Concentration ratio metrics included
  - Primary index: I_Concentration_Ratio (Iodine) and a broad suite of elements: Li, Be (<Be_Concentration_Ratio indicates a less-than value), Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni (<Ni with less-than), Cu, Zn, As, Se, Rb, Sr, Mo, Ag (<Ag), Cd, Cs, Ba (Ba_Concentration_Ratio presented as two fields: Ba_Concentration_Ratio_1 and Ba_Concentration_Ratio_2), Tl (<Tl), Pb, U (<U with two-part notation).
  - Each concentration ratio is defined as: Fresh Mass Vole (whole body) divided By Dry Mass Soil.

- Data formatting and interpretation notes
  - Most units are not applicable (Units = n/a).
  - Some column names and formatting show inconsistencies or typographical irregularities (e.g., "<Be" and "<Ni" markers, duplicated or split field names like Ba_Concentration_Ratio_1/2, Tl_Concentration_Ratio_1/2).
  - Several fields indicate upper-bound values or values less than a threshold (indicated by the < marker).
  - The dataset relies on a related soil sample to compute the concentration ratio for each vole sample.

- Data quality and provenance considerations
  - Missing or inapplicable values are denoted as n/a, requiring careful handling in analyses.
  - Harmonizing field names and ensuring consistent interpretation of the concentration ratio definitions is important when integrating with other datasets.

- Analytical use and implications
  - Enables examination ofElement-specific uptake patterns and environmental transfer by correlating vole tissue concentrations with soil concentrations.
  - Supports cross-element comparisons, trend analyses by site/date, and potential modeling of uptake pathways, while accounting for data gaps and formatting inconsistencies.