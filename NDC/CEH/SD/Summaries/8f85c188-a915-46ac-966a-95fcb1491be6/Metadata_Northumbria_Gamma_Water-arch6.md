# TREE_Northumbria_Gamma_Water

- The dataset provides radiochemistry analysis of water samples from Northumbria, with a UKCEH radiochemistry lab sample identifier, site of sampling, mass of sample analysed, and decay date (taken as the sampling date). It includes activity concentrations for potassium-40 (K-40) and cesium-137 (Cs-137) in Bq per kilogram of fresh mass, along with two-sigma counting errors and minimum detectable activities (MDA). The data also indicate when a value is below the MDA, and general notes for context.

## Key fields and their meanings

- CEH_Sample_Identifier: UKCEH radiochemistry laboratory unique sample identifier.
- CEH_Sample_Description: Description of the UKCEH sample.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of the sample analysed (in grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken and used as the decay date.
- K-40_Bq_per_kg_FM: Activity concentration of K-40 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40 concentration.
- K-40_<: Indicator that the K-40 concentration is given as a "<" value (below MDA).
- MDA_K-40_Bq_per_kg_FM: Minimum Detectable Activity for K-40 (Bq per kg fresh mass).
- Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137 concentration.
- Cs-137_<: Indicator that the Cs-137 concentration is given as a "<" value (below MDA).
- MDA_Cs-137_Bq_per_kg_FM: Minimum Detectable Activity for Cs-137 (Bq per kg fresh mass).
- General_Notes: General notes related to the data.

## Data quality and interpretation considerations

- Data may be patchy and come from multiple formats or systems, requiring harmonisation.
- Some values may be reported as below the detection limit (indicated by the K-40_< or Cs-137_< markers) and are associated with an MDA value.
- Units for sample mass and activity are specified (grams for mass; Bq per kg fresh mass for activities), with some fields using "n/a" in the Units column.
- Counting errors provide uncertainty around activity measurements and should be incorporated in any analysis or visualization.
- The "Sampling_Date_Used_As_Decay_Date" implies a decay-correction context may be relevant for longitudinal interpretation.

## How to use and potential data products

- Self-serve dashboards or pivot tables by:
  - Site or sampling date to monitor radiological activity trends.
  - Compare K-40 and Cs-137 concentrations across samples.
  - Flag and filter censored data (below MDA) for appropriate statistical treatment.
  - Show counting uncertainty alongside measured activities.
- Data products to enable:
  - Site-level summaries of K-40 and Cs-137 with MDAs and uncertainties.
  - Time-series views to assess changes over sampling periods.
  - Context-rich reports incorporating CEH sample descriptions and general notes.
- Analytical considerations:
  - Treat "<" values as censored data using their corresponding MDA values in analyses.
  - Include counting errors to convey measurement precision in visualisations and reports.
  - Use decay-date context for any decay-corrected calculations if needed.

## Notes and metadata

- Source: UKCEH radiochemistry laboratory identifiers and sample descriptions.
- Decay-date context is provided via Sampling_Date_Used_As_Decay_Date.
- General notes field is available for supplemental information.