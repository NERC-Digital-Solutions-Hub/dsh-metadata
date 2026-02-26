# Elemental concentrations (Ca, Cs, K, Mg, Sr) in a range of crops and associated soils from the UK and Spain

## Overview
- Dataset of elemental concentrations (Ca, Cs, K, Mg, Sr) in crops, soils, pore waters, and irrigation waters.
- Measurements include NH4-N and NPOC; analytical methods: ICPMS, ICPOES, or high-temperature combustion for NPOC.
- Collected from two plant growth studies: UK (CEH Lancaster) in spring/summer 2018–2019 and Spain (University of Extremadura) in summer 2018.
- Crops studied include radish, lettuce, grass, chard, courgette, strawberry, and potato, grown in diverse soil types with varying pH (4.5–7.9) and organic matter (LOI 3.1–23.7%).
- Samples were prepared to minimize contamination, freeze-dried, ground, digested or extracted as appropriate, and analysed with strict QA/QC protocols.

## Data scope and samples
- Sample types:
  - Crops: multiple tissues (e.g., radish leaves and edible roots; strawberry leaves and berries; lettuce leaves; etc.).
  - Soils: diverse soil types described (e.g., Top, Heath, Allotment, Clay loam, Loamy sand, Spanish).
  - Pore waters: rhizon-collected samples (end of 2018 UK study; select soils; some irrigation waters).
  - Irrigation waters: analyzed directly for certain constituents.
- Geographic scope: United Kingdom and Spain.
- Temporal scope: harvest years embedded in the dataset (1998–present not specified; focus on 2018–2019 growth studies).
- Data organization: a series of data dictionaries (tables) describing crops, soils, pore water samples, pH/LOI values, plant parts, and elemental concentrations.

## Methods and analytical workflow
- Sample preparation:
  - Crop samples: freeze-dried, ground to <2 mm; soil samples: air or oven-dried, ground to <2 mm.
  - Digestion: aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes using microwave digestion.
  - Alternative extraction: 0.1 M BaCl2 for soil extracts; pore and irrigation waters filtered and acidified.
- Instrumentation:
  - ICPMS for Cs and Sr; ICPOES for Ca, K, Mg.
  - Internal standards added (Ga, In, Re) to correct drift/matrix effects.
- Quality and validation:
  - External calibration; instrument detection limits (LODs) calculated from blanks.
  - Duplicate/sub-sample replicates; 20% data validated by someone other than the initial enterer.
  - NPOC measured with Shimadzu TOC-L; inorganic carbon removed prior to measurement.
- Data recording:
  - Results captured in Microsoft Excel workbooks from lab notebooks and instrument reports.

## Data structure and tables
- The dataset includes 14 data dictionaries (CONFIDENCE_ tables) detailing data organization and variables:
  - PlantGrowthStudy_Crop_SampleList: crop, year harvested, soil descriptor, sample IDs, counts, notes.
  - PlantGrowthStudy_Soil_SampleList: soil descriptor, sample IDs, crop grown in soil, year, replicates, notes.
  - PlantGrowthStudy_PoreWater_SampleList: sample descriptions, crop in soil, pore-water notes, counts.
  - PlantGrowthStudy_pH_LOI_Values: pH and LOI values by sample/soil/crop.
  - PlantGrowthStudy_RadishLeafAndEdibleRoot_FM_DM: mass measurements (fresh/freeze-dried) for radish leaves and edible roots, with derived ratios.
  - PlantGrowthStudy_StrawberryFruitAndLeaf_FM_DM: mass data for strawberry leaves and berries (with/without hulls) and derived ratios.
  - PlantGrowthStudy_PeeledPotatoAndPeel_FM_DM: mass data for potatoes with/without peel and related ratios, including notes.
  - PlantGrowthStudy_Courgette_FM_DM: individual fruit mass and freeze-dried mass with ratios; notes.
  - PlantGrowthStudy_Grass_FM_DM: grass leaf mass data (fresh/freeze-dried) and dry-to-fresh ratios.
  - PlantGrowthStudy_Chard_FM_DM: chard leaf mass data (fresh/freeze-dried) and ratios.
  - PlantGrowthStudy_Lettuce_FM_DM: lettuce leaf mass data (fresh/freeze-dried) and ratios.
  - PlantGrowthStudy_Crop_ElementalConcentrations: element concentrations (K, Ca, Mg, Sr; Cs with detection notes) in crops at harvest; unique sample identifiers; notes.
  - PlantGrowthStudy_Soil_ElementalConcentrations: AR and BaCl-extracted elemental concentrations by soil/crop combos; recovery notes and method caveats (e.g., K AR recoveries 51–63%).
  - PlantGrowthStudy_PoreWater_ElementalConcentrations: pore-water element concentrations (Ca, Cs, K, Mg, NPOC, Sr, Ti) with notes on detection limits.
