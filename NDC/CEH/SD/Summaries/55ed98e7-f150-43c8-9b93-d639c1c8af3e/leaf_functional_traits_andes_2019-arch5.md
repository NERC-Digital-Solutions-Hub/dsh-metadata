# Leaf functional trait data from three common garden sites along an elevation/temperature gradient in the Colombian Andes

## Overview
- A dataset of key leaf functional traits collected in 2019 across three elevation sites in the Colombian Andes to assess thermal acclimation in eight midsuccessional tropical montane forest species.
- Two CSV files:
  - leaf_functional_traits_absolute_values.csv (absolute trait values)
  - leaf_functional_traits_scaled_values.csv (scaled trait values)
- Lead author AJFC conducted data collection and analysis; some values are missing due to instrument error or post-processing quality control.

## Data files and structure
- Absolute values file includes:
  - Site, Species, and trait columns: LMA (g m^-2), LT (mm), LDMC (mg g^-1), LA (cm^2), LW (mm), Nm (g g^-1), Na (g m^-2), Pm (g g^-1), Pa (g m^-2), d13C (‰), g1 (kPa^0.5)
- Scaled values file includes:
  - Site, Climatic.origin, Species, Tmean, Site_temp, Stdev_of_Tmean, TDI, and scaled trait values
- Column descriptions and units are provided in Table 1 of the accompanying document.

## Experimental design
- Three sites at different elevations with distinct mean annual temperatures (MAT):
  - High elevation: ~2516 m, MAT ~14°C
  - Mid elevation: ~1357 m, MAT ~22°C
  - Low elevation: ~736 m, MAT ~26°C
- Common soils, 400 kg soil per tree, irrigation to maintain consistent soil moisture.
- Seed-grown in a nursery for two years at mid-elevation before planting (Nov–Dec 2018).
- Plot arrangement: 6 blocks per plot, 15 plants per block, 4 plots per site; one fertilized block per plot (Block 6).
- Eight species studied; data collected June–August 2019.

## Trait measurements and data processing
- Structural traits:
  - LT measured with high-precision calipers (three leaf areas per leaf; average used)
  - LA measured via leaf scans; processed with LeafArea (R) and ImageJ tools
  - LW derived from scanned leaves using LeafJ (ImageJ plugin)
  - LDMC determined from fresh and oven-dried leaf weights
  - LMA calculated as dry weight / leaf area
- Nutrient traits:
  - Nm (mass-based leaf N) via IRMS
  - Na (area-based N) calculated from Nm and LMA
  - Pm (mass-based P) via ICP-OES
  - Pa (area-based P) derived from Pm and LMA
- Isotopic and water-use traits:
  - δ13C obtained from IRMS
  - g1 (intrinsic water-use efficiency proxy) estimated from diurnal A and g_s measurements using the Medlyn et al. (2012) stomatal conductance model, with g1 fit via the plantphys R package
  - LI-COR LI-6400XT used for diurnal gas exchange measurements; environmental conditions replicated in cuvette for accurate fitting

## Scaled trait values and temperature-related metrics
- Temperature displacement index (TDI) calculated as a standardized difference between site mean temperature and species’ mean thermal distribution (based on WorldClim data).
- Scaled trait values (STVs) created by dividing each trait by the maximum value observed at the home elevation/temperature; STV = 1 denotes home-temperature trait value.
- WorldClim 2 climate data (Fick & Hijmans, 2017) used to contextualize species’ thermal distributions.
- Positive TDI indicates transplantation to a site warmer than the species’ home temperature; negative indicates cooler.

## Data quality and limitations
- Some isolated values missing due to instrument error or post-processing quality assessments.
- Data cover eight species across three sites, collected in a single growing season (2019).

## Usage notes and references
- Data intended to support analyses of thermal acclimation and trait variation across elevation and temperature.
- Methodological references include R packages for leaf trait analysis (LeafArea, LeafJ, plantecophys) and climate data (WorldClim 2).
- Lead author and site design details provided to aid provenance and reproducibility.