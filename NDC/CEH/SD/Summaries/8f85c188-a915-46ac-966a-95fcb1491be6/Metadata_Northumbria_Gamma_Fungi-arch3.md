# TREE_Northumbria_Gamma_Fungi

- A dataset header detailing measurements of gamma-emitting radionuclides in Fungi and soil from Northumbria, including K-40 and Cs-137 activity concentrations.
- Data captured for both dry mass (DM) and fresh mass (FM) bases, with associated uncertainties and detection limits.
- Includes fungal-to-soil concentration ratio fields and general notes for context.

## Data Elements and Structure

- Latin_Species_Name: Scientific name of the fungal sample (with n/a units).
- CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample ID.
- Site: Sampling location.
- Mass_of_Sample_analysed_g: Mass of sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: Date of sampling (also used as decay date in some analyses).
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass for soil samples.
- K-40_Bq_per_kg_DM: K-40 activity concentration in Bq/kg dry mass.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 (DM).
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity for K-40 (DM).
- K-40_<: Indicator that the reported value is a "<" (less than) value for K-40 (DM).
- Cs-137_Bq_per_kg_DM: Cs-137 activity concentration in Bq/kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 (DM).
- Cs-137_<: "<" marker for Cs-137 (DM).
- MDA_Cs-137_Bq_per_kg_DM: MDA for Cs-137 (DM).
- K-40_Bq_per_kg_FM: K-40 activity concentration in Bq/kg fresh mass.
- Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40 (FM).
- K40_<: "<" marker for K-40 (FM).
- MDA_K-40_Bq_per_kg_FM: MDA for K-40 (FM).
- Cs-137_Bq_per_kg_FM: Cs-137 activity concentration in Bq/kg fresh mass.
- Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137 (FM).
- Cs-137_<: "<" marker for Cs-137 (FM).
- MDA_Cs-137_Bq_per_kg_FM: MDA for Cs-137 (FM).
- Cs-137_Concentration_Ratio_Fungi_FM: Concentration ratio (Fungi FM / soil DM) for Cs-137.
- Cs-137_Concentration_Ratio_Fungi_DM: Concentration ratio (Fungi DM / soil DM) for Cs-137.
- CR_Notes: Notes on concentration ratios.
- General_Notes: General notes for the dataset.

## Measurement Details and Coverage

- Isotopes: Potassium-40 (K-40) and Cesium-137 (Cs-137).
- Matrices: Fungi and soil, with separate entries for dry mass (DM) and fresh mass (FM) bases.
- Units and bases: Concentrations reported in Bq/kg for both DM and FM; mass-based calculations require explicit handling of fresh vs. dry mass.
- Data quality markers: Two-sigma counting errors accompany activity concentrations; MDAs indicate detection limits; less-than markers denote censored values.
- Ratio metrics: Concentration ratios comparing fungi to soil data for Cs-137, enabling assessment of bioaccumulation potential.

## Metadata, Provenance, and Data Governance

- Source and identifier: Data originates from the UKCEH Radiochemistry Laboratory (CEH_Sample_Identifier provided).
- Sampling context: Site and sampling date recorded; decay date anchored to sampling date for radiological interpretation.
- Metadata completeness: Several fields labeled as n/a or with notes, indicating potential gaps in metadata needs for full reuse.
- Data sharing considerations: The dataset includes explicit structures for underlying data and annotations (CR_Notes, General_Notes), but some metadata may require enhancement to support broad data sharing and governance.
- Data quality governance: Presence of counting errors, MDAs, and explicit "<" markers supports transparent uncertainty characterization and governance planning.

## Implications for Monitoring Frameworks

- Useful structure for monitoring frameworks aiming to scrutinize environmental radioactivity and bioaccumulation pathways in ecosystems.
- Demonstrates the need for:
  - Clear data dictionaries with explicit definitions, units, and bases (DM vs FM).
  - Consistent handling of detection limits and censored data (MDA, "<" markers).
  - Comprehensive metadata coverage (sample IDs, site details, dates, mass measurements, decay alignment).
  - Data quality metrics (uncertainties, counting errors) and provenance tracking.
  - Data governance considerations around data sharing, metadata completeness, and standardised reporting formats.
- Highlights potential barriers highlighted for framework authors:
  - Incomplete metadata and inconsistent unit bases may impede data reuse.
  - Need for standardized handling and documentation of "<" values and MDAs.
  - Importance of breaking data silos and ensuring open, well-documented data streams from radiochemical analyses.