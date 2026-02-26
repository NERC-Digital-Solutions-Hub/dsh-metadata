# Elemental concentrations (Ca, Cs, K, Mg, Sr) in a range of crops and associated soils from the UK and Spain

## Overview
- Dataset of elemental concentrations for Ca, Cs, K, Mg, Sr, NH4-N and NPOC measured by ICPMS, ICPOES, or high-temperature combustion.
- Matrices include freeze-dried crops, soils, soil pore waters, and irrigation waters.
- Samples come from two UK plant growth studies (CEH Lancaster, spring/summer 2018 and 2019) and a 2018 study in Cáceres, Spain; seeds/plant material exchanged between UK and Spain.
- Crops studied: radish, lettuce, grass, chard, courgette, strawberry, and potato, grown to maturity on diverse soil types with varying pH (4.5–7.9) and LOI (3.1–23.7%).

## Study context and provenance
- UK studies conducted at CEH Lancaster; Spanish study conducted at the University of Extremadura.
- Plant material and soil movement occurred to enable cross-site comparisons (soil moved to Spain for some crops; strawberry plants movement restricted by plant health legislation).
- Good laboratory practice observed; contamination controls included non-metallic containers and agate milling processes; samples freeze-dried or dried appropriately before analysis.

## Sample types and study design
- Crop types and harvest details captured (e.g., radish leaves and edible roots; strawberry leaves and berries; peeled potatoes; courgette fruits; lettuce and chard leaves; grass).
- Soils labeled by descriptor (e.g., Top, Heath, Allotment, Clay loam, Loamy sand, Spanish); some soils designated as "Unused" if no crop was grown there.
- Measurements include crop biomass (fresh and dry/mass ratios), organ-specific samples (leaves, roots, berries, fruits, tubers), and pore waters.
- Pore waters collected using rhizons; irrigation water analyzed; LOI and pH measured for selected samples.

## Analytical methods and quality assurance
- Digestion: aqua regia (HNO3:HCl, 3:1) at 175°C for 12 minutes using microwave digestion; an additional BaCl2 extraction applied to some soil samples.
- Element analysis: Cs and Sr by ICPMS; Ca, K and Mg by ICPOES.
- Internal standards used to correct drift/matrix effects (Ga, In, Re); external calibration for quantification.
- NPOC measured with Shimadzu TOC-L (TNM-L) after acidification and purging inorganic carbon; results reported as NPOC.
- Data dilution: all samples diluted 100-fold prior to analysis.
- QA: data recorded from laboratory notebooks and instrument reports; approximately 20% of data validated by a reviewer other than the original data entrant.
- Detection notes: Cs measurements and BaCl/AR extraction recoveries discussed (e.g., K recoveries from AR extraction ~51–63% due to incomplete dissolution of clays).

## Data structure and metadata
- Data are organized into multiple data tables, with 14 defined data dictionaries (CONFIDENCE_…):
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
  - PlantGrowthStudy_Soil_ElementalConcentrations
  - PlantGrowthStudy_PoreWater_ElementalConcentrations
- Data fields span sample identifiers, crop/soil descriptors, harvest years, replicates, and detailed concentration measurements.
- Concentration units vary by matrix:
  - Dry-mass basis: mg/kg (K, Ca, Mg, Sr, Cs)
  - Pore water/solution: mg/L or µg/L (Cs in pore water)
  - NPOC in µg/L for pore water contexts
- Some entries note “<” for below-detection, and several rows include interpretive notes (e.g., unused soils, replicates).

## Data quality, limitations, and notes
- Cross-site and cross-method considerations addressed via QA protocols; calibration with internal standards mitigates drift.
- AR extraction yields for K in soils show partial recovery due to incomplete dissolution of clays; reported explicitly (51–63% recoveries).
- For Cs, some BaCl/AR entries flagged as below detection in certain rows.
- Some rows reference “Unused” soils or batches with no crop data, requiring careful handling during integration.
- Data are provided as Excel workbooks with accompanying data dictionaries to aid harmonization and self-service use.

## Access, usage, and potential data products
- Data are structured to enable cross-crop and cross-soil comparisons, including relationships among soil properties (pH, LOI) and elemental uptake in crops.
- Suitable for creating dashboards or self-serve analyses of element distributions across crops, soils, and water matrices, or for meta-analyses of plant-soil-nutrition interactions.
- Data dictionaries help map fields across tables to support data integration and reproducible analysis.

## Acknowledgments and provenance
- Part of the CONFIDENCE project under the CONCERT EJP, funded by the European Union’s Horizon 2020 programme (grant No. 662287).
- Authors and affiliations listed: CEH Lancaster (UK) and University of Extremadura (Spain).
- Data description and structure were prepared to support broader data use and reuse.