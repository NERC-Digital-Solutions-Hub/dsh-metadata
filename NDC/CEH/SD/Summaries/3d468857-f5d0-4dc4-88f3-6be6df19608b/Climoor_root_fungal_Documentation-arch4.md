# Soil sampling

## Overview
- Study date: 1 April 2015; climate treatments were inactive for 6 months prior to sampling.
- Objective: minimize destructive sampling by limiting soil core extractions to a single 8 cm diameter core per plot, yielding 3 replicates across control, drought, and warming treatments.
- Sampling context: cores taken near the base of Calluna vulgaris shrubs; samples stored at 4°C until processing.

## Data collected and processing methods

- Root extraction and identification
  - C. vulgaris roots isolated by sectioning cores (1 cm depth chunks), washed to remove soil, and verified to be C. vulgaris before collection.
  - Large roots (>1 mm) identified by distinctive woody, kinked morphology; fine roots confirmed via tracing to larger connected roots.
  - Necrotic/rotten roots discarded; cleaned roots stored in deionised water at 4°C for measurements.

- Root measurements (WinRHIZO)
  - Metrics: root length, diameter, number of root tips; analysis performed on flatbed scanner with 5 mm water depth.
  - Fine roots (≤1 mm) targeted for microscopy; other roots dried at 70°C for dry weight data.
  - Parameters captured via WinRHIZO: analyzed region area, total root length, total surface area, average diameter, length per volume, total root volume, and root tip count.

- Fungal colonisation measurements
  - Fine root fragments underwent chemical pretreatment (KOH) and rinses; stained with vinegar-ink solution for microscopy.
  - Ericoid mycorrhizal (ErM) colonisation identified by hyphal coils within cells using a compound microscope with a 40x objective.
  - DSE (Dark Septate Endophytes) also scored.
  - Colonisation scored per root segment with detailed categorical schemes (0% to 100% ErM; various intervals including 0-1%, 1-10%, 10-50%, 50-90%, 90-100%); counts recorded for multiple root segments across Root 1–5.
  - Methodological rigor supported by bleaching concentration/duration trials and reference photographs to ensure consistency.

## Data structure and schema

- Dataset size: 72 rows, 53 columns.
- Key fields
  - Entry/ID: Unique plot-depth combination.
  - Plot: Plot number.
  - Depth: Sample depth in cm.
  - Treatment: One of warming, control, drought.
  - AnalysedRegionArea_cm2, Length_cm2, SurfArea_cm2: WinRHIZO analysis areas and metrics.
  - AvgDiam_mm: Average root diameter.
  - LenPerVol_cm_m3: Length per volume metric.
  - RootVol_cm3: Total root volume analyzed.
  - Tips: Total root tips identified.
  - DryWeightAll_g, DryWeight2mm_g: Dry weights for all roots and for >2 mm roots.
  - Length_Root1 to Length_Root5: Length measurements for root segments.
  - ErM_0_Root1 to ErM_0_Root5; ErM_0_1_Root1 to ErM_0_1_Root5; ErM_1_10_Root1 to ErM_1_10_Root5; ErM_10_50_Root1 to ErM_10_50_Root5; ErM_50_90_Root1 to ErM_50_90_Root5; ErM_90_100_Root1 to ErM_90_100_Root5.
  - DSE_Root1 to DSE_Root5: Counts of root segments with DSE presence.
  - Additional columns capture longitudinal and segment-level colonisation data across five root samples per plot.

## Quality control and data validation

- Consistency checks
  - Root bleaching experiments conducted at 10% and 2.5% KOH for varying durations; results compared to ensure no method-induced differences.
  - Preliminary testing and reference photographs established before full data collection to prevent measurement drift.
- Data integrity
  - Outlier and improbable value checks performed on the dataset.

## Data management and accessibility

- Sample handling and storage
  - Roots stored in 4°C conditions; careful handling to preserve moisture and prevent contamination.
- Documentation and metadata
  - Detailed column descriptions included (unit, description) for most variables to support discoverability and reuse.
  - Clear workflow from field collection to image analysis and microscopy.

## Use cases and considerations for data leaders

- Potential uses
  - Multi-treatment comparisons of root architecture and ErM/DSE colonisation under warming, drought, and control conditions.
  - Integration with other datasets to model belowground responses to climate treatments in heathland ecosystems.
  - Analyses of relationships between morphological root traits andExtent of mycorrhizal colonisation.
- Considerations and challenges
  - High dimensional colonisation data (multiple_root_segment across several roots) requiring careful aggregation for cross-study comparability.
  - Verifying root identity and consistent categorisation of ErM/DSE across datasets to maintain data standardisation.
  - The dataset is richly annotated with metadata, but harmonisation with external studies may require alignment of units and scoring schemes.

## Highlights for governance and future improvements

- Strong emphasis on data quality, traceability, and methodological transparency.
- Comprehensive metadata supports reproducibility and cross-study synthesis.
- Opportunities to enhance discoverability and interoperability through standardised data schemas and shared ontologies for root traits and mycorrhizal colonisation.