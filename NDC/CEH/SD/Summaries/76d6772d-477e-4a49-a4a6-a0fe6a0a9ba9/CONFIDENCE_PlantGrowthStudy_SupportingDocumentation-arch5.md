# Elemental concentrations (Ca, Cs, K, Mg, Sr) in a range of crops and associated soils from the UK and Spain

## Purpose and scope
- Presents elemental concentrations (Ca, Cs, K, Mg, Sr) in crops, soils, soil pore waters, and irrigation water from the UK and Spain.
- Additional measurements include NH4-N and NPOC (Non-Purgeable Organic Carbon).
- Data collected from plant growth studies in 2018–2019 (UK) and 2018 (Spain) to enable reuse in the human food chain context.
- Analyses performed with ICPMS, ICPOES, or high-temperature combustion catalytic oxidation; samples were processed with care to avoid metal contamination and were stored appropriately.

## Study design and sampling
- Crops grown: radish, lettuce, grass, chard, courgette, strawberry, potato (peeled and peeled), with multiple cultivars indicated.
- Soil types: varied across sites (e.g., Top, Heath, Allotment, Clay loam, Loamy sand, Spanish) with pH range 4.5–7.9 and LOI 3.1–23.7%.
- Experimental setup: UK and Spanish collaborations; seed and tuber exchange; some movement of soil between countries due to regulatory constraints.
- Sampling plan: crops harvested at maturity; soils sampled (random or targeted); pore water collected via rhizons; irrigation water sampled.
- Sample handling: post-harvest washing, freezing at -20°C; soils dried (air or oven) and ground; pore waters filtered and acidified; samples prepared for digestion or extraction as required.

## Analytical methods and quality control
- Analytes: Ca, Cs, K, Mg, Sr; NH4-N; NPOC; plus pore-water and irrigation-water metrics.
- Technologies:
  - ICPMS for Cs and Sr.
  - ICPOES for Ca, K, Mg.
  - TOC-L with TNM-L for NPOC.
- Sample preparation:
  - Digestion with aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes using a microwave system.
  - BaCl2 extraction for soil subsets.
  - Pore waters and irrigation waters analyzed directly after filtration and acidification.
  - Dilution: all samples diluted 100-fold prior to analysis.
- Quality assurance:
  - Internal standards (Ga, In, Re) to monitor drift and matrix effects.
  - External calibration; LODs calculated from blanks.
  - Contamination minimization through non-metallic containers and agate tools.
  - Data entry tracked in Excel; about 20% of data validated independently.
- Documentation and references cited for methods (e.g., Allen 1989; Lofts et al. 2001).

## Data structure and metadata
- Data organized into multiple tables (13–14 data dictionaries) with explicit field definitions:
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
  - PlantGrowthStudy_Soil_ElementalConcentrations (continues)
  - PlantGrowthStudy_PoreWater_ElementalConcentrations (continues)
- Key measurement units:
  - Wood/dry-mass basis for crops: mg/kg for K, Ca, Mg, Sr; Cs reported with specific notes on detection limits.
  - Pore water: mg/L for Ca, K, Mg; µg/L for Cs and Sr; NPOC in µg/L; Ti as a potential contamination marker.
- Includes unique sample identifiers, crop-soil associations, year of harvest, and replication details.
- Comprehensive notes fields for data rows and explicit handling of below-LOD cases and non-reported values.

## Provenance, reproducibility, and data quality
- Data generated under Good Laboratory Practice; careful contamination controls and documentation enable traceability.
- Detailed procedural notes allow replication (sample prep, digestion conditions, extraction methods, calibration, and QA procedures).
- Data validation performed (partial cross-checks) to enhance reliability.
- Clear provenance links to contributing institutions (UKCEH and University of Extremadura) and the CONFIDENCE/CONCERT EJP framework.

## Accessibility, reuse, and documentation
- Data stored in Microsoft Excel workbooks with accompanying instrument reports and data dictionaries to support discoverability and reuse.
- Each data row and table includes descriptive field names and units to facilitate integration with other datasets.
- Acknowledgements and references provide context and provenance for methods and collaboration.

## Considerations and limitations for data stewardship
- Extraction method limitations:
  - AR (aqua regia) extraction shows partial recovery for K in soils (51–63%); clays affect dissolution and total-extractable estimates.
- Data gaps and detection issues:
  - Some Cs data flagged as below detection limit or not reported; several fields marked n/a where not applicable.
  Some samples are labeled as 'Unused' (no crops grown in those soils) or have aggregated notes for multiple samples.
- Variability in sample types and methods:
  - Multiple extraction/analysis schemes (AR vs BaCl2) and differing units across tables require careful harmonization for cross-table analyses.
- Pore water and irrigation water data may be limited by sampling scope and end-of-study collection constraints.

## Implications for data governance and sharing
- Rich, table-driven metadata and explicit unit definitions support discovery and reuse by data stewards, researchers, and end-users.
- To maximize interoperability, consider harmonizing variable naming and units across datasets and documenting any method-specific biases (e.g., AR recoveries) in a central data quality report.