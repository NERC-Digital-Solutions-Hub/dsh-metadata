# Summary

- This dataset includes key leaf functional trait data from three common garden sites along an elevation/temperature gradient in the Colombian Andes, collected between June and August 2019.
- Two CSV data sheets are provided:
  - leaf_functional_traits_absolute_values.csv: absolute trait values.
  - leaf_functional_traits_scaled_values.csv: scaled trait values (calculated using Equation 2 in the accompanying manuscript).
- Columns cover structural traits (LMA, LT, LDMC, LA, LW), nutrients (Nm, Na, Pm, Pa), δ13C, and g1; with explicit units described in the accompanying table.
- Some values are missing due to instrument error or post-processing quality filtering.

## Data sheets and column details

- Absolute values (Units provided):
  - Site (categorical): 1 = High elevation; 2 = Mid elevation; 3 = Low elevation
  - Species (N/A): genus and species, e.g., C.multiflora
  - LMA (g m^-2)
  - LT (mm)
  - LDMC (mg g^-1)
  - LA (cm^2)
  - LW (mm)
  - Nm (g g^-1)
  - Na (g m^-2)
  - Pm (g g^-1)
  - Pa (g m^-2)
  - d13C (‰)
  - g1 (kPa^0.5)
- Scaled values (Units and descriptions here mirror the absolute values with additional scaling fields):
  - Site
  - Climatic.origin
  - Species
  - Tmean (°C)
  - Site_temp (°C)
  - Stdev_of_Tmean
  - TDI (thermal displacement index)
  - Trait values (LMA, LT, etc.) scaled relative to home temperature
  - Additional fields to support interpretation (e.g., scaling factors)

## Experimental design

- Three experimental sites at different elevations in the Colombian Andes with distinct mean annual temperatures (MAT):
  - High elevation: ~2516 m, MAT ≈ 14°C
  - Mid elevation: ~1357 m, MAT ≈ 22°C
  - Low elevation: ~736 m, MAT ≈ 26°C
- Layout:
  - Each site contains six blocks; in each plot, one individual from each of eight species was planted (6 × 8 per plot; 4 × 90 plants per site total).
  - Block 6 at each plot received fertilised soil.
- Nursery-to-field timeline:
  - Trees were grown from seed for two years in a mid-elevation nursery, then planted at sites between November and December 2018.
- Species: data cover eight midsuccessional Andean tropical montane forest species.

## Trait measurement and data generation

- Structural traits:
  - LT: measured with high-precision calipers (three leaf locations per leaf; average used)
  - LA: leaf scans processed with LeafArea (R) to compute leaf area
  - LW: calculated from scanned images using LeafJ (ImageJ plugin)
  - LDMC: ratio of leaf dry mass to fresh mass after drying (70°C for ~48 h)
  - LMA: dry mass divided by LA
- Nutrient traits:
  - Nm (mass-based leaf N) and Na (area-based N) via IRMS after grinding leaf tissue
  - Pm (mass-based P) via ICP-OES; Pa (area-based P) derived from Pm/LMA
- Water-use efficiency traits:
  - δ13C via IRMS
  - g1 derived from diurnal measurements of AN and gs using the Medlyn et al. (2012) stomatal conductance model
  - Measurements with LI-6400XT; parameters fitted with plantecophys package in R
- Scaling and diurnal modelling:
  - Scaled trait values (STVs) computed as trait value divided by the maximum value observed at home elevation/temperature
  - TDI (Thermal Displacement Index) calculated as (Site_temperature − Tmean) / σ(Tmean) to describe displacement relative to species’ thermal distribution
  - A positive TDI indicates transplantation to a site warmer than the species’ home temperature; negative indicates cooler

## Data processing and provenance

- Data were collected and analyzed by AJFC (lead author)
- Methods and scripts referenced include:
  - LeafArea (R) for leaf area
  - ImageJ and LeafJ for leaf measurements
  - IRMS for N and δ13C
  - ICP-OES for P
  - Medlyn et al. (2012) stomatal conductance model for g1
  - R packages Plantecophys, LeafArea, and WorldClim data (Fick & Hijmans, 2017)
- Data provenance notes:
  - Some values missing due to instrument error or post-processing quality filtering
  - The dataset covers eight of the species present at the sites

## Considerations for analysis

- Cross-site comparability requires attention to scaling (STVs) and the TDI-based interpretation of trait shifts relative to home species distributions
- Data gaps should be accounted for in analyses, especially for traits with fewer observations at certain sites
- The dataset enables analyses of thermal acclimation potential, trait-climate correlations, and predictive modeling of trait responses to temperature gradients

## References (methods and tools)

- Duursma, R. A. Plantecophys (R package)
- Fick, S. E., & Hijmans, R. J. WorldClim 2
- Katabuchi, M. LeafArea (R package)
- Lin, Y. S. et al. Optimal stomatal behaviour
- Maloof, J. N. et al. LeafJ (ImageJ)
- Medlyn, B. E. et al. (2012) stomatal conductance model
- Pérez-Harguindeguy, N. et al. New handbook for standardised trait measurement
- R Core Team. R (statistical computing)
- Wilson, P. J. et al. Leaf dry matter content as predictor