# Net ecosystem carbon dioxide (CO2) exchange and meteorological observations from an eroded, high altitude, blanket bog, Scotland, 2018-2020

- What the dataset contains
  - Time series observations of net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and meteorological observations from an eroded upland blanket bog peatland (UK-BAL) in the Eastern Cairngorms, Scotland (56.93° N, -3.16° E, 642 m above sea level).
  - Site characteristics: maritime temperate montane climate; extensive peat erosion with bare peat gullies (0.5–3 m deep, 2–10 m wide). No experimental treatments during the observation period; peatland restoration planned for the future (gully reprofiling).
  - Data types and cadence: eddy covariance CO2, water, and energy fluxes (originally 20 Hz, processed to 30-minute means) plus accompanying meteorological observations (originally 15 min, processed to 30-minute means).
  - Time period: 04 July 2018 – 04 November 2020.
  - Data coverage: NEE 51%, LE 54%, H 76% across the monitoring period; biomet data capture 92–97% (except long-wave radiation at ~80% due to a faulty sensor in mid-2019). Gaps include 14 Nov–27 Dec 2019 due to a major power supply issue; wind-blown peat affected Li-7200 spectral response during that period, forcing discard of NEE and LE data until mid-August 2020 due to COVID-related travel restrictions preventing timely repair.

- Site and instrumentation
  - Eddy covariance (EC) system: enclosed-path EC with a Windmaster sonic anemometer at 3.2 m and LI-7200 CO2/H2O gas analyser; horizontal spacing 0.1 m; LI-7200 inlet tube 1.0 m; air temperature and relative humidity at 2 m above surface.
  - Additional micrometeorology and environmental sensors: net radiation, PAR, soil heat flux, soil temperature at multiple depths, soil volumetric water content, precipitation, water table depth.
  - Measurement height and fetch: canopy height assumed 0.25 m; fetch >1000 m in most wind directions except N (cliff edge limits fetch to ~400 m).
  - Field conditions: fully vegetated sampling site; semi-evergreen vegetation with light-to-moderate deer grazing.

- Calibration and data quality considerations
  - Gas analyser calibration performed prior to installation; due to remoteness, span/zero checks could not be conducted during data capture; post-cleaning in Aug 2020 the instrument performed near 99% signal fidelity.
  - Data screening and QA/QC: outlier detection, coordinate rotation and tilt corrections, cross-correlation lag removal, cospectral attenuation corrections, humidity correction, and density corrections for CO2/H2O.
  - Uncertainties: random uncertainties derived from variance of covariance; CO2 storage considered negligible at the measurement heights; turbulence-based exclusion criteria used (stationarity, reasonable flux ranges, and u* threshold of 0.17 m/s).

- Data processing, gap-filling, and flux partitioning
  - Flux calculation: 30-minute flux densities for NEE, LE, and H computed with EddyPRO (v7.0.6); data screened for physical plausibility and corrected for instrumental effects.
  - Gap-filling and partitioning: gap-filled NEE, LE, and H using marginal distribution sampling (MDS); partitioning of NEE into GEP and TER performed with REddyProc (v0.8-2/r14); annual sums aided by interpolation from Braemar station data.
  - Driving temperature for partitioning: Tair used due to gaps in Tsoil data.
  - Uncertainty propagation: standard deviation estimates for gap-filled fluxes.

- Data structure and format
  - Single CSV file with columns including: DateTime, NEE, NEE_unc, LE, LEE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G1, G2, Tsoil, WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
  - Units and descriptions provided in the dataset documentation (e.g., NEE in μmol CO2 m^-2 s^-1; fluxes in W m^-2; Pa in kPa; Tair in °C; etc.).
  - Metadata includes both raw (QC’ed but not gap-filled) and gap-filled values, plus associated uncertainties.

- Data availability, interpretation, and usage notes
  - This dataset is an update to a previously deposited dataset with shorter time series and daily data; see CEH catalogue link for related deposits.
  - Useful for analyses of net ecosystem exchange and energy fluxes in eroded upland blanket bogs, flux partitioning into gross primary production and ecosystem respiration, and understanding near-surface energy and moisture balance under high peat erosion conditions.
  - Limitations to consider when using the data: substantial data gaps (especially in 2019), partial sensor outages (long-wave radiation), and data loss periods due to power and restoration activities; some data were discarded (NEE/LE) during affected intervals.

- Availability and references
  - Related dataset update: CEH data catalogue entry (link provided in the dataset notes).
  - Key methodological references for processing and QA/QC of eddy covariance data and gap-filling/partitioning approaches (Mauder et al. 2013; Reichstein et al. 2016; Reichstein et al. 2005; Moncrieff et al. 1997, 2004; Webb et al. 1980; etc.).