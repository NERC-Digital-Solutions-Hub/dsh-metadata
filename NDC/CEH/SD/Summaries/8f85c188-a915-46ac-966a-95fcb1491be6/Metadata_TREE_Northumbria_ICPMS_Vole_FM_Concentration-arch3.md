# TREE_Northumbria_ICPMS_Vole_FM_Fresh_Mass_Concentration

## Overview
- A dataset detailing ICPMS-measured concentrations of multiple elements in vole tissue, with supporting sampling metadata.
- Purpose aligned with environmental health monitoring: provides exposure indicators to evaluate policy and inform future decisions.

## Data content and structure
- An extensive list of element concentrations measured as mg/kg in fresh mass (FM) of vole tissue, including I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, and U.
- For some elements, concentration values are reported as “less than” thresholds (e.g., <Be, <Ag, <U).
- Fresh_Mass_Ash_Mass_Ratio is provided, indicating the ratio of whole animal fresh mass to ash mass.
- All element concentrations are designated with the suffix _FM, indicating measurements on a fresh mass basis.

## Metadata and sampling details
- Latin_Species_Name and Common_Species_Name identify the vole species sampled.
- Site records the sampling location; Date_Sample_Collected notes when the sample was taken.
- CEH_Sample_Codes and CEH_Sample_Description provide standardized UKCEH identifiers and descriptive details.
- Sample_Details contains preparation notes; Tissue includes notes on how the vole tissue was handled (e.g., whether separate tissues were prepared).
- The dataset is structured to support traceability from field collection through laboratory analysis.

## Measurement specifics
- Concentrations are reported as mg/kg_FM for each listed element.
- The dataset includes explicit handling for censored data with less-than markers, which is important for data interpretation and quality assurance.

## Data quality and governance implications
- Rich metadata supports data provenance and reproducibility necessary for monitoring frameworks.
- Presence of censored values (< thresholds) requires clear handling in analyses and reporting.
- Standardized codes (CEH_Sample_Codes, CEH_Sample_Description) facilitate cross-dataset compatibility and data sharing.

## Potential monitoring applications
- Assess environmental exposure to a broad panel of elements in small mammals as indicators of ecosystem contamination.
- Compare contaminant profiles across sampling sites and collection dates to inform policy reviews and decision making.
- Track changes in metal burdens in relation to environmental management actions or regulatory changes.

## Relevance to monitoring framework authors
- Demonstrates the integration of biological sampling, laboratory chemical analysis, and detailed metadata essential for evaluating monitoring approaches.
- Highlights data governance considerations: metadata completeness, handling of censored data, and transparent sample provenance.
- Illustrates common challenges and data requirements for sharing and reuse within environmental health monitoring programs.