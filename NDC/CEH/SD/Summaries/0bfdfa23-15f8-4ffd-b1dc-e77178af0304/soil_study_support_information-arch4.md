# Colony forming units of Salmonella Typhimurium recovered from microplastics in two agriculturally relevant soils during persistence, leachate and sample transfer experiments

## Overview
- A dataset from mesocosm experiments examining the persistence of Salmonella enterica Serovar Typhimurium (S. Typhimurium) on microplastics and glass beads in two soils (podzol and loam).
- Includes persistence, leachate, and transfer experiments with flooding conditions to assess transfer potential and leachate gradients.
- Data collection occurred June–August 2023; four replicates per time point; timepoints range from days 1–35 (persistence) and 7–21 days (leachate/transfer).

## Data Content and Structure
- Four CSV data files:
  - 20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv
  - 20230626STyphimurium_leachate_soil_CFUs.csv
  - 20230619STyphimurium_persistence_soil_CFUs.csv
  - 20230626STyphimurium_transfer_CFUs.csv
- Recorded values and descriptions:
  - Persistence: concentrations of S. Typhimurium on plastic/glass in podzol or loam; CFU/g and related samples at multiple days.
  - Leachate: CFUs in leachate and on materials under ambient and flooded conditions; includes transfer potential to virgin plastics.
  - Transfer: CFUs in bottom soil, colonised materials, and virgin materials; includes recovered CFU per ml and per g.
- Units and data shapes:
  - CFU/g, CFU/ml, CFU_total/leachate_volume, etc.
  - Timepoints: days 0–35 for persistence; 7–21 days for leachate and transfer.
  - Replicates: 1–4.
  - Sample/material types: culture control (CC), polyethylene (PE), glass beads (GB); soils P (podzol), L (loam).
- Data processing note:
  - CFU counts converted from colonies at dilutions to final concentrations per ml or g (e.g., 10 colonies at 100-fold dilution in 50 μL suspension -> 5×10^4 CFU/ml).
- Data quality notes:
  - Some N/A entries explained by sampling/recording process (e.g., pre-colonisation status or start-of-experiment measurements).

## Experimental Design and Methods
- Persistence experiment:
  - Microplastics/glass beads inoculated with S. Typhimurium and embedded in 120 g of podzol or loam soil.
  - Destructive sampling at days 1, 2, 3, 4, 7, 10, 14, 21, 28, 35; beads retrieved, biofilm removed, samples resuspended in PBS, serial dilutions plated on LB-chloramphenicol.
- Leachate and flooding experiment:
  - Flooding simulated by adding water to soil columns; leachate collected and CFUs quantified; plastic/glass analyzed at final timepoint.
  - Transfer assessment: virgin plastics positioned below contaminated plastics; post-experiment analysis to determine transfer of S. Typhimurium to virgin plastics.
- Transfer experiment specifics:
  - Timepoints up to 14 days; includes bottom soil, colonised material, and new material (virgin plastics).
- Sampling and analysis workflow:
  - Destructive sampling for persistence; non-destructive leachate sampling with subsequent destructive analysis of solids; standard plating on selective media for CFU enumeration.

## Temporal and Spatial Coverage
- Temporal:
  - Persistence: days 1–35.
  - Leachate and transfer: days 7–21 (leachate) and up to 14 days (transfer) with multiple replicates.
- Spatial:
  - Soils: podzol (P) and loam (L).
  - Materials: polyethylene (P), glass beads (GB), and culture control (CC) conditions.

## Data Processing, Quality Control, and Provenance
- Data processing:
  - CFU counts converted to per ml or per g metrics; documentation includes example calculation method.
- Quality control:
  - Noted missing/NA values are tied to sampling stages (e.g., starting samples not recovered, or pre-colonisation statuses).
  - Some N/A in transfer dataset reflect values recorded before column mixing and thus not applicable to certain columns.
- Provenance:
  - Data linked to published article: Woodford et al. Survival and transfer potential of Salmonella enterica serovar Typhimurium colonising polyethylene microplastics in contaminated agricultural soils (Environ Sci Pollut Res, 2024). DOI provided.

## Relevance for Data Leadership and Governance
- Data scope supports assessment of microbial persistence and transfer risk in agricultural settings, aiding risk management and policy considerations.
- Repository highlights:
  - Clear file naming, unit definitions, and metadata descriptions to support discoverability and reuse.
  - Comprehensive documentation of experimental design, sampling regime, and data transformation steps.
- Considerations for adoption and integration:
  - Assess alignment with data strategy for environmental microbiology datasets (metadata standards, ontologies, and data quality protocols).
  - Ensure consistent metadata to enable cross-study comparisons (soil type, material type, sampling scheme, growth conditions, and plating methods).
  - Plan for long-term data stewardship, including archiving of raw CFU counts and derived concentrations.