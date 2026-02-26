# Carbon dioxide and methane fluxes and associated environmental observations from paired burned/unburned peatland undergoing restoration

- Purpose and scope
  - Time series of land surface–atmosphere exchanges including net ecosystem CO2 exchange (NEE), methane (CH4), sensible heat (H), latent heat (LE), and meteorological observations.
  - Two blanket bog sites on Forsinard RSPB Reserve, Flow Country, Scotland, within a former forestry block affected by a wildfire in May 2019.
  - Paired design: burned site (UK-DKF) and nearby restored/unburned site (UK-DKE-RESTORED) to assess effects of fire and restoration on fluxes.
  - Coordinate-level site locations provided; footprints and fetch described to inform spatial interpretation.

- Study design and location
  - UK-DKF: site within the former forestry block burned by wildfire; footprint largely in SW wind direction.
  - UK-DKE-RESTORED: located ~360 m SE of UK-DKF; area protected from fire to protect instrumentation; location moved slightly from previous measurements (2016–2017).
  - Coordinates (approximate): UK-DKF (58.431, -3.96); UK-DKE-RESTORED (58.428, -3.967).
  - Footprint/fetch: ~300 m in SW direction; minor obstruction from a small water course at ~115 m.
  - Vegetation and canopy: semi-evergreen peatland; canopy height relatively static post-burn; deer grazing pressure minimal to moderate.

- Data collected and temporal coverage
  - Fluxes: 30-minute densities of LE, H, NEE, CH4 (from eddy covariance, 20 Hz raw data aggregated to 30-minute means).
  - Meteorology and micrometeorology: 30-minute data for air temperature, relative humidity, wind, radiation (Rn, Rg, PPFD), soil temperature, soil moisture, soil heat flux, water table depth, and precipitation.
  - Time period: 25/09/2019 – 20/05/2021 (with significant data gaps due to instrument issues, weather, site management, and COVID-19). Data capture after 16/10/2020 (and noted after 16/10/2021 in some sections) includes additional gaps.
  - Data availability: both raw (mixing ratio) and processed fluxes provided to maximize data utility.

- Instrumentation and methods
  - Eddy covariance system: enclosed-path EC system with Windmaster Pro sonic anemometer (height ~2.3–2.55 m) and LI-COR LI-7200 gas analyser for H2O/CO2; open-path Li-7700 for CH4.
  - Additional sensors: Ta, RH (2 m), net radiation (Rn), incoming shortwave (Rg), PPFD; soil measurements (G, Ts, SWC) at multiple microforms within ~5 m; water table depth; precipitation gauge.
  - Data logging and processing: sensors logged at 20 Hz; 30-minute fluxes calculated with EddyPRO v7.0.6; QA steps include outlier screening, two-dimensional tilt correction, lag removal, cospectral corrections, humidity correction, and density corrections.
  - Calibration and QA: gas analysers calibrated per manufacturers’ instructions; no on-site span/zero checks during deployment; June 2021 zero/span check conducted; data screened minimally due to patchiness; quality flags included for future use.

- Data structure, units, and quality flags
  - Data structure: single CSV file with columns for DateTime and a comprehensive set of variables (e.g., SWC, Ts, Ta, RH, PPFD, Rn, Rg, P_rain, WTD, G, H, LE, co2_flux, h2o_flux, ch4_flux, co2_mixing_ratio, h2o_mixing_ratio, ch4_mixing_ratio, u*, L, wind_speed, wind_dir, (z-d)/L, etc.).
  - Flags: per variable quality flags indicating raw, primary, calibrated status, data gaps, interpolations, or model-filled values; maximum interpolation gap is 1 hour.
  - References for methods: Mauder et al. (2013), Vickers & Mahrt (1997), Wilczak et al. (2001), Nakai et al. (2006), Moncrieff et al. (1997, 2004), Schotanus et al. (1983), Webb et al. (1980).

- Spatial relevance for GIS
  - Provides geolocated flux data at two peatland sites with documented footprints and fetch, enabling landscape-scale integration and spatial analysis of fire/restoration effects on carbon and methane fluxes.
  - The dataset's 30-minute temporal resolution supports linking fluxes to time-sliced spatial layers (e.g., weather, soil moisture, vegetation condition) in GIS.
  - Clear site metadata and instrumentation layout aid mapping of measurement locations and surrounding topography/hydrology.

- Limitations and caveats for use
  - Patchy data coverage with notable gaps due to instrument faults, power supply issues, weather, site management, and COVID-19 restrictions.
  - Calibration and on-site maintenance limitations due to remoteness; zero/span checks performed but drift minimal as of June 2021.
  - Data are provided with minimal screening; users should leverage included quality flags and refer to the cited QA methodology for uncertainty assessment.

- References and access notes
  - Data submitted in the context of an EIDC submission; authors: Rebekka Artz, Mhairi Coyle, Adrian Bass, and Roxane Andersen.
  - Methodological references for flux calculation, quality control, and processing are included within the metadata.