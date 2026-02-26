# Dataset Description

## Overview
- Describes soil physico-chemical properties and oil palm nutrient concentrations across 25 smallholder farms in Perak, Malaysia.
- Sampling occurred April–May 2019; part of the NERC SUNRISE project; analyses conducted at Carmiel Agrotech Testing Laboratories, Malaysia; soil texture analyzed at UK Centre for Ecology & Hydrology, Bangor.
- The dataset comprises four CSV files with a total of 300 soil samples (physico-chemical) and 150 palm tissue samples (foliar nutrients).

## Data files and structure
- plot_information.csv
  - 8 columns: Plot_ID, Plot_Area, Planting_Density, Soil_Class, Year_of_first_planting, Time_under_oil_palm, Current_planting_date, Palm_age
- leaf_nutrients.csv
  - 8 columns: Plot_ID, Rep, Tissue, N, P, K, Mg, Ca
- soil_chemistry.csv
  - 12 columns: Plot_ID, Rep, Sampling_Location, Depth_Increment, Bulk_Density, Total_N, Total_organic_C, Available_P, Exchangeable_K, Exchangeable_Ca, Exchangeable_Mg, Soil_pH
- soil_texture.csv
  - 5 columns: Plot_ID, Depth_Increment, Clay, Silt, Sand
- Notes:
  - Blank cells = missing data; ND = results below method detection limit.

## Sampling design and context
- 25 farms within the Wild Asia Group Scheme; blocks of 24 palms per farm; 3 palms per block selected randomly.
- Two soil management zones per palm: Palm Circle (PC) and Inter-Row (IR); three soil cores per zone to 30 cm depth.
- Core sections: 0–15 cm and 15–30 cm (n=24 per plantation).
- Palm tissue sampling from 3 targeted palms using standard agronomic methods; leaf 17 collected, processed into leaflets and rachis, air-dried, and shipped for analysis.

## Analytical methods
- Soil: pH (1:2.5 slurry); soil organic carbon (C) and total nitrogen (N) by dry combustion (LECO); extractable phosphorus (P) by Olsen method; K, Mg, Ca by 1M ammonium acetate with atomic absorption spectroscopy; bulk density from oven-dried subsamples; soil textural analysis by laser diffraction.
- Leaves/rachis: foliar N by dry combustion (LECO); P by sulfuric acid–H2O2 digest with colorimetry; K, Mg, Ca by sulfuric digestion with atomic absorption spectroscopy.
- Soil texture samples processed at Bangor; narrative on organic matter removal prior to analysis.

## Metadata and data governance details
- Metadata provided for each CSV item, detailing:
  - Plot_ID as unique identifier; units/formats; descriptions of each column.
  - Rep, Depth_Increment, tissue types, and measurement units for all chemical properties.
- Data provenance: sampling conducted in 2019; analyses performed by specified laboratories; references for field methods and sampling design included.

## Data quality, limitations, and gaps
- Known missing data:
  - Bulk density and soil texture missing for Plot_ID 422 due to sample loss in transit.
  - Total organic carbon, total nitrogen, and pH missing for Plot_IDs 416 and 422 due to insufficient material.
- ND values indicate results below method detection limits.

## Provenance, references, and context
- SUNRISE project funding (NERC); field methods and agronomy references:
  - Fairhurst, Griffiths, Rankine (2019)
  - Mikutta et al. (2005)
  - Nelson, Banabas, Goodrick, Webb, Huth, O'Grady (2015)

## Reuse considerations for Data Stewards
- Ensure consistent cross-file joins using Plot_ID and Rep.
- Maintain documented handling of missing data (ND and blanks).
- Verify units and formats across files; apply harmonization if integrating with other datasets.
- Consider data sharing constraints related to plot-level information and any proprietary considerations from the Wild Asia Group Scheme.