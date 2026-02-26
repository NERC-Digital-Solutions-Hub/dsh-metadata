# Soil sampling

- Sampling date and context
  - Conducted on 1 April 2015
  - Climate treatments (warming, drought) inactive for 6 months prior to sampling
- Experimental design
  - Single 8 cm diameter soil core per plot (0-8 cm depth) to minimize destructive sampling
  - 3 replicates per treatment (control, drought, warming)
  - Cores taken near the base of Calluna vulgaris shrubs
  - Cores sealed in plastic bags to retain moisture and stored at 4°C until processing

## Root extraction and identification

- Procedures
  - Cores cut into 1 cm subsections; soaked in tap water for 20 minutes with occasional agitation
  - Only roots confidently identified as Calluna vulgaris were removed
  - Larger roots (>1 mm) identified by characteristic dark, woody, kinked morphology at stem junctions
  - Fine roots identified by tracing back to larger identifiable roots; necrotic/rotting roots discarded
  - Cleaned roots stored in deionised water at 4°C for measurements

## Root measurements

- Measurements and instrumentation
  - Root length, diameter, and number of root tips measured with WinRHIZO v3.2
  - Roots laid flat in 5 mm of tap water; scanned with 300 dpi, 24-bit color, professional mode
  - Fine roots (≤1 mm diameter) focused on for microscopy
  - Larger roots (>2 mm) dried at 70°C for 24 h to obtain dry weights
- Data captured
  - WinRHIZO outputs including area, length, surface area, average diameter, length per volume, root volume, tips
  - Dry weights for different root size classes (all roots and >2 mm)

## Fungal colonisation measurements

- Ericoid mycorrhizal (ErM) assessment
  - Fine root fragments treated with 10% KOH for 20 h, then rinsed
  - Stained with 5% vinegar-ink solution, heated to 90°C for 15 minutes, then rinsed and acidified
  - Hyphal coils observed under compound microscope (40x magnification)
  - Root sections prepared longitudinally (5 sections per subsection); examined along root length
  - ErM colonisation categorized by presence of hyphal coils across cells; direct counting unreliable due to occlusions
  - Presence/absence and degree of ErM colonisation recorded; Dark Septate Endophytes (DSE) also identified

## Quality control

- Method validation
  - Compared different KOH concentrations (10% vs 2.5%) and durations (10, 20, 30 min); no discernible difference found
  - Preliminary testing and reference photographs established for colonisation scoring to ensure consistency
  - Data checked for outliers and improbable values

## Details of data structure

- Dataset size
  - 53 columns and 72 rows
- Key fields
  - A: Entry (ID); B: Plot; C: Depth (cm); D: Treatment (warming, control, drought)
  - E: AnalysedRegionArea_cm2; F: Length_cm2; G: SurfArea_cm2; H: AvgDiam_mm; I: LenPerVol_cm_m3; J: RootVol_cm3
  - K: Tips; L: DryWeightAll_g; M: DryWeight2mm_g
  - N–R: Length_Root1 to Length_Root5 (root lengths per subsection)
  - S–W: ErM_0_Root1 to ErM_0_Root5 (0% ErM segments)
  - X–AQ, AS–AV, AX–BA: ErM_0_1, ErM_1_10, ErM_10_50, ErM_50_90, ErM_90_100 per Root1–Root5 (counts per 2 mm segment)
  - AW–BA: DSE_Root1 to DSE_Root5 (counts of DSE segments)
- Data structure purpose
  - Comprehensive capture of root morphology, biomass, and detailed ErM/DSE colonisation across multiple roots and depth plots, enabling correlation analyses and modelling of mycorrhizal associations with root traits under different climate treatments