# TREE_Northumbria_ICPMS_Vole_FM_Fresh_Mass_Concentration

- Purpose and scope
  - Describes ICP-MS measured concentrations of multiple elements in fresh-mass vole tissue from Northumbria.
  - Concentrations are reported as mg/kg of fresh mass (FM) for each element.

- Key sample metadata
  - Latin_Species_Name and Common_Species_Name: scientific and common names of the vole(s).
  - Site: sampling location.
  - Date_Sample_Collected: collection date.
  - CEH_Sample_Codes: UK Centre for Ecology & Hydrology sample identifiers.
  - Sample_Details: notes on sample preparation details.
  - CEH_Sample_Description: UKCEH’s sample description.
  - Tissue: notes on vole preparation (explicitly states separate tissues were not prepared).
  - Fresh_Mass_Ash_Mass_Ratio: ratio of whole-animal fresh mass to ash mass, indicating sample processing for ash-related calculations.

- Data columns for element concentrations
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM.
  - Units: milligram per kilogram fresh mass (mg/kg_FM).
  - Data nuances: some columns use a less-than indicator (e.g., <Be, <Ag, <U) to denote censored or upper-bound values.
  - Note: a few descriptions show typographical irregularities (e.g., “Fresh_Mass_Ash_Ma s_Ra tio”/spacing issues) but the intent is clear as concentration measurements.

- Data characteristics and considerations
  - The dataset combines geological/biological metadata with multi-element concentration measurements on the same biological samples.
  - Some fields show “n/a” where not applicable or missing.
  - The “Tissue” note indicates no separate tissue preparations were performed, implying whole-animal or non-dissected tissue measurements.
  - Presence of censored (<) values requires appropriate statistical handling in analyses.

- Potential analytical applications
  - Compare elemental concentrations across sites, dates, or vole species.
  - Explore correlations among elements or with biomass-related metrics like the Fresh_Mass_Ash_Mass_Ratio.
  - Develop predictive or explanatory models of exposure or bioaccumulation patterns.
  - Handle censored data (less-than values) using appropriate statistical methods.
  - Use CEH_Sample_Codes and metadata for traceability, replication, and integration with other datasets.