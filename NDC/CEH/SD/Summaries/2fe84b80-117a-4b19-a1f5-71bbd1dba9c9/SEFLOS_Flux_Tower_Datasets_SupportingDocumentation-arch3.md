# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a cropland and a grassland on lowland peatland soils, East Anglia Fens, UK, 2016 to 2019

## Overview of dataset
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured with eddy covariance (EC) at two lowland peatland environments in East Anglian Fens, England, UK.
- Sites: EF-SA (cropland for high-value horticultural crops) and EF-GF (managed grassland).
- Ancillary data: meteorological and soil physics observations, plus atmospheric turbulence variables.
- Timeframe: EF-SA from 2016-11-17 to 2018-09-24; EF-GF from 2017-04-27 to 2019-03-31.
- Outputs include gap-filled fluxes and partitioning products, along with associated metadata and quality indicators.

## Study sites
- Location: East Anglian Fens (Fenland), UK; region features extensive lowland peat soils with historical drainage.
- Climate: temperate maritime; mean annual temperature ~10.4°C and precipitation ~564 mm (1981–2010 baseline).
- Cropland site (EF-SA)
  - Coordinates: 52.44°N, 0.41°E, approximately 2 m above mean sea level.
  - Land use: production of lettuce, celery, cereals; peat over clay; drainage via sub-surface pipes and ditches; peat subsidence ~2 m since drainage began.
  - Soil: degraded fen peat with specific bulk density, pH, organic C content, and C/N ratio provided.
- Grassland site (EF-GF)
  - Coordinates: 52.47°N, -0.19°W, ~1 m amsl.
  - Land use: former arable peatland now rewetted/restored; low-intensity grazing and occasional cutting.
  - Soil: peat layer ~2 m; pH 5.2–6.0; organic C ~30%; total N ~1.4%.

## Sampling regime and flux data acquisition
- Flux measurements: horizontal and vertical fluxes above canopy at 2.6 m height using open-path EC systems.
- Instruments: LI-COR LI-7500 gas analyser; ultrasonic anemometers (Gill WindMaster at EF-SA; Solent R3 at EF-GF); 20 Hz raw data collected and logged with CR3000 data loggers.
- Turbulent fluxes: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), and τ (kg m^-1 s^-2).
- Ancillary sensors: air temperature, relative humidity, net radiation (SWin, SWout, LWin, LWout), soil heat flux (G), water level (relative depth), soil moisture (VWC) and soil temperature (Tsoil) at multiple depths, precipitation; all logged as 30-minute means (and sums for precipitation).

## Data processing and quality control
- Processing: flux calculations with EddyPRO® v6.1; 30-minute averaging; QC and corrections built into the EddyPRO workflow.
- Corrections included: angle-of-attack adjustment for sonic anemometers, 2D coordinate rotation, high/low-frequency co-spectral attenuation, humidity effects on H, density corrections on LE and CO2, and standard uncertainty estimation.
- Derived metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter z/L; flux footprints modeled per Kormann & Meixner.
- Data quality controls: outlier removal via median absolute deviation; non-stationary turbulence periods removed; flux ranges screened (H, LE, NEE bounds); nighttime NEE filtered; u* thresholds applied (EF-SA: 0.22 m s^-1; EF-GF: 0.16 m s^-1).
- Visual QC: weekly plots of flux and ancillary data to identify obvious errors.

## Gap-filling and flux partitioning
- Gap-filling: missing EC flux data (NEE, LE, H) filled using Marginal Distribution Sampling (Reichstein et al., 2005).
- Flux partitioning: NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using partitioning methods driven by air temperature data.
- Tools: REddyProc package (R) used for gap-filling and partitioning (Reichstein et al., 2016).

## Data structure and outputs
- Data delivery: two separate CSV files containing tabular time-series data; gap-filled and partitioned fluxes are provided for the observation period at each site.
- Data gaps: represented as -9999 in the datasets.
- Variables and units: comprehensive table (Table 1) describes fluxes (NEE, LE, H, τ), gap-filled values (NEE_filled, LE_filled, H_filled), partitioned products (GEP, TER), meteorological, soil, precipitation, water level, wind metrics, footprint metrics, and quality indicators (standard deviations, NEE_filled_sd, etc.).
- Time resolution: 30-minute averages for primary variables; some ancillary data provided as 30-minute means and sums.

## Metadata, data provenance, and governance
- Acknowledgments and funding: NERC awards and SEFLOS/UK-SCAPE projects; landowners’ permissions acknowledged.
- Data provenance: detailed methodological description, measurement standards, instrumentation, processing steps, QC criteria, and references to foundational methods and software (EddyPRO, REddyProc, and established flux processing literature).
- Accessibility and standards: dataset includes explicit metadata on variable names, units, data structure, and gap-filling/partitioning approaches; uses public tools and standard eddy-covariance processing workflows.

## Relevance for monitoring frameworks
- Measures provided align with policy-relevant environmental health monitoring: carbon balance (NEE, GEP, TER), energy fluxes (H, LE), and atmospheric exchanges (τ) in peatland agro-ecosystems.
- Demonstrates end-to-end data pipeline for monitoring: instrument deployment, high-frequency data capture, rigorous QC, gap-filling, flux partitioning, and clearly documented data products.
- Addresses common monitoring challenges: explicit metadata, data quality checks, transparent gap-filling/partitioning methods, and traceable data lineage, with described barriers and governance considerations (data access, metadata completeness, transformation needs, and data sharing).