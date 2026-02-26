# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- A metadata-rich dataset describing concentration ratios of various elements in bee samples relative to co-located soil samples.
- Key fields capture taxonomic details, sampling context, sample descriptions, and the calculation basis for concentration ratios (Fresh Mass Bee to Dry Mass Soil).

## Data model and key fields
- Taxonomy and naming: Latin_Species_Name, Common_Species_Name.
- Sampling context: Site, Date_Sample_Collected.
- Sample provenance: CEH_Sample_Codes, CEH_Sample_Description, Sample_Details, Notes.
- Provenance linkage: Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (description of the soil sample used for the ratio).
- Concentration ratio values: I_Concentration_Ratio plus a series of element-specific fields (Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio).
- Value characteristics: Most fields are presented as ratios with no units (Units = n/a). Some columns include a leading "<" to indicate less-than/sub-threshold values.
- Notes on structure: The dataset appears to include both an initial concentration ratio (I_Concentration_Ratio) and element-specific concentration ratios, reflecting the Bee-to-Soil calculation basis.

## Provenance, measurement, and calculation
- Samples are described with associated CEH codes and descriptions to enable traceability.
- The concentration ratio is defined as Fresh Mass Bee (whole body) concentration divided by Dry Mass Soil concentration, with a co-located soil sample used to compute the ratio.
- Some concentration-ratio fields may contain less-than values (indicated by a leading "<"), signaling detection limits or reported thresholds.
- The documentation explicitly links bee samples to their corresponding soil samples to support interpretation of transfer factors.

## Data quality considerations and limitations
- Metadata completeness is crucial: ensure all fields are populated (taxonomy, site, date, sample codes, soil linkage, and all relevant concentration ratios).
- Consistency in naming and coding (Site, Species names, CEH codes) is important for interoperability across datasets.
- Handling of < value entries needs clear policy to avoid misinterpretation during analysis.
- Units are not applicable (ratios), but clear interpretation guides are essential for downstream users.
- The format contains some ambiguous or garbled lines in places; data stewards should verify field definitions and ensure clean, machine-readable schema.

## Data governance and stewardship recommendations
- Standardize controlled vocabularies for Site and Species to improve cross-dataset interoperability.
- Enforce complete metadata for each record (especially taxonomic details, site, date, CEH codes, and soil linkage).
- Document the calculation method and any special cases (e.g., < threshold values) in a dataset-level metadata record.
- Implement data versioning and change-tracking for updates to sample descriptions or ratio calculations.
- Establish data sharing and publication rules, including embargoes or access restrictions if applicable.
- Create data quality checks to validate that co-located soil samples align with reported concentration ratios and that all element fields are consistently populated or clearly flagged as missing.
- Plan for data ingestion workflows that can handle heterogeneous formats and ensure interoperability with other ICPMS and environmental datasets.

## Practical use and operational steps for data stewards
- Ingest validation: check for presence of Latin_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio, and at least a subset of element concentration ratios.
- Consistency checks: ensure Site and Date_Sample_Collected align with CEH codes and soil linkage; verify that < values are properly flagged and documented.
- Documentation: attach a dataset-level metadata document describing the calculation method, data provenance, and any caveats related to < values or missing data.
- Publication readiness: align with repository schema for environmental datasets; provide a data dictionary, example records, and guidance for analysts.
- Ongoing stewardship: coordinate with data creators to obtain timely updates, maintain versioned releases, and track changes to sample descriptions or associated soil samples.