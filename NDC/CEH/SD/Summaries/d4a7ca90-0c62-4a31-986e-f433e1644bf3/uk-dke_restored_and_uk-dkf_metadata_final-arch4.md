# Metadata pertaining to EIDC submission: 'Carbon dioxide and methane fluxes and associated environmental observations from paired burned/unburned peatland undergoing restoration'

- Overview
  - Time-series observations of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), methane (CH4), sensible heat (H), latent heat (LE), plus meteorological data.
  - Two blanket bog sites on Forsinard RSPB Reserve, Flow Country, Scotland, formed from former forestry plantation affected by a 2019 wildfire.
  - Paired sites: UK-DKF (burned area footprint) and UK-DKE-RESTORED (restoration area protected from fire; instrumentation relocated slightly from prior site).
  - Time period: 25 Sep 2019 – 20 May 2021 (with data capture issues noted); notable gaps after 16 Oct 2020 due to instrumental problems and COVID-19 travel restrictions.

- Experimental design and scope
  - Objectives tied to peatland restoration effects on carbon, water, and energy fluxes under wildfire impact.
  - Restoration context: forestry felled in 2017, followed by wildfire in May 2019; RESTORED site located ~360 m SE of the burned site.
  - Footprint and wind: data collected in SW fetch direction with ~300 m fetch, affected by a small watercourse to the SW.

- Data collected and time resolution
  - Flux data: 30-minute averages of NEE, CH4, LE, and H derived from 20 Hz raw eddy covariance measurements.
  - Meteorology and environmental sensors: 15-minute data, processed to 30-minute means; includes air temperature, relative humidity, radiation, soil temperature, soil heat flux, soil water content, precipitation, and water table depth.
  - Data packages include raw mixing ratios and processed fluxes to maximize data availability.

- Measurement methods and instrumentation
  - Eddy covariance system: enclosed-path systems with Windmaster Pro sonic anemometers (height 2.3–2.55 m) and LI-COR LI-7200 gas analyser for water vapor and CO2.
  - Methane flux: open-path Li-7700 analyser.
  - Meteorological sensors: Ta, RH at 2 m; net radiation (Rn), incoming radiation (Rg), and photosynthetically active radiation (PPFD); soil measurements near the EC mast.
  - Canopy characteristics: static canopy height estimates; patchy vegetation due to burn recovery stage; deer grazing pressures present.
  - Spatial context: a nearby watercourse and varying microforms (plough furrow, planting ridge, peat surface) considered in soil measurements.

- Data processing and quality control
  - Primary processing with EddyPRO (v7.0.6) including:
    - 2D coordinate rotation, corrections for imperfect cosine response, time-lag removal, cospectral attenuation corrections, density corrections, and CO2 storage consideration.
    - Sign convention: positive fluxes from ecosystem to atmosphere.
  - Calibration and QA:
    - Gas analysers calibrated per manufacturer instructions; no on-site span/zero checks during data capture due to remoteness; June 2021 zero/span check performed with no significant drift.
    - Data screened minimally due to patchy capture; quality flags provided to indicate data status and processing steps.
  - Data flags:
    - Coding system includes raw, primary, calibrated, removed data, interpolations, and model-based fills with Mauder and Foken references; maximum gap interpolation allowed up to 1 hour.

- Data structure and units
  - Single CSV file containing columns for DateTime and all sensor variables (e.g., SWC, Ts, Ta, RH, PPFD, Rn, Rg, P_rain, WTD, G, H, LE, co2_flux, h2o_flux, ch4_flux, co2_mixing_ratio, h2o_mixing_ratio, ch4_mixing_ratio, u*, L, wind_speed, wind_dir, (z-d)/L) plus corresponding FLAG columns.
  - Units provided in the metadata (e.g., fluxes in W m-2 for H and LE, μmol CO2 m-2 s-1 for co2_flux, μmol CH4 m-2 s-1 for ch4_flux, m3 m-3 for soil water content, °C for temperatures, etc.).

- Calibration, data quality, and metadata references
  - Calibration: standard manufacturer procedures; on-site checks limited by remoteness; June 2021 check indicated no significant drift.
  - Quality references for methods: Mauder et al. (2013), Vickers & Mahrt (1997), Wilczak et al. (2001), Nakai et al. (2006), Moncrieff et al. (1997, 2004), Schotanus et al. (1983), Webb et al. (1980).

- Data availability, access, and limitations
  - Data provided to enable broad use: raw mixing ratios, 30-minute processed fluxes, and accompanying meteorological data.
  - Some data gaps due to equipment power issues, sonic anemometer problems, site management constraints, adverse weather, and COVID-19 travel restrictions; post-16 Oct 2020 data show notable gaps.
  - Additional data details available on request; dataset designed to support inter-site comparisons (burned vs. RESTORED) and restoration-related flux analyses.

- Implications for data strategy and reuse
  - Rich, high-frequency flux data with comprehensive metadata supports assessment of restoration impacts on carbon and energy exchange, as well as cross-site comparisons.
  - Important considerations for reuse: patchy data requiring careful handling of gaps and flag-informed quality assessment; clear documentation of instrumentation, calibration status, and site conditions.
  - Encourages adherence to open quality control practices and documentation to enable cross-network synthesis in peatland restoration studies.