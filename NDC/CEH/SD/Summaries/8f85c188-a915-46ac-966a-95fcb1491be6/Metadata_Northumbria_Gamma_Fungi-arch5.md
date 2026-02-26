# TREE_Northumbria_Gamma_Fungi

## Overview
- Dataset documenting gamma radiochemical measurements in fungi, with supporting data from soil, annotated for Northumbria (UKCEH Radiochemistry context).
- Core measurements include activity concentrations of K-40 and Cs-137, in both dry mass (DM) and fresh mass (FM), plus associated uncertainties and detection limits.
- Includes taxonomic (Latin species name), sample identifiers, sampling site, sample mass, and date information used for decay dating.
- Provides concentration ratios comparing fungi to soil and general notes on data handling.

## Data Model and Key Variables
- Latin_Species_Name: Latin species designation of the sampled fungi.
- CEH_Sample_Identifier: UKCEH Radiochemistry Lab unique sample ID.
- Site: Sampling site location.
- Mass_of_Sample_analysed_g: Mass of sample analysed (in grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken and used as the decay date.
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass for the soil/fungi sample.
- K-40_Bq_per_kg_DM: Activity concentration of K-40 in Bq per kg dry mass.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 (DM).
- K-40_<: Less-than indicator for K-40 concentration in DM.
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity of K-40 (DM).
- Cs-137_Bq_per_kg_DM: Activity concentration of Cs-137 in Bq per kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 (DM).
- Cs-137_<: Less-than indicator for Cs-137 concentration in DM.
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity of Cs-137 (DM).
- K-40_Bq_per_kg_FM: Activity concentration of K-40 in Bq per kg fresh mass.
- Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40 (FM).
- K40_<: Less-than indicator for K-40 concentration in FM.
- MDA_K-40_Bq_per_kg_FM: Minimum detectable activity of K-40 (FM).
- Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in Bq per kg fresh mass.
- Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137 (FM).
- Cs-137_<: Less-than indicator for Cs-137 concentration in FM.
- MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity of Cs-137 (FM).
- Cs-137_Concentration_Ratio_Fungi_FM: Concentration ratio of Cs-137 (fungi FM) relative to soil (FM).
- Cs-137_Concentration_Ratio_Fungi_DM: Concentration ratio of Cs-137 (fungi DM) relative to soil (DM).
- CR_Notes: Notes on concentration ratios.
- General_Notes: General notes about the dataset.

## Data Quality, Standards, and Interpretation
- Two-sigma counting errors accompany activity concentrations to convey measurement uncertainty.
- MDA (Minimum Detectable Activity) fields indicate detection limits for each measurement basis (DM and FM).
- Less-than markers (K-40_<, Cs-137_<) denote concentrations reported as below the detection threshold.
- Distinct DM (dry mass) and FM (fresh mass) reporting enables cross-comparison and proper normalization.
- Explicit metadata fields (Latin name, sample ID, site, date) support traceability and reproducibility.

## Provenance, Metadata, and Governance
- Data lineage centered on UKCEH Radiochemistry workflow, with clear sample identifiers and sampling context.
- Metadata supports reproducibility: species name, site, sample mass, and decay-date usage are recorded.
- Separate notes fields (CR_Notes, General_Notes) provide context for data interpretation and any limitations.

## Data Sharing, Access, and Updates
- Datasets are intended to be uploaded to relevant portals and catalogues, with dataset-level governance for updates.
- Documentation of work performed (quality assurance, cleaning, transformation) is implied through the dataset’s metadata structure and notes fields.

## Challenges and Risks for Data Stewards
- Incomplete understanding of user needs for multi-matrix (fungi vs soil) radiochemical data.
- Timely acquisition of samples and complete metadata from diverse sources.
- Ensuring metadata completeness (taxon, site, mass, date) and consistent units across DM and FM.
- Handling multiple systems and formats, including non-interoperable legacy databases.
- Managing large datasets with numerous detection-limit and uncertainty fields.
- Updating older databases to harmonize with current standards and ensure interoperability.

## Practical Recommendations for Data Stewards
- Enforce complete metadata capture: ensure Latin_Species_Name, CEH_Sample_Identifier, Site, Mass_of_Sample_analysed_g, Sampling_Date_Used_As_Decay_Date are filled for every record.
- Maintain clear documentation for DM vs FM measurements, including unit conventions and allowable values for MDAs and counting errors.
- Standardize handling of "<" threshold values and ensure downstream users can interpret MDAs correctly.
- Preserve and publish concentration ratio fields with transparent notes (CR_Notes, General_Notes) to aid interpretation.
- Establish robust provenance and change-tracking when datasets are updated or transformed.
- Align dataset with data governance policies to facilitate discoverability, accessibility, and reusability across portals.