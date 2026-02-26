# Shrubland primary production and soil respiration diverge along European climate gradient

## Overview
- Multi-site European study examining how shrubland primary production and soil respiration respond to warming and drought across a climate gradient.
- Data collected from 1998–2012 at 7 shrublands (UK, NL, DK-B, DK-M, HU, SP, IT) as part of the INCREASE network.
- Two datasets underpinning the study: annual metrics (ANPP, biomass, Rs) and aNPP/Rs with aridity and treatment-change information.
- Aimed at understanding ecosystem carbon balance under climate change across diverse sites; data suitable for cross-site comparisons and meta-analyses.

## Data Coverage and Context
- Geographic scope: 7 European shrublands spanning diverse precipitation and temperature regimes.
- Treatments: Control, Drought, Night-time Warming.
- Climate metrics: Mean annual precipitation (MAP), mean annual temperature (MAT), and Gaussen Index (GI) of aridity (GI = MAP / (2 × MAT), adjusted for treatment effects).
- Measurements spanned 1998–2012, with some years/methods varying by site.

## Experimental Design and Treatments
- Plot layout: 4 m × 5 m plots with three plots per treatment (total n = 9 per site).
- Warming treatment: Night-time warming using curtains triggered by dawn light sensors; curtains retracted at sunrise.
- Drought treatment: Curtains reduce nighttime precipitation during rain events; drought duration 1–3 months; reduced soil moisture by 15–50%.
- Site-specific variations: Curtain operation adjusted to wind conditions (curtains removed at wind speeds >10 m/s).
- Measurements paused during winter or adverse weather to protect equipment.

## Measurements and Computation
- Aboveground biomass (SB) and aboveground net primary production (aNPP)
  - SB estimated with the pin-point method; minimum 300 measurement points per site.
  - Litterfall collected monthly or semi-monthly; dried and weighed.
  - aNPP calculated from SB increment plus litterfall, with site-specific rules (e.g., HU deciduous leaves; UK perennial Calluna vulgaris).
  - aNPP converted to carbon (×0.5, assuming 50% carbon content in plant material).
- Soil respiration (Rs)
  - Measured with soil collars of varying diameters; vegetation inside collars removed to measure vegetation-free respiration (root + microbial respiration).
  - Site-specific equipment: gas-chamber methods (portable IRGA) or CO2 sampling with gas-tight lids; measurement frequency ranged from monthly to biweekly or campaign-based.
  - Rs measurements paused in winter or bad weather; Rs up-scaled to annual values.
- Data processing
  - Annual Rs and aNPP derived from site-specific time series; aNPP in g C m^-2 year^-1 and biomass in g C m^-2 year^-1.
  - Litterfall and SB used to compute aNPP; SB increment used when calculating annual aNPP.

## Climate Data and Aridity Metric
- MAP and MAT sourced from Kröel-Dulay et al. (2015); used to compute GI.
- GI (aridity) computed for control plots and adjusted for treatment-induced changes in MAP and MAT.
- Treatment effects on aridity quantified as mean percentage changes for aNPP and Rs, with associated standard errors.

## Data Structure and Files
- Data files provided:
  - CLM_Biome_paper_annual.csv
    - 8 columns, 316 rows
    - Variables: Year, Country, Treatment, ANPP_gCm2, ANPP_gbiomass, Biomass_gCm2, Biomass_gbiomass, Rs_gCm2
    - Units primarily in g C or g biomass per m^2; ANPP and Biomass expressed in carbon equivalents (g C m^-2), with biomass values given for the same year.
  - CLM_Biome_paper_aNPP_Rs.csv
    - 7 columns, 29 rows
    - Variables: Variable, Country, Treatment, Gaussen_index_of_aridity, Treatment_difference_Gaussen_index, Mean_change_from_control_percent, SE_change_from_control_percent
    - Provides aridity metrics and percent changes in response to drought and warming treatments, plus associated uncertainty.
- Coding/labels
  - Countries: UK, NL, DK-B, DK-M, HU, SP, IT
  - Treatments: Control, Drought, Warming
- Data gaps: Empty cells indicate years with no measurements.

## Data Quality, Gaps, and Limitations
- Methodological heterogeneity across sites for Rs measurement (different instruments and protocols).
- Varied measurement frequencies and seasonal pauses (winter interruptions, weather-related pauses).
- Missing data in some years or sites, reflected as empty cells.
- Aridity adjustments depend on treatment-induced changes, introducing potential uncertainty in GI-based comparisons.

## Reuse, Governance, and Implications
- Rich, cross-site dataset enabling comparative analysis of carbon balance responses to warming and drought across a climate gradient.
- Clear documentation of methods, units, and calculation steps supports reproducibility and meta-analyses.
- Data are suitable for assessing:
  - How aNPP and Rs respond differently to warming and drought across sites.
  - The role of aridity (GI) in modulating carbon flux responses.
  - Consequences for shrubland carbon budgets under varying climate change scenarios.
- Beneficial for data stewardship practices: standardized metadata, explicit calculation rules (e.g., aNPP from SB increments and litterfall, carbon conversion Factor 0.5), and explicit treatment effects on aridity.