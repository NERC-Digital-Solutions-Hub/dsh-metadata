# Dataset Description

## Overview
- Describes soil physico-chemical properties and oil palm nutrient concentrations across 25 smallholder farms in Perak, Malaysia.
- Samples collected April–May 2019 as part of the NERC SUNRISE project; analyses conducted at Carmiel Agrotech Testing Laboratories, Malaysia; soil texture measured at UK Centre for Ecology & Hydrology, Bangor.
- Four CSV files comprise the dataset; blank cells denote missing data; "ND" indicates results below method detection limit.
- Total samples: 300 soil samples for physico-chemical analyses and 150 palm tissue samples for chemical analysis.

## Dataset structure
- plot_information.csv
  - Plot_ID, Plot_Area, Planting_Density, Soil_Class, Year_of_first_planting, Time_under_oil_palm, Current_planting_date, Palm_age.
- leaf_nutrients.csv
  - Plot_ID, Rep, Tissue, N, P, K, Mg, Ca.
- soil_chemistry.csv
  - Plot_ID, Rep, Sampling_Location, Depth_Increment, Bulk_Density, Total_N, Total_organic_C, Available_P, Exchangeable_K, Exchangeable_Ca, Exchangeable_Mg, Soil_pH.
- soil_texture.csv
  - Plot_ID, Depth_Increment, Clay, Silt, Sand.

## Sampling design and field methods
- 25 smallholder oil palm farms sampled via blocks of 24 palms; within each block, three palms randomly selected.
- Sampling locations per farm: palm circle (PC) and inter-row (IR) to represent ~76% of soil surface area.
- Three soil cores per management zone to 30 cm depth; cores divided into 0–15 cm and 15–30 cm; fresh mass recorded for each section.
- Palm tissue sampling from 3 targeted palms; leaf 17 cut, eight leaflets (four left, four right) plus rachis sample collected; samples air-dried and sent for analysis.
- Soil and foliar samples transported to respective laboratories; one subsample of air-dried soil shipped for texture analysis.
- Field notes on irregularities: Bulk density and soil texture for Plot_ID 422 missing due to sample loss; Total organic C, Total N, and pH missing for Plot_IDs 416 and 422 due to insufficient material.

## Analytical methods
- Soil samples: air-dried, sieved to 2 mm; pH measured on soil:water slurry (1:2.5). C and total N via dry combustion (LECO analyzer). Olsen method used for extractable P with 880 nm analysis. Extractable K, Mg, Ca via 1 M ammonium acetate and atomic absorption spectroscopy. Bulk density calculated from oven-dried subsamples. Soil texture analyzed at Bangor using laser granulometry on composite samples (0–15 and 15–30 cm per plantation) after organic matter removal by peroxide digestion.
- Leaf and rachis samples: air-dried, milled; foliar N by dry combustion; foliar P via sulfuric acid–hydrogen peroxide digest with 880 nm colorimetry; K, Mg, Ca by sulfuric acid digestion and atomic absorption spectroscopy.

## Data quality, gaps, and metadata
- Metadata provided for each file detailing column descriptions, units, formats, and data types.
- Missing data explicitly noted: specific Plot_IDs with missing Bulk Density, soil texture, Total_N, Total_organic_C, and pH due to sample loss or insufficient material.
- ND markers indicate results below method detection limits.
- Sampling design and methods aim to account for lateral variability and edge effects, with explicit depth increments and management zone distinctions.

## Metadata and data dictionary
-plot_information.csv, leaf_nutrients.csv, soil_chemistry.csv, and soil_texture.csv each include detailed descriptions of variables, units, and formats to support reproducibility and interpretation.

## Usage, openness, and governance notes
- The dataset emphasizes transparency through metadata and standardised analytical methods.
- Data sharing considerations noted via explicit reporting of missing data and detection limits; some data gaps may affect longitudinal monitoring and cross-site comparisons.
- References underpinning methodology and field practices are provided.

## References
- Fairhurst, T., W. Griffiths, and I. Rankine (2019). TCCL Field Handbooks. Oil Palm - Agronomy.
- Mikutta, R., M. Kleber, K. Kaiser, and R. Jahn (2005). Organic matter removal from soils using hydrogen peroxide, sodium hypochlorite, and disodium peroxodisulfate. Soil Science Society of America Journal 69:120-135.
- Nelson, P., M. Banabas, I. Goodrick, M. Webb, N. Huth, and D. O'Grady (2015). Soil sampling in oil palm plantations: a practical design that accounts for lateral variability at the tree scale. Plant and Soil 394.