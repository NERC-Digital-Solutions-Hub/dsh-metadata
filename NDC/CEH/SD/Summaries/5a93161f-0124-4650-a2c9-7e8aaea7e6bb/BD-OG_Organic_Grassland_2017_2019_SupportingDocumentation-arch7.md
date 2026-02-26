# Supporting information for: Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019

- Data access, licensing and citation
  - Data must be cited as Morrison, R.; Cooper, H.; Cumming, A.; Scarlett, P.; Thornton, J.; Winterbourn, J.B. (2019). Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019. NERC Environmental Information Data Centre. https://doi.org/10.5285/5a93161f-0124-4650-a2c9-7e8aaea7e6bb
  - Full terms of use available at the provided DOI link.

- Overview of dataset
  - BD-OG_Organic_Grassland_2017_2019.csv contains time series of land surface–atmosphere exchanges: NEE, sensible heat (H), latent heat (LE), and momentum (τ), plus atmospheric turbulence descriptors.
  - Fluxes were measured with eddy covariance (EC) at 30-minute intervals over 2017-01-01 to 2019-11-16.
  - Includes ancillary weather and soil physics observations and turbulence-related variables.
  - Site code: BD-OG, located at Sheepdrove Organic Farm, Berkshire Downs, UK.

- Study site
  - Coordinates: 51°31'48.78" N, 1°28'54.99" W; elevation ~184 m amsl.
  - Organically managed, extensively grazed grassland.
  - Climate: temperate maritime; mean annual temp ~9.6 °C and precipitation ~740 mm (1981–2010 baseline).
  - Soils: shallow chalky, silty loams with flints over chalk.

- Sampling regime
  - Automated flux, meteorological and soil observations from 2017-01-01 00:30 to 2019-11-16 00:00.
  - Flux data collected at a canopy height of 2.0 m.

- Flux data acquisition
  - EC system: Windmaster ultrasonic anemometer thermometer and LI-7500 CO2 analyser.
  - Raw 20 Hz data: three velocity components, sonic temperature, and gas densities (H2O, CO2).
  - Data logging: CR3000 Micrologger.

- Ancillary data acquisition
  - Co-located COSMOS-UK station for Ta, barometric pressure, RH.
  - Net radiation (Rnet) and components; soil heat flux (G) at two locations; soil moisture (VWC) and soil temperature; precipitation (Pluvio 2).
  - Observations logged as 30-minute means (and sums for precipitation).

- Data processing
  - Turbulent fluxes computed with EddyPRO v6.1; 30-minute block averages.
  - Processing steps include QC of 20 Hz data, tilt/coordinate rotation, corrections for cospectral attenuation, humidity and density effects, and uncertainty estimates.
  - Derived metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).

- Quality control (QC)
  - Outliers removed via median absolute deviation; non-stationary turbulence flagged and fluxes removed.
  - Flux ranges: H (-200 to 500 W m-2), LE (-60 to 600 W m-2), NEE (-70 to 35 μmol CO2 m-2 s-1).
  - NEE excluded at night when negative, and when u* < 0.18 m s-1.
  - Flux representativeness checked with footprint model; retain fluxes where ≥80% originates from target grassland.
  - Weekly visual checks; obviously erroneous values removed.

- Data gap-filling and flux partitioning
  - Gaps in EC data filled with Marginal Distribution Sampling (Reichstein et al. 2005).
  - NEE partitioned into GEP and TER using Ta-driven partitioning (Reichstein et al. 2005).
  - Gap-filling and partitioning performed with REddyProc (R).

- Details of data structure
  - Time series provided as a single BD-OG_Organic_Grassland_2017_2019.csv with tabular columns described in Table 1.
  - Gap-filled and partitioned data included; time range from 2017-01-01 00:30 to 2019-11-16 00:00.
  - Missing records indicated by -9999.

- Nature and units of recorded values
  - Variables include: NEE, NEE_filled, NEE_filled_sd; LE, LE_filled, LE_filled_sd; H, H_filled, H_filled_sd; Tau, Tau_filled, Tau_filled_sd.
  - Environmental and soil variables: Pa (kPa), Ta (°C), RH (%), VPD (hPa), SWin, SWout, LWin, LWout, Rnet; G1, G2 (soil heat flux); Tsoil1, Tsoil2 (°C); VWC1, VWC2 (%); Precipitation (mm per 0.5 h); Windspeed (m s-1); Winddir (degrees); FootprintFraction (%); Ustar (m s-1); TKE (m^2 s^-2); L (Obukhov length); zL (dimensionless stability).
  - NEE_filled, LE_filled, H_filled; and partitioned GEP, TER values are included for complete time series.

- Acknowledgments and references
  - Funded by Natural Environment Research Council (NE/R016429/1) under UK-SCAPE National Capability.
  - COSMOS-UK data contributions acknowledged.
  - Field and technical support from site hosts and collaborators.
  - Key methodological references listed (EddyPRO, QC and processing standards, footprint modeling, gap-filling and partitioning methodologies).