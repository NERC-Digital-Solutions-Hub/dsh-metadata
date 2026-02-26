# Survival and transfer potential of Salmonella Typhimurium and Vibrio cholerae colonising plastic mulch onto basil and spinach salad leaves

- Objective and relevance
  - Assess whether Salmonella Typhimurium (S. Typhimurium) and Vibrio cholerae can transfer from plastic mulch plastisphere to ready-to-eat basil or spinach leaves and persist on leaf surfaces.
  - Evaluate implications for food safety as plastic mulches become more common in intensive agronomic systems.

- Experimental design (overview)
  - Basil and spinach leaves placed in petri dishes with wet cotton pads; leaves oriented adaxial or abaxial.
  - Materials (plastic mulch, hay, or culture) applied to leaf surfaces and incubated.
  - Timepoints: 0, 1, 2, 3, 4, 7, 10, 14 days; four replicates per timepoint.
  - Sampling included negative controls (leaves with no bacteria).
  - Three analysis components:
    - Endophytic: bacteria recovered from leaf interior after surface sterilization.
    - Epiphytic: bacteria recovered from leaf surface washes.
    - Persistence: bacteria recovered from plastic, hay, or culture materials.
  - Processing: wash and serial dilutions, plating on LB agar with chloramphenicol, incubation at 37°C for 24 h; CFU counts reported.

- Data collection and processing (summary)
  - Data recorded as CFU counts; converted to concentrations per ml, per leaf, or per sample as appropriate.
  - All data documented in CSV format; raw data processed to final CFU metrics.
  - Quality control: no missing data points; zeros indicate no colonies recovered.

- Key findings
  - Both S. Typhimurium and V. cholerae persisted on plastic mulch for up to 14 days.
  - Within 24 hours, both pathogens could dissociate from plastic surface and transfer to the surfaces of both basil and spinach leaves.
  - Implication: removal of adherent plastics and washing of ready-to-eat crops may not completely remove these pathogens, highlighting contamination risk in plastic-mulch–based systems.

- Datasets and file descriptions (CSV format)
  - Cholera_Endophytic_CFUs.csv
    - Data: concentrations of recovered Cholera from endophytic leaf tissues (CFU per leaf or per ml equivalents).
  - Cholera_epiphytic_CFUs.csv
    - Data: concentrations of recovered Cholera on leaf surfaces (epiphytic CFU per leaf or per ml equivalents).
  - Cholera_persistence_plastic_hay_CFUs.csv
    - Data: CFU recovered from plastic mulch, hay, or culture materials (persistence component).
  - Salmonella_Endophytic_CFUs.csv
    - Data: concentrations of recovered Salmonella from endophytic leaf tissues.
  - Salmonella_Epiphytic_CFUs.csv
    - Data: concentrations of recovered Salmonella on leaf surfaces.
  - Salmonella_persistence_plastic_hay_CFUs.csv
    - Data: Salmonella CFU data for persistence on plastic mulch and hay.
  - STyphimurium_R_squared_Gradient_K_value_D_value.csv
    - Data: linear decline analysis for S. Typhimurium; includes material (plastic, hay, culture), plant_type (basil/spinach), leaf_surface (adaxial/abaxial), Rsquared, Gradient, K (per day), D-value (days).

- Variables and units (highlights)
  - Sample_ID: composite code (plant, material, leaf surface, timepoint, replicate).
  - timepoint_days: sampling day (0, 1, 2, 3, 4, 7, 10, 14).
  - Colonies: CFU counts on media.
  - CFU_per_leaf, CFU_per_ml, CFU_per_mm2: derived bacterial concentrations as appropriate.
  - Dilution: 10-fold dilution factor used for plating.
  - Replicate: 1–4 replicates per condition.

- Temporal coverage and collection context
  - Experiments conducted between October and November 2023.
  - Data published from a study by Woodford et al. (2024) in Heliyon (DOI: 10.1016/j.heliyon.2024.e31343).

- Methodological notes and scope
  - No SOPs referenced; all sampling and analysis conducted within the described framework.
  - Colony counts used to quantify bacterial presence; both endophytic and epiphytic compartments were analyzed.
  - Data processing included converting CFU counts to standardized concentration metrics; all data reported as CFU counts.

- Publication and data availability
  - Data accompanying the scientific article: Woodford L, Fellows R, White HL, et al. 2024. Salmonella Typhimurium and Vibrio cholerae can be transferred from plastic mulch to basil and spinach salad leaves. Heliyon 10:e31343. DOI: 10.1016/j.heliyon.2024.e31343.