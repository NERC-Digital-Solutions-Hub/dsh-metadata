# Elemental concentrations (Ca, Cs, K, Mg, Sr) in a range of crops and associated soils from the UK and Spain

## Overview
- Data describe elemental concentrations of Ca, Cs, K, Mg, Sr, NH4-N, and NPOC.
- Analytes measured by ICPMS (Cs, Sr), ICPOES (Ca, K, Mg), or high-temperature combustion catalytic oxidation.
- Sample types: freeze-dried crops, soil, soil pore waters, and irrigation water.
- Studies span spring/summer 2018 and 2019 at CEH Lancaster (UK) and a 2018 study at the University of Extremadura (Spain); seeds and potato tubers shipped between sites; soil from Spain grown in the UK for some crops.
- Crops studied: radish, lettuce, grass, chard, courgette, strawberry, potato (with specific cultivars listed); grown to maturity.
- Soils: several descriptors/types (Top, Heath, Allotment, Clay loam, Loamy sand, Spanish) with pH 4.5–7.9 and LOI 3.1–23.7%.
- Post-harvest processing: samples washed, freeze-dried, ground; pore waters collected with rhizons; irrigation water collected.
- Pore water samples and data include various element concentrations; some samples and soils are flagged as “Unused” if no crops were grown in them.

## Methods and quality assurance
- Good laboratory practice followed; contamination controls (non-metallic containers, ceramic tools, agate mills).
- Sample prep: crop samples freeze-dried, ground; soil samples dried and ground; aqua regia digestion (3:1 HNO3:HCl) at 175°C for 12 minutes using microwave digestion; a second BaCl2 extraction used for soils.
- Pore waters and irrigation waters analyzed directly; all digests/extracts diluted 100-fold before analysis.
- Instrumentation: ICPMS for Cs and Sr; ICPOES for Ca, K, Mg.
- Internal standards: Ga, In, Re to correct drift/matrix effects.
- Calibration via external standards; LODs calculated from blanks; AR and BaCl extractions used with note on recoveries.
- NPOC measured with Shimadzu TOC-L (TNM-L module): acidify, purge inorganic carbon, combustion at 720°C with catalyst; CO2 detected by IR.
- Data handling: recorded in Excel; approximately 20% of data validated by someone other than the original entry.

## Provenance and data structure
- Part of the CONFIDENCE project within the CONCERT EJP, funded by the EU Horizon 2020 programme (grant No 662287).
- Data designed to be discoverable and usable, with detailed metadata and standardized tables.
- Data are organized into 14 data tables covering crop and soil samples, pore water samples, pH/LOI values, and crop-specific elemental data (including radish, strawberry, potato, courgette, grass, chard, lettuce) as well as elemental concentrations for crops and soils and pore waters.
- Tables include:
  - PlantGrowthStudy_Crop_SampleList
  - PlantGrowthStudy_Soil_SampleList
  - PlantGrowthStudy_PoreWater_SampleList
  - PlantGrowthStudy_pH_LOI_Values
  - PlantGrowthStudy_RadishLeafAndEdibleRoot_FM_DM
  - PlantGrowthStudy_StrawberryFruitAndLeaf_FM_DM
  - PlantGrowthStudy_PeeledPotatoAndPeel_FM_DM
  - PlantGrowthStudy_Courgette_FM_DM
  - PlantGrowthStudy_Grass_FM_DM
  - PlantGrowthStudy_Chard_FM_DM
  - PlantGrowthStudy_Lettuce_FM_DM
  - PlantGrowthStudy_Crop_ElementalConcentrations
  - PlantGrowthStudy_Soil_ElementalConcentrations
  - PlantGrowthStudy_PoreWater_ElementalConcentrations
  - PlantGrowthStudy_PoreWater_ElementalConcentrations (Pore water section)

## Data variables and units (highlights)
- Crops: K, Ca, Mg, Sr, Cs concentrations reported as mg/kg dry mass; NH4-N reported for relevant crop datasets; NPOC values included where applicable.
- Pore waters and irrigation waters: Ca, K, Mg, Cs, Sr reported in mg/L or µg/L; NPOC in µg/L; Ti used as a contamination marker in some pore-water measurements.
- Cs data: Some entries flagged with < (below detection) or n/a; BaCl- and AR-extracted data include notes on detection and recovery.
- Sample descriptors: Year harvested, soil descriptor, crop grown in soil, sample identifiers, and notes about data rows.
- Some soil entries marked "Unused" when no crop was grown in those soils.

## Experimental design highlights
- Crops grown in multiple soil types with varied pH and organic matter content (LOI).
- Cross-site design: UK and Spain, with seed/tubers and soils exchanged to enable comparative uptake studies.
- Harvest and processing conducted to maturity; standardised preparation facilitates cross-table comparisons.

## Analytical considerations and limitations
- AR extraction recoveries for soils (K, Ca, Mg, Sr, Cs) reported in the 51–63% range, indicating incomplete dissolution of certain minerals (notably clays) and caution when interpreting total-Ca/K/Mg/Sr from AR extracts.
- Cs data can be below detection limits in some BaCl- or AR-extracted datasets.
- Some soils/crops are flagged as unused or have variable sample sizes across years and crops.
- Data quality controlled with 20% independent validation; careful attention to units and extraction methods needed when merging tables.

## How the data can support analysis
- Facilitate soil-to-crop transfer studies for Ca, K, Mg, Sr, and Cs across multiple crops and soil types.
- Enable cross-country comparisons (UK vs Spain) and evaluation of how soil characteristics (pH, LOI) influence crop elemental composition.
- Allow assessment of method-related biases (AR vs BaCl extraction) and their impact on recovered element concentrations.
- Provide pore-water chemistry context (Ca, K, Mg, Sr, Cs, NPOC, Ti) to interpret mobility and availability in the rhizosphere.

## Acknowledgements and accessibility
- Data generated under the CONFIDENCE project (CONCERT EJP) with Horizon 2020 funding.
- Authors and institutions acknowledged; dataset designed for discoverability via metadata and structured tables.