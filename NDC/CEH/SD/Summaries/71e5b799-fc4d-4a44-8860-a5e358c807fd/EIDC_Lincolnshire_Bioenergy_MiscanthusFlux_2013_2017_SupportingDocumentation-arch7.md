# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2013 to 2017 Ross Morrison, Hollie M. Cooper, Rebecca L. Rowe & Niall P. McNamara

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured via eddy covariance (EC) from 2013-07-05 00:30 to 2017-11-07 00:00.
- Includes ancillary weather and soil physics observations and variables describing atmospheric turbulence.
- Primary data file: Lincolnshire_Bioenergy_Miscanthus_2013_2017.csv; gap-filled and partitioned data provided; missing values denoted as -9999.
- Data are provided as 30-minute averaged records; observations logged at various instrument sampling rates and processed with quality control.

## Study site
- Location: Miscanthus flux site at 53°19'10.07"N, 0°35'18.65"W; 11.5 ha commercial bioenergy plantation about 10 km north of Lincoln, UK.
- Climate: temperate maritime; mean annual temperature ~9.8°C; mean annual precipitation ~614 mm.
- Soils: Beccles 1 association; seasonally waterlogged fine loams; pH 6.8–7.3; soil organic carbon ~68 t C ha^-1; total nitrogen ~11 t N ha^-1.
- Land-use history: established 2006 on former arable land; annual harvests since 2008; improvements and soil amendments applied in 2013–2016.

## Sampling regime
- Automated flux, meteorological, and soil physics measurements conducted from 2013-07-05 to 2017-11-07.

## Flux data acquisition
- Measurement setup: open-path EC on a mast at plantation center; height ≈ twice the mean Miscanthus canopy height.
- Instruments: R3 sonic anemometer-thermometer and LI-7500 CO2/H2O sensor; data logged with a CR3000.
- Raw data: 20 Hz sampling of three wind components, sonic temperature, CO2 and H2O concentrations; Ta and RH at 2 m height.
- Data aggregation: 30-minute flux averages; Ta and RH logged as 30-minute means.

## Ancillary data acquisition
- Above-canopy net radiation components (Rnet, SWin, SWout, LWin, LWout) measured with CNR1 net radiometer; BF3 sunshine sensor for total and diffuse shortwave radiation.
- Below-canopy PPFD (PPFDbc) measured at three locations; soil heat flux (G) at two locations; soil water content (VWC) at two locations; soil temperature (Tsoil) at 0.05 m; precipitation measured by tipping bucket.
- All ancillary data are provided as 30-minute means (and sums for precipitation).

## Data processing
- Flux calculations: EddyPRO v6.1 used to derive fluxes from raw EC data; includes quality control, angle-of-attack correction, 2D rotation, cospectral corrections, humidity and density corrections.
- Derived metrics: wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter z/L.
- Data quality checks included footprint assessment (target ecosystem representativeness >75%), and visual inspection with weekly plots.

## Quality control
- Outlier removal using median absolute deviation; non-stationary conditions flagged and excluded.
- Flux ranges: H [-200, 400] W m^-2; LE [-100, 500] W m^-2; NEE [-70, 35] μmol CO2 m^-2 s^-1.
- NEE treated specially: night-time negative fluxes excluded; a friction velocity threshold (u*) of 0.14 m s^-1 applied.
- Spatial representativeness checked via footprint modelling; data filtered to fluxes representative of target ecosystem (>75% within ecosystem).
- Manual review: weekly plots used to remove obviously erroneous data.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (MDS) for EC flux gaps; meteorological gaps filled with linear relationships from adjacent weather stations.
- Flux partitioning: NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Ta-driven methods.
- Tools: REddyProc (R) used for gap-filling and partitioning.

## Details of data structure
- Time series stored in a single CSV with columns as described in the dataset documentation.
- Gap-filled and partitioned data included; missing records remain as -9999.

## Nature and units of recorded values
- Core time series: DateTime (UTC), NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, and derived terms (CO2_strg, LE_strg, H_strg, etc.).
- Auxiliary variables cover CO2 and H2O densities, pressures (Pa), air temperature (Ta), relative humidity (RH), specific humidity (SH), vapor pressure deficit (VPD), dew point (Tdew), radiative components (SWin, SWout, LWin, LWout, Rnet, SWin_total, SWin_diffuse), PPFD under canopy (PPFDbc), soil fluxes (G), soil temperature (Tsoil), soil water content (VWC), precipitation, wind metrics (Windspeed, Winddir), footprint fraction, u*, TKE, L, zL.
- Units: largely in μmol CO2 m^-2 s^-1 for NEE/GEP/TER, W m^-2 for heat fluxes, and standard SI units for meteorological variables.

## Acknowledgments
- Data collection funded by the National Environment Research Council; thanks to landowners and CEH staff for support and maintenance of instruments.

## References
- Includes methodological and site-related references for EC processing, QC, footprint analysis, gap-filling, and previous site studies.