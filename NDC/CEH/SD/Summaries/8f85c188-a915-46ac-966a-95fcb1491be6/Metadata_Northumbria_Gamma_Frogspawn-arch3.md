# TREE_Northumbria_Gamma_Frogspawn

## Purpose and scope
- A dataset of radiochemical measurements in Northumbria frogspawn, focusing on potassium-40 (K-40) and cesium-137 (Cs-137).
- Designed to support environmental health monitoring, policy scrutiny, and decision-making by providing activity concentrations in tissue and derived ratios.

## Dataset structure and key fields
- Biological and sampling metadata
  - Latin_Species_Name, Common_Species_Name
  - Site (sampling site)
  - CEH_Sample_Identifier (UKCEH unique sample identifier)
  - CEH_Sample_Description (UKCEH Radiochemistry Laboratory sample description)
  - Sampling_Date_Used_As_Decay_Date (date used as decay date)
  - Dry_Mass_Of_Sample_Analysed_g (dry mass in grams)

- Activity concentrations (per mass)
  - K-40_Bq_per_kg_DM (activity concentration of K-40 in Bq/kg dry mass)
  - K-40_Bq_per_kg_FM (activity concentration of K-40 in Bq/kg fresh mass)
  - Cs-137_Bq_per_kg_DM (activity concentration of Cs-137 in Bq/kg dry mass)
  - Cs-137_Bq_per_kg_FM (activity concentration of Cs-137 in Bq/kg fresh mass)

- Measurement quality and detection limits
  - Counting_Error_K-40_Bq_per_kg_DM / Counting_Error_K-40_Bq_per_kg_FM
  - Counting_Error_Cs-137_Bq_per_kg_DM / Counting_Error_Cs-137_Bq_per_kg_FM
  - MDA_K-40_Bq_per_kg_DM / MDA_K-40_Bq_per_kg_FM (minimum detectable activity for K-40)
  - MDA_Cs-137_Bq_per_kg_DM / MDA_Cs-137_Bq_per_kg_FM (minimum detectable activity for Cs-137)
  - K-40_< / Cs-137_DM_< / Cs-137_FM_< / K-40_FM_< (indicators when concentrations are below detection)

- Derived concentration ratios
  - Cs-137_Concentration_Ratio_DM (Cs-137 concentration ratio per DM)
  - Cs-137_Concentration_Ratio_FM (Cs-137 concentration ratio per FM)
  - Cs-137_Concentration_Ratio_DW_<, FM_< (non-detect indicators for concentration ratios)

- Notes and context
  - Notes_Related_To_Cs-137_Concentration_Ratio (general notes on Cs-137 concentration ratios)

## Units and measurement notes
- DM = dry mass; FM = fresh mass
- Concentrations reported in Bq per kg (DM or FM)
- MDAs indicate the smallest activity reliably detectable; “<” values denote non-detects
- Two-sigma counting error provided for quality context

## Data quality, limitations, and interpretation
- Non-detects and MDAs require careful interpretation in trend analysis and policy reporting
- Some fields indicate missing or not measured data; transformation or metadata may be needed for full verification
- Data require appropriate metadata management and transparent data sharing to support governance

## Data provenance and governance considerations for monitoring frameworks
- Provenance elements include CEH_Sample_Identifier and CEH_Sample_Description, linking to UKCEH Radiochemistry Laboratory processes
- Decay-date alignment via Sampling_Date_Used_As_Decay_Date supports time-adjusted radiological assessments
- Clear documentation of units, detection limits, and measurement errors supports reproducibility and transparency

## How this supports monitoring and policy decisions
- Provides tissue-based radiological concentration data (K-40, Cs-137) to inform environmental risk assessments and regulatory decisions
- Enables calculation of Cs-137 concentration ratios between frogspawn and water, aiding understanding of transfer pathways
- Supports evaluation of data quality, gaps, and the need for metadata standards and governance measures in monitoring frameworks