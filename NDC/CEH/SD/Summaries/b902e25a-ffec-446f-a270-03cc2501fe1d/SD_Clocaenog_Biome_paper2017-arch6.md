# Shrubland primary production and soil respiration diverge along European climate gradient

## Overview
- Multi-site European study (1998–2012) examining how aboveground production and soil respiration respond to a climate gradient and experimental treatments.
- Sites span UK, Netherlands, Denmark (two sites), Hungary, Spain, and Italy within the INCREASE shrubland network.
- Climate manipulations include nighttime warming and extended drought; treatments applied to multiple plots per site with control plots for comparison.
- Two core data products accompany the paper: annual aboveground biomass and productivity estimates, and aridity-adjusted treatment effects on aNPP and Rs.

## Experimental design and site details
- Seven shrubland sites across Europe with climate manipulations initiated between 1999 and 2006 depending on site.
- Plot setup: 4 m x 5 m plots; for most sites, 9 plots per site (3 control, 3 drought, 3 warming).
- Warming achieved with horizontally moving curtains triggered by dawn and retracted at sunrise; drought achieved by curtains reducing rainfall during the growing season.
- Measurements paused during winter or adverse weather; net effect aims to simulate increased temperature and more extreme drought during the plant growing season.

## Measurements and variables
- Standing aboveground biomass (SB) and aboveground net primary production (aNPP)
  - SB measured with the pin-point method; annual SB increments used to derive aNPP (with litterfall added when SB increment is positive).
  - Litterfall collected monthly or semi-annually; samples dried and weighed.
  - Biomass and aNPP converted to carbon using a 0.5 conversion factor (carbon content assumption).
  - Site-specific rules for aNPP calculation (e.g., HU deciduous dynamics; UK perennial vegetation considerations).
- Soil respiration (Rs)
  - Measured with permanent soil collars of varying diameters across sites; vegetation removed inside collars to capture autotrophic plus heterotrophic respiration.
  - Different RS measurement technologies used by site (gas-tight lids with syringes, portable IRGAs, or open/closed systems) and varying measurement frequencies.
  - Rs measurements paused in winter or during unsuitable conditions; Rs values upscaled to annual estimates.
- Climate context
  - Mean annual precipitation (MAP) and mean annual temperature (MAT) used to compute the Gaussen Index (GI = MAP / (2 × MAT)).
  - GI adjusted for climate treatment effects on MAP and MAT to reflect the aridity context of each treatment.

## Climate treatments and analysis
- Treatments evaluated as deviations from untreated controls:
  - Drought and warming effects on ecosystem carbon gain (expressed as percent differences in aNPP and Rs).
- Gaussen Index (GI) is provided for control plots and adjusted under treatment scenarios to enable aridity-context interpretation of responses.

## Data structure and contents
- Two primary datasets are provided, forming the basis for Reinsch et al. (2017):
  - CLM_Biome_paper_annual.csv
    - 8 columns, 316 rows
    - Key fields: Year, Country (UK, NL, DK-B, DK-M, HU, SP, IT), Treatment (Control, Drought, Warming), ANPP_gCm2, ANPP_gbiomass, Biomass_gCm2, Biomass_gbiomass, Rs_gCm2
    - ANPP and Biomass values are reported in carbon terms (g C m^-2); biomass values in g biomass m^-2
    - ANPP and Biomass derived from measurements with a 0.5 carbon conversion factor
  - CLM_Biome_paper_aNPP_Rs.csv
    - 7 columns, 29 rows
    - Key fields: Variable (ANPP or Rs), Country, Treatment, Gaussen_index_of_aridity, Treatment_difference_Gaussen_index, Mean_change_from_control_percent, SE_change_from_control_percent
    - Summaries of aridity-adjusted treatment effects and their variability
- Data gaps
  - Empty cells indicate years or plots where measurements were not performed.

## Data quality, methods, and considerations
- Cross-site methodological variation in Rs measurement equipment and frequency; winter pauses to protect equipment.
- aNPP computations incorporate site-specific nuances (e.g., leaf phenology and perennial vs deciduous vegetation) that influence how SB increments translate to productivity.
- Treatments are designed to isolate the effects of warming and drought on carbon fluxes, with aridity context provided via GI.
- Data are designed for cross-site comparison of drought and warming impacts on carbon gain, enabling aridity-informed interpretation of responses.

## How to use the data
- Compare warming vs drought responses in aNPP and Rs across a European aridity gradient.
- Examine how aridity (GI) and treatment differences relate to changes in carbon gain (percent changes) and their uncertainty.
- Use annual dataset to analyze temporal dynamics (1998–2012) and correlate SB increments, litterfall, and Rs with climate variables.
- Leverage the explicit data transformation notes (e.g., 0.5 conversion to carbon) for reproducible carbon budgeting.

## Context and related works
- Data underpin a broader set of climate manipulation experiments across shrublands in Europe.
- Related publications document experimental design and site-specific climate manipulation outcomes, with the Reinsch et al. paper synthesizing divergences in carbon fluxes along climate gradients.
- Key references provide methodological context for drought and warming experiments, soil respiration measurements, and vegetation biomass estimation techniques.