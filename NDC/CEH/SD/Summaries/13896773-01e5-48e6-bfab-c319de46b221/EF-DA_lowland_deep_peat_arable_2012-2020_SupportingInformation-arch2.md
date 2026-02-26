# Eddy Covariance measurements of carbon dioxide, energy and water flux at an intensively cultivated lowland deep peat soil, East Anglia, UK, 2012 to 2020.

- Overview of dataset
  - Time series of land surface–atmosphere fluxes: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured at EF-DA site from 2012-06-22 00:30 to 2020-01-01 00:00.
  - Turbulent fluxes obtained with an open-path eddy covariance system; auxiliary weather and soil physics observations included; turbulence characterization available.

- Study site and crop details
  - Location: East Anglian Fens, UK (The Fenland) with the largest contiguous lowland peat in the UK.
  - Agricultural setting: drainage-driven peatland used for crops; site at Rosedene Farm (52°31'N, 0°29'E).
  - Climate: temperate maritime (mean 1981–2010 values: T ~10.4°C, precipitation ~564 mm yr⁻¹).
  - Time-varying crops over the study period (lettuce, leek, celery, sugar beet, potatoes); detailed management and yields described by the dataset authors.

- Sampling regime and data collection
  - Automated, colocated flux, meteorological, and soil physics measurements.
  - Flux tower height: 1.5 m above canopy; sampling at 20 Hz; 30-minute flux averages.
  - EC instrumentation: LI-7500 IRGA for CO2/H2O and CSAT3 sonic anemometer; sites oriented to SW wind.
  - Ancillary sensors: net radiation and components (Rnet, Rg), PAR, air temperature, relative humidity, precipitation; soil heat flux, soil temperature, volumetric peat moisture content; multiple sensor locations.

- Data processing and quality control
  - Flux calculation with EddyPRO v6.1; QC includes 20 Hz data screening, 2-D rotation, corrections for co-spectral attenuation, density effects, and humidity.
  - Random uncertainties derived using established methods; non-stationary turbulence periods removed; flux ranges screened (H, LE, NEE).
  - Footprint filtering to ensure >70% of flux originates from the target ecosystem; weekly visual QA and manual outlier removal.

- Gap-filling and flux partitioning
  - Data gaps in EC fluxes filled using Marginal Distribution Sampling (Reichstein et al., 2005).
  - NEE partitioned into gross ecosystem production (GEP) and total ecosystem respiration (TER) via standard Reichstein-based approach driven by air temperature.
  - Gap-filling and partitioning performed with the REddyProc package in R.

- Data structure and content
  - Delivered as a CSV time series with 30-minute records; missing data flagged as -9999.
  - Variables include NEE, NEE_filled, NEE_filled_sd, LE, H, Tau, and their respective uncertainty terms; storage terms and CO2, energy, and momentum components.
  - Ancillary variables cover atmospheric (Ta, RH, VPD, Pa, wind speed/direction), radiative (Rnet, Rg, G), soil (Tsoil, VWC), precipitation, footprint fraction, Ustar, TKE, L, z/L, and NEE_filled related outputs.
  - Documentation describes each variable, its units, and data description (DateTime in UTC, 30-minute time steps, with -9999 for gaps).

- Site access and acknowledgments
  - Long-term support and collaborations noted; data created under NERC/Defra-supported projects; farm owners and managers acknowledged for site access.

- Practical considerations for analysts
  - Be aware of periods with radiometer downtime and site maintenance that affect data completeness.
  - Use gap-filled products (GEP, TER, NEE_filled) with their uncertainties for ecosystem-scale analyses.
  - Consider footprint and quality-control flags when aggregating or comparing to other sites.