# Elemental concentrations (Ca, Cs, K, Mg, Sr) in a range of crops and associated soils from the UK and Spain

## Overview
- A multi-site dataset measuring elemental concentrations (Ca, Cs, K, Mg, Sr) plus NH4-N and NPOC in crops, soils, soil pore waters, and irrigation waters.
- Methods include ICPMS, ICPOES, and high-temperature combustion catalytic oxidation; samples collected from UK and Spain across 2018–2019 plant growth studies.
- Crops studied: radish, lettuce, grass, chard, courgette, strawberry (leaf and fruit), and potato (peel and flesh).
- Cross-border logistics: UK experiments complemented by Spain-based growth using exchanged seeds/soils; includes details on which soils were used and movement of materials due to regulations.

## Data content and structure
- Elements measured: Ca, Cs, K, Mg, Sr, NH4-N, NPOC. Pore waters and irrigation waters analysed as appropriate.
- Sample types:
  - Crops: freeze-dried and analyzed; various crop parts (e.g., radish leaves, strawberry leaves/berries, potato flesh/peel, courgette fruits, lettuce leaves, chard leaves, grass).
  - Soils: multiple soil types with differing pH (4.5–7.9) and loss on ignition (LOI 3.1–23.7%).
  - Pore waters: collected from rhizons; irrigation water samples.
- Data tables (14 total), each with detailed metadata:
  - CONFIDENCE_PlantGrowthStudy_Crop_SampleList
  - CONFIDENCE_PlantGrowthStudy_Soil_SampleList
  - CONFIDENCE_PlantGrowthStudy_PoreWater_SampleList
  - CONFIDENCE_PlantGrowthStudy_pH_LOI_Values
  - CONFIDENCE_PlantGrowthStudy_RadishLeafAndEdibleRoot_FM_DM
  - CONFIDENCE_PlantGrowthStudy_StrawberryFruitAndLeaf_FM_DM
  - CONFIDENCE_PlantGrowthStudy_PeeledPotatoAndPeel_FM_DM
  - CONFIDENCE_PlantGrowthStudy_Courgette_FM_DM
  - CONFIDENCE_PlantGrowthStudy_Grass_FM_DM
  - CONFIDENCE_PlantGrowthStudy_Chard_FM_DM
  - CONFIDENCE_PlantGrowthStudy_Lettuce_FM_DM
  - CONFIDENCE_PlantGrowthStudy_Crop_ElementalConcentrations
  - CONFIDENCE_PlantGrowthStudy_Soil_ElementalConcentrations
  - CONFIDENCE_PlantGrowthStudy_PoreWater_ElementalConcentrations
- Units and data types:
  - Crop/soil element concentrations in mg/kg dry mass (AR extraction) or mg/kg (BaCl extraction) depending on table.
  - Pore water element concentrations in mg/L or µg/L as specified.
  - Mass measurements in g or mL, and ratios (dimensionless) for dried/fresh mass comparisons.
  - Unique sample identifiers for AR-extracted data; extraction method details included per table.
- Data handling:
  - External calibration with internal standards (Ga, In, Re) to correct drift.
  - LODs calculated from blanks; 20% of data validated by independent check.
  - Data recorded in Microsoft Excel; notes sections capture relevant row-specific caveats.

## Methods and quality control
- Sample preparation:
  - Crop samples: freeze-dried, ground; digested with aqua regia (3:1 HNO3:HCl) at 175°C in microwave system; a second BaCl2 extraction performed for comparison.
  - Soil samples: prepared similarly; some analyses use AR extraction, others BaCl2 extraction.
  - Pore water and irrigation waters: filtered and acidified; analyzed directly.
- Instrumentation:
  - ICPMS for Cs and Sr; ICPOES for Ca, K, Mg.
  - TOC-L analyser for NPOC (with acidification to remove inorganic carbon and purging prior to measurement).
- Quality and provenance controls:
  - Care to avoid metal contamination; non-metallic containers; dedicated sample processing protocols.
  - Internal standards (Ga, In, Re) to correct for drift and matrix effects.
  - LOQ/LOD established from reagent blanks; data validation performed on a subset (approx. 20%).
- Documentation and references:
  - Data handling guided by established methods (Allen 1989; Lofts et al. 2001).
  - Comprehensive methodological notes embedded within the dataset tables.

## Provenance and context
- Studies underpinning the data:
  - Two UK plant growth studies conducted at CEH Lancaster (spring/summer 2018 and 2019).
  - A complementary study at the University of Extremadura (Cáceres) in summer 2018.
- Material movements:
  - Seeds and potato varieties exchanged UK↔Spain; Spanish soils used to grow UK crops and vice versa due to regulatory constraints.
  - Pore water and irrigation water samples collected within respective study contexts.
- Funding and acknowledgements:
  - CONFIDENCE project under CONCERT EJP, funded by the EU Horizon 2020 programme (grant No 662287).
  - Additional thanks to individuals for assistance during experiments and data preparation.

## Metadata, discoverability, and governance
- Data structure is explicitly documented via 14 standardized tables, each with field-level explanations (sample descriptors, soil descriptors, harvest years, replicate IDs, notes, and data provenance).
- Unique identifiers:
  - Unique_Sample_ID for AR-extracted crop/soil data; separate identifiers for BaCl-extracted data.
- Data stewardship:
  - Clear provenance trail from growth experiments to analytical results; cross-table references enable integrative queries (e.g., crop in soil, harvest year, element concentrations by extraction method).
- Accessibility and reuse:
  - Data are organized for cross-study comparability across crops, soils, and extraction methods, with explicit caveats and notes per row to guide interpretation.

## Limitations and considerations for reuse
- Extraction-related caveats:
  - Potassium recovery in aqua regia extractions is 51–63% in soils, indicating AR extraction may underestimate total K due to incomplete dissolution of clays.
- Coverage and sampling:
  - LOI and pH values measured on selections rather than all samples; pore-water data may be limited to specific soil/crop combinations.
  - Some rows marked as "Unused" soils or with n/a fields; incomplete replication across all tables for every crop/soil pair.
- Data quality considerations:
  - Data entry validation is partial (about 20% validated by others); users should consider cross-checking critical rows against instrument reports.

## Key data assets for Data Leaders
- Data assets:
  - Crop, soil, pore water, and irrigation water elemental concentration data across UK and Spain.
  - Cross-lab analytical methods (ICPMS, ICPOES, HT combustion) with detailed preparation protocols.
  - 14 interlinked data tables with comprehensive metadata and standard definitions.
- Data governance needs:
  - Ongoing curation to maintain consistent units and extract method mappings; ensure cross-border data harmonization and update provenance records.
  - Documentation of data gaps, limitations, and recovery caveats to inform policy, reporting, and data-sharing decisions.
- Reuse potential:
  - Comparative analysis of crop mineral uptake by soil type and region; evaluation of data quality and extraction method effects on reported concentrations; informing food-chain element risk assessments and soil-crop transfer models.