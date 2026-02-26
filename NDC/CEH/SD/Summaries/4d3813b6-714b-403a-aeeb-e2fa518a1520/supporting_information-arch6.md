# Dataset Description

- Overview
  - Describes soil physico-chemical properties and oil palm nutrient concentrations across 25 smallholder farms in Perak, Malaysia.
  - Collected April–May 2019 as part of the SUNRISE project; analyses conducted in Malaysia; soil texture measured at UK Centre for Ecology & Hydrology, Bangor.
  - Four CSV files totaling 300 soil samples (physico-chemical) and 150 palm tissue samples.
  - ND indicates results below method detection limit.

- Data Files and Key Fields
  - plot_information.csv
    - Plot_ID: Unique plot identifier
    - Plot_Area: Area of plot (hectares)
    - Planting_Density: Palms per hectare
    - Soil_Class: Mineral or Organic soil
    - Year_of_first_planting: YYYY
    - Time_under_oil_palm: Years under cultivation
    - Current_planting_date: YYYY
    - Palm_age: Age in years
  - leaf_nutrients.csv
    - Plot_ID: Unique plot identifier
    - Rep: Replicate (1–3 palms per plot)
    - Tissue: Leaf or Rachis
    - N, P, K, Mg, Ca: Nutrient concentrations (% or appropriate units)
  - soil_chemistry.csv
    - Plot_ID: Unique plot identifier
    - Rep: Replicate (1–3 palms per plot)
    - Sampling_Location: IR (Inter-Row) or PC (Palm Circle)
    - Depth_Increment: 0–15 cm or 15–30 cm
    - Bulk_Density: g cm^-3
    - Total_N: Total nitrogen concentration
    - Total_organic_C: Total organic carbon concentration
    - Available_P: Available phosphorus (mg kg^-1)
    - Exchangeable_K, Exchangeable_Mg, Exchangeable_Ca: cmol kg^-1
    - Soil_pH: pH
  - soil_texture.csv
    - Plot_ID: Unique plot identifier
    - Depth_Increment: 0–15 cm or 15–30 cm
    - Clay, Silt, Sand: Percent composition
  - Notes
    - Missing data: Blank cells indicate missing data.
    - ND: Results below method detection limit.

- Sampling Design and Scope
  - 25 farms sampled across the Wild Asia Group Scheme in Perak.
  - Blocks of 24 palms per farm; 3 palms per block randomly selected.
  - Edge effects avoided by selecting palms at least one row from plantation edges/tracks.
  - Soil sampling: two management locations per palm – palm circle (PC) and inter-row (IR) – representing ~76% of plantation soil surface area.
  - Within each location: three soil cores to 30 cm depth; cores divided into 0–15 cm and 15–30 cm sections (n=24 per plantation).
  - Palm tissue sampling: leaf 17 from 3 targeted palms; leaflets and rachis prepared and dried for analysis.
  - Palm tissue samples: 150 in total (across plots/replicates).
  - Note: Soil texture analysis conducted on composite samples (one per depth per plantation) at Bangor; some sample losses in transit caused missing Bulk Density for Plot_ID 422; two additional samples (416, 422) missing Total_N and Total_organic_C due to insufficient material.

- Analytical Methods
  - Soil
    - pH: fresh soil, 1:2.5 soil:water slurry
    - Soil organic carbon (C) and total nitrogen (N): dry combustion (LECO)
    - Extractable phosphorus (P): Olsen method, 880 nm colorimetry
    - Extractable K, Mg, Ca: 1 M ammonium acetate extraction; measured by atomic absorption spectroscopy
    - Bulk density: from oven-dried subsamples
    - Soil texture: laser granulometry after organic matter removal
  - Palm tissue
    - Leaf N: dry combustion (LECO)
    - Leaf P: H2SO4-H2O2 digest; colorimetry at 880 nm
    - Leaf K, Mg, Ca: H2SO4 digestion; atomic absorption spectroscopy
  - Metadata
    - Detailed column descriptions, units, and formats are provided for each CSV to support data integration and analysis.

- Metadata and Data Structure
  - plot_information.csv, leaf_nutrients.csv, soil_chemistry.csv, soil_texture.csv
  - Column-level metadata includes description and unit/format guidance to support correct interpretation and merging across files.
  - Depth increments consistently used (0–15 cm, 15–30 cm) where applicable.

- Data Quality, Gaps, and Considerations
  - Missing data notes:
    - Bulk density missing for Plot_ID 422 (sample loss in transit)
    - Total_N and Total_organic_C missing for Plot_ID 416 and 422 (insufficient material)
  - Some samples may be ND (below detection limit) for certain constituents.
  - Sampling design provides robust within-plot replication (Rep) but limited to 25 farms; results may reflect local variability within this region.
  - Data harmonization needed when merging tissue and soil datasets (consistent Plot_ID and Rep mapping; Tissue vs. Leaf/Rachis distinction).

- Potential Data Products and Uses
  - Dashboards and self-serve explorers to compare soil properties (pH, N, organic C, P, K/Mg/Ca, texture) by depth, location (IR vs PC), and plantation.
  - Cross-table analyses linking soil properties with palm tissue nutrient concentrations to identify nutrient management gaps.
  - Reports and visualizations for policy or agronomy guidance aimed at improving soil fertility management in smallholder oil palm systems.
  - Data quality checks and provenance dashboards highlighting missing data points and sample losses.

- References
  - Fairhurst, T., W. Griffiths and I. Rankine (2019). TCCL Field Handbooks. Oil Palm - Agronomy.
  - Mikutta, R., M. Kleber, K. Kaiser and R. Jahn (2005). Organic matter removal from soils using hydrogen peroxide, etc.
  - Nelson, P., M. Banabas, I. Goodrick, M. Webb, N. Huth and D. O'Grady (2015). Soil sampling in oil palm plantations: a practical design...