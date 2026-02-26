# Net ecosystem carbon dioxide (CO2) exchange and meteorological observations from an eroded, high altitude, blanket bog, Scotland, 2018-2020

- Purpose and scope
  - Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), plus accompanying meteorological observations.
  - Site: eroded upland blanket bog peatland (UK-BAL) in the Eastern Cairngorms, Scotland (56.93° N, -3.16° E, 642 m a.s.l.).
  - Context: peat erosion with bare peat gullies; future restoration planned (gully reprofiling) but no treatment during the study period.

- Experimental design and temporal coverage
  - Data types and resolution: 20 Hz eddy covariance (EC) CO2, water and energy fluxes processed to 30-minute means; meteorological data from 15-minute records processed to 30 minutes.
  - Observation window: 04/07/2018 – 04/11/2020.
  - Data availability issues:
    - Overall data capture: NEE ~51%, LE ~54%, H ~76% (30-minute flux data).
    - Biomet data 92–97% complete except long-wave radiation (LWout) around 80% due to a sensor fault in mid-2019.
    - Major power supply issue caused loss of data 14 Nov–27 Dec 2019; peat restoration activity during this time introduced wind-blown peat particles affecting the Li-7200 RS spectral response.
    - COVID-19 travel restrictions hindered repairs; NEE and LE data until mid-August 2020 were discarded.

- Collection methods and instrumentation
  - Fluxes: enclosed-path EC system with Windmaster sonic anemometer at 3.2 m and LI-7200 gas analyser for CO2 and H2O; Ta and RH measured at 2 m.
  - Additional measurements: net radiation (Rnet), short- and long-wave components, photosynthetically active radiation (PAR), soil heat flux, soil temperature at multiple depths, soil water content, precipitation, water table depth.
  - Site characteristics affecting data: fetch >1000 m in most directions; canopy height 0.25 m; semi-evergreen vegetation with light–moderate deer grazing.

- Calibration and data quality
  - Gas analyser calibrated per manufacturer guidelines prior to installation; limited on-site calibration during data capture due to remoteness.
  - QC steps included: outlier screening (MAD), stationarity tests, physically plausible flux limits, and friction velocity (u*) thresholds to exclude low-turbulence periods.
  - Flux processing: MAuder et al. (2013) framework; coordinated rotations and corrections for density effects, cospectral attenuation, and humidity influence; error estimates for fluxes derived from covariance variance.

- Data processing, gap-filling, and uncertainty
  - Gap-filling and partitioning: REddyProc (v0.8-2/r14) for gap-filling NEE, LE, and H; flux partitioning into GEP and TER.
  - Gap-filling method: marginal distribution sampling (MDS); Tair used as driving temperature for partitioning due to gaps in Tsoil.
  - Uncertainty: standard deviations of observations used to represent gap-filled flux uncertainties; annual sums enabled via interpolation of Braemar station data for driving variables.
  - Data status: NEE_filled, LE_filled, H_filled and corresponding uncertainties provided; storage terms included (CO2_strg, LE_strg, H_strg).

- Data structure and content
  - Delivered in a single CSV file with columns:
    DateTime, NEE, NEE_unc, LE, LEE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, Lwin, LWout, Rnet, G1, G2, Tsoil, WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP
  - Documentation clarifies unit definitions and descriptions (e.g., μmol CO2 m⁻² s⁻¹ for NEE, W m⁻² for LE/H, etc.).

- Data availability and provenance
  - Update to a previous deposit; this dataset provides a longer time series with 30-minute resolution.
  - Related metadata and prior deposits available via the CEH catalogue: https://catalogue.ceh.ac.uk/documents/b8c9fd3df9ea-4fd8-9557-9022884f711d
  - References for methodologies and QC standards are provided (e.g., Mauder et al. 2013; Reichstein et al. 2016; Moncrieff et al. 1997/2004).

- Relevance for environmental monitoring and policy
  - Delivers standardized, quality-controlled flux and meteorological data suitable for assessing ecosystem carbon balance and energy exchange over time.
  - Enables tracking of environmental health indicators, comparison with standards and policy performance, and integration with other datasets to enhance data value and accessibility.
  - Highlights challenges in remote-sensor data continuity, restoration activities, and data gaps, informing future monitoring design and data governance.

- Key considerations for analysts
  - Pay attention to data gaps and their treatments (gap-filled NEE/LE/H and uncertainty estimates).
  - Consider potential residual sensor issues around late 2019 to mid-2020 (e.g., Li-7200 spectral response during restoration and power-related losses).
  - Use provided respiration and production partitions (TER, GEP) for ecosystem productivity assessments.
  - Access to the full QC and processing documentation to understand applied corrections and uncertainty estimates.