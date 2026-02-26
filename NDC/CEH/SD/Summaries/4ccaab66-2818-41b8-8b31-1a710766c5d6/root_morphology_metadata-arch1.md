# AFEX Experiment

## Study location and climate
- Conducted in the AFEX project area at the Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Brazil.
- Climate: mean air temperature ~26°C; mean annual precipitation ~2,400 mm; relative humidity 75–92% across seasons.

## Experimental design
- Full factorial nutrient addition with eight treatments: control, N, P, cations (Ca, Mg, K), and combinations (N+P, N+cations, N+P+cations).
- 4 replicates per treatment across 4 independent blocks (total 32 plots).
- Plot size: 50 m x 50 m; central 30 m x 30 m area used for main measurements.
- Nutrient application rates (annual): N 125 kg/ha (urea); P 50 kg/ha (triple superphosphate); Ca 50 kg/ha; Mg 20 kg/ha; K 50 kg/ha (KCl).
- Spatial design ensures at least 250 m between blocks.

## Root sampling framework
- In each plot (n=32), five 12 cm-diameter, 30 cm-deep ingrowth cores installed in August 2017 within the central 30 x 30 m area.
- Cores collected every three months; cores homogenised by plot and soil depth (0–10 cm; 10–30 cm); total N per plot = 64.
- Targeted fine roots produced between Nov 2017 and Feb 2018 (middle of wet season); root extraction conducted in 60-minute intervals.
- Extrapolation to 180 minutes using Michaelis-Menten asymptotic curve to estimate total root biomass sampled.

## Root processing and morphological analysis
- Fine roots (<2 mm) subsampled from both depths; dried at 60°C for dry mass.
- Roots scanned at 600 dpi and analyzed with WinRHIZO to obtain:
  - Root mean diameter (mm)
  - Total root length (cm)
  - Root area (cm²)
  - Root volume (cm³)
- Derived metrics:
  - Specific root length (SRL, cm g⁻¹)
  - Specific root area (SRA, cm² g⁻¹)
  - Root tissue density (RTD, g cm⁻³)

## Data structure and variables
- Spreadsheet fields:
  - Block: 1–4 (experimental blocks)
  - Plot: 1–8 within each block
  - TRT: 8 nutrient treatments
  - Depth: 0–10 cm or 10–30 cm
  - root_volume (cm³)
  - tot_weight (g)
  - SRL (cm g⁻¹)
  - SRA (cm² g⁻¹)
  - RTD (g cm⁻³)
  - diameter (mm)

## Purpose and analytical potential
- Enables evaluation of how N, P, and cation additions (and their interactions) influence fine-root production and morphology across soil depths.
- Facilitates analysis of treatment and depth effects on root biomass and structural traits, with data standardized across replicates, blocks, and sampling times.
- Method includes careful data provenance and a clear pathway for extracting (and extrapolating) biomass over a defined sampling window, supporting robust comparisons and modeling.

## References
- Araújo AC (2002). J Geophys Res.
- Metcalfe DB et al. (2007). New Phytologist.
- Metcalfe DB et al. (2008). Plant and Soil.