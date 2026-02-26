# Soil sampling

- Date and context: Sampling conducted on 1 April 2015; climate treatments had been inactive for 6 months.
- Sampling protocol: Destructive sampling minimized by limiting soil cores to a single 8 cm diameter core per plot (0–8 cm depth), yielding 3 replicates per treatment (control, drought, warming).
- Location and handling: Cores extracted near Calluna vulgaris shrubs, sealed in plastic bags to retain moisture, and stored at 4°C until processing.

## Root extraction and identification

- Extraction method: Cores cut into 1 cm subsections, soaked in tap water for 20 minutes with occasional agitation to loosen soil; only C. vulgaris roots retained using forceps and thoroughly washed.
- Identification criteria: Larger C. vulgaris roots characterized as dark, woody, kinked at right angles; fine roots often reddish and non-woody; fine roots collected only after verification by tracing to larger identifiable roots.
- Sample preservation: Cleaned roots stored in deionised water at 4°C for measurements; necrotic/rotting roots discarded.

## Root measurements

- Measurement tool and setup: Root length, diameter, and number of root tips measured with WinRHIZO v3.2 on a flatbed scanner; roots positioned to avoid overlap and submerged in 5 mm of tap water.
- Focus and parameters: Fine roots (≤ 1 mm) targeted for microscopy analyses; acquisition parameters configured in professional mode with 24-bit color and 300 dpi.
- Data collection: Total length, surface area, and average diameter recorded; length per volume and root volume calculated; dry weights obtained after oven-drying roots (< and > 2 mm) at 70°C for 24 h.

## Fungal colonisation measurements

- Preparation: Fine root fragments treated with 10% KOH for 20 h, then rinsed; fragments stained in a 5% vinegar-ink solution and heated to 90°C for 15 minutes; subsequently acidified in tap water with vinegar.
- Assessment method: Direct counting unreliable; Ericoid mycorrhizal (ErM) colonisation inferred by detecting hyphal coils within cells using a compound microscope with a scale bar graticule; 2 mm passes along root lengths examined to determine ErM presence.
- Scoring: ErM colonisation categorized by the level of hyphal coil presence across cells; presence vs absence determined; difficulties acknowledged (mycelia, hyphae, and pigmentation can obscure observations).
- DSE assessment: Dark Septate Endophytes (DSE) recorded alongside ErM observations.

## Quality control

- Method validation: Tested 10% and 2.5% KOH concentrations and durations to confirm no discernible differences.
- Method stability: Colonisation scoring methodology validated with preliminary testing and reference photographs to prevent measurement drift.
- Data integrity: Data screened for outliers and improbable values.

## Data structure and variables

- Dataset size: 53 columns and 72 rows.
- Key identifiers and structure: 
  - ID and Plot identifiers; Depth (cm); Treatment (warming, control, drought).
- Root morphometrics (WinRHIZO-derived): 
  - AnalysedRegionArea_cm2, Length_cm2, SurfArea_cm2, AvgDiam_mm, LenPerVol_cm_m3, RootVol_cm3, Tips, DryWeightAll_g, DryWeight2mm_g.
  - Root length measurements across five sub-samples (Length_Root1 to Length_Root5).
- ErM and DSE colonisation data: 
  - ErM_0_RootN to ErM_0_1_RootN, ErM_1_10_RootN, ErM_10_50_RootN, ErM_50_90_RootN, ErM_90_100_RootN (counts per 2 mm root segment with corresponding percentages) for Root1–Root5.
  - DSE_RootN counts per 2 mm root segment (Root1–Root5) across similar subdivisions.
- Purpose: Dataset designed for standardized environmental monitoring outputs, enabling quality-assured analysis of root morphology and fungal colonisation across treatments, with emphasis on data provenance, comparability, and storage for portal upload.