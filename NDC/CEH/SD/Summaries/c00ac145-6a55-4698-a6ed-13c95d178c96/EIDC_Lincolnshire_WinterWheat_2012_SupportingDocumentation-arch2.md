# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a winter wheat field, Lincolnshire, UK, 2012

## Overview of dataset
- Time series observations of surface-atmosphere exchanges (fluxes) of net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) over a winter wheat crop in Lincolnshire, UK during the 2012 growing season.
- Fluxes measured with eddy covariance (EC) at 3.0 m height from 2012-04-05 00:30 to 2012-08-08 00:00 (GMT/UTC).
- Includes ancillary weather and soil physics observations and variables describing atmospheric turbulence.
- Data are provided as a complete time series with gap-filled and partitioned outputs; missing records denoted by -9999.

## Study site
- Location: flux tower on arable cropland north of Lincoln, UK (53°19'17.89"N, 0°35'7.83"W).
- Climate: temperate maritime (mean annual temperature ~9.8°C, precipitation ~614 mm/year, 1981–2010 basis).
- Soils: Beccles 1 association, seasonally waterlogged fine loams over Charnmouth Mudstone; bulk densities ~1.46–1.53 g cm^-3; soil texture 49% sand, 36% silt, 15% clay; soil pH ~6.32.
- Context: site details linked to prior work (Drewer et al., 2012; Robertson et al., 2017).

## Sampling regime
- Automated flux, meteorological, and soil observations collected 2012-04-05 to 2012-08-08 (UTC).
- EC flux tower setup: 3.0 m height at field center.

## Flux data acquisition
- EC system: open-path EC with R3 sonic anemometer thermometer and LI-7500 CO2/H2O analyzer.
- Raw data: three velocity components, sonic temperature, water vapor density, and CO2 density at 20 Hz, logged by a CR3000 Micrologger.
- Fluxes computed as 30-minute averages: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), and τ (kg m^-1 s^-2).

## Ancillary data acquisition
- Net radiation (Rnet) and components of shortwave/longwave radiation measured at 1.5 m above canopy.
- Soil heat flux (G) at 0.05 m depth at two locations.
- Air and soil temperatures (Ta at 2 m; Ts at 0.05 and 0.1 m); relative humidity (RH); soil moisture (VWC) at 0.05 and 0.1 m; precipitation; wind speed/direction.
- Data logged as 30-minute means; additional meteorological data provided from adjacent weather stations.

## Data processing
- Flux calculation with EddyPRO software (v6.1) and 30-minute averaging.
- QC steps embedded in EddyPRO: 20 Hz data quality control, tilt/angle corrections, 2D rotation to local terrain, corrections for spectral attenuation, density corrections for LE and CO2, and humidity effects on H.
- Derived metrics: wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).
- Random uncertainties for fluxes estimated following established methods.

## Quality control
- Outlier removal using median absolute deviation; non-stationary conditions exclude fluxes.
- Plausible range checks: H (-200 to 400 W m^-2), LE (-100 to 500 W m^-2), NEE (-70 to 35 μmol CO2 m^-2 s^-1).
- NEE rejection at night when night CO2 fluxes negative with low net radiation; friction velocity threshold (u* > 0.07 m s^-1) applied.
- Footprint analysis (ART Footprint Tool) to ensure >75% of flux originates from target ecosystem.
- Weekly visual checks of flux and ancillary data to remove clearly erroneous values.
  
## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling approach for EC flux gaps (NEE, LE, H).
- Meteorological gaps filled using linear relationships from adjacent weather stations.
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) via flux partitioning using Ta-driven algorithms (Reichstein et al. 2005).
- Gap-filling and partitioning performed with REddyProc (R) package (Reichstein et al. 2016).

## Details of data structure
- Data delivered as a single CSV file with tabular columns described in the dataset documentation.
- Gap-filled and partitioned outputs accompany the primary measurements.
- Time resolution: 30-minute intervals; time axis in GMT/UTC.
- Missing records indicated by -9999.

## Nature and units of recorded values
- DateTime: yyyy-mm-dd HH:MM (GMT/UTC).
- NEE: μmol CO2 m^-2 s^-1; NEE_unc: μmol CO2 m^-2 s^-1.
- LE: W m^-2; LE_unc: W m^-2.
- H: W m^-2; H_unc: W m^-2.
- Tau: kg m^-1 s^-2; Tau_unc: kg m^-1 s^-2.
- CO2_strg, LE_strg, H_strg: storage terms for CO2, LE, H.
- Ta, RH, VPD, Pa, etc., with standard meteorological units.
- Radiative, soil, and turbulence descriptors (SWin, SWout, LWin, LWout, G, Tsoil, VWC, Precipitation, Windspeed, Winddir, Ustar, TKE, L, zL, footprint metrics, etc.).
- NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP: gap-filled and partitioned outputs with associated uncertainties.

## Acknowledgments and references
- Dataset supported by UK Natural Environment Research Council (NERC) funding and related projects (e.g., UK-SCAPE, Carbo-Biocrop).
- Data produced with collaboration from landowners and site contributors; methodological references cited for QC, processing, and partitioning approaches.