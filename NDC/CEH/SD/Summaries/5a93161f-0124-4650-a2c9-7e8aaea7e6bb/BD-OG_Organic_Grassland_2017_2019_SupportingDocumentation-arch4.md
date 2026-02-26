# Supporting information for: Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019

- Data access, licensing and citation
  - Users must cite Morrison et al. (2019) as listed: Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019. NERC Environmental Information Data Centre. DOI provided.
  - Full terms on use and access available at the provided DOI link.

- Overview of the dataset
  - Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
  - Site: BD-OG organically managed grassland, Berkshire Downs, UK; data collected 2017-01-01 to 2019-11-16.
  - Ancillary observations: weather and soil physics data, plus turbulence-characterising variables.
  - Fluxes measured with micrometeorological eddy covariance (EC) technique at 2.0 m height; data quality controlled and gap-filled.

- Study site
  - Location: 51°31'48.78" N, 1°28'54.99" W, 184 m above sea level; Sheepdrove Organic Farm, ~4.0 km NE of Lambourn.
  - Climate: temperate maritime; mean annual air temperature ~9.6 °C; mean annual precipitation ~740 mm.
  - Soils: shallow chalky, silty loams with flints over chalk; bulk density and soil organic carbon ~1.03 g cm^-3 and 0.06 g g^-1.
  - Flux observations focus on a target grassland ecosystem with observed footprint fraction assessed.

- Sampling regime
  - Automated flux, meteorological and soil measurements conducted 2017-01-01 00:30 to 2019-11-16 00:00.
  - Time resolution: 30-minute means for fluxes and ancillary data; high-frequency (20 Hz) raw data for EC measurements.

- Flux data acquisition
  - EC system: open-path, measurement height 2.0 m; NEE (μmol CO2 m^-2 s^-1), LE (W m^-2), H (W m^-2), τ (kg m^-1 s^-2).
  - Instruments: Windmaster ultrasonic anemometer thermometer; LI-7500 IR gas analyser; raw 20 Hz data logged with CR3000.
  - Turbulence data: three velocity components, sonic temperature, water vapour and CO2 densities.

- Ancillary data acquisition
  - Co-located COSMOS-UK station for meteorological and soil measurements: Ta, pressure, RH, Rnet and components, soil heat flux (G1, G2), soil temperature (Tsoil), soil water content (VWC), precipitation.
  - Data logged as 30-minute means (or sums for precipitation).

- Data processing
  - Flux calculations: using EddyPRO software (v6.1); 30-minute block averaging; QC of 20 Hz data; corrections for angle of attack, coordinate rotation, spectral attenuation, density effects, and stability corrections.
  - Uncertainty: random uncertainties per flux calculated per standard approaches; additional turbulence and footprint metrics computed.

- Quality control
  - Outlier removal via median absolute deviation; non-stationary turbulence periods removed; flux value clipping with specified ranges for H, LE, NEE.
  - NEE screened to remove night-time negative fluxes and low friction velocity (<0.18 m s^-1).
  - Footprint checks using ART Footprint Tool; fluxes retained if >80% originated within target grassland.
  - Regular visual checks (weekly plots) with manual removal of clearly erroneous data.

- Gap-filling and flux partitioning
  - Gaps in EC data (NEE, LE, H) filled with Marginal Distribution Sampling (Reichstein et al., 2005).
  - NEE partitioned into GEP and TER using temperature-driven algorithm (Reichstein et al., 2005).
  - Gap-filling and partitioning performed with REddyProc (R) package.

- Details of data structure and variables
  - Data provided as a single CSV: BD-OG_Organic_Grassland_2017_2019.csv; includes both raw and gap-filled/partitioned values.
  - Key columns (examples): DateTime (UTC), NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G1, G2, Tsoil1, Tsoil2, VWC1, VWC2, Precipitation, Windspeed, Winddir, FootprintFraction, Ustar, TKE, Tstar, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
  - Missing data denoted as -9999.
  - Various storage terms (CO2_strg, LE_strg, H_strg) and energy/flux components with corresponding uncertainties.

- Nature and units of recorded values
  - DateTime: yyyy-mm-dd HH:MM (UTC)
  - NEE: μmol CO2 m^-2 s^-1
  - NEE_unc: μmol CO2 m^-2 s^-1
  - LE: W m^-2
  - LE_unc: W m^-2
  - H: W m^-2
  - H_unc: W m^-2
  - Tau: kg m^-1 s^-2
  - Tau_unc: kg m^-1 s^-2
  - CO2_strg, LE_strg, H_strg: μmol CO2 m^-2 s^-1, W m^-2, W m^-2 (respectively)
  - Pa: kPa
  - Ta: °C
  - RH: %
  - VPD: hPa
  - SWin, SWout, LWin, LWout, Rnet: W m^-2
  - G1, G2: W m^-2
  - Tsoil1, Tsoil2: °C
  - VWC1, VWC2: %
  - Precipitation: mm per 0.5 hour
  - Windspeed: ms^-1
  - Winddir: degrees
  - FootprintFraction: %
  - Ustar: ms^-1
  - TKE: m^2 s^-2
  - Tstar: °K
  - L: dimensionless Obukhov length measure? (described as Obukhov length with units M in table)
  - zL: dimensionless stability parameter
  - NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd: gap-filled fluxes and their uncertainties
  - TER, GEP: μmol CO2 m^-2 s^-1

- Reproducibility, tools and provenance
  - Processing and analysis relied on EddyPRO (v6.1) for flux calculations.
  - Gap-filling and partitioning using REddyProc (R package).
  - Results and methods aligned with standard references and quality-control protocols in the eddy covariance community.

- Data governance, acknowledgments and provenance
  - Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability.
  - COSMOS-UK data support acknowledged; landowners thanked for access.
  - Field and technical support acknowledged.