# Soil sampling

## Purpose and context
- Study of Calluna vulgaris roots under warming, drought, and control treatments.
- Sampling date: 1 April 2015; climate treatments inactive for 6 months prior.
- To minimize destructive sampling, only a single 8 cm diameter core per plot (0–8 cm depth) was collected, giving 3 replicates per treatment.
- Cores taken near the base of C. vulgaris shrubs; stored at 4°C until processing.

## Sampling and processing methods
- Cores cut into 1 cm subsections; submerged in tap water for ~20 minutes; soil aggregates loosened to form a uniform slurry.
- Only roots confidently identified as C. vulgaris were removed; larger roots identified by morphology; fine roots verified by tracing to larger roots.
- Necrotic/rotten roots discarded; cleaned roots stored in deionised water at 4°C for measurements.

## Root extraction and measurements
- Root metrics measured with WinRHIZO v3.2 (2005) on a flatbed scanner with roots in 5 mm water.
- Fine roots (≤1 mm) are the primary focus for microscopy; larger roots (>2 mm) dried at 70°C for dry weight data.
- Acquired data include: total root length, surface area, diameter, length per volume, total root volume, and number of root tips.
- Specific root lengths and multiple root-length measurements (Root1–Root5) are recorded.

## Fungal colonisation assessment
- Ericoid mycorrhizal (ErM) colonisation identified by presence of hyphal coils in root cells using a compound microscope (40×) with a scale bar.
- Preparation involved: 10% KOH soak, rinsing, staining with vinegar–ink, heating at 90°C, then rinsing and final observation.
- Quantification relies on presence/absence of coils across cells, with categorisation based on observed colonisation levels.
- DSE (Dark Septate Endophytes) also recorded per root.

## Quality control
- Method comparison: 10% vs 2.5% KOH at varying durations showed no meaningful differences.
- Preliminary testing with reference photographs to prevent measurement drift.
- Data checked for outliers and improbable values.

## Data structure and schema
- Dataset composition: 53 columns, 72 rows.
- Core identifiers and fields:
  - A: ID; B: Plot; C: Depth (cm); D: Treatment (warming, control, drought).
  - E–G: WinRHIZO-derived areas and lengths (AnalysedRegionArea_cm2, Length_cm2, SurfArea_cm2).
  - H: AvgDiam_mm; I: LenPerVol_cm/m3; J: RootVol_cm3; K: Tips; L: DryWeightAll_g; M: DryWeight2mm_g.
  - N–R: Length_Root1–Length_Root5 (cm).
  - S–W: ErM_0_Root1–ErM_0_Root5 (counts for 0% ErM colonisation).
  - X–BA and beyond: ErM and DSE colonisation counts categorized by root segments (0–1%, 1–10%, 10–50%, 50–90%, 90–100%) for Root1–Root5.
- Structure indicates per-plot, per-depth measurements with detailed ErM/DSE colonisation gradations across multiple root length samples.

## GIS-relevant implications
- Data are inherently spatial at the plot level and include depth-related measurements, enabling:
  - Map-based visualization of root density, length, surface area, diameter, and biomass per plot/depth.
  - Layered representation of ErM and DSE colonisation intensities across roots and treatments.
  - Integration with plot coordinates to produce spatial distributions, comparisons across warming/drought/control treatments, and potential time-series analyses if extended.

## Considerations for use
- Highly multi-dimensional dataset with many derived fields; careful data management required to align units and categories.
- Quality control measures documented, supporting data reliability for mapping and analyses.

## Potential data products
- Spatial maps of root metrics (length, surface area, diameter, biomass) by plot and depth.
- Visualisations of mycorrhizal and DSE colonisation patterns across treatments.
- Dashboards combining root structure metrics with treatment conditions for policy or outreach purposes.