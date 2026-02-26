# Net ecosystem carbon dioxide (CO2) exchange and meteorological observations from an eroded, high altitude, blanket bog, Scotland, 2018-2020

## Overview
- Time-series dataset of land surface–atmosphere exchanges, including net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and a suite of meteorological observations.
- Focused on an eroded upland blanket bog peatland (UK-BAL) in the Eastern Cairngorms, Scotland, at 642 m a.s.l.
- Data span: 04/07/2018 – 04/11/2020; future peatland restoration via gully reprofiling anticipated.
- Fluxes derived from an eddy covariance system and processed to 30-minute intervals; accompanying meteorology processed to 30-minute means.

## Site and experimental context
- Location: 56.93° N, -3.16° E; maritime temperate montane climate (Köppen Dfc).
- Peat erosion widespread; bare peat gullies 0.5–3 m deep and 2–10 m wide.
- Site had no treatment within the flux footprint during observation; potential restoration planned for the future.
- Vegetation: semi-evergreen, canopy height ~0.25 m; deer grazing present.
- Sensor fetch: SW direction >1000 m (except N due to a cliff with ~400 m fetch).

## Data collected and measurements
- Fluxes: NEE, LE, H measured with an enclosed-path eddy covariance system; 20 Hz raw data aggregated to 30-minute means.
- Meteorology: wind, temperature, humidity, radiation (Rnet, SWin, SWout, LWin, LWout), PAR, precipitation, water table depth, soil temperature, soil moisture, and soil heat flux.
- Auxiliary: CO2 storage term, multiple atmospheric and soil parameters included in the dataset.

## Methods, instrumentation, and processing
- Flux measurement setup:
  - EN system: Windmaster sonic anemometer at 3.2 m; LI-COR LI-7200 gas analyzer; air temperature and RH at 2 m.
  - Radiation: SN500 Net Radiometer at 2.06 m; PAR at 2.25 m.
  - Soil: two HFP01SC soil heat flux plates; Tsoil at multiple depths; TDT probes for soil moisture; water table depth sensor; tipping-bucket rainfall gauge.
- Calibration and maintenance:
  - Gas analyser calibrated per manufacturer; no on-site span/zero checks during data capture due to remoteness; post-cleaning (Aug 2020) sensor performance returned near 99%.
- Data processing:
  - QC and processing with EddyPRO and REddyProc:
    - Outlier screening (robust statistical criteria).
    - Coordinate rotation and cospectral corrections.
    - Corrections for density effects (WPL corrections) and humidity influence.
    - Random uncertainty estimates via variance-based approach.
  - Data gap-filling and partitioning:
    - Gap-filled NEE, LE, H using marginal distribution sampling (MDS).
    - Flux partitioning yields GEP and TER from NEE.
    - Tair used as driving temperature for partitioning due to gaps in Tsoil.
    - Gaps bridged using Braemar station data for annual sums.
  - Quality control criteria:
    - Stationarity tests; plausible value ranges; low turbulence identified via u* threshold (u* < 0.17 m/s excluded).
- Data governance and openness:
  - Emphasis on data provenance, quality, and clear presentation of uncertainty.
  - Data prepared for sharing with underlying measurements and gap-filled products documented.

## Nature and units of recorded values
- Variables include: DateTime (UTC), NEE, NEE_unc, LE, LEE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G1, G2, Tsoil, WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
- NEE_filled, LE_filled, H_filled and related uncertainties reflect gap-filled products; TER and GEP provide partitioned flux components.

## Data quality, gaps, and limitations
- Gaps in data coverage: NEE (51%), LE (54%), H (76%) across the observation window.
- Notable data losses and issues:
  - 14 Nov – 27 Dec 2019: major power supply problem caused data loss during a period of peat restoration activity that introduced wind-blown peat particles affecting Li-7200 spectral response.
  - Mid-2019: wind-blown peat particles from restoration affected gas analyzer performance.
  - COVID-19 restrictions delayed maintenance and repair until Aug 2020.
- Data update context:
  - This dataset updates a previously deposited record by providing longer, higher-frequency (30-minute) data versus a shorter daily-time-series version.

## Data structure and accessibility
- Data stored in a single CSV file with clearly labeled columns corresponding to the variables described above.
- Dataset linked to a prior deposition, described as an update with documentation and an external reference for the full data lineage.

## Data provenance and references
- References to quality and uncertainty methods for eddy covariance (Mauder et al. 2013; Vickers & Mahrt 1997; Wilczak et al. 2001; Nakai et al. 2006; Moncrieff et al. 1997, 2004; Schotanus et al. 1983; Webb et al. 1980; Papale et al. 2006; Reichstein et al. 2016) and data processing tools (REddyProc) used for processing, gap-filling, and uncertainty estimation.
- Data provenance note: update to a previously deposited dataset; link provided for additional metadata and context.