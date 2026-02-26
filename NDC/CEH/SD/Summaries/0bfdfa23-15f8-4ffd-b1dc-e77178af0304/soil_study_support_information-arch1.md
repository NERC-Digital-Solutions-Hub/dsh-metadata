# Colony forming units of Salmonella Typhimurium recovered from microplastics in two agriculturally relevant soils during persistence, leachate and sample transfer experiments.

## Aim
- Quantify the persistence and transfer potential of Salmonella enterica Serovar Typhimurium (S. Typhimurium) on microplastics and glass beads in two soils (podzol and loam).
- Explore leachate dynamics and transfer to virgin plastics under ambient and flooded conditions.
- Provide data suitable for modelling persistence, transfer, and decay (including R-squared, gradient, K, and D-values).

## Datasets and File Structure
- Four CSV files containing experimental data:
  - 20230619STyphimurium_persistence_soil_CFUs.csv — CFU concentrations during the persistence experiment.
  - 20230626STyphimurium_leachate_soil_CFUs.csv — CFUs in leachate and on plastics during leachate/flooding experiments.
  - 20230626STyphimurium_transfer_CFUs.csv — CFUs from the transfer experiment.
  - 20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv — results of linear decline analyses (R-squared, gradient, rate constants, D-values) across experiments.
- All data are provided in .csv format.
- File naming conventions reflect experiment type and analysis details (e.g., timepoints, gradients, and K/D values).

## Experimental Design and Materials
- Soils: Podzol and loam.
- Materials within jars: Microplastics and glass beads.
- Inoculum: S. Typhimurium colonising plastics or beads prior to soil introduction.
- Experimental setup:
  - Persistence: 120 g of soil per jar with beads/plastics; ambient room temperature; destructive sampling at multiple timepoints.
  - Leachate/flooding: flooding with water to simulate saturation; percolation of water through columns with plastics/beads; leachate collected and analyzed; final column dismantling to assess remaining biofilms.
  - Transfer: virgin plastics placed below contaminated materials to assess transfer to new surfaces.
- Replicates: Four replicates per timepoint.
- Timepoints:
  - Persistence: days 1, 2, 3, 4, 7, 10, 14, 21, 28, 35.
  - Leachate and transfer: measured at 7, 14, and 21 days (for CFUs in samples and leachate; transfer data includes timepoints up to 14 days).

## Measurements and Data Processing
- CFU quantification:
  - Biofilms detached from plastics/glass by resuspension in PBS and vortexing.
  - Serial dilutions plated on LB agar with chloramphenicol.
  - Incubation: 37°C for 24 h; colonies counted to determine CFU per g (persistence) or CFU per ml (transfer/leachate), with conversions to final concentrations (e.g., CFU per g or per ml).
- Data processing:
  - Raw CFU counts converted per dilution to final concentrations (e.g., 10 colonies at 100-fold dilution in 50 μL suspension → 5×10^4 CFU/ml).
  - Separate processing for persistence, leachate, and transfer components.
- Measured variables and units:
  - Sample_ID, Timepoint, Sample_type (CC = culture control; PE = polyethylene; GB = glass beads; P = podzol; L = loam).
  - Recovered material specifics: weight (g) of recovered plastics/soil; CFU counts per ml or per g; CFU_total per leachate volume or per total volume; recovered volume (ml) for CFU calculations.
  - Additional analytical descriptors in the R_squared_Gradient_K_value_D_value file: Rsquared, Gradient, K(day-1), D-value (days).
- Quality control notes:
  - Missing/NA values noted in transfer CSVs for samples recorded prior to mixing with soils (not considered colonised material and not part of CFU calculations).
  - Some sample_type entries in transfer data are NA for the first 16 samples, reflecting pre-mixing conditions.

## Temporal and Spatial Coverage
- Temporal: June–August 2023 (experiments conducted within this window).
- Spatial/Material scope: Two agriculturally relevant soils (podzol and loam) with microplastics and glass beads as colonisation substrates.

## Data Access and Documentation
- Data are published in the scientific article:
  Woodford, L., Fellows, R., White, H.L. et al. Survival and transfer potential of Salmonella enterica serovar Typhimurium colonising polyethylene microplastics in contaminated agricultural soils. Environmental Science and Pollution Research, 31: 5135351363 (2024). DOI: 10.1007/s11356-024-34491-4

## Key Considerations for Analysts
- Data enable analysis of persistence, leachate transfer, and surface-to-surface transfer under varying soil types and flood conditions.
- Data processing steps and units are explicit, allowing integration into models of bacterial survival and transfer in soils with microplastics.
- Be mindful of NA/missing values in transfer data and their pre-mixing context when performing cross-dataset analyses.