- Units and notations:
  - Concentrations in mg/kg dry mass for crops/soils; Cs reported with detection markers; some <LOD indicators.
  - Pore water concentrations in mg/L or µg/L depending on element.

## Provenance, quality and uncertainty
- Provenance:
  - Conducted under the CONFIDENCE project within the CONCERT EJP; Horizon 2020 funding.
  - UK and Spain collaborations; seeds and plant material exchanged between sites.
- Quality controls:
  - Good laboratory practices; contamination controls (non-metallic containers, agate mills, etc.); regular instrument maintenance.
  - Use of internal standards and calibration strategies; LODs based on reagent blanks.
  - Data validation: approximately 20% of entries cross-checked by third parties.
- Uncertainties and caveats:
  - AR extraction partial recovery for K and potential underestimation of total K due to incomplete dissolution of clays.
  - Some Cs values flagged as below detection or not reported; several “n/a” entries where data not applicable or not collected.
  - Pore-water and BaCl/AR extraction data include notes on sample-specific limitations and notes columns for row-specific caveats.

## GIS opportunities and considerations
- Potential to create map-based data products that visualize spatial patterns of elemental concentrations across crops and soils.
- Key fields suitable for GIS joins:
  - Soil_Descriptor, Sample_IDs, Year_Harvested, Crop_Grown_In_Soil, and element concentration fields (K, Ca, Mg, Sr, Cs) with corresponding units.
  - Extraction method (AR vs BaCl) to indicate chemical speciation context.
  - Pore water data (Ca, Cs, K, Mg, Sr, NPOC) and irrigation water data for hydrological-context mapping.
  - pH and LOI as soil property layers to contextualize nutrient availability.
- Map products could include:
  - Spatial overlays of crop element concentrations by crop type and soil type.
  - Layered maps linking crop tissue concentrations with corresponding soils and pore-water chemistry.
  - Multi-criteria maps combining soil type, pH/LOI, and measured element concentrations for risk or nutrition assessment.
- Data integration considerations:
  - Aligning non-spatial tables (14 dictionaries) with spatial soil and land-use layers; handle 'Unused' soils and missing data appropriately.
  - Handling units and detection flags (e.g., <LOD) to avoid misinterpretation in visualizations.
  - Accounting for differing extraction methods (AR vs BaCl) when comparing across samples.

## Limitations and data gaps
- Data are tied to designated soil descriptors and crop growth studies; may lack precise geospatial coordinates or national-scale coverage.
- Incomplete or missing values (marked n/a, below detection) in several fields; some notes required for interpretation.
- Differences in sample processing and extraction methods introduce comparability considerations (AR recoveries for K, total extraction vs partial dissolution of clays).
- Some data rows refer to ‘Unused’ soils where no crops were grown, requiring careful handling in GIS analyses.

## Provenance and acknowledgement
- Acknowledges contributions from CEH Lancaster, University of Extremadura, and funding from the EU Horizon 2020 CONFIDENCE/CONCERT EJP program (grant No 662287).
- Data compiled into structured data dictionaries and published as part of the CONFIDENCE Plant Growth Studies.

## Keywords
- Element, Human Food Chain, ICPMS, ICPOES, Plant Growth Study, Soil, Grass, Radish, Potato, Strawberry, Lettuce, Courgette, Chard, Pore water, NH4-N, NPOC