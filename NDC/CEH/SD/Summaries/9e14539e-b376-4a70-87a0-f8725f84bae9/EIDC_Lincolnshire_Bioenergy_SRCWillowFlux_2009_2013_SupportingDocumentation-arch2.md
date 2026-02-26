# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a short rotation coppice willow ( Salix viminalis ) plantation, Lincolnshire, UK, 20092013

## Overview
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Measurements via open-path eddy covariance (EC) above a SRC willow canopy.
- Coverage: 2009-10-14 00:30 to 2013-10-01 00:00.
- Dataset also includes ancillary meteorological and soil observations, plus variables describing atmospheric turbulence and QC.

## Study site
- Location: SRC willow flux site, 53°19'10.37"N, 0°35'3.06"W; 9.4 ha mature commercial bioenergy plantation, ~10 km north of Lincoln, UK.
- Climate: temperate maritime; mean annual air temperature 9.8 ± 0.7 °C; mean annual precipitation 614 ± 93.5 mm (1981–2010 reference).
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; bulk density ~1.4 ± 0.2 g cm^-3; pH ~5.8 ± 0.3; upper 0.3 m soil organic C ~68.3 t ha^-1; N ~11.0 t ha^-1.
- Land use history and management: former arable land (established 2000); coppiced in 2001; biomass harvests in 2011 and 2013; limited inputs post-harvest (micronutrients, lime, compost wood waste in 2011); rainfed, no irrigation.

## Sampling regime
- Automated flux, meteorological, and soil measurements from 2009-10-14 to 2013-10-01.
- Flux measurements: open-path EC system mounted on a tall mast, center of the plantation; measurement height increased periodically to be ~2x willow canopy height.
- Instruments: Mk4 Hydra sonic anemometer–thermometer; LI-7500 CO2/H2O infrared gas analyser; 20 Hz data logging; 30-minute flux averaging.
- Ancillary data: net radiation (SWin, SWout, Rnet, etc.), below-canopy PPFD, soil heat flux (G), soil moisture (VWC), soil temperature (Tsoil), air temperature (Ta), relative humidity (RH).
- Data logging: 30-minute means or sums (precipitation).

## Flux data acquisition
- Eddy covariance system for NEE, H, LE, and τ; raw turbulence data collected at 20 Hz.
- Data processed to produce flux estimates and turbulence metrics (wind speed/direction, u*, TKE, Obukhov length L, z/L).

## Ancillary data
- Meteorological and soil physics observations logged as 30-minute means.
- Includes radiative fluxes, PAR below canopy, soil heat flux, soil moisture and temperature, precipitation, wind metrics, and footprint indicators.

## Data processing
- Software: EddyPRO® Flux Calculation Software Version 6.1.
- Processing steps: 30-minute block averaging; QC of 20 Hz data; angle-of-attack correction; 2D coordinate rotation; corrections for co-spectral attenuation; humidity and density corrections; random uncertainties estimated per standard methods.
- Outputs: wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).

## Quality control
- Outlier removal using median absolute deviation; QC flags: EddyPRO quality flag > 1 leads to exclusion.
- Flux range checks: H (-200 to 600 W m^-2), LE (-100 to 600 W m^-2), NEE (-55 to 25 μmol CO2 m^-2 s^-1).
- Flux representativeness: footprint analysis with ART Footprint Tool; retain fluxes if >75% originates within target ecosystem.
- Weekly visual inspections of flux and ancillary data; clearly erroneous values removed.

## Data gap-filling and flux partitioning
- Gap filling: Marginal Distribution Sampling (MDS) approach (Reichstein et al., 2005).
- Partitioning NEE into GEP and TER via flux partitioning approach (Reichstein et al., 2005) using air temperature to drive the algorithm.
- Tools: REddyProc package in R (Reichstein et al., 2016) for gap-filling and partitioning.
- Outputs include gap-filled NEE (NEE_filled) and partitioned components (GEP, TER), plus associated uncertainties (NEE_filled_sd, LE_filled_sd, H_filled_sd, etc.).

## Data structure and units
- Data provided as a single CSV: Lincolnshire_Bioenergy_SRCWillow_2009_2013.csv.
- Time stamps: end of each 30-minute flux averaging period (UTC).
- Key variables (examples):
  - NEE (μmol CO2 m^-2 s^-1) and NEE_filled; NEE_unc (uncertainty).
  - LE (W m^-2) and LE_filled; LE_filled_sd.
  - H (W m^-2) and H_filled; H_filled_sd.
  - Tau (kg m^-1 s^-2) and Tau_filled.
  - GEP (μmol CO2 m^-2 s^-1) and TER (μmol CO2 m^-2 s^-1).
  - CO2 storage term (CO2_strg, μmol CO2 m^-2 s^-1).
  - Meteorological: Ta (°C), RH (%), VPD (hPa), Pa (kPa).
  - Radiation: SW_in/ SW_out, LW_in/ LW_out, R_net.
  - PAR below canopy (PPFDbc), soil variables (G, Tsoil, VWC, Ts), wind metrics, footprint fraction.
- Missing data denoted by -9999.

## Acknowledgments and references
- Funded by the Natural Environment Research Council (CarboBiocrop) and the CEH Integrating Fund.
- Data collected with permission from landowners.
- References provided for methods and datasets used in processing and analysis.