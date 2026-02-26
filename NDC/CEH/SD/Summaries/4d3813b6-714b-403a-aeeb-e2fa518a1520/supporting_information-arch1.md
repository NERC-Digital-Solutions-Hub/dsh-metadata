# Dataset Description

- Overview of the dataset describing soil physico-chemical properties and oil palm nutrient concentrations across 25 smallholder farms in Perak, Malaysia. Samples collected April–May 2019 as part of the NERC SUNRISE project and analyzed in Malaysia; soil texture analysis conducted in the UK. Four CSV files are provided, capturing field attributes, leaf/nutrient data, soil chemistry, and soil texture.

## Key content and scope

- Total samples: 300 soil samples for physico-chemical analyses; 150 palm tissue samples for chemical analysis.
- Farms: 25 smallholder oil palm farms (Wild Asia Group Scheme) in Perak.
- Sampling design: blocks of 24 palms with 3 palms randomly sampled per block; sampling avoids edges by staying at least one palm row from edges/tracks.
- Management zones per palm: Palm Circle (PC) and Inter-Row (IR), representing ~76% of soil surface area.
- Soil sampling: three cores per management zone to 30 cm depth; cores split into 0–15 cm and 15–30 cm sections; fresh mass recorded.
- Palm tissue sampling: leaf 17 collected from 3 targeted palms; eight largest leaflets per leaflet pair; middle 15–20 cm segment from each leaflet; rachis piece ~20 cm; samples air-dried and shipped to laboratories.

## Data files and structure

- plot_information.csv: 8 columns (Plot_ID, Plot_Area, Planting_Density, Soil_Class, Year_of_first_planting, Time_under_oil_palm, Current_planting_date, Palm_age).
- leaf_nutrients.csv: 8 columns (Plot_ID, Rep, Tissue, N, P, K, Mg, Ca).
- soil_chemistry.csv: 12 columns (Plot_ID, Rep, Sampling_Location, Depth_Increment, Bulk_Density, Total_N, Total_organic_C, Available_P, Exchangeable_K, Exchangeable_Ca, Exchangeable_Mg, Soil_pH).
- soil_texture.csv: 5 columns (Plot_ID, Depth_Increment, Clay, Silt, Sand).
- ND indicates results below method detection limit; some missing data noted in specific Plot_ID entries.

## Analytical methods

- Soil preparation: air-dried, sieved to 2 mm, milled; pH measured on 1:2.5 soil:water slurry.
- Soil chemistry: total C and N by dry combustion (LECO); Olsen P by colorimetric method at 880 nm; extractable K, Mg, Ca by 1M ammonium acetate and atomic absorption spectroscopy (AAS).
- Bulk density: calculated from oven-dried subsamples.
- Texture: laser granulometry after peroxide digestion; one sample per depth increment per plantation.
- Organic matter: measured after digestion (Mikutta et al. 2005).
- Leaf and rachis analysis: foliar N by dry combustion; leaf/rachis P by sulfuric acid-H2O2 digest and colorimetry; K, Mg, Ca by sulfuric acid digestion and AAS.

## Metadata and data provenance

- Metadata descriptions accompany each CSV, clarifying variable formats (numeric/text), units, and meanings (e.g., Plot_ID as unique plot identifier; Depth_Increment as 0–15 cm or 15–30 cm; Tissue types for leaves/rachis).
- Data collection and analysis references: Fairhurst et al. 2019; Mikutta et al. 2005; Nelson et al. 2015.

## Data quality and missing data

- Missing samples/measurements:
  - Plot_ID 422: Bulk density and soil texture missing due to sample loss in transit.
  - Plot_ID 416 and 422: Total_organic_C, Total_N, and Soil_pH missing due to insufficient material for laboratory analysis.
- Blank cells in CSVs indicate missing data; some measurements are below detection limits (ND).

## Potential uses

- Assess correlations between soil properties (pH, N, C, P, K, Mg, Ca; texture; bulk density) and oil palm tissue nutrient concentrations.
- Compare nutrient status across depth increments (0–15 cm vs. 15–30 cm) and management zones (PC vs. IR).
- Support modeling of soil-plant nutrient dynamics in smallholder oil palm systems in Malaysia.
- Provide a dataset with detailed metadata to facilitate reproducibility and re-use in related agronomy and soil science studies.

## References

- Fairhurst, T., W. Griffiths and I. Rankine (2019). TCCL Field Handbooks. Oil Palm - Agronomy.
- Mikutta, R., M. Kleber, K. Kaiser and R. Jahn (2005). Organic matter removal from soils using hydrogen peroxide, sodium hypochlorite, and disodium peroxodisulfate. Soil Science Society of America Journal 69:120-135.
- Nelson, P., M. Banabas, I. Goodrick, M. Webb, N. Huth and D. O'Grady (2015). Soil sampling in oil palm plantations: a practical design that accounts for lateral variability at the tree scale. Plant and Soil 394.