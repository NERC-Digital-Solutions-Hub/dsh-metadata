# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a cropland and a grassland on lowland peatland soils, East Anglia Fens, UK, 2016 to 2019

## Overview
- Time series observations of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Two managed lowland peatland environments in East Anglian Fens, England, UK: cropland (EF-SA) and grassland (EF-GF).
- Data span: 2016-11-17 to 2018-09-24 at EF-SA; 2017-04-27 to 2019-03-31 at EF-GF.
- Ancillary weather and soil physics measurements accompany the flux data; includes turbulence characterisation.

## Study sites
- East Anglian Fens (The Fenland): largest contiguous area of lowland peatland soils in the UK; historic drainage and agriculture.
- Cropland site EF-SA: high-value horticultural crops (lettuce, celery) and cereals; peat over clay; drainage via sub-surface pipes; peat surface subsided ~2 m.
- Grassland site EF-GF: former arable peatland, planned rewetting/restoration; low-intensity grazing; drainage network present but not connected to regional system; peat depth ~2 m.
- Climate: temperate maritime (mean annual temperature ~10.4°C; ~564 mm/year).

## Sampling regime
- Flux, meteorological, and soil sensors operated automatically during the recording periods specified above.
- Flux observations above canopy at 2.6 m height; 20 Hz data captured and logged.

## Flux data acquisition
- Open-path eddy covariance systems measuring NEE, H, LE, and τ.
- Instruments: ultrasonic anemometer, LI-7500 CO2/H2O analyzer; site-specific wind instruments (Gill WindMaster at EF-SA; Solent R3 at EF-GF).
- Raw data include three velocity components, sonic temperature, water vapor density, and CO2 density.

## Ancillary data acquisition
- Air temperature (Ta) and relative humidity (RH) at 2 m; net radiation (SWin, SWout, LWin, LWout) and net radiation (Rnet); soil heat flux (G) at two locations.
- Water table/pressure monitoring; soil moisture content (VWC) and soil temperature (Tsoil) at various depths; precipitation from co-located gauges.
- Data logged as 30-minute means (and sums for precipitation).

## Data processing
- Turbulent fluxes calculated with EddyPRO v6.1; 30-minute block-averaged fluxes.
- Quality control (QC) includes: 20 Hz data QC, orientation/tilt corrections, spectral corrections, humidity and density corrections; random uncertainties estimated (per standard methods).
- Derived metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L), and flux footprints.

## Quality control
- Outliers removed via median absolute deviation; non-stationary turbulence periods excluded.
- Flux ranges applied: H, LE, NEE within defined bounds; NEE rejected at night or below u* thresholds.
- Footprint criterion: retain fluxes where >75% originate from the target ecosystem.
- Weekly visual QA to identify and remove clear errors.

## Data gap-filling and flux partitioning
- Gap-filling for EC data (NEE, LE, H) using Marginal Distribution Sampling.
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using standard partitioning approaches driven by Ta.
- Gap-filled and partitioned data produced with REddyProc (R).

## Data structure and availability
- Data provided as two separate .csv files containing tabular time-series (ascii format).
- Gap-filled and partitioned flux and ancillary data included for the full period at each site.
- Missing records denoted by -9999.

## Variables and units (summary)
- Fluxes: NEE (μmol CO2 m^-2 s^-1), LE (W m^-2), H (W m^-2), τ (kg m^-1 s^-2); NEE and related stores/further terms included as NEE_filled, LE_filled, H_filled, etc.
- Ancillaries: Ta (°C), RH (%), VPD (hPa), SWin/SWout/LWin/LWout (W m^-2), Rnet (W m^-2), G (W m^-2), Tsoil (°C) at multiple depths, VWC (%), Precipitation (mm), WaterLevel (mm), Windspeed (m s^-1), Winddir (degrees).
- Derived QA/diagnostic variables: u*, TKE, L, zL, x_peak, x_70, x_90, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.

## Data provenance and acknowledgments
- Funded by Natural Environment Research Council (NERC) under UK-SCAPE and SEFLOS projects; landowners permission for sensor installation; COSMOS-UK data referenced for EF-SA.
- Key methodological references for EC processing, QC, gap-filling, and partitioning cited.