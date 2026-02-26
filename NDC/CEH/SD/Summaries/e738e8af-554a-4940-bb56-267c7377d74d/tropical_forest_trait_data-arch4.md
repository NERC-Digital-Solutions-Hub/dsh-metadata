# Danum_Valley_Seedling_Traits.csv

## Overview
- Dataset documenting trait measurements for 399 seedlings representing 15 species, across primary (DVCA) and adjacent selectively logged forests (USFR) in Sabah, Malaysia.
- Sampling occurred January–February 2020, following mast fruiting events in Sept–Oct 2019.
- Seedling plots: established 1 m2 plots in both primary and logged forests; 87 plots in primary, 96 in logged (actively restored vs naturally regenerating). trait sampling covered 75 plots (46 primary; 26 logged) with some plots not sampled due to mortality or access issues.
- Sampling strategy: three seedlings per plot, plus an additional ten seedlings for foliar analyses; supplementary samples taken 20–40 m from plots when necessary to improve replication.
- Species and forest coverage: 15 species analyzed; seven species found in more than one plot and sampled in both forest types (except Dryobalanops lanceolata, sampled only in logged forest). Some species sampled only in primary or only in logged forest.
- Life forms: most studied species are canopy or emergent trees; one liana (Agelaea sp.) and one small-tree species (Buchanania sessifolia) included.

## Study Site and Sampling Context
- DVCA: unlogged primary forest, 438 km2, high rainfall (2305 mm/year), mean temperature ~25.8°C; upper Segama River catchment.
- USFR: adjacent selectively logged forest, historically logged 1981–1993; varied logging intensity; reduced-impact logging trial implemented in 1993 for some areas; rehabilitation efforts under Innoprise-FACE Foundation.
- Plots established during mast fruiting: seedling trials located both inside DVCA ForestGEO Danum Valley 50 ha plot and INDFORSUS project plots within USFR.

## Sampling Design and Species
- Species representation: mixed approach to cover >80% of seedlings on plots; enables intraspecific comparisons between logged and unlogged conditions.
- Plot-level sampling: three individuals per seedling plot; additional sampling outside plots to exceed replication; where needed, extra samples collected 20–40 m away to improve trait mean estimates.
- Logged forest details: 26 plots (19 actively restored with management, 7 natural regeneration) sampled within this study; some plots inaccessible or with high seedling mortality limiting sampling.

## Trait Measurements and Laboratory Analyses
- Measured 14 traits per seedling:
  - Biomass components: Leaf Mass Fraction (LMF), Root Mass Fraction (RMF), Total Biomass
  - Morphology: Leaf Mass per Area (LMA), Leaf Thickness, Leaf Area:Shoot Area (LA:SA), Root Length:Shoot Length (RS), Specific Maximum Root Length (SMRL)
  - Leaf chemistry: Leaf Nitrogen (N leaf), Phosphorus (P leaf), Calcium (Ca leaf), Magnesium (Mg leaf), Potassium (K leaf)
  - Nutrient balance: Leaf Nitrogen to Phosphorus ratio (N:P)
- Field-to-lab workflow:
  - Seedslings harvested in morning; separated into above- and below-ground organs; kept moist during transit.
  - Measurements: longest root and shoot lengths; shoot diameter measured below first branch; leaf area via flatbed scanning and ImageJ; leaf thickness measured on three leaves; LFP measured with digital force gauge.
  - Drying: biomass determined after oven-drying at 50°C for 48 hours.
  - Leaf chemistry: leaves ground, digested with H2O2–H2SO4; N and P via colorimetry; Ca, K, Mg via spectrometry; moisture content used to correct to oven-dry basis.
  - N:P calculated as N leaf divided by P leaf.
- Data handling: a subset of leaves pooled per plot for foliar analyses.

## Data Structure and Fields
- Primary data file: Danum_Valley_Seedling_Traits.csv
- Key fields (with descriptions and units):
  - Date (Date collected)
  - Forest (Primary or Logged)
  - Management (Natural Regeneration or Active Restoration)
  - Species (Scientific name)
  - Family (Plant family)
  - Seedling.Plot (Plot identifier)
  - Individual (Seedling identifier)
  - Biomass (Total biomass, g)
  - RL:SL (Root Length : Shoot Length, mm/mm)
  - LMF (Leaf Mass Fraction, g g-1)
  - RMF (Root Mass Fraction, g g-1)
  - LMA (Leaf Mass per Area, g m-2)
  - Leaf.Thickness (Leaf thickness, mm)
  - LFP (Leaf Force to Punch, N)
  - LA:SA (Leaf Area : Shoot Area, cm2 per mm2)
  - Leaf.N (Leaf nitrogen, mg g-1)
  - Leaf.P (Leaf phosphorus, mg g-1)
  - Leaf.Ca (Leaf calcium, mg g-1)
  - Leaf.K (Leaf potassium, mg g-1)
  - Leaf.Mg (Leaf magnesium, mg g-1)
  - Leaf.N:P (Leaf N:P ratio, g g-1)
  - SMRL (Specific Maximum Root Length, mm g-1)
- Each field includes methodological notes on calculation where applicable (e.g., how LMA, LA:SA, and SMRL are derived).

## Data Quality, Limitations, and Gaps
- Mortality and accessibility: high seedling mortality in logged plots and some access constraints limited sampling success in certain plots.
- Coverage gaps: some species sampled only in primary or only in logged forests; Dryobalanops lanceolata sampled only in logged forest due to absence in primary plots.
- Plot representation: 75 of the available plots were sampled for trait data, with potential geographic and temporal gaps due to mast fruiting timing and sampling windows.
- Across-plot variability: high variability in seedling establishment and survival across plots may influence trait means; additional samples were taken beyond plots when necessary to improve replication.

## Data Governance, Access, and Reusability
- Rich metadata and explicit trait definitions support discoverability and reuse.
- Clear documentation of methods, instruments, and calculation steps (e.g., N:P, SMRL) enhances reproducibility.
- Data are anchored to a single dataset with a consistent naming convention (Danum_Valley_Seedling_Traits.csv) and a defined field dictionary, facilitating integration with related forest dynamics and restoration datasets.
- For organizational use, dataset supports cross-forest comparisons of seedling functional traits, informs restoration and management strategies, and enables cross-site collaboration.

## Implications and Opportunities for Data Leaders
- Emphasize robust metadata and standardized measurement protocols to improve discoverability and interoperability across datasets and networks.
- Address data gaps proactively by documenting sampling limitations, mortality contexts, and plot-level constraints to guide future data collection and governance.
- Promote data integration by aligning field codes, units, and calculation methods (e.g., N:P, SMRL) with broader data schemas and ontologies.
- Encourage data-sharing practices with clear licensing, versioning, and provenance to maximize reuse by policy colleagues, researchers, and practitioners in forest restoration and ecology networks.