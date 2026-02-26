# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Purpose and scope
- Provides concentration ratio data comparing bee tissue concentrations to corresponding dry mass soil concentrations at sampling sites.
- Based on ICP-MS measurements, intended to support environmental health monitoring, scrutiny of policy decisions, and future decision-making.

## Data structure and key fields
- Species and site metadata
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
- Co-located soil reference
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio values
  - I_Concentration_Ratio
  - Be_Concentration_Ratio
  - Li_Concentration_Ratio
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio
  - Mn_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio
- Notes on special values
  - Some concentration ratio fields use a less-than marker (e.g., <Be, <Se, <U) to indicate upper-bound values.

## Calculation method
- Concentration_Ratio = Fresh Mass Bee (whole body) concentration divided by Dry Mass Soil concentration.
- The dataset distinguishes explicit numeric ratios and marked “less than” values where appropriate.

## Data quality, metadata, and governance considerations
- Metadata and data provenance are essential to verify suitability for policy decision-making.
- Data challenges likely include: gaps or low quality data, data access issues, organizational silos, and the need for open data sharing.
- Some datasets may require transformation or substantial metadata to be readily usable.
- Governance for datasets should address storage, sharing, versioning, and up-to-date maintenance.

## How this supports monitoring frameworks
- Enables assessment of ecological exposure pathways by linking bee tissue contamination to soil conditions.
- Facilitates cross-site comparisons, trend analysis, and identification of contamination hotspots.
- Supports reporting to stakeholders through clear calculations and transparent data sources.

## Practical considerations for implementation
- Ensure consistent metadata: species, site, sampling date, sample IDs, and soil context for each concentration ratio.
- Verify data quality: QA/QC of ICP-MS measurements, consistency in bee and soil sampling, and proper calculation of ratios.
- Plan data sharing and governance: clear data availability, documentation of any restrictions, and appropriate data management at the source.

## Endnotes and caveats
- The usefulness of concentration ratios depends on data completeness, timely updates, and clear communication of any upper-bound values or data transformations applied.