# Supporting information for: Eddy Covariance measurements of carbon dioxide, energy and water flux at an intensively cultivated lowland deep peat soil, East Anglia, UK, 2012 to 2020.

## Overview of dataset
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Turbulent fluxes measured with eddy covariance (EC) at an intensively cultivated lowland deep peat site (EF-DA) in East Anglia, UK.
- Data span 2012-06-22 00:30 to 2020-01-01 00:00; raw 20 Hz observations and 30-minute block-averaged fluxes.
- Ancillary meteorological and soil-physics observations and variables describing atmospheric turbulence are included.
- Provided as gap-filled and partitioned time series (NEE into GEP and TER) along with associated uncertainties.

## Study site (including site activity, crop details)
- Location: East Anglian Fens, UK; EF-DA flux site at 52°31'N, 0°29'E, 0 m a.m.s.l. within Rosedene farm.
- Landscape: large peat-dominated lowland peatland used for agriculture; fields arranged with hedgerows and ditch networks.
- Climate: temperate maritime; mean 1981–2010 temp ~10.4°C, precipitation ~564 mm/year.
- Site history: drained and converted post-WWII for agriculture; peat depth ~2 m remains with mixed mineralization near the surface.
- Management and crops over the study period include lettuce (2012, 2014, 2016, 2018), leek (2013), celery (2015), sugar beet (2017), and potatoes (2019).

## Sampling regime
- Automated measurements of fluxes, meteorology, and soil physics collected throughout the study period (2012-06-22 00:30 to 2020-01-01 00:00).

## Flux data acquisition
- EC observations above canopy at 1.5 m height.
- Instrumentation: LI-COR LI-7500 open-path CO2/H2O IRGA and CSAT3 sonic anemometer, oriented to wind from 225°.
- Raw data: three velocity components, sonic temperature, water vapour and CO2 densities; sampled at 20 Hz and logged with a CR3000 Micrologger.
- Wind direction measured relative to prevailing south-west wind; footprint considerations applied in quality checks.

## Ancillary data acquisition
- Radiometry: NRLite2 and CNR4 radiometers for net radiation (Rnet) and short/longwave components.
- PAR: SKP01 Quantum sensor.
- Air conditions: Ta and RH measured in a shielded sensor at 2 m.
- Precipitation: ARG100 tipping-bucket gauge 4 m from EC setup.
- Soil physics: two arrays beneath EC: soil heat flux (HFP01-SC), averaging soil temperature sensors (TCAV), and time-domain reflectometry for volumetric peat moisture (CS616).
- Data were logged as 30-minute means or sums (precipitation).

## Data processing
- Flux calculation: Fluxes derived with EddyPRO v6.1; 30-minute block averages; QC applied to 20 Hz data.
- Corrections: 2D coordinate rotation, high/low-frequency co-spectral attenuation, humidity effects on H, density corrections for LE and CO2.
- Uncertainties: random uncertainties computed per standard methods.
- Additional outputs: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L), and half-hour footprint estimates (ART/Neftel model).

## Quality control
- Outliers removed using median absolute deviation; non-stationary turbulence periods excluded.
- Flux ranges for QC: H: -200 to 400 W m^-2; LE: -200 to 600 W m^-2; NEE: -40 to 40 μmol CO2 m^-2 s^-1.
- NEE removal during night when fluxes negative.
- Footprint criterion: retained if >70% of flux originated from target ecosystem as predicted by footprint model.
- Weekly plotting and manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (MDS) approach (Reichstein et al., 2005) for EC data gaps (NEE, LE, H).
- Partitioning: NEE split into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Reichstein et al. framework; driven by air temperature (Ta).
- Tools: REddyProc package in R for gap-filling and partitioning.

## Details of data structure
- Data delivered as a CSV with tabular ASCII format; includes described columns (see Table 1 in the dataset documentation).
- Gap-filled and partitioned time series provided for the full period of record.
- Missing records denoted by -9999.

## Nature and units of recorded values
- Time: DateTime in yyyy-mm-dd HH:MM:SS (GMT/UTC).
- NEE: μmol CO2 m^-2 s^-1; NEE_unc: μmol CO2 m^-2 s^-1.
- LE: W m^-2; LE_unc: W m^-2.
- H: W m^-2; H_unc: W m^-2.
- Tau: kg m^-1 s^-2; Tau_unc: kg m^-1 s^-2.
- Additional fields include CO2_strg, LE_strg, H_strg, Pa, Ta, RH, VPD, Rnet, Rg, G, Tsoil, VWC, Precipitation, Windspeed, Winddir, FootprintFraction, Ustar, TKE, Tstar, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, and related uncertainty terms.

## Acknowledgements
- EF-DA flux site established by NERC Urgency grant NE/K001590/1; ongoing support from NERC and affiliated programs.
- Long-term collaboration with landowners and farm management; gratitude extended to site coordinators and field staff.