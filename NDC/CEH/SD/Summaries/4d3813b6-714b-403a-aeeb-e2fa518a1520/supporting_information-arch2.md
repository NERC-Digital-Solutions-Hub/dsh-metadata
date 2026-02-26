# Dataset Description

- The dataset describes soil physico-chemical properties and oil palm nutrient concentrations across 25 smallholder farms in Perak, Malaysia. Samples were collected in April–May 2019 as part of the NERC SUNRISE project and analyzed at Carmiel Agrotech Testing Laboratories (Malaysia); soil texture measurements were performed at the UK Centre for Ecology & Hydrology, Bangor. The dataset comprises four CSV files and includes 300 soil samples for physico-chemical analyses and 150 palm tissue samples for chemical analysis.

## Data files and structure

- Four CSV files:
  - plot_information.csv: eight columns describing each plot (Plot_ID, Plot_Area, Planting_Density, Soil_Class, Year_of_first_planting, Time_under_oil_palm, Current_planting_date, Palm_age).
  - leaf_nutrients.csv: eight columns for palm tissue (Plot_ID, Rep, Tissue, N, P, K, Mg, Ca).
  - soil_chemistry.csv: twelve columns (Plot_ID, Rep, Sampling_Location, Depth_Increment, Bulk_Density, Total_N, Total_Organic_C, Available_P, Exchangeable_K, Exchangeable_Ca, Exchangeable_Mg, Soil_pH).
  - soil_texture.csv: five columns (Plot_ID, Depth_Increment, Clay, Silt, Sand).
- Data values:
  - Blank cells indicate missing data.
  - “ND” denotes results below the method detection limit.
- Sample counts:
  - 300 soil samples (physico-chemical analyses).
  - 150 palm tissue samples (chemical analyses).

## Sampling design and methods

- Study population: 25 smallholder oil palm farms within the Wild Asia Group Scheme in Perak, Malaysia.
- Within-farm sampling: blocks of 24 palms; 3 palms randomly selected per block.
- Spatial design: soil sampled from two management zones per palm plantation per farm – Palm Circle (PC) and Inter-Row (IR) – representing about 76% of soil surface area.
- Soil sampling: three soil cores per management zone, collected to 30 cm depth; cores split in the field into 0–15 cm and 15–30 cm segments (n=24 per plantation).
- Palm tissue sampling: from 3 targeted palms, leaf 17 harvested; eight largest leaflets and rachis sampled, air-dried, and sent to labs.
- Handling: leaves and soil shipped to Carmiel Agrotech Testing Laboratories (Malaysia); a subset of soil was sent to CEH Bangor for texture analysis.
- Notable issues: Bulk density data for Plot_ID 422 missing due to sample loss; Total organic C, Total N, and pH missing for Plot_ID 416 and 422 due to insufficient material.

## Analytical methods

- Soil analyses:
  - pH: fresh soil, 1:2.5 soil:water slurry.
  - Soil organic carbon (C) and total nitrogen (N): dry combustion (LECO 628).
  - Extractable phosphorus (P): Olsen method, measured at 880 nm (UV-VIS).
  - Extractable potassium (K), magnesium (Mg), calcium (Ca): 1 M ammonium acetate extraction; measured by atomic absorption spectroscopy.
  - Bulk density: derived from oven-dried subsamples.
  - Soil texture: laser granulometry after peroxide digestion; one sample per depth per plantation.
- Palm tissue analyses:
  - Leaf N, P: dry combustion (N) and acid digestion with colorimetric analysis for P.
  - Leaf K, Mg, Ca: extractions and atomic absorption spectroscopy.

## Data quality and limitations

- Standardised sampling and laboratory procedures were used across plots.
- Some missing data points due to sample loss or insufficient material (see above).
- Metadata provides explicit descriptions for each column to support consistency and comparability.

## Metadata details (file-by-file overview)

- plot_information.csv
  - Plot_ID: Unique plot identifier.
  - Plot_Area: Area (hectares).
  - Planting_Density: Palms per hectare.
  - Soil_Class: Mineral or Organic soil classification.
  - Year_of_first_planting: Year plot first planted.
  - Time_under_oil_palm: Years under continuous oil palm cultivation.
  - Current_planting_date: Year palms were planted.
  - Palm_age: Age of standing palms (years).

- leaf_nutrients.csv
  - Plot_ID: Plot identifier.
  - Rep: Replicate (1–3 per plot).
  - Tissue: Tissue type (Leaf or Rachis).
  - N, P, K, Mg, Ca: Nutrient concentrations (percent or appropriate units).

- soil_chemistry.csv
  - Plot_ID: Plot identifier.
  - Rep: Replicate (1–3).
  - Sampling_Location: IR (Inter-Row) or PC (Palm Circle).
  - Depth_Increment: 0–15 cm or 15–30 cm.
  - Bulk_Density: Bulk density (g cm-3).
  - Total_N: Total nitrogen (% or appropriate unit).
  - Total_organic_C: Total organic carbon (% or appropriate unit).
  - Available_P: Available phosphorus (mg kg-1).
  - Exchangeable_K, Exchangeable_Mg, Exchangeable_Ca: Exchangeable cations (cmol kg-1).
  - Soil_pH: pH (unitless).

- soil_texture.csv
  - Plot_ID: Plot identifier.
  - Depth_Increment: 0–15 cm or 15–30 cm.
  - Clay, Silt, Sand: Percent composition.

## References

- Fairhurst, T., W. Griffiths and I. Rankine (2019). TCCL Field Handbooks. Oil Palm - Agronomy.
- Mikutta, R., M. Kleber, K. Kaiser and R. Jahn (2005). Organic matter removal from soils using hydrogen peroxide, sodium hypochlorite, and disodium peroxodisulfate. Soil Science Society of America Journal.
- Nelson, P., M. Banabas, I. Goodrick, M. Webb, N. Huth and D. O'Grady (2015). Soil sampling in oil palm plantations: a practical design that accounts for lateral variability at the tree scale. Plant and Soil.