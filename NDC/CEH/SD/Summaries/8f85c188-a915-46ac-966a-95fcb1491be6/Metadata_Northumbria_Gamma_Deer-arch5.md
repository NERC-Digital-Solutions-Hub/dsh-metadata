# TREE_Northumbria_Gamma_Deer

- Overview
  - Dataset describing radiochemical analysis of Cs-137 in Roe deer samples, including sample metadata, measurement results (activity concentrations), uncertainties, and concentration ratios. Sourced from UKCEH Radiochemistry Laboratory workflows.

- Key fields and meanings
  - Latin_Species_Name: Latin name of species (Roe deer).
  - CEH_Sample_description: UKCEH sample description.
  - Tissue: Tissue type analyzed (e.g., muscle).
  - CEH_Sample_code: UKCEH Radiochemistry Laboratory unique sample identifier.
  - Site: Sampling site.
  - Fresh_Mass_Of_Sample_Analysed_g: Fresh mass of the analyzed sample in grams.
  - Sampling_date_Used_As_Decay_date: Date the sample was taken, also used as decay date for activity.
  - Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in Bq per kg fresh mass at the day of sampling.
  - Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error of Cs-137 in Bq per kg dry mass.
  - Cs-137 <: Marker indicating a concentration value is below the reported level (less than MDA).
  - MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity concentration of Cs-137 in Bq per kg fresh mass.
  - Cs-137_Concentration_Ratio_FM: Cs-137 concentration ratio (fresh mass) defined as muscle Bq/kg FM divided by soil Bq/kg DM.
  - CR_Notes: Notes related to the concentration ratio.

- Data quality and units
  - Units used: Bq per kg (FM or DM) for activity; g for mass; n/a where not applicable.
  - Uncertainty: Includes two-sigma counting error.
  - Special values: Use of "<" marker for values below MDA; MDA field stores the detection limit.
  - Metadata completeness: Requires consistent species name, sample description, site, tissue, and unique sample code.

- Data governance considerations for Data Stewards
  - Metadata completeness: Ensure all fields have clear definitions (as above) and consistent terminology; standardize tissue types and site names where possible.
  - Data provenance: Preserve CEH_Sample_code, sampling date, and decay date linkage; document sample description and notes (CR_Notes).
  - Interoperability: Align field names and units with other radiochemistry datasets to enable cross-study queries (e.g., standardize Cs-137 measurements, MDA handling, and concentration ratios).
  - Data accessibility and sharing: Prepare dataset for uploading to relevant data portals/catalogues; include full definitions and unit specifications in metadata.
  - Data quality checks: Validate numeric fields (mass in grams, Cs-137 concentrations in Bq/kg FM/DM, MDA, and counting error); verify handling of "<" values and decay-date usage.
  - Update and versioning: Track updates to sample metadata, mass measurements, decay dates, or re-calculated concentrations; maintain an audit trail.

- Practical considerations and recommendations
  - Ensure Latin_Species_Name corresponds to the Roe deer and remains consistent across datasets.
  - Confirm CEH_Sample_code uniqueness and link to CEH_Sample_description.
  - Clarify soil context if present when interpreting Cs-137_Concentration_Ratio_FM; ensure soil mass units are defined (DM) for ratio calculations.
  - Document any CR_Notes or context that affects interpretation of concentration ratios (e.g., methodology differences, sample handling).
  - Prepare guidance on handling and displaying censored data (values marked as Cs-137 <) in analyses and portals.

- End goal
  - Enable discoverability, consistent interpretation, and reliable reuse of Cs-137 data from Roe deer samples for ecological transfer and radiological exposure assessments.