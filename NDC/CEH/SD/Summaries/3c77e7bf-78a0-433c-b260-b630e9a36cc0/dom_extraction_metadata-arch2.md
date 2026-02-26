# Data deposit for: Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S.

## Aim and scope
- Provide a deposited dataset of water chemistry and elemental content of dissolved organic matter (DOM) extracted from UK freshwaters (2018–2019).
- Data are quality controlled and prepared to enable environmental health monitoring and policy performance assessment over time.
- Methods are described in a companion manuscript (A comparison of methods for the extraction of dissolved organic matter from freshwaters, Water Research 2020).

## Data structure and files
- Five CSV files:
  - DOMextraction SITES: waterbody types, site identifiers, elevation, catchment area, pH, DOC, POC, dominant soil type; minimum/maximum values for each waterbody type.
  - DOMextraction CHN: DOC concentration, total %C, %N, %H, OrganicC%, processing rate, recovery percentage; values relative to RE samples.
  - DOMextraction REreps: total C, N, H of DOM in replicates after rotary evaporation.
  - DOMextraction RECOVERY: volume, DOM mass, carbon content, DOC mass, DOC concentration, and recovery percentage used to calculate overall recovery.
  - DOMextraction SCORES: method details (rate, recovery, cost), large equipment cost, and the overall scoring metric (sum of rate, recovery, cost scores plus equipment penalty) and final rank.
- All data are stored as CSVs and linked by site and method identifiers.

## Methods and quality control
- Data collection and generation methods are outlined in the accompanying manuscript (Water Research 2020).
- Data quality control applied, including handling values below detection limits.
- Extraction methods represented in CHN/RECOVERY/SCORES include: DRY-6, RE (rotary evaporation), RO-DF, RO-RE, SPE, DRY-F, FD, DIA-FD, and DIA-FH.
- Recovery calculations account for differences in sample processing and filtration (e.g., recovery can exceed 100% due to filter size differences).

## Key variables and meanings
- Waterbody characteristics (SITES): type (headwater, stream, lake/loch, reservoir inlet/outlet), site numbers, elevation, catchment area, pH, DOC, POC, dominant soil type.
- DOM composition (CHN): DOC concentration; total %C, %N, %H; OrganicC% relative to total carbon; processing rate; time; recovery; comparison relative to reference (RE) samples.
- DOM mass and concentration (RECOVERY): sample volume, DOM mass, DOM total C, DOC mass, DOC concentration, DOC mass per volume, and recovery percentage.
- Processing performance (SCORES): number of samples (N), mean rate, mean recovery, cost per sample, large equipment cost, and composite scores; higher performance yields lower scores; overall rank is 1 for best combination of rate, recovery, cost, and equipment impact.

## How analysts can use the dataset
- Monitor environmental health by comparing DOM composition and DOC across UK freshwater types and sites.
- Assess method performance and cost-effectiveness via SCORES (ranking of extraction methods).
- Link water chemistry with DOM content to evaluate ecosystem carbon dynamics and nutrient processing.
- Integrate with other datasets for broader assessments of environmental policy performance over time.

## Access, provenance, and considerations
- Data deposited with provenance details in the 2018–19 UK freshwater study; methods align with the Water Research 2020 manuscript.
- Quality-controlled data include explicit notes on recovery and method-specific processing differences.
- Users should consider methodological differences across extraction techniques when interpreting recovery and composition results (e.g., RE relative references, filtration effects).

## Practical implications for monitoring and policy
- Provides a standardised, citable dataset to track changes in water chemistry and DOM content across years and sites.
- Enables cross-site comparisons by waterbody type and by extraction method, supporting evaluation of environmental health standards.
- The scoring framework helps identify cost-effective and efficient methods for routine monitoring, aiding resource allocation decisions.