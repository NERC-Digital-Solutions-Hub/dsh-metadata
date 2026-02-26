# Soil_C_budgets_to_depth.csv

## Overview
- A dataset describing soil carbon and nitrogen budgets to depth, based on multi-site sampling using a consistent laboratory workflow.
- Data are organized by land use, site, replicate, soil level, and depth increments, with derived carbon and nitrogen stocks reported per hectare.

## Sampling and Laboratory Methods
- Soil sampling
  - Two soil samples per site using a 4 cm width auger, collected to the deepest practical depth.
  - Samples sieved with a 2 mm aperture to remove stones and roots.
  - Stones >2 cm weighed to determine gravel content.
  - Cores split into 5 cm depth increments; dried at 80 °C for 48 hours after sieving; stored at 25 °C until processing.

- Bulk density (BD)
  - BD calculated as mass divided by volume.
  - Gravel is accounted for by adjusting BD: Adjusted BD = Unadjusted BD × (1 − %gravel/100).

- Carbon and nitrogen analysis
  - Each depth fraction is ground (ball mill, 25 s⁻¹ for 2 minutes).
  - Carbonates removed with 37% HCl; samples redried.
  - Approximately 10 mg samples combusted in a Vario EL analyser, calibrated with acetanilide (10.45% N, 71.4% C).
  - Stocks calculated per depth using: CN post-acid, and C post-acid/N post-acid.

- Calculations for stocks
  - Carbon and nitrogen stocks per depth: C_t ha and N_t ha derived using core depth, 0–100 scale, corrected BD, and raw %C/%N.

## Data Quality and Control
- Quality control
  - Standards and blanks run every 20 samples on the combustion analyser.
  - 5% analytical replicates included to assess precision.

## Data Structure and Metadata (Soil_C_budgets_to_depth.csv)
- Data columns and definitions
  - Land Use: Type of land use.
  - Site: Site identifier.
  - Replicate: Replicate number (1 or 2).
  - Soil level: Top, middle, or bottom of the soil column.
  - Soil Depth from surface: Depth from surface (in 5 cm increments where possible).
  - Core depth: Length of the core (not always 5 cm increments if conditions prevented it).
  - Core diameter: Diameter of the auger.
  - Core volume: π r² h, total core volume.
  - Dry wt: Dry soil weight for the increment.
  - Gravel wt: Weight of stones >2 cm diameter.
  - %gravel: Proportion of core volume constituted by gravel.
  - Bulk density with gravel: BD including gravel.
  - BD corrected for gravel: BD adjusted to exclude gravel impact.
  - N post acid: Total nitrogen after carbonate removal.
  - C post acid: Total carbon after carbonate removal.
  - C_t ha: Carbon stock (tonnes per hectare).
  - N_t ha: Nitrogen stock (tonnes per hectare).
  - CN post acid: Carbon-to-nitrogen ratio after acid treatment.

## Data Governance Considerations for Data Stewards
- Standardization and metadata
  - Ensure consistent depth increments (5 cm where possible) and clear documentation of any deviations from 5 cm increments.
  - Maintain clear units and calculation methods for BD, post-acid measurements, and stock calculations.
  - Preserve metadata on sampling depth, core depth, and soil level (top/middle/bottom) to support reproducibility.

- Documentation and provenance
  - Record laboratory methods (milling frequency, HCl treatment, calibration standard, analyser model) for traceability.
  - Document all data processing steps used to derive C_t ha and N_t ha from raw C/N percentages and BD.

- Data quality and validation
  - Retain quality-control results (standards, blanks, replicates) to enable independent assessment of accuracy and precision.
  - Flag any anomalies due to incomplete cores, missing increments, or measurement deviations.

- Data formats and interoperability
  - Use a clear, machine-readable CSV structure with explicit data definitions (as provided in the data dictionary).
  - Ensure consistent field naming to support cross-dataset integration and portal cataloguing.

- Sharing, stewardship, and updates
  - Plan for versioning and updating the dataset as new data are collected or methods are refined.
  - Respect data sharing constraints and disclose any limitations or embargo periods that may apply to specific fields or sites.

## Potential Challenges for Data Stewards
- Incomplete depth data
  - Some cores may not be divisible into 5 cm increments; ensure clear documentation of any deviations.
- Heterogeneous data formats
  - Data may originate from multiple systems; implement mapping to the standard field definitions to maintain interoperability.
- Large datasets and transfer issues
  - Large volumes from extensive sites or long-term studies may require robust storage and transfer processes, especially for raw and QC data.
- Metadata completeness
  - Ensure all fields (e.g., core depth, replicate, soil level) are consistently captured to avoid gaps in downstream analyses.