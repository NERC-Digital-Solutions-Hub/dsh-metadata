# TREE_Northumbria_ICPMS_Toad_FM_Concentration

## Overview
- A dataset of toad samples from Northumbria with ICP-MS–measured element concentrations on a fresh mass basis.
- Includes both specimen metadata and concentrations for a wide range of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).
- Data are intended to support environmental monitoring and ecotoxicology analyses by enabling cross-sample comparisons and data-driven insights.

## Metadata and sample information
- Latin_Species_Name: Latin taxonomic name of the species.
- Common_Species_Name: Common name of the species.
- Site: Sampling site identifier.
- Date_Sample_Collected: Collection date.
- CEH_Sample_Code: UKCEH sample code.
- CEH_Sample_Description: Description of the UKCEH sample.
- Fresh_Mass_Ash_Mass_Ratio: Ratio of whole-body fresh mass (excluding gut) to ash mass.
- Notes: Miscellaneous notes related to toad preparation (e.g., whether separate tissues were prepared).
- Notes on data quality: Some metadata explanations appear misaligned or repetitive (potential copy-paste errors in field explanations).

## Concentration data (elements)
- I_mg_kg_FM to U_mg_kg_FM (fresh mass basis), each with:
  - Units: mg/kg.
  - Explanation: Concentration of the element in milligrams per kilogram fresh mass.
- Field names follow the pattern Element_mg_kg_FM, with accompanying explanatory text (some entries exhibit inconsistencies, e.g., multiple lines incorrectly stating “Concentration of Cr” or mismatched element names in explanations).
- A broad panel of elements is covered, enabling multi-element exposure assessments across samples.

## Data quality considerations
- Field explanations contain inconsistencies and copy-paste errors (e.g., incorrect “Concentration of Cr” references for several elements, mismatched element descriptions).
- Metadata consistency issues to watch for: date formats, site identifiers, and CEH sample codes.
- Data are on a wide format; potential need for normalization or restructuring for certain analyses.

## Potential uses
- Environmental exposure assessment for toads across sites.
- Cross-sample comparisons of trace element concentrations on a fresh mass basis.
- Integration with site metadata to explore spatial and temporal patterns.
- Supporting dashboards or reports that summarize elemental burdens by site, species, or collection date.

## Data preparation and quality assurance recommendations
- Verify and correct metadata explanations to align with actual measurements (fix mislabeling in element descriptions).
- Normalize dates and standardize site codes and CEH_sample_codes.
- Consider converting to a long-format dataset for flexible analyses (element, sample, concentration).
- Validate units and ensure all element fields are represented consistently (mg/kg FM).
- Create a robust data dictionary detailing each field, its unit, and its derivation (especially for the concentration fields).
- Assess completeness across samples to identify patchy data and plan imputation or exclusion as appropriate.