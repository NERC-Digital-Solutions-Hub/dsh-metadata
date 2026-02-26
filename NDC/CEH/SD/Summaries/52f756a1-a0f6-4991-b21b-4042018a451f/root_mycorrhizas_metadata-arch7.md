# Site description

- Location and context
  - AFEX project area at the Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Amazonas, Brazil.
  - Coordinates: 02° 25' 00'' S, 59° 43' 00'' W.
  - Climate: mean air temperature ~26 °C; mean annual precipitation ~2,400 mm; relative humidity 75–92% across the year.

- Experimental design (AFEX Experiment)
  - Full factorial nutrient addition with eight treatments: Control, N, P, cations (Ca, Mg, K), and their combinations (N+P, N+cations, N+P+cations).
  - 4 replicates per treatment, arranged in 4 independent blocks with at least 250 m spacing between blocks.
  - Total: 32 plots, each 50 m × 50 m.
  - Measurements concentrated in the central 30 m × 30 m area of each plot.

- Spatial layout and data-ready structure
  - Plots laid out on plateau with a consistent grid; blocks span 1–4 and contain 8 plots each.
  - For GIS-ready analysis, data describe spatial units at multiple scales: blocks, plots, and central focus area (30 m × 30 m).

- Root sampling and biomass estimation (data collection)
  - In each plot (n=32), five 12 cm-diameter, 30 cm-deep ingrowth cores installed August 2017 within the central 30 × 30 m area (2 cm plastic mesh bags).
  - Cores collected every three months; four cores per plot aggregated per time interval (N=64 across all plots and depths).
  - Fine-root biomass in November 2017–February 2018 (wet season mid-point) used for analysis.
  - Biomass extrapolation to 180 minutes using Michaelis-Menten asymptotic curve to estimate sampling efficiency at longer durations (60–180 minutes).

- Root processing and mycorrhizal assessment (data collection)
  - Fine roots from 0–10 cm depth subsampled; mycorrhizal colonisation determined from root tips (<1 mm dia).
  - Root cleaning, clearing, staining, and mounting following tropical-root protocols:
    - Clearing with 2.5% KOH, autoclaving (~120°C, ~10 min).
    - Bleaching with alkaline H2O2 (~30 min).
    - Acidification with 2% HCl (~30 min).
    - Staining with Trypan Blue (0.05% for 30 min).
  - Quantification: percentage of root length colonised by AM fungi, based on 10 uniformly stained 1 cm root fragments examined at 40×.

- Data schema and variables (spreadsheet details)
  - Block: block identifier where plots are installed (1–4).
  - Plot: plot identifier within each block (1–8).
  - TRT: nutrient treatment applied (8 categories; Control, P, N, cations, N+P, N+cations, N+P+cations).
  - no_am: percentage of root length not colonised by arbuscular mycorrhiza.
  - hyphae: percentage of root length colonised by AM hyphae.
  - hyphae_arbuscule: percentage of root length with hyphae and arbuscule structures.
  - hyphae_vesicle: percentage of root length with hyphae and vesicle structures.
  - hyphae_arb_ves: percentage of root length with AM structures including arbuscules and vesicles.
  - total_col: total percentage of root length colonised by mycorrhizal structures.

- GIS and data-management implications
  - Spatially explicit design (blocks, plots, central sampling area) enables map-based visualization of treatment effects and root-mycorrhizal patterns.
  - Multiple data layers to integrate: plot boundaries, treatment allocation, soil depth strata (0–10 cm, 10–30 cm), sampling times, and AM colonisation metrics.
  - Data integration challenges addressed by a structured spreadsheet schema and clear variable definitions to support cleaning, standardization, and transformation across datasets.

- Key references (methods and context)
  - Metcalfe et al. (2007) on root extraction method and sampling efficiency.
  - McCormack et al. (2015); McGonigle et al. (1990); Brundrett et al. (1984); Wurzburger & Wright (2015) for AM colonisation assessment and interpretation.
  - Araújo et al. (2002) for site climate context.

- Considerations for quality and reproducibility
  - Data are collected across multiple plots, depths, and time points, requiring careful harmonization of units and time references.
  - Potential GIS challenges include aligning non-uniform data sources, ensuring consistent plot delineation across blocks, and maintaining resolution suitable for map-based visualization of nutrient treatments and mycorrhizal status.