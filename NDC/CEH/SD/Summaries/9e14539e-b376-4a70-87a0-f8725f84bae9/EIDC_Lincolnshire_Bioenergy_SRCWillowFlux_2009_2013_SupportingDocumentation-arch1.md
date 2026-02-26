# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a short rotation coppice willow ( Salix viminalis ) plantation, Lincolnshire, UK, 20092013

- This dataset provides time series of surface-atmosphere exchanges including net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured by eddy covariance (EC) at a short rotation coppice willow plantation in Lincolnshire, UK.
- Monitoring period: 2009-10-14 to 2013-10-01, with ancillary meteorological and soil observations and data quality metadata.

## Study site

- Location: SRC willow flux site near Lincoln, UK (53°19'10.37"N, 0°35'3.06"W); mature 9.4 ha commercial plantation.
- Climate and soils: temperate maritime climate; mean annual air temperature ~9.8 °C and precipitation ~614 mm yr^-1 (1981–2010 baseline). Soils are Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; details include bulk density ~1.4 g cm^-3, pH ~5.8, and upper 0.3 m soil C and N contents of ~68.3 t C ha^-1 and 11.0 t N ha^-1.
- Land use history and management: established on former arable land in 2000; coppiced in 2001; biomass harvests in March 2011 and October 2013; minimal management otherwise; inputs after 2011 harvest include micronutrients, lime, and compost wood waste. The plantation is rainfed with no irrigation.
- Canopy and biomass context: plantation designed for bioenergy, with willow varieties including Salix viminalis types (e.g., Tora, Jora, Jorunn, Orm, Ulv, Rapp).

## Sampling regime and flux data acquisition

- Flux measurements: open-path eddy covariance system mounted on a mast near canopy center; height periodically raised to ~twice the mean canopy height.
- Target variables: NEE (μmol CO2 m^-2 s^-1), sensible heat H (W m^-2), latent heat LE (W m^-2), and momentum τ (kg m^-1 s^-2).
- Instrumentation: Mk4 Hydra sonic anemometer-thermometer and LI-7500 CO2/H2O infrared gas analyser; 20 Hz data logging.
- Ancillary meteorology and soil: separate scaffold tower measurements including net radiation, shortwave/longwave components, below-canopy PPFD, soil heat flux, soil moisture, soil temperature, precipitation, air temperature, and relative humidity.

## Data processing

- Primary processing: EddyPRO v6.1 for flux calculations; 30-minute flux averages.
- QC and corrections: quality control of 20 Hz data, angle-of-attack corrections, 2D coordinate rotation, corrections for high/low-frequency attenuation, humidity and density corrections, and flux-setup-derived turbulence metrics (u*, TKE, L, z/L).
- Uncertainty: random uncertainties for fluxes quantified; footprint analysis performed to ensure representativeness (≥75% flux within target ecosystem).
- Gap-filling and partitioning: missing EC data filled with Marginal Distribution Sampling; NEE partitioned into GEP and TER using Reichstein et al. (2005) approach driven by air temperature; gap-filled data processed with REddyProc in R.

## Quality control

- Outliers removed using median absolute deviation; EddyPRO quality flag thresholds (flag > 1) lead to exclusion.
- Flux ranges enforced (e.g., H: -200 to 600 W m^-2; LE: -100 to 600 W m^-2; NEE: -55 to 25 μmol CO2 m^-2 s^-1).
- Representativeness assessed with footprint model; weekly visual checks with manual corrections as needed.

## Data gap-filling and flux partitioning

- Gap-filling: Marginal Distribution Sampling to fill NEE, LE, and H gaps.
- Partitioning: NEE decomposed into GEP and TER via flux-partitioning approach using Ta as driver; REddyProc used for implementation.
- Outputs include gap-filled NEE (NEE_filled) and partitioned components (GEP, TER), plus associated uncertainties.

## Details of data structure

- Data delivered as a single CSV file (Lincolnshire_Bioenergy_SRCWillow_2009_2013.csv) with 30-minute records; gap-filled and partitioned data provided as a complete time series from 2009-10-14 to 2013-10-01.
- Time stamps correspond to the end of each 30-minute averaging period; missing records denoted by -9999.

## Nature and units of recorded values

- Variables include: DateTime (UTC), NEE, NEE_unc, LE, LE_unc, H, H_unc, τ, τ_unc, CO2_storage, Pa, Ta, RH, VPD, SW_in, SW_out, LW_in, LW_out, R_net, PPFDbc (below-canopy PPFD), soil heat flux (G), soil temperature (Tsoil), soil volumetric water content (VWC), precipitation, wind speed and direction, footprint fraction, friction velocity (U*)
- Additional filled and diagnostic fields: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, along with their uncertainties.

## Acknowledgments and references

- Funding: National Environment Research Council (CarboBiocrop project) and CEH Integrating Fund.
- Acknowledgments to landowners for site access.
- References to foundational methods and related studies on eddy covariance processing, footprint analysis, gap-filling, and flux partitioning (e.g., Reichstein et al.; Mauder et al.; Moncrieff et al.; Papale et al.; Wickham-related REddyProc references).