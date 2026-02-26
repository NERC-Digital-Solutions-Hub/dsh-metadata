# Eco-physiological data collected at Alice Holt Forest from July 2023

## Overview
- Dataset of photosynthesis and gas exchange measurements collected at the Alice Holt Forest during a field campaign on photosynthesis and forest structure.
- Fieldwork conducted 18–20 July 2023, with leaf-level measurements taken only during the day.
- Data collected from a tower setup among two oak trees and hazel understory, using Handy PEA+ and LI-COR 6400 instruments.

## Data content
- Photosynthetic parameters (from a single CSV): F0, Fm, Fv/Fm, P_Index, Tfm, Intensity, P, and hierarchical identifiers (P, T, B, C) describing the spatial context (Platform, Tree, Branch, Leaf cluster).
- Gas exchange parameters (multiple CSVs): real-time metadata (HHMMSS, FTime), photosynthetic rate (Photo), conductance (Cond), intercellular CO2 (Ci), transpiration (Trmmol), vapor pressure deficit (VpdL), in-chamber leaf area (Area), stomatal ratio (StmRat), boundary layer conductance (BLCond), temperatures (Tair, Tleaf, TBlk), CO2 in reference and sample cells (CO2R, CO2S), water content (H20R, H20S), relative humidity (RH_R, RH_S), flow, light parameters (PARi, PARo), atmospheric pressure (Press), and quality indicators (StableF, Status).

## File formats and naming
- All files provided as CSV.
- Photosynthetic parameters: a single CSV file.
- Gas exchange files: named following 2023_07_DD_XXX_PX_BX_CX.csv, where Oak or Haz indicates the tree or understory measurement, and platform/branch/leaf-cluster are encoded (P, B, C). File naming conveys spatial/vertical context for mapping.
- Units provided for each parameter in the dataset documentation (e.g., Photo in μmol CO2 m^-2 s^-1, Ci in μmol CO2 mol^-1, etc.).

## Collection methods and instrumentation
- Sampling performed on a tower between two oak trees, spanning six platforms (P1–P6) at 2 m intervals.
- Leaves sampled from branch clusters (C) on branches (B); hazel understory sampled similarly.
- Measurements taken with Handy PEA+ and LI-COR 6400 instruments.

## Data organization and identifiers
- Hierarchical identifiers facilitate spatial referencing:
  - P: Platform
  - T: Tree
  - B: Branch
  - C: Leaf cluster
- File naming encodes tree context (Oak or Haz) and the precise spatial location (platform, branch, leaf cluster).

## Quality control and limitations
- Not all branches or leaf-clusters were measured; some branches were removed by wind between labelling and measurement, reducing sample completeness.
- Measurements represent daytime conditions and may reflect transient environmental factors during the campaign days.

## Measurement details by date (highlights)
- 18 July 2023: Multiple A/Ci measurements at various times starting mid-day.
- 19 July 2023: Oak measurements with A/Ci readings, using codes reflecting platform/branch/leaf cluster (e.g., Oak_P2_B1_C1; Oak_P2_B3_C1; Oak_P5_B1_C1, etc.).
- 20 July 2023: Hazeln understory and oak measurements with LRC (light response curves) and A/Ci measurements; several observations tagged with Obs Codes indicating specific platform/branch/leaf cluster combinations.

## GIS relevance and integration notes
- The dataset is inherently map-referenced through the identifiers P, T, B, and C, enabling linkage to spatial GIS layers (tower platforms, tree locations, branch structures, and leaf clusters).
- Parameters provide both static (structure-related) and dynamic (physiological) attributes suitable for spatial analyses of how physiology varies across microhabitats within the site.
- Suitable for creating spatially explicit maps of photosynthetic capacity and gas exchange responses when combined with site geometry and vegetation layers.

## Considerations for use
- Aligns with data integration workflows requiring curved or multi-resolution data by platform/branch/leaf cluster.
- Requires careful handling of missing measurements due to wind-related data gaps.
- Temporal scope is limited to three days in July 2023 and daytime measurements only; seasonal and diurnal variability should be considered when extrapolating beyond the dataset.