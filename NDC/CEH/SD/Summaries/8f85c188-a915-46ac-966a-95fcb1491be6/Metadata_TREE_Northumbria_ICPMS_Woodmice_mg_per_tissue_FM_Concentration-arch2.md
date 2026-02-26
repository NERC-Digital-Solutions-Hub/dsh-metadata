# TREE_Northumbria_ICPMS_Woodmice_mg_per_tissue_FM_Concentration

- Purpose and scope
  - A data dictionary describing concentrations of various elements in wood mouse tissues, measured by ICP-MS, for environmental monitoring in Northumbria.
  - Designed to support consistent reporting of environmental health and policy performance over time.

- Key data components
  - Taxonomic and sample identifiers
    - Latin_Species_Name, Common_Species_Name: scientific and common names of the wood mouse.
    - Site: sampling location.
    - Date_Sample_Collected: date of collection.
    - CEH_Sample_Codes, CEH_Sample_Description: UKCEH sample codes and descriptions.
    - Tissue: name of the wood mouse tissue sampled (e.g., total tissue; note mentions of specific tissues not collected in some cases).
  - Data flags and qualifiers
    - <I, <Al, <V, <Cr, <Mo, <Pb, <Ba, <Ni, <U: markers indicating that the reported concentration is a “less than” value (non-detects or below detection limit).
    - I_mg_per_tissue_FM, Li_mg_per_tissue_FM, Na_mg_per_tissue_FM, Al_mg_per_tissue_FM, P_mg_per_tissue_FM, K_mg_per_tissue_FM, Ca_mg_per_tissue_FM, Ti_mg_per_tissue_FM, V_mg_per_tissue_FM, Cr_mg_per_tissue_FM, Mn_mg_per_tissue_FM, Fe_mg_per_tissue_FM, Co_mg_per_tissue_FM, Ni_mg_per_tissue_FM, Cu_mg_per_tissue_FM, Zn_mg_per_tissue_FM, As_mg_per_tissue_FM, Se_mg_per_tissue_FM, Rb_mg_per_tissue_FM, Sr_mg_per_tissue_FM, Mo_mg_per_tissue_FM, Ag_mg_per_tissue_FM, Cd_mg_per_tissue_FM, Cs_mg_per_tissue_FM, Tl_mg_per_tissue_FM, Pb_mg_per_tissue_FM, U_mg_per_tissue_FM: concentrations of elements in milligrams per total wood mouse tissue (fresh mass). Some entries note variations like “collected for woodmice thyroid” or specify tissue type.
  - Data coverage notes
    - Some tissues have no data (e.g., Hind Leg Bone, woodmice liver for certain samples; thyroid data for several elements).
    - Several fields indicate where data was not collected for thyroid tissue.
  - Units and interpretation
    - Concentrations are reported as mg per total wood mouse tissue in fresh mass (FM).
    - Some columns explicitly indicate that a value is less than a detected threshold.

- Data quality and processing (as per archetype approach)
  - Verification and quality assurance of source data from established sampling programs.
  - Cleaning and transformation to ensure consistency across samples and sites.
  - Standardised reporting formats (clear formats such as reports, maps, and charts) for dissemination.
  - Datasets stored and uploaded to appropriate portals for accessibility and reuse.

- Outputs and use cases
  - Outputs typical for analysts monitoring the environment:
    - Temporal and spatial comparisons of metal/element concentrations in wood mice.
    - Assessments of environmental health against standards.
    - Visualisations (maps, charts) and summarized reports for policy scrutiny.
  - Cross-dataset utility
    - Enables combination with other relevant datasets to enhance value beyond single-use analyses.
    - Supports access to underlying data used to derive final outputs for transparency and further analysis.

- Challenges and considerations
  - Data gaps: missing data for certain tissues (e.g., hind leg bone, liver in some samples; thyroid data for several elements); some samples indicate non-detects or below-detection values.
  Less-than values require careful treatment in analyses (imputation or censoring considerations).
  - Consistency: ensuring uniform tissue terminology and unit interpretation across sites and time.
  - Data access: facilitating broad access to underlying data while maintaining data quality and provenance.

- Practical notes for analysts
  - Prioritize verification of sample metadata (site, date, CEH codes) before analysis.
  - Handle non-detects and less-than values according to established statistical approaches for censored data.
  - When aggregating across tissues or sites, account for tissues with no data to avoid biased summaries.
  - Leverage the standardized dataset structure to generate comparable health indicators and trend analyses over time.