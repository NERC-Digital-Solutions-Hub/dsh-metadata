# Dataset Description

## Overview
- Dataset describing soil physico-chemical properties and oil palm nutrient concentrations across 25 smallholder farms in Perak, Malaysia.
- Collected April–May 2019 under the NERC SUNRISE project; analyses conducted at Carmiel Agrotech Testing Laboratories, Malaysia; soil texture measurements at UK Centre for Ecology & Hydrology, Bangor.
- Contains four CSV files describing plots, foliar nutrients, soil chemistry, and soil texture.
- Total samples: 300 soil samples for physico-chemical analyses; 150 palm tissue samples for nutrient analysis.

## Data files and structure
- plot_information.csv: 8 columns – Plot_ID, Plot_Area, Planting_Density, Soil_Class, Year_of_first_planting, Time_under_oil_palm, Current_planting_date, Palm_age.
- leaf_nutrients.csv: 8 columns – Plot_ID, Rep, Tissue, N, P, K, Mg, Ca.
- soil_chemistry.csv: 12 columns – Plot_ID, Rep, Sampling_Location, Depth_Increment, Bulk_Density, Total_N, Total_organic_C, Available_P, Exchangeable_K, Exchangeable_Ca, Exchangeable_Mg, Soil_pH.
- soil_texture.csv: 5 columns – Plot_ID, Depth_Increment, Clay, Silt, Sand.
- Note: Blank cells indicate missing data; ND indicates results below method detection limit. Metadata provides column descriptions and units/formats.

## Sampling design
- 25 smallholder oil palm farms within the Wild Asia Group Scheme in Perak.
- Blocks of 24 palms; within each block, 3 palms selected randomly.
- Sampling locations per plantation: palm circle (PC) and inter-row (IR) to capture lateral variability (~76% of soil surface area in plantations).
- Soil sampling: three cores per management zone to 30 cm depth, split into 0–15 cm and 15–30 cm segments; fresh mass recorded.
- Palm tissue sampling: leaf 17 from three targeted palms; leaflets and rachis collected, dried, and shipped for analysis.
- Sample counts: 300 soil samples; 150 palm tissue samples.
- Notable data caveats: Bulk density and soil texture missing for Plot_ID 422 due to sample loss in transit; total organic C, total N, and pH missing for Plot_IDs 416 and 422 due to insufficient material.

## Analytical methods
- Soil pH: measured on fresh soils in a 1:2.5 soil:water slurry.
- Soil organic carbon (C) and total nitrogen (N): dry combustion (LECO 628).
- Extractable phosphorus (P): Olsen method; measured at 880 nm with UV-VIS.
- Exchangeable potassium (K), magnesium (Mg), calcium (Ca): extracted with 1 M ammonium acetate; measured by atomic absorption spectroscopy.
- Bulk density: derived from oven-dried subsamples.
- Soil texture: laser granulometry after peroxide digestion; one composite sample per depth increment per plantation.
- Foliar N: dry combustion (LECO); foliar P via sulfuric acid–H2O2 digest and colorimetry; K/Mg/Ca via digestion and AAS.

## Metadata and documentation
- Metadata blocks accompany each CSV, detailing variable descriptions, units, and formats (as described in the dataset’s metadata sections for plot_information, leaf_nutrients, soil_chemistry, and soil_texture).

## Data quality, limitations, and notes
- Missing data: several plots have incomplete measurements (e.g., Plot_IDs 416, 422).
- ND values indicate measurements below method detection limits.
- Texture data is based on a single composite sample per depth increment per plantation, which may affect within-plot variability assessments.
- Sampling design aims to minimize edge effects and capture spatial variability across management zones.

## Governance, reuse, and potential applications (Data Leaders perspective)
- Provenance: SUNRISE project; laboratory analyses and field sampling well-documented.
- Data stewardship: four clearly named CSVs with comprehensive metadata enhances discoverability and reusability; standardized analytical methods support comparability.
- Opportunities for use: cross-farm comparisons of soil properties and palm nutrient status; modeling relationships between soil chemistry, texture, and palm tissue nutrients; informing management decisions in oil palm smallholder systems.
- Considerations for access and integration: verify missing data gaps (Plot_ID 416, 422) and potential need for lab reports; ensure alignment with local data protection and collaboration agreements if integrating with network data.