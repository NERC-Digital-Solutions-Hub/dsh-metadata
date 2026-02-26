# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration_Ratio

## Purpose and scope
- Defines a data schema for calculating concentration ratios of elements in vegetation (fresh mass) relative to dry mass soil.
- Designed to support environmental health monitoring, data transparency, and informed policy decisions.

## Key entities and fields
- Species information: Latin_Species_Name, Common_Species_Name
- Sampling context: Site, Date_Sample_Collected, CEH_Sample_Identifier, CEH_Sample_Description
- Vegetation preparation and notes: Notes
- Link to soil: Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio data: I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Dual-field structure per ratio: Each element has a pair of related fields (e.g., Ca_Concentration_Ratio with an accompanying descriptor noting its interpretation) and markers for potential less-than values (e.g., <I, <Li, <Be, etc.)

## Concentration ratio fields and interpretation
- For each element, the dataset captures the concentration ratio as the ratio of Fresh Mass Vegetation to Dry Mass Soil.
- Notation for less-than values is supported via marker prefixes such as <I, <Li, <Be, <Mo, <Sr, <Tl, <As, <Se, <Cr, <Pb, <U, and others described in the header.
- Some fields appear as paired entries (e.g., 1 = n/a and 2 = the actual Concentration Ratio description), indicating structured references or variants within the schema.
- Specific elements covered include major and trace metals: Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Tl, Pb, U, with Sr-based variants indicating Sr-associated concentration ratio interpretations.

## Metadata, provenance, and data linkage
- Includes detailed sample identifiers (CEH_Sample_Identifier) and descriptive notes (CEH_Sample_Description, Notes) to enable traceability of vegetation samples.
- Explicitly records the co-located soil sample used to calculate each concentration ratio, establishing a clear linkage between vegetation and soil data.
- Date of collection and site information support temporal and spatial analyses critical for monitoring frameworks.

## Data quality and governance considerations (aligned with monitoring frameworks)
- Metadata richness supports verification of requirements and reproducibility of concentration-ratio calculations.
- The presence of notes on vegetation preparation and data provenance aids transparency and quality assurance.
- The schema anticipates data gaps and transformation needs (variable indicators for less-than values) and emphasizes the need to manage and document the inputs used to derive the concentration ratios.

## Practical implications for policy evaluation and decision-making
- Provides a structured dataset to assess how tree vegetation accumulates or reflects soil metal concentrations, informing risk assessments and environmental health evaluations.
- Enables cross-site and cross-species comparisons of uptake patterns, informing monitoring priorities and remediation decisions.
- Supports reporting dashboards and clear communication of findings to stakeholders through standardized fields and documented methodologies.