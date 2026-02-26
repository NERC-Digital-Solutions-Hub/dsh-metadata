# Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019

- Data access and citation
  - Data must be cited as Morrison et al. (2019) in the NERC Environmental Information Data Centre.
  - DOIs: https://doi.org/10.5285/5a93161f-0124-4650-a2c9-7e8aaea7e6bb and full terms at https://doi.org/10.5285/5a93161f-0124-4650a2c9-7e8aaea7e6bb

- Overview of dataset
  - Time series of NEE, H, LE, and τ measured above an organically managed grassland (BD-OG) on Berkshire Downs, 2017-01-01 00:30 to 2019-11-16 00:00.
  - Variables include ancillary weather/soil observations and turbulence descriptors.
  - Data file: BD-OG_Organic_Grassland_2017_2019.csv; gap-filled and partitioned data provided; missing data labeled as -9999.

- Study site
  - Location: BD-OG flux site, Sheepdrove Organic Farm, ~4.0 km NE of Lambourn, 51°31'48.78" N, 1°28'54.99" W, 184 m a.s.l.
  - Environment: organically managed, extensively grazed grassland; temperate maritime climate.
  - Soils: shallow chalky, silty loams with flints over white chalk; bulk density 1.03 g cm-3; SOC 0.06 g g-1; sand/silt/clay fractions 37/44/19%.

- Sampling regime
  - Automated flux, meteorological and soil measurements from 2017-01-01 00:30 to 2019-11-16 00:00.
  - Flux observations at 2.0 m height using open-path EC system.

- Flux data acquisition
  - Fluxes: NEE (μmol CO2 m-2 s-1), H (W m-2), LE (W m-2), τ (kg m-1 s-2) and related variables.
  - Instruments: Windmaster ultrasonic anemometer, LI-7500 IRGA; raw 20 Hz data logged by CR3000.
  - Raw data: three velocity components, sonic temperature, water vapor and CO2 densities.

- Ancillary data acquisition
  - Co-located COSMOS-UK station for Ta, Pa, RH, SWin, SWout, LWin, LWout, Rnet, G, VWC, Tsoil, etc.
  - Precipitation from Pluvio 2.
  - Data summarized as 30-minute means (and 30-minute sums for precipitation).

- Data processing
  - Processing software: EddyPRO v6.1; 30-minute flux averages.
  - Corrections and QC: coordinate rotation, tilt adjustments, high/low-frequency attenuation, density corrections, humidity effects, and storage term corrections.
  - Uncertainty: random flux uncertainties computed; additional turbulence metrics (u*, TKE, L, z/L) calculated.
  - Representativeness: footprint analysis with ART Footprint Tool; fluxes retained if >80% originated from target grassland.

- Quality control
  - Outlier removal using median absolute deviation; non-stationary turbulence periods removed; flux bounds applied for H, LE, NEE.
  - NEE QC: night-time negative flux checks and a u* threshold (0.18 m s-1).
  - Weekly visual QA; fluxes/ancillaries plotted and clearly erroneous values removed.

- Data gap-filling and flux partitioning
  - Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005) for NEE, LE, H.
  - NEE partitioning: into GEP and TER using Reichstein et al. (2005) approach driven by Ta.
  - Tools: REddyProc (R) for gap-filling and partitioning (Reichstein et al., 2016).

- Details of data structure
  - Time series provided as a single CSV with columns described in Table 1 (see dataset).
  - Gap-filled/partitioned data included; missing data denoted by -9999.

- Nature and units of recorded values
  - DateTime: yyyy-mm-dd HH:MM (GMT/UTC).
  - Primary fluxes: NEE, LE, H, Tau (with respective uncertainties).
  - Storage terms: CO2_strg, LE_strg, H_strg.
  - Meteorology/soil: Pa (kPa), Ta (°C), RH (%), VPD (hPa), SWin, SWout, LWin, LWout, Rnet, G1, G2, Tsoil1, Tsoil2, VWC1, VWC2, Precipitation (mm/0.5 h), Windspeed, Winddir.
  - FootprintFraction and Ustar, TKE, L, zL, Tstar; NEE_filled and corresponding uncertainties; GEP and TER after partitioning.

- Acknowledgments
  - Funded by Natural Environment Research Council (NE/R016429/1) under UK-SCAPE; COSMOS-UK data contributions.
  - Thanks to landowners and field/technical support from Evans and colleagues.

- References
  - Key methodological and processing references for EC data handling, QC, gap-filling, and footprint analysis (e.g., Reichstein et al., Mauder et al., Moncrieff et al., Papale et al., NEEP/REddyProc, etc.).