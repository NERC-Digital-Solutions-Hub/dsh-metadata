# Supporting information for: Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019

## Data access, licensing and citation
- Data must be cited as Morrison, R.; Cooper, H.; Cumming, A.; Scarlett, P.; Thornton, J.; Winterbourn, J.B. (2019). Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019. NERC Environmental Information Data Centre. https://doi.org/10.5285/5a93161f-0124-4650-a2c9-7e8aaea7e6bb
- Full terms of use and access are available at https://doi.org/10.5285/5a93161f-0124-4650a2c9-7e8aaea7e6bb

## Overview of dataset
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured at BD-OG Organic Grassland, Berkshire Downs, UK (site code BD-OG).
- Turbulent flux densities collected with eddy covariance (EC) between 2017-01-01 00:30 and 2019-11-16 00:00.
- Includes ancillary weather and soil physics observations and variables describing atmospheric turbulence.
- Data prepared to support analysis of ecosystem carbon, energy, and water fluxes with gap-filled and partitioned flux estimates.

## Study site
- BD-OG flux observation site at Sheepdrove Organic Farm, ~4.0 km NE of Lambourn.
- Coordinates: 51°31'48.78" N, 1°28'54.99" W; 184 m above mean sea level.
- Organically managed, extensively grazed grassland; temperate maritime climate.
- Soils: shallow chalky, silty loams with flints over white chalk; bulk density ~1.03 g cm^-3; soil organic carbon ~0.06 g g^-1; sand:silt:clay ~37:44:19.
- Climate specifics referenced from Evans et al. (2016).

## Sampling regime
- Automated flux, meteorological, and soil-physics measurements from 2017-01-01 00:30 to 2019-11-16 00:00.

## Flux data acquisition
- Eddy covariance fluxes measured above canopy at 2.0 m height using open-path EC system.
- Fluxes: NEE (μmol CO2 m^-2 s^-1), LE (W m^-2), H (W m^-2), τ (kg m^-1 s^-2).
- Sensors: Windmaster ultrasonic anemometer (Gill Instruments) and LI-7500 IR gas analyser (LI-COR).
- Raw data (three wind components, sonic temperature, water vapor and CO2 densities) sampled at 20 Hz and logged with a CR3000 Micrologger.

## Ancillary data acquisition
- Co-located COSMOS-UK station for air temperature (Ta), barometric pressure, and relative humidity (RH) at 2 m.
- Net radiation (Rnet) and components (SWin, SWout, LWin, LWout); soil heat flux (G1, G2) at 0.03 m; soil volumetric water content (VWC) and soil temperature (Tsoil1, Tsoil2) at 0.05 m; precipitation (Pluvio 2).
- Data logged as 30-minute means and sums for precipitation.

## Data processing
- Flux densities computed from raw EC data with EddyPRO v6.1 using 30-minute block averages.
- Processing steps include: QC of 20 Hz data, angle of attack correction for Gill anemometers, 2D rotation to align with terrain, corrections for high/low-frequency cospectral attenuation, humidity and density corrections for LE and CO2, and flux storage terms.
- Random uncertainties estimated per Finkelstein & Sims (2001).
- Derived metrics: wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).

## Quality control
- Outliers removed via median absolute deviation (Papale et al., 2006).
- Exclusion during non-stationary turbulence (Foken et al., 2004).
- Flux ranges applied: H (-200 to 500 W m^-2), LE (-60 to 600 W m^-2), NEE (-70 to 35 μmol CO2 m^-2 s^-1).
- NEE removed at night when fluxes negative; friction velocity threshold (u* > 0.18 m s^-1) per Reichstein et al. (2016).
- Flux representativeness assessed with a footprint model (Kormann & Meixner, 2001) via ART Footprint Tool; retain fluxes with >80% originating within target grassland.
- Weekly visual checks of all flux and ancillary data; manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning
- Gaps in EC data (NEE, LE, H) filled using Marginal Distribution Sampling (Reichstein et al., 2005).
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Ta-driven algorithm (Reichstein et al., 2005).
- Gap-filling and partitioning performed with REddyProc (Reichstein et al., 2016) in R.

## Details of data structure
- Time series data provided in a single CSV file with columns as described in Table 1; gap-filled and partitioned series included.
- Time range: 2017-01-01 00:30 to 2019-11-16 00:00.
- Missing records denoted by -9999.

## Nature and units of recorded values
- Variables include DateTime (UTC), NEE and NEE_unc, LE and LE_unc, H and H_unc, Tau and Tau_unc; storage terms (CO2_strg, LE_strg, H_strg); atmospheric pressure (Pa), Ta, RH, VPD, irradiance components, radiation balance (Rnet), soil fluxes (G1, G2), soil temperatures (Tsoil1, Tsoil2), VWC (VWC1, VWC2), Precipitation, Windspeed, Winddir, FootprintFraction, Ustar, TKE, L, zL; NEE_filled and NEE_filled_sd; LE_filled and LE_filled_sd; H_filled and H_filled_sd; TER and GEP.
- Units detailed in table descriptions, with timestamps in yyyy-mm-dd HH:MM format.

## Acknowledgments
- Funded by Natural Environment Research Council (award NE/R016429/1) as part of UK-SCAPE; COSMOS-UK support acknowledged; landowners' permission and field staff acknowledged.

## References
- Key methodological references for QC, processing, footprint analysis, gap-filling, and partitioning (e.g., Evans et al. 2016; Finkelstein & Sims 2001; Reichstein et al. 2005, 2016; Moncrieff et al. 1997, 2004; Papale et al. 2006; Kormann & Meixner 2001; etc.).