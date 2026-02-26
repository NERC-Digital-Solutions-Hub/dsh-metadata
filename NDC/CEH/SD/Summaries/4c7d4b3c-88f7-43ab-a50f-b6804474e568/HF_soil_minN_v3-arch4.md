# Details of data structure to ' HF_soil_minN.csv '

## Overview
- Supplement to the supporting documentation for data series referenced as Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Describes the structure and contents of HF_soil_minN.csv.
- Dataset: 11 columns, 608 rows.
- Contains soil NH4-N and NO3-N + NO2-N concentrations, soil moisture contents, soil pH, and electrical conductivity (EC).
- Source: grassland fertiliser trial 2016, Henfaes Research Station (Bangor University).

## Dataset structure and contents
- For each observation (row):
  - Date: Sampling date.
  - N_app: 1, 2, or 3 denotes fertiliser application occasions.
    - 1st & 2nd applications: 90 kg ha^-1
    - 3rd application: 60 kg ha^-1
  - Block: 1–4, randomized block design.
  - Plot: 1–16, plot sampled.
  - Treatment: AN, U, IU, C
    - AN = ammonium nitrate
    - U = urea
    - IU = inhibited urea (Agrotain)
    - C = 0N control
  - Soil_NH4_mgNkg: ammonium concentration in soil (mg NH4-N kg^-1), dry weight basis.
  - Soil_NO3_mgNkg: nitrate concentration in soil (mg NO3-N kg^-1), dry weight basis.
  - moisture_dry: soil moisture on a dry weight basis (g H2O g dry soil^-1).
  - moisture_wet: soil moisture on a wet weight basis (g H2O g wet soil^-1).
  - pH: soil pH.
  - EC: soil electrical conductivity (µS cm^-1).

## Data collection methods and units
- Sampling: soil 0–10 cm depth using a 1 cm diameter corer; 6 samples per plot were collected and bulked.
- Extraction: 5 g soil extracted with 25 ml 0.5 M K2SO4, shaken 30 min at 200 rpm.
- Chemical analyses:
  - Nitrate (NO3-N): colorimetric method (Miranda et al., 2001).
  - Ammonium (NH4-N): method (Mulvaney, 1996).
- Moisture: determined by drying at 105°C for 24 hours.
- pH and EC: measured with standard electrodes using a 1:2.5 soil to deionised water suspension.

## Experimental design and site context
- Site: Henfaes Research Station, Bangor University.
- Experiment: grassland fertiliser trial conducted in 2016.
- Design features: randomized block design with 4 blocks; 16 plots per block? (plots numbered 1–16 per description) and treatments assigned across plots within blocks.

## Data provenance and supporting documentation
- This dataset and its structure are described as a supplement to a broader data series documentation.
- Full context, data checks, and related series are referenced in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.

## Implications for data leadership and governance
- Data completeness and standardization:
  - 11 columns, 608 rows; ensure consistent unit conventions (dry weight basis for NH4-N and NO3-N; moisture units).
  - Metadata should capture sampling date, block, plot, treatment, and N_app details for traceability.
- Data quality and interoperability:
  - Document measurement methods and reference protocols (Miranda et al., Mulvaney; 0.5 M K2SO4 extraction; 105°C drying) to support cross-dataset compatibility.
  - Be mindful of unit consistency when integrating with other soil datasets (e.g., moisture basis, EC units).
- Data discoverability and reuse:
  - Link this dataset to the broader CINAg experiments documentation and any other fertility or soil-chemistry datasets from the same trial.
  - Provide data dictionary and lineage to support reuse in policy-relevant or modelling work across networks.
- Potential analyses:
  - Assess effects of fertiliser type and application schedule on soil N forms, moisture, pH, and EC.
  - Compare across blocks and plots to evaluate spatial variability within the field trial.
- Gaps and next steps:
  - If needed, seek additional metadata (e.g., GPS coordinates of plots, weather during sampling) to enhance contextual understanding and cross-site comparability.