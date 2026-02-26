# Soil physico-chemical properties 2007 [Countryside Survey], Great Britain

## Overview
- A dataset describing soil physico-chemical properties collected in 2007 across Great Britain as part of Countryside Survey (CS).
- Up to 591 1km squares surveyed; soils sampled from 0-15 cm depth in relation to five Main Plot corners within each square.
- Columns cover site identifiers, year, and a suite of soil properties and derived metrics.
- Data are published as part of Countryside Survey outputs and come with formal acknowledgment and licensing requirements.

## Data content and structure
- Core variables (examples):
  - SQUARE, PLOT, YEAR
  - PH (fresh soil pH in water)
  - LOI (loss on ignition)
  - C_CONC_LOI (carbon concentration from LOI; derived as 0.55 x LOI)
  - C_STOCK_LOI (carbon stock from LOI; derived as 0.55 x LOI)
  - BULK_DENSITY, MOISTURE
  - N_PERCENT, N_STOCK
  - PO4_OLSEN (Olsen Phosphorus)
  - LC07, LC07_NUM (ITE Land Class 2007)
  - COUNTRY, COUNTY07, EZ_DESC_07 (environmental descriptors)
- Derived measures:
  - C_CONC_LOI and C_STOCK_LOI use a CS-specific 0.55 conversion to estimate carbon content from LOI.
- Sample scope:
  - LOI: up to 3145 black core samples analyzed.
  - Olsen-P: up to 1280 samples analyzed (original 256 squares with 5 X-plots per square).
  - Total N: up to 1280 samples analyzed.
- Metadata and descriptors to aid discovery and interpretation (e.g., Land Class, country, and environmental zone descriptions).

## Measurement protocols and laboratory methods
- Soil pH measurements:
  - Two measurements per subsample: pH in water and in 0.01M CaCl2.
  - Fresh soil pH in water: 10 g soil with 25 ml deionised water; measurements taken after 30 minutes, with calibrated, temperature-consistent buffers; electrode cleaned between measurements.
- Quality control for pH:
  - Batch calibration checks with pH 4 and pH 7 buffers; re-calibration if deviations >0.02 pH units.
  - Standards, certified reference soil, and duplicates included per batch of 25 samples.
- LOI (Loss on Ignition):
  - Up to 3145 black cores analyzed; soil dried, weighed, and combusted (105°C: 16 h; 375°C: 16 h); LOI calculated from weight loss.
  - Uses CEH Lancaster UKAS-accredited SOP3102; cross-checks with standards and repeats in batches.
  - Rationale: CS2007 reanalyzed CS2000 soils with the 1978 LOI method for consistency across CS surveys.
- Bulk Density (BD) and texture:
  - Same material as LOI; BD determined with exact core dimensions and weights; stone content considered to adjust density.
  - QC notes acknowledge lack of a perfect control soil but propose proxies (consistency with soil type expectations, cross-checks with previous surveys).
- Olsen-P:
  - Up to 1280 samples; 5 g air-dried, sieved soil extracted with 100 ml 0.5M NaHCO3 (pH 8.5); phosphorus quantified by molybdenum blue colorimetry with a Skalar analyzer.
  - Critical methodological considerations: drying effects, extraction temperature, soil:solution ratio, organic matter influence; to ensure comparability with CS2000.
  - QA: replicate analysis plus standard soil and certified reference soil per 25-sample batch; consistent extraction conditions with CS2000.
- Total Nitrogen:
  - Up to 1280 samples analyzed using CEH Lancaster UKAS-accredited SOP3102 with Elementar Vario-EL analyzer.
  - Combustion, oxidation, and detection workflow described; in-house reference materials used for QC.
- Quality assurance and documentation:
  - All QA/QC procedures align with Defra/NERC/BBSRC Joint Codes of Practice.
  - Detailed protocols, cross-comparisons, power analyses, and statistical approaches are documented in CS Soils Manual (CS Technical Report No. 3/07) and related CS publications.

## Sampling design and coverage
- Sampling strategy:
  - Great Britain stratified by Land Classes (ITE framework) to capture environmental gradients.
  - 591 1km squares surveyed in 2007 (289 England, 107 Wales, 195 Scotland).
  - Field collection centered on the western corner of Main Plots in 2007; earlier surveys used other corners to ensure spatial spread.
- Power and representativeness:
  - Power analyses conducted prior to sampling to ensure robust reporting for major measurements (pH, LOI) across broad habitats and countries; smaller samples suffice for some analytes (e.g., metals) while retaining required confidence.
- Processing and archiving:
  - Field and laboratory processing protocols provided; cores logged, processed for basic measurements, chemical analyses, and archiving.
- Documentation and cross-lab validation:
  - Procedures cross-checked where methodologies changed; inter-lab comparisons and re-analyses performed as needed.
- Documentation availability:
  - Key methodological details compiled in Emmett et al. (2008) Countryside Survey Soils Manual and CS2007 technical reports.

## Data usage, licensing, and provenance
- Data ownership and rights:
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; copyright and database rights apply.
- Acknowledgement requirements:
  - All uses must acknowledge Countryside Survey data and CEH ownership on copies, publications, presentations, and any derived products.
- Primary references and lineage:
  - Soils Manual (Emmett et al., 2008) and Countryside Survey technical reports provide comprehensive methods and QA details.
  - Related CS outputs and UK results papers document broader survey methodology and national results.

## Relevance for data leadership and strategy
- Provides a rich, well-documented soil property dataset with standardized protocols and QA aligned with high governance standards.
- Clear metadata (LC07, EZ_DESC_07, COUNTRY, COUNTY07) supports cross-context analysis and integration with other datasets.
- Demonstrates emphasis on consistency over time (1978 LOI method retained for CS2007) to enable longitudinal comparisons.
- Licensing and acknowledgement requirements highlight governance considerations for data reuse and attribution.
- Sampling design and power analysis insights support planning for representative data collection and prioritization of future data gathering efforts.