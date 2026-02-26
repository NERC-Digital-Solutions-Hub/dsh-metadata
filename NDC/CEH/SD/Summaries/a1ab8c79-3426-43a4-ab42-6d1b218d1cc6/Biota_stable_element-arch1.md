# Supporting documentation for Biota_Stable_Element.csv

- The document is a data dictionary for Biota_Stable_Element.csv, detailing sample identifiers, sample descriptions, collection timing, and a comprehensive set of element concentration measurements with associated detection limits.
- It codifies how data are stored, labeled, and interpreted to support analytical questions about correlations, distributions, and potential predictive relationships.

## Key fields and structure

- Sample_Code: Unique sample identifier.
- RAP: Sample type based on International Commission on Radiological Protection (ICRP) Reference Animals and Plants (RAPs); serves as a taxonomic/biological category.
- Sample_Description: Additional explanation of the sample; notes that samples RCN119, RCN120, and RCN121 are replicate soil samples.
- Collection_Date: Date of soil sample collection, format as dd-mmm-yyyy.
- I-127_mg_kg_fw, Li_mg_kg_fw, Be_mg_kg_fw, B_mg_kg_fw, Na_mg_kg_fw, Mg_mg_kg_fw, Al_mg_kg_fw, P_mg_kg_fw, S_mg_kg_fw, K_mg_kg_fw, Ca_mg_kg_fw, Ti_mg_kg_fw, V_mg_kg_fw, Cr_mg_kg_fw, Mn_mg_kg_fw, Fe_mg_kg_fw, Co_mg_kg_fw, Ni_mg_kg_fw, Cu_mg_kg_fw, Zn_mg_kg_fw, As_mg_kg_fw, Se_mg_kg_fw, Rb_mg_kg_fw, Sr_mg_kg_fw, Mo_mg_kg_fw, Ag_mg_kg_fw, Cd_mg_kg_fw, Cs_mg_kg_fw, Ba_mg_kg_fw, Tl_mg_kg_fw, Pb_mg_kg_fw, U_mg_kg_fw: concentrations of respective elements on a fresh mass basis (mg/kg fw).
- For each element, a corresponding Detection_Limit_<element>_mg_kg_fw field exists, specifying the detection limit for that sample.
- Notes: An accompanying field describing analyses or how samples were used in estimating whole-organism concentration.

## Concentration and detection-limit semantics

- Concentration fields (e.g., I-127_mg_kg_fw) represent element concentrations on a fresh mass basis.
- Detection_Limit_<element>_mg_kg_fw fields provide the detection limit per sample.
- When concentration fields are blank, they indicate non-detects; blanks in detection-limit fields indicate contextual notes about detection or reporting per column conventions.
- The documentation repeatedly notes that, for many elements, “Notes” explain how to interpret blanks (e.g., below detection limit or detectable in a given column’s logic). The general pattern is that blanks in concentration fields denote concentrations below detection limits, while blanks in certain detection-limit fields reflect how the data were reported or interpreted for that sample.

## Replicates and data provenance

- Replicate soil samples are explicitly indicated by Sample_Description (e.g., RCN119, RCN120, and RCN121), enabling assessment of measurement precision and replication.

## Data quality and usability considerations

- The RAP classification and collection-year details support stratified analyses by biological reference category and time.
- The extensive set of detection limits across many elements allows handling censored data in analyses (e.g., survival/left-censoring models, substitution rules, or appropriate statistical methods for non-detects).
- The Notes field provides context on analyses or how samples were used to estimate whole-organism concentrations, aiding reproducibility and traceability.
- The data are organized to support cross-element comparisons on a consistent fresh-mass basis (mg/kg_fw) with explicit detection thresholds, facilitating correlation and predictive modeling across elements.

## Practical implications for analysts

- When modeling or testing hypotheses, incorporate detection-limit information to properly handle censored observations.
- Use the replicate samples to assess measurement variability and improve confidence in estimated relationships.
- Leverage RAP-based grouping to explore ecological or biological patterns across sample types.
- Pay attention to the Sample_Description and Notes to understand sample provenance and any adjustments made during analysis or estimation.