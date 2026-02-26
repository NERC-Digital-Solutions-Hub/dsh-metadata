# Shrubland primary production and soil respiration diverge along European climate gradient

## Overview
- Investigates how shrubland primary production (aboveground) and soil respiration diverge along a north-south European climate gradient.
- Utilizes climate manipulation experiments (warming and drought) across seven shrubland sites in the INCREASE network, spanning 1998–2012.
- Data underpin two datasets and support comparisons of control, drought, and warming treatments across sites.

## Experimental design
- Sites: seven European shrublands across the UK, the Netherlands, Denmark (two sites), Hungary, Spain, and Italy.
- Treatments: control, drought (reduced precipitation), warming (night-time warming).
- Plot design: 4 m x 5 m plots with three plots per treatment (total n = 9 per site; 3 control, 3 drought, 3 warming).
- Warming method: horizontal curtains triggered by dawn/dusk light sensors; drought via curtains triggered by rain sensors, reducing rainfall by 15–50%.
- Timeline: warming and drought initiated in 1999 at SP, DK-M, NL, UK; IT and HU began in 2002; DK-B in 2006; high wind events prompted curtain removal as needed.
- Measurements paused during winter or adverse weather to protect equipment.

## Measurements and data collected
- Aboveground standing biomass (SB) and aboveground net primary productivity (aNPP):
  - SB estimated with the pin-point method; at least 300 points per site per year.
  - Litterfall measured with collectors; timing varied by site.
  - aNPP calculated from SB increments plus litterfall (with site-specific rules for HU and UK).
  - All aNPP values converted to carbon by multiplying by 0.5.
- Soil respiration (Rs):
  - Measured with soil collars of varying numbers by plot; vegetation removed to capture autotrophic and heterotrophic respiration.
  - Instruments varied by site (gas-tight lids with syringe measurements; portable IR gas analyzers; open-system leaf chamber approach).
  - Measurement frequency varied (monthly, biweekly, or campaign-based) and paused in winter or bad weather.
  - Rs extrapolated to annual values.
- Climate data:
  - Mean annual precipitation (MAP) and mean annual temperature (MAT) used to compute the Gaussen Index (GI) of aridity.
  - GI = MAP / (2 × MAT), adjusted for treatment-induced changes in MAP and MAT.

## Climate data and aridity index
- GI calculated for each site under control conditions; adjustments made for drought and warming treatments.
- The study uses GI to contextualize aridity and interpret treatment effects on carbon fluxes.

## Data structure and datasets
- Two primary datasets underpin the paper:
  - CLM_Biome_paper_annual.csv
    - 8 columns, 316 rows.
    - Variables: Year (A), Country (B; UK, NL, DK-B, DK-M, HU, SP, IT), Treatment (C; Control, Drought, Warming), ANPP_gCm2 (D; g C m^-2), ANPP_gbiomass (E; g biomass m^-2), Biomass_gCm2 (F; g C m^-2), Biomass_gbiomass (G; g biomass m^-2), Rs_gCm2 (H; g C m^-2).
    - Notes: ANPP and biomass converted to carbon via factor 0.5.
  - CLM_Biome_paper_aNPP_Rs.csv
    - 7 columns, 29 rows.
    - Variables: Variable (A; ANPP or Rs), Country (B), Treatment (C), Gaussen_index_of_aridity (D), Treatment_difference_Gaussen_index (E), Mean_change_from_control_percent (F), SE_change_from_control_percent (G).
    - Provides aridity-adjusted treatment effects and percent changes relative to control.
- Data gaps: empty cells indicate years with no measurements; site- and year-to-year measurement frequency varied across sites.

## Analytical focus and utility
- Enables cross-site comparisons of SB, aNPP, and Rs under control, drought, and warming across a latitudinal gradient.
- Facilitates calculation of aridity-adjusted treatment effects via Gaussen index and percent changes in carbon fluxes.
- Highlights data heterogeneity across sites and years, and the need for careful upscaling and cross-site standardization.
- Supports testing correlations between aboveground productivity and soil carbon efflux in response to climate perturbations.

## Related context
- Grounded in a broad set of referenced work on drought and warming experiments (e.g., Beier et al., 2004; de Dato et al., 2010; Penuelas et al., 2007; Kröel-Dulay et al., 2015) and broader climate change experimentation (CLIMAITE, etc.).