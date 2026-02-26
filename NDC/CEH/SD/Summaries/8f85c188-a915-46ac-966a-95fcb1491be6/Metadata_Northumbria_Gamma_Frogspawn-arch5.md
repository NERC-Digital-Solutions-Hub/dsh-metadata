# TREE_Northumbria_Gamma_Frogspawn

## Summary at a glance
- Metadata-rich radiochemical dataset describing frogspawn samples from Northumbria, focusing on K-40 and Cs-137 activity.
- Captures both dry mass (DM) and fresh mass (FM) activity concentrations, associated uncertainties, and detection limits.
- Includes sample identifiers, species, sampling site, and sample descriptions; notes use of sampling date as decay date.
- Provides concentration ratios between frogspawn and other media, plus notes on how to interpret "<" (below detection) values.

## Data content and structure
- Biological and sampling metadata
  - Latin_Species_Name; Common_Species_Name
  - Site; CEH_Sample_Identifier; CEH_Sample_Description
  - Sampling_Date_Used_As_Decay_Date
- Mass measurements
  - Dry_Mass_Of_Sample_Analysed_g (grams)
- K-40 measurements
  - K-40_Bq_per_kg_DM; Counting_Error_K-40_Bq_per_kg_DM; K-40_<; MDA_K-40_Bq_per_kg_DM
  - K-40_Bq_per_kg_FM; Counting_Error_K-40_Bq_per_kg_FM; K-40_<; MDA_K-40_Bq_per_kg_FM
- Cs-137 measurements
  - Cs-137_Bq_per_kg_DM; Counting_Error_Cs-137_Bq_per_kg_DM; Cs-137_DM_<; MDA_Cs-137_Bq_per_kg_DM
  - Cs-137_Bq_per_kg_FM; Counting_Error_Cs-137_Bq_per_kg_FM; Cs-137_FM_<; MDA_Cs-137_Bq_per_kg_FM
- Detection limits and qualifiers
  - MDA_K-40_Bq_per_kg_DM; MDA_K-40_Bq_per_kg_FM; MDA_Cs-137_Bq_per_kg_DM; MDA_Cs-137_Bq_per_kg_FM
  - < markers indicate values below the specified MDA
- Cs-137 concentration ratios
  - Cs-137_Concentration_Ratio_DM; Cs-137_Concentration_Ratio_FM
  - Cs-137_Concentration_Ratio_DM, FM_<; Notes_Related_To_Cs-137_Concentration_Ratio
- Explanatory notes
  - Clarifications on the interpretation of concentration ratios and related notes

## Measurement details and units
- Isotopes measured: K-40 and Cs-137
- Units used
  - Bq per kg DM (dry mass)
  - Bq per kg FM (fresh mass)
  - Mass: grams (g)
- Data qualifiers
  - Counting Error fields provide two-sigma uncertainties
  - Not measured values indicated where applicable
  - MDA fields indicate minimum detectable activity
- Concentration ratios
  - Ratios compare frogspawn activity to reference media (e.g., filtered water)
  - DM vs FM ratios provided, with corresponding "<" qualifiers where applicable

## Data governance and sharing considerations
- Dataset appears to be designed for cataloguing and sharing within radiochemical and ecological data portals
- Rich metadata supports discovery, provenance, and reuse (sample identifiers, descriptions, and mass measurements)
- Clear handling of detection limits and measurement uncertainties aids reproducibility and data quality
- Emphasis on documentation of transformations or calculations when deriving concentration ratios

## Data quality considerations and challenges
- Handling of incomplete user needs and ensuring the dataset meets those needs
- Ensuring timely data provision from data creators
- Consistency across many fields, especially between DM and FM measurements and their qualifiers
- Managing multiple measurement formats and units
- Large data volumes and potential legacy database constraints requiring bespoke solutions

## Recommendations for Data Stewards
- Validate completeness of essential metadata (species, site, sample identifiers, decay date, mass, and both isotope measurements)
- Enforce consistent units and clear documentation of DM vs FM for all samples
- Track and document data transformations leading to concentration ratios
- Explicitly capture and communicate < and MDA values to users and downstream systems
- Maintain update workflows to reflect new samples and revised measurements; document provenance and QA steps
- Develop clear guidance for data creators on metadata standards and measurement reporting to reduce interoperability issues
- Plan for data access controls and update mechanisms, especially if embargoes or restricted data apply