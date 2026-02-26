# Supporting information for: Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019

## Data access, licensing and citation
- Data must be cited as Morrison, R.; Cooper, H.; Cumming, A.; Scarlett, P.; Thornton, J.; Winterbourn, J.B. (2019). Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019. NERC Environmental Information Data Centre. https://doi.org/10.5285/5a93161f-0124-4650-a2c9-7e8aaea7e6bb
- Full terms of use and access are available at the provided DOI link.

## Overview of dataset
- Contains a time series (BD-OG_Organic_Grassland_2017_2019.csv) of land surface–atmosphere exchanges: NEE (net ecosystem CO2 exchange), H (sensible heat), LE (latent heat), and τ (momentum).
- Measurement period: 2017-01-01 00:30 to 2019-11-16 00:00.
- Includes ancillary weather and soil physics observations and variables describing atmospheric turbulence.
- Data are provided as a single CSV with gap-filled and partitioned flux data; missing values indicated by -9999.

## Study site
- BD-OG flux station at Sheepdrove Organic Farm, Berkshire Downs (coordinates 51°31'48.78" N, 1°28'54.99" W; 184 m amsl).
- Organically managed, extensively grazed grassland.
- Climate: temperate maritime; mean annual temperature ~9.6°C and precipitation ~740 mm (1981–2010).
- Soils: shallow chalky, silty loams with flints over chalk; bulk density 1.03 g cm⁻³; soil organic carbon 0.06 g g⁻¹; sand/silt/clay ~37/44/19%.

## Sampling regime
- Automated flux, meteorological, and soil physics measurements conducted continuously from 2017-01-01 00:30 to 2019-11-16 00:00.

## Flux data acquisition
- Eddy covariance fluxes measured above canopy at 2.0 m height using open-path EC system.
- Instruments: Windmaster ultrasonic anemometer thermometer; LI-7500 IRGA.
- Raw data at 20 Hz (three velocity components, sonic temperature, density of water vapor and CO2); logged with CR3000.
- Derived fluxes and turbulence metrics computed from raw data.

## Ancillary data acquisition
- Co-located COSMOS-UK station for meteorology and soil physics: Ta, barometric pressure, RH, SWin/SWin, LWin/LWout, G, VWC, soil temperature (0.05 m), soil moisture, precipitation, wind speed and direction.
- Data aggregated to 30-minute means (and 0.5-hour precipitation sums).

## Data processing
- Flux calculations with EddyPRO v6.1 using 30-minute blocks.
- Corrections included: QC of 20 Hz data, angle-of-attack correction, 2D coordinate rotation, cospectral attenuation corrections, humidity correction for H, density correction for LE and CO2.
- Random uncertainties estimated (Finkelstein & Sims 2001).
- Additional variables computed: wind speed/direction, u*, Turbulent Kinetic Energy, Obukhov length, z/L.
- Footprint analyses performed to ensure representativeness.

## Quality control
- Outliers removed via median absolute deviation; non-stationary turbulence periods removed.
- Flux ranges: H (-200 to 500 W m⁻²), LE (-60 to 600 W m⁻²), NEE (-70 to 35 μmol CO2 m⁻² s⁻¹).
- NEE filtered to exclude night-time negative fluxes and low u* (<0.18 m s⁻¹).
- Flux representativeness assessed with footprint model; retain fluxes with >80% from target grassland.
- Weekly visual QA and manual cleaning for obvious errors.

## Data gap-filling and flux partitioning
- Gaps in EC data filled with Marginal Distribution Sampling (Reichstein et al., 2005).
- NEE partitioned into GEP and TER using temperature-driven partitioning (Reichstein et al., 2005).
- Gap-filling and partitioning performed with REddyProc (R) package (Reichstein et al., 2016).

## Details of data structure
- Time series stored in a single CSV with columns described in Table 1; gap-filled and partitioned data provided for the full period.
- Missing records denoted by -9999.

## Nature and units of recorded values
- Time: DateTime in yyyy-mm-dd HH:MM (UTC).
- NEE: μmol CO2 m⁻² s⁻¹; NEE_unc: μmol CO2 m⁻² s⁻¹.
- LE: W m⁻²; LE_unc: W m⁻².
- H: W m⁻²; H_unc: W m⁻².
- Tau: kg m⁻¹ s⁻²; Tau_unc: kg m⁻¹ s⁻².
- CO2_strg, LE_strg, H_strg (storage terms): μmol CO2 m⁻² s⁻¹, W m⁻², W m⁻² respectively.
- Pa: KPa; Ta: °C; RH: %; VPD: hPa.
- SWin, SWout, LWin, LWout, Rnet: W m⁻².
- G1, G2: W m⁻² (soil heat flux).
- Tsoil1, Tsoil2: °C.
- VWC1, VWC2: %.
- Precipitation: mm per 0.5 hour.
- Windspeed: m s⁻¹; Winddir: degrees.
- FootprintFraction: %.
- Ustar: m s⁻¹; TKE: m² s⁻²; Tstar: °K; L: m; zL: dimensionless.
- NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP: filled fluxes and uncertainties.

## Acknowledgments
- Funded by Natural Environment Research Council (NE/R016429/1) under the UK-SCAPE programme.
- COSMOS-UK provided additional meteorological and soil data.
- Landowners provided access; field and technical support acknowledged.

## References
- Key methodological and processing references for eddy covariance techniques, QC, gap-filling, and partitioning are cited to underpin data processing and interpretation.