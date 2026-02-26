# Dataset Description

## Overview
- Describes soil physico-chemical properties and oil palm nutrient concentrations across 25 smallholder farms in Perak, Malaysia.
- Sampling occurred in April–May 2019 as part of the SUNRISE project; analyses conducted at Carmiel Agrotech Testing Laboratories, Malaysia, with soil texture measured at UK Centre for Ecology & Hydrology, Bangor.
- Comprises four CSV files: plot_information.csv, leaf_nutrients.csv, soil_chemistry.csv, soil_texture.csv.
- Total samples: 300 soil samples (physico-chemical analyses) and 150 palm tissue samples (nutrients).

## Dataset files and content
- plot_information.csv
  - Columns: Plot_ID, Plot_Area, Planting_Density, Soil_Class, Year_of_first_planting, Time_under_oil_palm, Current_planting_date, Palm_age.
- leaf_nutrients.csv
  - Columns: Plot_ID, Rep, Tissue, N, P, K, Mg, Ca.
- soil_chemistry.csv
  - Columns: Plot_ID, Rep, Sampling_Location, Depth_Increment, Bulk_Density, Total_N, Total_organic_C, Available_P, Exchangeable_K, Exchangeable_Ca, Exchangeable_Mg, Soil_pH.
- soil_texture.csv
  - Columns: Plot_ID, Depth_Increment, Clay, Silt, Sand.
- Metadata sections describe each column's meaning and units; missing data are represented as blanks, and ND indicates results below method detection limit.

## Sampling design and data collection
- 25 farms sampled across the Wild Asia Group Scheme in Perak.
- For each plantation, blocks of 24 palms were marked; 3 palms were randomly selected per block.
- Two management zones per selected palm: Palm Circle (PC) and Inter-Row (IR).
- Soil sampling: three cores per zone to 30 cm depth, subdivided into 0–15 cm and 15–30 cm sections; fresh mass recorded.
- Palm tissue sampling: leaf 17 from the three targeted palms; eight largest leaflets combined, plus rachis piece, air-dried and sent for analysis.
- Soil and leaf samples analyzed for various physico-chemical and nutrient metrics; a subsample of soil was sent for texture analysis.
- Notes on data gaps: Bulk density and texture results for Plot_ID 422 missing due to sample loss; total organic C, total N and pH missing for Plot_IDs 416 and 422 due to insufficient material.

## Analytical methods
- Soil
  - pH: 1:2.5 soil:water slurry with calibrated probe.
  - Organic carbon (OC) and total nitrogen (N): dry combustion (LECO).
  - Available phosphorus (P): Olsen method, 880 nm colorimetry.
  - Exchangeable K, Mg, Ca: 1 M ammonium acetate extraction, analyzed by atomic absorption spectroscopy.
  - Bulk density: oven-dried subsample weight (for 0–15 cm and 15–30 cm cores).
  - Texture: laser granulometry after peroxide digestion (one sample per depth increment per plantation); organic matter removed prior to analysis.
- Leaves
  - Foliar N: dry combustion (LECO).
  - P: sulfuric acid–hydrogen peroxide digest, colorimetry at 880 nm.
  - K, Mg, Ca: sulfuric acid digestion, atomic absorption spectroscopy.

## Data quality and limitations
- ND denotes results below method detection limit.
- Specific missing data noted for Plot_IDs 416 and 422 (soil chemical/texture measurements; bulk density missing for 422).
- Data collected from two depth increments (0–15 cm and 15–30 cm) and two management zones per palm, enabling within-plot spatial comparisons.

## Metadata and field definitions
- plot_information.csv: Plot_ID is the unique plot identifier; Plot_Area (ha); Planting_Density (palms/ha); Soil_Class (Mineral or Organic); Year_of_first_planting (YYYY); Time_under_oil_palm (years); Current_planting_date (YYYY); Palm_age (years).
- leaf_nutrients.csv: Rep identifies each of the three palms per plot; Tissue indicates Leaf or Rachis; N, P, K, Mg, Ca as percentages.
- soil_chemistry.csv: Rep per palm; Sampling_Location (IR or PC); Depth_Increment (0–15 cm or 15–30 cm); Bulk_Density (g/cm3); Total_N (%); Total_organic_C (%); Available_P (mg/kg); Exchangeable_K, Mg, Ca (cmol/kg); Soil_pH (unitless).
- soil_texture.csv: Depth_Increment (0–15 cm or 15–30 cm); Clay, Silt, Sand (%).

## GIS considerations and potential visualizations
- Spatial integration: join by Plot_ID to distribute soil properties and leaf nutrients across locations; depth increments treated as layers for multi-layer mapping (0–15 cm vs 15–30 cm).
- Visualization ideas:
  - Thematic maps of pH, total N, OC, Available_P, and exchangeable cations by plot and depth.
  - Soil texture maps showing Clay/Silt/Sand composition by depth increment.
  - PC vs IR zone maps to illustrate within-plot spatial variability.
  - Overlay farm boundary data if available to contextualize plots within larger regions.
- Data structuring tips:
  - Create separate GIS layers for surface (0–15 cm) and deeper (15–30 cm) soil properties; if needed, unpivot depth into a single Depth_Label field for easier GIS joins.
  - Normalize Plot_Area and Planting_Density to compare plots of differing sizes.
- Limitations to consider in GIS workflows:
  - No explicit geographic coordinates in the CSVs; coordinate data would be needed to map plots spatially unless provided externally.
  - Some missing values and ND entries; handle with NA-informed symbology or imputation as appropriate.

## References
- Fairhurst, T., W. Griffiths and I. Rankine (2019). TCCL Field Handbooks. Oil Palm - Agronomy.
- Mikutta, R., M. Kleber, K. Kaiser and R. Jahn (2005). Organic matter removal from soils using hydrogen peroxide, sodium hypochlorite, and disodium peroxodisulfate. Soil Science Society of America Journal 69: 120-135.
- Nelson, P., M. Banabas, I. Goodrick, M. Webb, N. Huth and D. O'Grady (2015). Soil sampling in oil palm plantations: a practical design that accounts for lateral variability at the tree scale. Plant and Soil 394.