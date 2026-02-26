# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a cropland and a grassland on lowland peatland soils, East Anglia Fens, UK, 2016 to 2019

- Purpose and scope
  - Time series observations of land surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) at two peatland sites in East Anglian Fens, UK.
  - Includes ancillary weather and soil physics data and variables characterising atmospheric turbulence.
  - Data processed to provide gap-filled fluxes and partitioning of NEE into gross ecosystem production (GEP) and total ecosystem respiration (TER).

- Study sites and context
  - Cropland site EF-SA: 52.44°N, 0.41°E, -2 m amsl; horticultural salad crops and cereals; degraded fen peats over clay; intensive drainage via sub-surface pipes.
  - Grassland site EF-GF: 52.47°N, -0.19°W, -1 m amsl; former arable peatland restored to wetland; low-intensity grazing and occasional mowing; drainage network present but not connected to regional system.
  - Region features: Fenland, UK’s largest contiguous lowland peatlands; temperate maritime climate, mean 1981–2010 temperature ~10.4°C, precipitation ~564 mm yr^-1.

- Sampling regime and data acquisition
  - Flux observations via eddy covariance above the canopy at 2.6 m height.
  - Open-path EC systems: LI-7500 gas analyzer; ultrasonic anemometers (Gill at EF-SA; Solent R3 at EF-GF).
  - Raw data: 20 Hz measurements of three velocity components, sonic temperature, and gas densities; logged with CR3000 dataloggers.
  - Ancillary measurements colocated with EC stations: air temperature, relative humidity, net radiation, short/longwave radiation components, soil heat flux, water table, soil moisture, soil temperature, precipitation.

- Flux data processing and quality control
  - Flux calculation with EddyPRO v6.1; 30-minute averaging.
  - QC procedures include: 20 Hz data QC, angle-of-attack corrections, 2D rotation to local terrain, spectral correction for attenuation, density corrections, and flux corrections for humidity and density effects.
  - Random uncertainties computed; non-stationary turbulence periods removed; fluxes outside specified physical ranges excluded.
  - Night-time NEE removal when fluxes were negative or below friction velocity thresholds (u*): 0.22 m s^-1 (EF-SA) and 0.16 m s^-1 (EF-GF).
  - Footprint check: retain fluxes with >75% predicted origin from the target ecosystem.
  - Weekly visual QC; manual outlier removal as needed.

- Data gap-filling and flux partitioning
  - Gap-filling of EC fluxes (NEE, LE, H) using Marginal Distribution Sampling (MDS) approach.
  - NEE partitioned into GEP and TER using Reichstein et al. (2005) methodology driven by air temperature.
  - Gap-filling and partitioning performed with REddyProc (R) package.

- Data structure and content
  - Time series provided in two separate ASCII CSV files; missing data indicated by -9999.
  - Data include both observed and gap-filled/partitioned fluxes for each site and corresponding ancillary variables.
  - Variables described in Table 1 (names, units, and descriptions); columns reflect thirty-minute time series.
  - Additional derived (gap-filled) products include NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, and GEP.

- Variables, units, and data coverage
  - Flux densities: NEE (μmol CO2 m^-2 s^-1), LE (W m^-2), H (W m^-2), τ (kg m^-1 s^-2); NEE_filled, LE_filled, H_filled, and corresponding uncertainties.
  - Derived terms: CO2 storage terms (CO2_strg), LE_strg, H_strg; GEP (μmol CO2 m^-2 s^-1); TER (μmol CO2 m^-2 s^-1).
  - Meteorology and environment: Ta (°C), RH (%), VPD (hPa), Pa (kPa), SWin, SWout, LWin, LWout, Rnet (W m^-2), G1/G2 (W m^-2), Tsoil1–Tsoil4 (°C), VWC1–VWC4 (%), Precipitation (mm per 0.5 h and total), WaterLevel (mm), Windspeed (m s^-1), Winddir (degrees), footprint metrics (x_peak, x_70, x_90).
  - Site-specific notes: EF-SA includes VWC at 0.1 m, soil moisture at 0.1–0.25 m; EF-GF includes corresponding measures at multiple depths.
  - Time coverage: EF-SA 2016-11-17 to 2018-09-24; EF-GF 2017-04-27 to 2019-03-31.

- Provenance and acknowledgments
  - Funded by NERC (SEFLOS, UK-SCAPE) and related projects; data collected with landowner permission and COSMOS-UK collaboration.
  - References and methodological sources cited for processing and gap-filling algorithms.

- Governance and stewardship considerations
  - Clear, standards-aligned data processing chain (raw 20 Hz to 30-minute fluxes; QC checks; footprint filtering; u* thresholds).
  - Comprehensive metadata and documentation of variables, units, and processing steps (EddyPRO, Reichstein 2005, REddyProc).
  - Gap-filled products accompany observed data, enabling reproducibility of flux partitioning analyses.
  - Data are organized for portal/dataset sharing with explicit handling of missing data (-9999) and quality flags implied by QC steps.