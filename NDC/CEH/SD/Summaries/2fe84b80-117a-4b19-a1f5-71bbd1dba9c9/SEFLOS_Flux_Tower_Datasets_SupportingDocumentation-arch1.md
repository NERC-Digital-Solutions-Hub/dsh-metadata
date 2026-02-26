# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a cropland and a grassland on lowland peatland soils, East Anglia Fens, UK, 2016 to 2019

## Overview
- Time series of land surface–atmosphere fluxes: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Observations at two managed lowland peatland environments in East Anglian Fens, England: cropland site EF-SA (salad crops) and grassland site EF-GF.
- Data collected 2016-11-17 to 2018-09-24 (EF-SA) and 2017-04-27 to 2019-03-31 (EF-GF) using micrometeorological eddy covariance (EC) methods, plus ancillary weather and soil observations and turbulence variables.

## Study sites
- Location: East Anglian Fens (Fenland), UK — large contiguous area of lowland peatland soils; historically drained and heavily peat-based agricultural land.
- Climate: temperate maritime; mean annual temperature ~10.4 °C and precipitation ~564 mm (1981–2010 baseline).
- Cropland (EF-SA): highly degraded fen peats over clay; drainage via sub-surface pipes; crops include high-value lettuce, celery, cereals.
- Grassland (EF-GF): managed grassland within the Great Fen Project; former arable peatland being rewetted/restored; low-intensity grazing and occasional mowing; peat depth ~2 m.

## Sampling regime
- Flux observations above canopy at 2.6 m height; open-path EC systems.
- 20 Hz raw data collected; 30-minute flux averages produced.
- Ancillary meteorological and soil sensors colocated with EC stations; period-specific data collection windows per site.

## Flux data acquisition
- Variables measured: NEE (μmol CO2 m^-2 s^-1), LE (W m^-2), H (W m^-2), τ (kg m^-1 s^-2).
- Instruments: LI-7500 CO2 sensor, ultrasonic anemometer/thermometer, and site-specific wind sensors; turbulence-related metrics (u*, TKE, L, z/L) computed.

## Ancillary data
- Meteorology: air temperature (Ta), relative humidity (RH), net radiation (Rnet), incoming/outgoing shortwave and longwave radiation, precipitation, among others.
- Soil physics: soil temperature at multiple depths (Tsoil), volumetric water content (VWC) at multiple depths, soil heat flux (G) at two locations, water level sensors.
- Regional data: wind speed and direction from EC system; footprint estimates.

## Data processing
- Flux calculations with EddyPRO software (v6.1); 30-minute averaging; QC and corrections for airodynamic/sonic tilt, coordinate rotation, high/low-frequency co-spectral attenuation, density corrections, and storage effects.
- Random uncertainties estimated; additional processing to derive footprints, u*, L, and stability metrics.

## Quality control
- Outlier removal via median absolute deviation; non-stationary turbulence periods excluded.
- Flux ranges enforced: H, LE, NEE within defined bounds; NEE filtered to exclude night fluxes or low friction velocities per site thresholds.
- Manual review of weekly plots to remove clearly erroneous values.
- Footprint criteria applied: fluxes retained if ≥75% of flux originates from target ecosystem.

## Gap-filling and flux partitioning
- Data gaps in NEE, LE, H filled using Marginal Distribution Sampling (MDS).
- NEE partitioned into gross ecosystem production (GEP) and total ecosystem respiration (TER) using Reichstein et al. (2005) approach, with Ta driving the partitioning.
- Gap-filling and partitioning implemented with REddyProc (R).

## Details of data structure
- Time series provided in two separate CSV files per site; gap-filled and partitioned data included for the full period of record.
- Missing records denoted by -9999.

## Nature and units of recorded values
- Variables described with clear units for 30-minute time series (e.g., NEE in μmol CO2 m^-2 s^-1; LE/H in W m^-2; τ in kg m^-1 s^-2; pressure Ta, RH, VPD; radiation components; G, Tsoil, VWC; Precipitation; WaterLevel; Windspeed and Winddir; u*, TKE, L, zL; NEE_filled, LE_filled, H_filled, TER, GEP, etc.).
- Includes both raw (before gap-filling) and gap-filled values along with associated uncertainties.

## Acknowledgments and references
- Funding and support from NERC (UK-SCAPE and SEFLOS projects) and landowner permissions; dataset contributors acknowledged.
- References provided for data processing methods and related datasets and software (EddyPRO, REddyProc, and key methodological papers).