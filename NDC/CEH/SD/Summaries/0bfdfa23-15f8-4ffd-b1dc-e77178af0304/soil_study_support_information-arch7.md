# Colony forming units of Salmonella Typhimurium recovered from microplastics in two agriculturally relevant soils during persistence, leachate and sample transfer experiments.

## Overview
- A dataset of mesocosm experiments assessing Salmonella enterica Serovar Typhimurium persistence on microplastics and glass beads in podzol and loamy soil.
- Includes persistence, leachate, and transfer experiments with CFU counts after destruction sampling and through leachate collection.
- Four CSV files containing CFU data, plus a separate file with regression/kinetic metrics (R-squared, gradient, rate constants, and D-values).
- Data collected June–August 2023; four replicates per time point.

## Data files and structure
- 20230619STyphimurium_persistence_soil_CFUs.csv
  - CFU concentrations (CFU/g) for persistence experiments.
  - Columns include Sample_ID, Sample_type, Days, Weight (g), Concentration (CFU/g); includes podzol and loam, plastics (polyethylene) and glass beads.
- 20230626STyphimurium_leachate_soil_CFUs.csv
  - CFU data for leachate and associated experiments; includes Experiment (Persistence, Leachate, Transfer), Material (Plastic, culture, Glass), Replicate (1–4), soil_type (Podzol, Loam), Rsquared, Gradient, K(day-1), D-value (days), timepoints (Days 7–21).
- 20230626STyphimurium_transfer_CFUs.csv
  - CFU data for transfer experiments; includes sample_type (Bottom soil, colonised material, new material), Timepoint (Days 0–14), Weight (g), CFU_per_ml, CFU_per_g, CFU_total/leachate_volume; notes N/A for pre-colonisation values.
- 20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv
  - Statistical metrics for linear decline analyses across persistence, leachate, and transfer experiments (R^2, Gradient, K(day-1), D-value).

## Data content and variables
- Persistence (CSV): 
  - Sample_ID, Sample_type (CC, PE, GB; P= podzol, L = loam), Days (0–35), Weight (g), Concentration (CFU/g).
- Leachate (CSV): 
  - Experiment (Persistence, Leachate, Transfer), Material (Plastic, culture, Glass), Replicate (1–4), soil_type (Podzol, Loam), Rsquared, Gradient, K(day-1), D-value, timepoint (Days 7–21), plus material and sampling details.
- Transfer (CSV):
  - Sample_ID, Column_ID (CC, PE, GB; P= podzol, L = loam), Timepoint (Days 0–14), sample_type (Bottom soil, colonised material, new material), weight_(g), CFU_per_ml, CFU_per_g, CFU_per_total/leachate_volume.
- R-squared/Gradient/D-value file:
  - Contains regression metrics (e.g., Rsquared, Gradient, K(day-1), D-value) for the different experimental parts.

## Experimental design and methods
- Persistence: microplastics and glass beads placed in 120 g of podzol or loam; sampling at days 1, 2, 3, 4, 7, 10, 14, 21, 28, 35; beads retrieved, biofilm removed with PBS, serial dilutions plated on LB agar with chloramphenicol; CFUs counted after 24 h at 37°C.
- Leachate and transfer: flooding by adding water to simulate rainfall; leachate collected and CFUs quantified by serial dilution and plating; final column dismantling to assess remaining biofilm on plastics/glass; transfer assessed by checking virgin plastics below contaminated plastics for new colonisation.
- CFU calculation: colonies at a given dilution converted to CFU per ml or per g using standard dilution chemistry (e.g., 10 colonies at 100-fold dilution in 20 μL suspension yields 5×10^4 CFU/ml).

## Temporal and spatial scope
- Temporal: June–August 2023; persistence measurements across days 0–35; leachate and transfer measurements at days 7, 14, 21 (and related timepoints per experiment).
- Spatial/geographic: laboratory mesocosms using two soil types (podzol and loam); no geographic coordinates provided; data linked to soil type and material rather than field locations.

## Quality, provenance and limitations
- Some missing values noted:
  - In transfer data (first 16 samples), sample_type is N/A, recorded pre-mixing; documented in quality notes.
  - D2–D13 in the leachate/transfer CSVs show N/A where samples were recorded before colonisation.
- No explicit SOPs referenced; data captured as described and processed to derive CFU per ml/g from colony counts and dilutions.
- Data are associated with a published article: Woodford et al., 2024, Environmental Science and Pollution Research.

## GIS relevance and data integration notes
- Potential GIS applications:
  - Map CFU concentration by soil type (podzol vs loam) and material (polyethylene, glass beads) across timepoints.
  - Model transfer potential and persistence by soil type and moisture state (simulated flooding).
  - Integrate with soil property layers (pH, organic matter, texture) to assess risk contexts in agricultural soils.
- Considerations for GIS use:
  - Current data are lab-scale mesocosm results; geographic coordinates and in-field metadata are not included.
  - To enable spatial analyses, link to spatial soil maps and environmental layers, and add field- or site-level metadata (location, climate, soil properties).
  - Ensure unit consistency (CFU/g vs CFU/ml) when joining datasets and align timepoint references across files.
- Metadata requirements:
  - Clear definitions of sample_type codes (CC, PE, GB, P, L, etc.), timepoint interpretation, and replication scheme.
  - Documentation of dilution factors used to compute CFU per ml/g for reproducibility in mapping or modeling.

## Source and access
- Data published in Woodford, L. et al. Survival and transfer potential of Salmonella enterica serovar Typhimurium colonising polyethylene microplastics in contaminated agricultural soils. Environmental Science and Pollution Research (2024). DOI: 10.1007/s11356-024-34491-4
- Data format: CSV files; no additional SOP documentation included within the dataset description.