# Colony forming units of Salmonella Typhimurium recovered from microplastics in two agriculturally relevant soils during persistence, leachate and sample transfer experiments.

## Overview
- Quantifies persistence of Salmonella enterica Serovar Typhimurium (S. Typhimurium) on microplastics and glass beads in two soils (podzol and loamy soil) under persistence, leachate, and transfer conditions.
- Measures surviving CFUs after destructive sampling of mesocosm jars; includes a flooding/transfer scenario with leachate gradients and transfer potential to virgin plastics.
- Experiments run June–August 2023 with multiple replicates and timepoints.

## Data content and structure
- Four CSV data files containing:
  - Persistence: concentrations of recovered S. Typhimurium during the persistence experiment.
  - Leachate: CFUs recovered from leachate and related samples.
  - Transfer: CFUs recovered during transfer experiments.
  - An additional file with R-squared, gradient, K (day^-1), and D (decimal reduction time) values for linear decline analyses across experiments.
- Data cover three experimental parts: persistence, leachate, and transfer; with soil types Podzol (P) and Loam (L); materials plastic (P), polyethylene (PE), and glass beads (GB).
- Replicates 1–4; timepoints include days 1–35 for persistence and days 7–21 for leachate/transfer, plus 0–14 days for transfer timepoints.

## File formats and naming
- All files are CSV (.csv).
- File names:
  - 20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv
  - 20230626STyphimurium_leachate_soil_CFUs.csv
  - 20230619STyphimurium_persistence_soil_CFUs.csv
  - 20230626STyphimurium_transfer_CFUs.csv

## Variables and units
- Key data columns include:
  - Sample_ID, Sample_type (CC, PE, GB), soil type (P, L), timepoints (days), replicate.
  - Recovered weight (g); CFU_per_ml; CFU_per_g; CFU_total/leachate_volume.
  - For leachate/transfer data: timepoint (days 0–21 or 0–14), column/material type, recovered volumes, and CFU counts.
  - Additional regression metrics: Rsquared, Gradient, K (day^-1), D-value (days).
- Notes on data values:
  - Some cells are marked N/A due to sampling specifics (e.g., starting samples, dilution contexts).
  - Data units include CFU per mL or per g; volumes in mL or g as applicable.

## Experimental design and collection methods
- Persistence experiment:
  - Plastic and glass beads colonised with S. Typhimurium mixed into 120 g of podzol or loam soil in glass jars; sampled at multiple days; beads removed, biofilm dissolved in PBS, then serially diluted and plated on LB agar with chloramphenicol.
- Leachate/flooding experiment:
  - Water added to columns to simulate flooding; leachate collected and serially diluted/plated; final column dismantling to assess remaining biofilm on plastics/glass.
- Transfer experiment:
  - Virgin plastics placed below contaminated plastics; after mixing, transfer of S. Typhimurium to virgin plastics assessed by analyzing washed, newly formed biofilms.
- Data processing:
  - Colony counts converted to final CFU per mL or per g using dilution math (example provided in documentation).

## Temporal and geographic scope
- Temporal coverage: June–August 2023; sampling times span up to 35 days in persistence, with 7–21 days for leachate and transfer components.
- Geographic scope: not explicitly stated; soils are podzol and loamy soils described as agriculturally relevant.

## Quality control and metadata considerations
- Data notes:
  - Missing or N/A values documented where appropriate (e.g., early transfer samples prior to colonisation).
  - A quality control note explains missing sample_type values in the transfer CSV prior to mixing materials.
- Documentation context:
  - No SOPs referenced; sampling and analysis conducted in 2023; raw CFU data processed to per-volume/ per-mass concentrations.
- Provenance:
  - Data linked to a published article: Woodford et al. 2024, Environmental Science and Pollution Research, with DOI provided.

## Data governance, sharing, and reuse considerations for Data Stewards
- Data structure is clear and machine-readable (CSV) with explicit file naming and documented variable descriptions.
- Metadata coverage:
  - Described soils, materials, timepoints, replicates, and measurement method; however, some contextual metadata (e.g., full SOPs, storage conditions, embargo status) are not present.
- Reproducibility and interoperability:
  - Detailed calculation example for converting CFU counts to concentrations; regression metrics provided for cross-experiment analyses.
- Accessibility and licensing:
  - Dataset is associated with a peer-reviewed publication; ensure repository-level metadata and licensing are explicit for reuse.
- Recommendations for stewardship:
  - Include a complete data dictionary (with all variable definitions, units, and allowed values).
  - Add clear provenance, storage, and any embargo or access restrictions.
  - Consider linking to the associated publication DOI and providing a stable access point or DOI for dataset.
  - Ensure availability of SOPs or a concise methods appendix to support reuse and replication.

## Related publication and provenance
- Published article: Woodford, L., Fellows, R., White, H.L. et al. Survival and transfer potential of Salmonella enterica serovar Typhimurium colonising polyethylene microplastics in contaminated agricultural soils. Environ Sci Pollut Res 31, 513-536 (2024). DOI: 10.1007/s11356-024-34491-4.