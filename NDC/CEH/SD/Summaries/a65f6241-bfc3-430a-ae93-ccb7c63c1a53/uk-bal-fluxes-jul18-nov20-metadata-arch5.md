# Metadata pertaining to EIDC submission: 'Net ecosystem carbon dioxide (CO2) exchange and meteorological observations from an eroded, high altitude, blanket bog, Scotland, 2018-2020'

- Overview
  - Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), plus meteorological observations.
  - Study site: eroded upland blanket bog peatland (UK-BAL) in the Eastern Cairngorms, Scotland, UK (56.93° N, -3.16° E, 642 m a.s.l.).
  - Climate: maritime temperate montane; peat erosion with bare peat gullies; no treatment during observation period; future restoration planned.
  - Time period: 04/07/2018 to 04/11/2020.
  - Data gaps and issues: partial data coverage, major gaps due to power loss (Nov–Dec 2019) and wind-blown peat particles during restoration affecting Li-7200 RS spectral response; COVID travel restrictions delayed repairs until Aug 2020; NEE and LE data discarded until mid-August 2020; data capture percentages vary by variable.

- Dataset contents
  - Flux data: 30-minute processed flux densities for NEE, LE, H, plus associated storage terms (CO2_strg, LE_strg, H_strg) and related uncertainties.
  - Meteorological and ancillary data: air temperature, relative humidity, vapor pressure deficit, radiation components (SWin, SWout, LWin, LWout, Rnet), soil parameters (Tsoil at multiple depths, soil heat flux G1, G2, soil water content, water level), precipitation, wind metrics, friction velocity, Obukhov length, stability parameter, etc.
  - Gap-filled products and partitioned fluxes: NEE_filled, LE_filled, H_filled, plus standard deviations; TER (total ecosystem respiration) and GEP (gross ecosystem production) from flux partitioning.
  - Units and structure: data stored in a single CSV with columns including DateTime (UTC) and the full set of variables listed above, plus descriptive fields for each variable and its uncertainty.

- Site and data collection methods
  - Measurement system: enclosed-path eddy covariance (EC) setup with Windmaster sonic anemometer (3.2 m height) and LI-7200 gas analyser; 20 Hz sampling, aggregated to 30-minute means.
  - Additional micrometeorological sensors: net radiometer, PAR sensor, soil sensors (temperature at 0.05 m, 2, 5, 10, 20, 50 cm; volumetric water content), soil heat flux plates, rain gauge, water table pressure sensor.
  - Field conditions: fully vegetated surface; fetch >1000 m (SW) except N direction (~400 m due to cliff edge); canopy height assumed static at 0.25 m.
  - Calibration and maintenance: gas analyser calibrated per manufacturer; no on-site span/zero checks during data capture due to remoteness; instrument readings remained near 99% until mid-2019 and after cleaning in Aug 2020.

- Quality control and data processing
  - Flux calculation: EddyPRO v7.0.6; data screened for outliers; coordinate rotation and tilt corrections applied; lag removal; attenuation corrections; humidity corrections for LE; density corrections for CO2/ H2O exchange.
  - Uncertainty estimation: standard deviations derived from variance of covariance for 30-minute fluxes.
  - QC criteria: outlier screening (MAD), stationarity check (<100% deviation), physical bounds for fluxes, u* threshold (≥0.17 m/s) to exclude low-turbulence periods.
  - Gap-filling and partitioning: REddyProc (v0.8-2/r14) for gap-filling and NEE partitioning; marginal distribution sampling (MDS) for H, LE, NEE gap-filling; annual sums via interpolation to a nearby Braemar station for missing inputs; driving temperature used due to gaps in soil temperature data.

- Data structure and fields
  - Primary file: single CSV with columns such as DateTime, NEE, NEE_unc, LE, LEE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, Lwin, LWout, Rnet, G1, G2, Tsoil, WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.
  - Documentation references in metadata describe each field and units (e.g., NEE in μmol CO2 m^-2 s^-1; fluxes in W m^-2; temperatures in °C; pressures in kPa).

- Data provenance, availability and updates
  - This dataset updates a previously deposited data record (shorter time series, daily data rather than 30-minute data).
  - Related documentation and data availability: dataset update linked to CEH catalogue document; prior and supplementary details available through the CEH portal.
  - References underpinning methods and QC guidelines are listed (e.g., Mauder et al. 2013; Reichstein et al. 2016; others on flux processing and quality control).

- Particular data limitations and caveats for stewardship
  - Substantial data gaps in key variables, particularly NEE, LE, and H during several periods; data quality contingent on instrument performance and site conditions.
  - Spectral response issues in Li-7200 RS during wind-blown peat events; some data discarded due to restoration activities and power issues.
  - Gap-filled estimates rely on models and ancillary inputs; uncertainties are provided but users should treat gap-filled products with appropriate caution.
  - Some inputs (e.g., Tsoil) had missing periods, necessitating the use of driving temperature for flux partitioning.

- Governance and stewardship notes
  - Clear metadata on collection design, instruments, calibration, QC criteria, and gap-filling procedures to support reproducibility.
  - Documentation of data limitations and known issues to inform discovery, reuse, and data governance decisions.
  - Data are prepared for sharing through appropriate data portals and linked to broader catalogues; future data management should plan for ongoing updates, especially regarding restoration-related measurements and sensor maintenance.