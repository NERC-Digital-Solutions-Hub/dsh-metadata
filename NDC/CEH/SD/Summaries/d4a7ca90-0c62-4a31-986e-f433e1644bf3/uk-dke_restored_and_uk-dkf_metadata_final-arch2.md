# Carbon dioxide and methane fluxes and associated environmental observations from paired burned/unburned peatland undergoing restoration

- Location and context
  - Forsinard RSPB Reserve, Flow Country, Caithness and Sutherland, Scotland
  - Two peatland sites within former forestry blocks: UK-DKF (burned area by wildfire, SW wind footprint) and UK-DKE-RESTORED (area protected from fire 360 m SE of UK-DKF)
  - Former forestry felled in Nov 2017; large wildfire May 2019; restoration as first hydrological peatland restoration step
  - Timeframe: 25/09/2019 to 20/05/2021 (data capture through 16/10/2020 with notable gaps; some data post-2020 with additional power/logger issues)

- What was measured
  - Eddy covariance fluxes (30-minute) and meteorology
    - Net ecosystem CO2 exchange (NEE)
    - Methane flux (CH4)
    - Sensible heat flux (H) and latent heat flux (LE)
  - Raw data at 20 Hz; processed to 30-minute values
  - Meteorological and micrometeorological variables (30-minute): air temperature, relative humidity, wind speed/direction, friction velocity, Obukhov length, net radiation, incoming shortwave radiation, photosynthetically active radiation, soil heat flux, soil temperature, soil water content, water table depth (later in 2021), precipitation
  - Additional soil and canopy observations: canopy height (static post-fire), peat slope microforms (plough furrow, planting ridge, original peat surface)

- Instrumentation and collection methods
  - Enclosed path eddy covariance system for LE, H, NEE; open-path for CH4
  - Sonic anemometer heights: 2.3–2.55 m
  - Gas analysers: LI-COR LI-7200 (H2O/CO2) and Li-7700 (CH4)
  - Temperature, humidity, and radiation sensors at ~2 m height
  - Data loggers and sampling: 20 Hz (EC), 15-minute to 30-minute aggregation; micrometeorology at 0.1 Hz aggregated to 30-minute means
  - Calibration: per manufacturers; limited on-site span/zero checks due to remoteness; one zero/span check June 2021 with no significant drift

- Data processing and quality control
  - Flux calculations with EddyPRO v7.0.6
  - Standard micrometeorological data processing: coordinate rotation, density corrections, cospectral attenuation, time-lag removal, etc.
  - Sign convention: positive fluxes from ecosystem to atmosphere
  - Quality control notes
    - Extremely patchy data capture; dataset submitted without full screening
    - Quality flags included for future use
  - Data provenance and references for QA standards included (Mauder et al. 2013; Mauder & Foken 2004; Wilczak et al. 2001; Nakai et al. 2006; Moncrieff et al. 1997, 2004; Schotanus et al. 1983; Webb et al. 1980)

- Data structure and contents
  - Single CSV file
  - Columns include:
    - DateTime; NEE, CH4_flux, co2_flux, h2o_flux, LE, H
    - Environmental variables: SWC_1_1_1, SWC_2_1_1, SWC_3_1_1; Ts_1_1_1, Ts_2_1_1, Ts_3_1_1; Ta_1_1_1; RH_1_1_1; PPFD_1_1_1; Rn_1_1_1; Rg_1_1_1; P_rain_1_1_1
    - Soil and energy flux: G (soil heat flux), WTD (water table depth, later flag)
    - Turbulence and stability: u*, L (Obukhov length), wind_speed, wind_dir, (z-d)/L
    - Flags: FLAG SWC_*, FLAG Ts_*, FLAG Ta_*, FLAG RH_*, etc. with codes for raw, reviewed, calibrated, data gaps, interpolations, etc.
  - Flagging scheme
    - 000 = raw data; 001 = primary data; 002 = calibrated; 003 = no data; 004 = removed faulty data
    - 01#/02#/03# = interpolated, filled with alternative data, or modeled data
    - 1##/2##/3## = Mauder and Foken (2004) data quality flags
    - Maximum interpolation gap: 1 hour

- Temporal coverage and gaps
  - Primary period: 25/09/2019 – 20/05/2021
  - 16/10/2020 onward: data gaps due to sonic anemometer/power supply issues at both towers; later 2021 gaps due to power/logger faults
  - Water table depth was not installed at FIRE until later in 2021

- Key context and limitations for analysts
  - Paired burned vs. unburned/restored peatland provides a restoration context to study CO2 and CH4 exchange dynamics
  - Data patchiness and limited on-site calibration may affect absolute accuracy; users should leverage quality flags and be mindful of gaps
  - Some post-2020 data may have limited coverage due to hardware issues and external constraints (weather, COVID)

- References and methodological provenance
  - Data processing and QA references include Mauder et al. (2013), Vickers & Mahrt (1997), Wilczak et al. (2001), Nakai et al. (2006), Moncrieff et al. (1997, 2004), Schotanus et al. (1983), Webb et al. (1980)