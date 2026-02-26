# Supporting information for: Eddy Covariance measurements of carbon dioxide, energy and water flux at an intensively cultivated lowland deep peat soil, East Anglia, UK, 2012 to 2020.

## Overview of the dataset
- Time series observations of land-surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ).
- Measurement period: 2012-06-22 00:30 to 2020-01-01 00:00.
- Site: EF-DA flux site on intensively cultivated lowland deep peat in East Anglian Fens, UK (site code EF-DA).
- Ancillary data: meteorological and soil physics observations and variables describing atmospheric turbulence.
- Data processing: flux calculations, quality control, gap-filling, and partitioning of NEE into GEP and TER; generation of fully gap-filled time series and associated uncertainties.

## Study site and scope
- Location: East Anglian Fens (The Fenland), UK; 52°31'N, 0°29'E, 0 m amsl.
- Land use: drained peatland, intensive arable farming with multiple crops; farm management at Rosedene Farm (>100 fields, ~1,400 ha).
- Climate: temperate maritime (mean 1981–2010: Ta 10.4 ± 0.6 °C, precipitation 564 mm yr^-1).
- Soil and drainage: deep peat with relatively high bulk density in upper layers; ongoing drainage increasing mineral content with depth.
- Cropping over the period: lettuce (2012, 2014, 2016, 2018), leek (2013), celery (2015), sugar beet (2017), potatoes (2019).

## Data acquisition and instrumentation
- Flux measurements: eddy covariance (EC) above canopy at 1.5 m height; open-path LI-7500 CO2/H2O infrared gas analyser; CSAT3 sonic anemometer; wind direction ~225°.
- Sampling: 20 Hz raw data; 30-minute aggregation for fluxes.
- Ancillary meteorology and soil data: NRLite2 and CNR4 radiometers for net radiation; PAR sensor; air temperature and humidity sensors; tipping-bucket precipitation gauge.
- Soil instrumentation: two arrays with soil heat flux sensors (G), thermocouples for Tsoil, and CS616 time-domain reflectometer for soil moisture (VWC); sensors spaced ~2 m apart.
- Data logging: 30-minute means (and sums for precipitation) to CR3000 Micrologger.

## Data processing and quality control
- Primary processing: EddyPRO v6.1; 30-minute flux averages; QC of 20 Hz data; 2D rotation to align with local terrain; corrections for high/low-frequency co-spectral attenuation; density corrections; humidity-corrected sensible heat flux; density-corrected LE and CO2 fluxes.
- Uncertainty: random uncertainties computed per Finkelstein & Sims (2001).
- Quality control steps: outlier removal via median absolute deviation; non-stationary turbulence screening; flux range checks (-200 to 400 W m^-2 for H; -200 to 600 W m^-2 for LE; -40 to 40 μmol CO2 m^-2 s^-1 for NEE); night-time NEE removal; footprint filtering to ensure >70% of flux originates from target ecosystem (ART footprint tool); weekly visual QC for obvious errors.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005).
- Flux partitioning: NEE divided into GEP and TER using Reichstein et al. (2005) framework with air temperature driving partitioning.
- Tools: REddyProc package in R (Reichstein et al., 2016) for gap-filling and partitioning.

## Data structure, content, and units
- Primary time series: 30-minute, ASCII CSV format with columns described in Table 1 (e.g., DateTime in UTC, NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, and many derived/auxiliary variables).
- Gap-filled and partitioned data provided for the full period of record; missing records denoted as -9999.
- Variables include: Pa, Ta, RH, VPD, Rnet, Rg, G (soil heat flux at multiple locations), Tsoil, VWC, Precipitation, Windspeed, Winddir, FootprintFraction, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.
- Units: standardized across LI-COR/eddy covariance conventions and Reichstein et al. references; detailed table (Table 1) provides the full description.

## Metadata, discoverability and data quality
- Clear documentation of variables, units, and data processing steps to support reuse and integration with other datasets.
- Data include both raw and processed (gap-filled/partitioned) time series, enabling validation, recalculation, or alternative gap-filling approaches.
- Footprint information available to assess representativeness of fluxes for the target ecosystem.

## Reuse, access and governance
- Data produced under NERC funding and university partnerships; acknowledgments indicate long-term site support and collaboration with landowners.
- Suitable for cross-site synthesis and meta-analyses in carbon, energy, and water flux budgets; compatible with standard eddy covariance processing workflows (EddyPRO, REddyProc).
- Emphasis on data quality control, traceable processing steps, and availability of uncertainty estimates to support robust interpretation and policy-relevant research.

## Limitations and considerations
- Site-specific context: peatland agriculture in The Fenland; results may be influenced by drainage status, crop sequence, and management practices.
- Data gaps exist due to instrument downtime and QC exclusions; gap-filled products rely on model assumptions (e.g., Marginal Distribution Sampling).
- Metadata completeness is provided, but users should consult the accompanying documentation for detailed variable definitions and processing choices.

## Acknowledgements and references
- Site established and maintained with NERC funding; collaborations across academia and industry; thanks to landowners for access.
- References provided for data processing methods, QC standards, gap-filling and partitioning algorithms, and data processing tools (EddyPRO, REddyProc, etc.).