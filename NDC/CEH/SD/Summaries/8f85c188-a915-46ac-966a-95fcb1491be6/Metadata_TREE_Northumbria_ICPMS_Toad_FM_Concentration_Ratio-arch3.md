# TREE_Northumbria_ICPMS_Toad_FM_Concentration_Ratio

- Purpose and scope
  - Defines a data schema for concentration ratio measurements in toads relative to surrounding soil, to support environmental health monitoring, policy scrutiny, and future decision-making.
  - Specifically focuses on ICPMS-derived element concentration ratios in toads, enabling assessment of exposure pathways from soil to a bioindicator species.

- Key entities and fields
  - Species and site information
    - Latin_Species_Name, Common_Species_Name
    - Site
  - Sampling details
    - Date_Sample_Collected
    - CEH_Sample_Code, CEH_Sample_Description
    - Notes (about preparation of toads)
  - Reference and provenance
    - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (description of the soil sample used for ratio calculation)
  - Concentration ratio data (dimensionless)
    - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
    - Explanation for each ratio: Fresh Mass Toad (wholebody) divided By Dry Mass Soil
  - Metadata conventions
    - Units for most fields are listed as n/a, reflecting dimensionless concentration ratios
    - Descriptions provide explicit meaning for each concentration ratio field

- Data quality, metadata, and provenance considerations
  - Emphasizes the need for clear sample identification (CEH Sample codes and descriptions) and prep notes to support reproducibility.
  - Highlights the importance of linking to a co-located soil sample used in ratio calculations to ensure contextual relevance.
  - The schema supports traceability of data through explicit sample codes and descriptive notes.

- Implications for monitoring framework authors
  - Provides a structured template to capture bioindicator–soil exposure relationships across elements, enabling consistent reporting and comparability.
  - Facilitates transparent data governance by documenting sample provenance, preparation, and calculation method for each ratio.

- Potential challenges and governance considerations
  - Data availability and completeness: many fields rely on comprehensive field and lab metadata; gaps could hinder cross-site comparisons.
  - Metadata quality: clear explanations and consistent naming are essential to avoid misinterpretation of ratios.
  - Data sharing: the need to publicly share underlying datasets may require robust data governance and privacy or confidentiality considerations for sensitive site information.
  - Data transformation: ratio-based metrics require careful handling to maintain data integrity during cleaning and transformation.

- End use and applications
  - Enables policy-relevant analysis of soil-to-toad transfer for numerous elements, informing environmental health assessments and management decisions.
  - Supports dashboards and reports that communicate exposure patterns and potential regulatory implications to stakeholders.