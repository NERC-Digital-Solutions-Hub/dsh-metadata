Metadata pertaining to EIDC submission: 'Net ecosystem carbon dioxide (CO2) exchange and meteorological observations from an eroded, high altitude, blanket bog, Scotland, 2018-2020'

## Overview
- Time-series measurements of net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and meteorology from an eroded upland blanket bog in Scotland (UK-BAL, Eastern Cairngorms).
- Dataset covers 04/07/2018 to 04/11/2020; data include 30-minute fluxes (NEE, H, LE) and 30-minute meteorology derived from 20 Hz and 15 min measurements.
- Observations faced data gaps due to sensor issues, power problems, peat restoration-related disturbances, and COVID-related access delays; some NEE/LE data discarded after mid-August 2020.
- No treatments applied during the observation period; peatland restoration (gully reprofiling) planned for the future.

## Study site and context
- Location: 56.93° N, -3.16° E, 642 m a.s.l.; maritime temperate montane climate (Köppen Dfc edge).
- Landscape: eroded blanket bog with bare peat gullies 0.5–3 m deep and 2–10 m wide.
- Vegetation: fully vegetated surface; canopy height ~0.25 m; semi-evergreen with deer grazing.
- Purpose: provide eddy covariance fluxes and meteorology to inform carbon and energy exchange at degraded peatlands; future restoration activities may influence fluxes.

## Data collected
- Fluxes: 30-minute NEE (μmol CO2 m^-2 s^-1), LE (W m^-2), H (W m^-2); NEE gap-filled (NEE_filled) and associated uncertainties; CO2 storage term (CO2_strg) and related storage terms (LE_strg, H_strg).
- Meteorology and auxiliary data: Pa, Tair, RH, VPD; radiation (SWin, SWout, LWin, LWout, Rnet); soil temperature (Tsoil at multiple depths), soil moisture (VWC), soil heat flux (G1, G2); precipitation; water level; wind (WS, WD); friction velocity (Ustar); turbulence metrics (TKE, zL, L).
- Data quality indicators: NEE_unc, LE_unc, H_unc; filled data (NEE_filled, LE_filled, H_filled) with associated uncertainties (sd).

## Collection methods and instrumentation
- Eddy covariance system: Windmaster sonic anemometer at 3.2 m; LI-COR LI-7200 enclosed-path gas analyzer for CO2 and H2O; 0.1 m sensor separation; 1.0 m inlet tube.
- Ancillary sensors: air temperature and RH at 2 m (Rotronic Hygroclip); net radiometer (SWin, SWout, LWin, LWout) above canopy; PAR at 2.25 m; soil probes for Tsoil, VWC; soil heat flux plates; tipping-bucket precipitation gauge; water table pressure sensor.
- Data logging: 20 Hz sampling for EC and micrometeorology, later averaged to 30-minute means; site features potential fetch limitations due to cliff edge to the north.

## Calibration and data quality
- Gas analyser calibrated per manufacturer guidelines prior to installation; limited on-site span/zero checks during data collection due to remoteness; instrument performance remained near 99% until late 2019; cleaning in Aug 2020 improved performance.
- Data scrubbing and quality checks followed established protocols; outlier removal, stationarity checks, and physically implausible value filters applied.
- Measurements corrected for cospectral attenuation, humidity effects, and density fluctuations; CO2 storage considered negligible at measurement height; sign convention: positive fluxes mean ecosystem to atmosphere.

## Processing, quality control, and gap-filling
- Flux calculation: 30-minute flux densities computed with EddyPRO v7.0.6; cross-correlation for lag removal; standard corrections for atmospheric conditions and sensor response; random uncertainties derived from variance of covariances.
- Gap-filling and partitioning: NEE partitioned into GEP and TER via REddyProc; gap-filling for H, LE, and NEE using marginal distribution sampling; annual data gaps bridged using Braemar station observations; Tair used as driving temperature for partitioning due to gaps in Tsoil.
- Uncertainty: gap-filled flux uncertainties estimated as the standard deviation of observations used to fill gaps.

## Data structure and metadata
- Data stored in a single CSV file with columns: DateTime, NEE, NEE_unc, LE, LEE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, Lwin, LWout, Rnet, G1, G2, Tsoil, WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
- Documentation includes detailed definitions and units for each field; data are aligned to GMT (UTC).

## Limitations, data gaps, and notable issues
- Data coverage varied: 51% (NEE), 54% (LE), 76% (H); longwave radiation data missing ~20% due to sensor fault (mid-2019).
- November–December 2019: data loss due to major power supply issue; peatland restoration nearby caused wind-blown peat contamination affecting Li-7200 LiDAR spectral response; data discarded for NEE and LE up to mid-August 2020.
- COVID-19 restrictions delayed site maintenance and data validation; some corrections and fixes could not be performed until August 2020.

## Availability and references
- Dataset is an update to previously deposited data; shorter time series and daily data in the updated release.
- Related data and metadata available at the CEH catalogue: https://catalogue.ceh.ac.uk/documents/b8c9fd3df9ea-4fd8-9557-9022884f711d
- References for methods and processing (Mauder et al. 2013; Vickers & Mahrt 1997; Wilczak et al. 2001; Nakai et al. 2006; Moncrieff et al. 1997, 2004; Schotanus et al. 1983; Webb et al. 1980; Papale et al. 2006; Reichstein et al. 2016; Reichstein et al. 2005).