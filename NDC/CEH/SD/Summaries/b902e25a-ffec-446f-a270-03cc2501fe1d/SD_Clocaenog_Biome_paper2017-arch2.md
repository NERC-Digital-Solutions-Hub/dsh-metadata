# Shrubland primary production and soil respiration diverge along European climate gradient

## Overview
- A multi-site European shrubland study (1998–2012) examining aboveground productivity and soil respiration across climate gradients.
- Sites: United Kingdom, The Netherlands, Denmark (two sites), Hungary, Spain, Italy (7 shrublands).
- Part of the INCREASE network; includes climate manipulations simulating warming and summer drought.
- Aims to quantify environmental condition and policy-relevant ecosystem responses using standardised measurements and outputs.

## Experimental design and sites
- Plot setup: at each site, plots of 4 m x 5 m with 9 plots total (3 per treatment: Control, Drought, Warming).
- Treatments: nighttime warming and extended growing-season drought implemented with moving curtains triggered by light and rain sensors; drought reduced incoming precipitation by 15–50%.
- Timing: warming and drought implemented at SP, DK-M, NL, UK from 1999; IT and HU from 2002; DK-B from 2006.
- Seasonal considerations: curtains retracted at high winds (>10 m/s); measurements paused during winter or adverse weather.

## Measurements and data processing
- Standing aboveground biomass (SB) and aboveground net primary productivity (aNPP)
  - SB measured via pin-point method; annual SB increment used to derive aNPP along with litterfall.
  - Litterfall collected monthly or every 2–6 months, dried, and weighed.
  - aNPP calculated from SB increment plus litterfall in most sites; site-specific rules applied for HU and UK.
  - aNPP converted to carbon by multiplying by 0.5.
- Soil respiration (Rs)
  - Measured with soil collars (10 cm diameter; other collars vary by site) to capture autotrophic + heterotrophic respiration.
  - Instruments varied by site (gas-tight lids with syringe in NL, SP, IT, UK; EGM portable IRGA; open-system in HU); measurement frequency ranged from monthly to biweekly, with pauses in winter or bad weather.
  - Rs data up-scaled to annual values.
- Data quality and standardisation
  - Methods align with prior Beier, Emmett, and colleagues’ work; data are structured for cross-site comparison and trend analysis over time.

## Climate data and aridity
- Climate context from Kröel-Dulay et al. (2015): mean annual precipitation (MAP) and mean annual temperature (MAT) used.
- Gaussen index (GI) of aridity calculated as GI = MAP / (2 × MAT).
- GI and treatment-adjusted climate metrics used to interpret ecosystem responses under control vs. treatment conditions.

## Treatment effects and key findings
- Ecosystem carbon gain (aNPP and Rs) analyzed as differences between drought/warming and control plots.
- The study captures how primary production and soil CO2 efflux diverge along a north–south European climate gradient under altered temperature and moisture regimes.
- Site-specific responses reflect differences in sensitivity to drought and warming, contributing to understanding of carbon balance in shrubland ecosystems across Europe.

## Data resources and structure
- Two primary datasets accompanying the paper:
  - CLM_Biome_paper_annual.csv
    - 8 columns, 316 rows
    - Variables include Year, Country (UK, NL, DK-B, DK-M, HU, SP, IT), Treatment (Control, Drought, Warming), ANPP_gCm2, ANPP_gbiomass, Biomass_gCm2, Biomass_gbiomass, Rs_gCm2.
    - ANPP and Biomass reported as g carbon per m2; conversions to biomass and carbon are documented.
  - CLM_Biome_paper_aNPP_Rs.csv
    - 7 columns, 29 rows
    - Variables include Variable (ANPP or Rs), Country, Treatment, Gaussen_index_of_aridity, Treatment_difference_Gaussen_index, Mean_change_from_control_percent, SE_change_from_control_percent.
    - Provides aridity-adjusted contrasts and percent changes for drought and warming treatments.
- These datasets reflect measurements across 1998–2012 for seven shrublands under three treatments, enabling cross-site comparative analyses and monitoring.

## Related publications and context
- The study builds on a network of climate manipulation experiments and related methodological papers on drought and nighttime warming in shrublands.
- Key references provide methodological grounding for plot design, measurement techniques, and interpretation of climate change effects on shrubland productivity and soil respiration.