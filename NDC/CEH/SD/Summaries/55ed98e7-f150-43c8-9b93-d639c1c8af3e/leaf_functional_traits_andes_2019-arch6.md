# Leaf functional traits dataset from three common garden sites along an elevation/temperature gradient in the Colombian Andes

## Overview
- A dataset of key leaf functional trait data collected from three common garden sites across an elevation/temperature gradient in the Colombian Andes.
- Collections occurred between June and August 2019.
- Available in two CSV files:
  - leaf_functional_traits_absolute_values.csv: absolute trait values
  - leaf_functional_traits_scaled_values.csv: scaled trait values
- The dataset focuses on eight midsuccessional Andean tropical montane forest species; some isolated values are missing due to instrument error or quality control during post-processing.

## Data sheets and column descriptions
- Absolute values (absolute values file):
  - Site: 1 = High elevation; 2 = Mid elevation; 3 = Low elevation
  - Species: genus and species (e.g. C.multiflora)
  - LMA: Leaf mass per unit area (g m^-2)
  - LT: Leaf thickness (mm)
  - LDMC: Leaf dry matter content (mg g^-1)
  - LA: Leaf area (cm^2)
  - LW: Leaf width (mm)
  - Nm: Leaf nitrogen (mass-based; g g^-1)
  - Na: Leaf nitrogen (area-based; g m^-2)
  - Pm: Leaf phosphorus (mass-based; g g^-1)
  - Pa: Leaf phosphorus (area-based; g m^-2)
  - d13C: δ13C (‰)
  - g1: Intrinsic water-use efficiency (kPa^0.5)
- Scaled values (scaled values file):
  - Site: 1 = N/A; 2 = High/ Mid / Low as applicable
  - Climatic.origin: 2 indicates cold- or warm-affiliated; 1 = N/A
  - Species: 2 indicates the species names; 1 = N/A
  - Tmean: Mean temperature at which each species is observed across its geographic distribution (°C)
  - Site_temp: Mean annual temperature at each experimental site (°C)
  - Stdev_of_Tmean: Standard deviation of the species' thermal mean
  - TDI: Thermal displacement index (°C normalization; see below)
  - Trait values (LMA, LT, etc.): Scaled trait values per trait
  - TDI and other fields explain how species perform relative to home temperature

## Scaled trait values and Thermal Displacement Index (TDI)
- TDI calculation:
  - TDI = (Site temperature − Mean temperature of species) / σ (standard deviation of the species' thermal range, from WorldClim data)
  - Positive TDI indicates the species is transplanted to a site warmer than its home temperature; negative indicates cooler.
- Scaled trait values (STVs):
  - Each trait value divided by the maximum value observed at the home elevation/temperature.
  - STV = 1 at home; >1 means trait increases away from home; <1 means trait decreases away from home.

## Experimental design
- Three experimental sites at different altitudes with distinct mean annual temperatures (MAT):
  - High elevation: ~2516 m, MAT ≈ 14°C
  - Mid elevation: ~1357 m, MAT ≈ 22°C
  - Low elevation: ~736 m, MAT ≈ 26°C
- Experimental layout: at each site, one individual from each of eight species planted in six blocks per plot (6x15 plants per plot; 4x90 plants per site). Block 6 at each plot used fertilised soil.
- Pre-planting: Trees grown from seed for two years in a nursery at mid-elevation before transplanting to the sites between November and December 2018.
- Common soils: All sites used identical soils with 400 kg soil per tree; irrigation maintained constant soil moisture.
- Data collection: eight species represented; data collected on absolute and scaled trait values.

## Leaf trait measurement methods (absolute values)
- LT (leaf thickness): Measured with precision electronic callipers at three leaf areas (excluding mid-vein); average used.
- LA (leaf area): Scanned leaves; processed with LeafArea R package and ImageJ workflow.
- LW (leaf width): Calculated from scanned leaf images using LeafJ plugin in ImageJ.
- LDMC (leaf dry matter content): Wet weight measured, leaves dried at 70°C for ~48 hours, then dry weight used to compute LDMC.
- LMA (leaf mass per unit area): Dry weight divided by LA.

## Leaf nutrient data (absolute values)
- Nm (mass-based leaf N) and Na (area-based leaf N): Ground leaf powder analyzed by IRMS; Na derived by dividing Nm by LMA.
- Pm (mass-based leaf P) and Pa (area-based leaf P): Sample digested and analyzed by ICP-OES; Pa derived by dividing Pm by LMA.

## Water-use efficiency data (absolute values)
- δ13C (d13C): Obtained from IRMS analysis.
- g1 (stomatal conductance parameter): Derived from diurnal measurements (A n and g s) using the Medlyn et al. (2012) stomatal conductance model; data collected with LI-6400XT under controlled ambient conditions. g1 calculated via fitting with the plantecophys R package.

## Notes on data quality
- Some isolated trait values are missing due to instrument error or post-processing quality assessments.

## References
- Duursma, R. A. (2015). Plantecophys: an R package for analysing and modelling leaf gas exchange data. PLoS One.
- Fick, S. E., & Hijmans, R. J. (2017). WorldClim 2: new 1-km climate surfaces.
- Katabuchi, M. (2015). LeafArea: an R package for leaf area analysis.
- Lin, Y. S. et al. (2015). Optimal stomatal behaviour around the world. Nature Climate Change.
- Maloof, J. N. et al. (2013). LeafJ: an ImageJ plugin for leaf shape measurement.
- Medlyn, B. E. et al. (2012). Reconciling optimal and empirical approaches to modelling stomatal conductance.
- Pérez-Harguindeguy, N. et al. (2016). New handbook for standardized leaf trait measurements.
- R Core Team (2022). R: A language and environment for statistical computing.
- Wilson, P. J. et al. (1999). Leaf area and LDMC as predictors of plant strategies.