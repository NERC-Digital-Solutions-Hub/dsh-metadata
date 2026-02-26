# Survival and transfer potential of Salmonella Typhimurium and Vibrio cholerae colonising plastic mulch onto basil and spinach salad leaves

## Overview
- Investigates whether Salmonella Typhimurium (S. Typhimurium) and Vibrio cholerae can transfer from plastisphere on plastic mulch to basil and spinach leaves and persist on leaf surfaces.
- Demonstrates persistence on plastic mulch on leaves for up to 14 days and transfer to leaf surfaces within 24 hours, posing food-safety risks even after plastic removal or washing.
- Highlights urgency of understanding co-pollutant pathogen risks in agricultural systems with increasing plastic mulch use.

## Datasets and structure
- Seven CSV files containing bacterial measurements related to endophytic, epiphytic, and plastic-hay persistence, plus a dataset for linear decline analysis.
  - Cholera_Endophytic_CFUs.csv
  - Cholera_epiphytic_CFUs.csv
  - Cholera_persistence_plastic_hay_CFUs.csv
  - Salmonella_Endophytic_CFUs.csv
  - Salmonella_Epiphytic_CFUs.csv
  - Salmonella_persistence_plastic_hay_CFUs.csv
  - STyphimurium_R_squared_Gradient_K_value_D_value.csv
- Key variables and units:
  - Sample_ID encodes plant type (B/S), material (PE/GR/CO: plastic, hay/grass, culture), leaf surface (A/B), timepoint (days), and replicate.
  - Timepoint in days (0–14).
  - Colonies (CFU) and CFU_per_leaf/CFU_per_ml/CFU_per_mm2, including dilution factors.
  - For STyphimurium dataset: material (Plastic, hay, culture); plant_type (Basil/Spinach); leaf_surface (Adaxial/Abaxial); Replicate; Rsquared; Gradient; K(day-1); D-value (days).

## Experimental design and methods
- Basil and spinach leaves placed in petri dishes with wet cotton pads; materials applied to leaf surfaces (adaxial/abaxial) and left for sampling.
- Sampling on days 0, 1, 2, 3, 4, 7, 10, 14; four replicates per timepoint.
- Materials analyzed by washing leaves with PBS, diluting, and plating on LB agar with chloramphenicol; CFU counted after 24 h at 37°C.
- Endophytic samples: leaves washed with PBS, then ethanol wash, leaf crushing, resuspension, and plating.
- Negative controls included; no samples missing; data reported as CFU counts.
- Quality control notes: no SOPs referenced; no data adjustments; zeros indicate no colonies.

## Key findings
- S. Typhimurium and V. cholerae persisted on plastic mulch on leaf surfaces for up to 14 days.
- Both pathogens transferred from plastic mulch to basil and spinach leaf surfaces within 24 hours.
- Implication: removal of plastic or washing leaves may not fully eliminate these pathogens, elevating food-safety concerns in plastic-mulch–based farming.

## Temporal and experimental scope
- Experiments conducted October–November 2023.
- Timepoints include 0, 1, 2, 3, 4, 7, 10, 14 days across all three experimental parts (material persistence, epiphytic, endophytic).
- Four replicates per combination; data points complete across all timepoints.

## GIS and mapping implications
- Data are structured to support temporal, material-type, plant-type, and leaf-surface analyses; suitable for creating:
  - Time-series risk maps of pathogen transfer and persistence linked to mulch material, plant type, and leaf surface.
  - Spatially explicit risk surfaces if linked to field coordinates or plots (not provided in dataset but feasible to attach).
  - Layered visualizations showing endophytic vs. epiphytic vs. plastic-hay CFU distributions over time.
- Variables (CFU counts per leaf/ml/mm2, timepoints, and material type) enable aggregation by scenario to support policy and operational decision-making in produce safety.

## Data quality and metadata
- All data points present; no missing data reported.
- Negative results explicitly captured as zeros.
- Data are raw CFU counts converted to concentrations per ml or per leaf; no adjustments noted.
- Documentation includes detailed sample coding and measurement procedures; linked to a published Heliyon article (2024).

## Data availability and references
- Data published in:
  - Woodford L, Fellows R, White HL, Ormsby MJ, Quilliam RS (2024) Salmonella Typhimurium and Vibrio cholerae can be transferred from plastic mulch to basil and spinach salad leaves. Heliyon 10:e31343. https://doi.org/10.1016/j.heliyon.2024.e31343
- File naming and contents provided above; CSV format for all datasets.