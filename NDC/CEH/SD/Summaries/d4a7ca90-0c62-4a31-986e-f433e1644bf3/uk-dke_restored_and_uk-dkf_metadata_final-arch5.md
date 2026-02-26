# Carbon dioxide and methane fluxes and associated environmental observations from paired burned/unburned peatland undergoing restoration

## Overview
- Time series of land surface–atmosphere exchanges: NEE (CO2 flux), CH4 flux, sensible heat (H), latent heat (LE), plus meteorological observations.
- Two blanket bog sites on Forsinard RSPB Reserve, Flow Country, Caithness and Sutherland, Scotland: one burned area within a former forestry block (UK-DKF) and a nearby restored area protected from fire (UK-DKE-RESTORED).
- Context: former forestry cleared in 2017; a wildfire occurred May 2019; restoration and instrumentation relocation around 2016–2021.
- Time period covered: 25/09/2019 – 20/05/2021, withFootprint SW wind direction; limited data capture after 16/10/2020 due to equipment and weather-related issues; additional gaps reported after 16/10/2021.
- Data provided at multiple resolutions: raw 20 Hz eddy-covariance data and processed 30-minute fluxes; accompanying meteorology at 15-minute to 30-minute intervals.

## Experimental design and scope
- Paired site design: burned versus restored peatland to assess restoration effects on carbon and energy fluxes.
- Footprint considerations: measurements largely representative of the SW fetch (~300 m) with a nearby watercourse affecting the RESTORED site.
- Instrumentation arrangements reflect semi-natural peatland conditions with static canopy assumptions post-burn.

## Data collection and instrumentation
- Eddy covariance system for CO2, CH4, LE, and H:
  - Sonic anemometer: Windmaster Pro at 2.3–2.55 m above surface.
  - Gas analyzers: LI-7200 for CO2/H2O; Li-7700 open-path for CH4.
- Meteorology and ancillary measurements:
  - Air temperature (Ta), relative humidity (RH) at 2 m; net radiation (Rn), incoming shortwave (Rg), PAR (PPFD).
  - Soil measurements: soil heat flux (G), soil temperature (Tsoil), soil moisture (VWC) at three microforms; water table depth (WTD).
  - Precipitation (unheated tipping bucket) and wind metrics (speed, direction, friction velocity u*, stability parameter L).
- Sampling and processing:
  - EC data: 20 Hz; meteorology: 15-minute to 30-minute averages.
  - Flux calculations: 30-minute intervals using EddyPRO v7.0.6; QC applied per standard micrometeorology procedures.
- Site notes:
  - Performance issues: sonic anemometer power supply problems and weather-related access constraints; COVID-19 travel restrictions affected site maintenance.
  - Calibration: pre-installation calibration; no on-site span/zero checks during data capture; June 2021 zero/span check indicated no significant drift.

## Data processing, quality control, and provenance
- Flux processing and corrections:
  - Coordinate rotation, lag removal, cospectral corrections, density corrections; H flux corrected for humidity; NEE assumed equal to turbulent CO2 flux; CO2 storage considered negligible.
  - Sign convention: positive fluxes from ecosystem to atmosphere.
- Quality control approach:
  - Due to patchy data capture, datasets are submitted without post hoc screening; quality flags included to guide future users.
  - Standard QC references cited (Mauder et al. 2013; Vickers & Mahrt 1997; Wilczak et al. 2001; Nakai et al. 2006; Moncrieff et al. 1997, 2004; Schotanus et al. 1983; Webb et al. 1980).
- Documentation of data quality:
  - Detailed flagging scheme (000 = raw, 001 = primary, 002 = calibrated, 003 = no data, etc.), including various interpolation and model-fill codes.
  - Maximum interpolation gap: 1 hour.
- Data lineage and availability:
  - Raw 20 Hz EC data, mixing ratios, and processed fluxes are provided to maximize usability and transparency.
  - Full instrumentation details available on request.

## Data structure, units, and contents
- Data format:
  - Single CSV file with a comprehensive set of columns.
- Core variables (examples):
  - Time, soil moisture (SWC_1_1_1, SWC_2_1_1, SWC_3_1_1), soil temperature (Ts_1_1_1, Ts_2_1_1, Ts_3_1_1), air temperature (Ta_1_1_1), relative humidity (RH_1_1_1), PAR (PPFD_1_1_1), radiation (Rn_1_1_1, Rg_1_1_1), precipitation (P_rain_1_1_1), water table depth (WTD), soil heat flux (G), sensible heat (H), latent heat (LE), CO2 flux (co2_flux), water vapor flux (h2o_flux), CH4 flux (ch4_flux), gas mixing ratios, turbulence metrics (u*, L, wind_speed, wind_dir, (z-d)/L), etc.
- Units:
  - Standard micrometeorological units (e.g., Ta °C, RH %, PPFD µmol m^-2 s^-1, NEE/CH4/H/LE in W m^-2 or µmol m^-2 s^-1 as applicable).
- Metadata and flags:
  - Each variable has associated FLAG fields describing data quality and processing status.
  - Flags follow a documented scheme linking to data provenance and potential gap-filling methods.

## Data availability, limitations, and caveats
- Temporal coverage and gaps:
  - Monitoring period: 25/09/2019 – 20/05/2021 with notable gaps due to instrument and power issues; additional gaps noted after 16/10/2020 and after 16/10/2021.
- Data quality caveats:
  - Patchy data capture led to no dataset-wide screening; users should rely on the included quality flags for filtering.
  - Calibration occurred off-site due to remoteness; limited on-site calibration checks during the campaign.
- Contextual interpretation:
  - Two-site design provides a contrast between burned and restored peatland contexts, but data gaps may affect trend detection; cross-reference with site metadata for interpretation.
- Documentation and metadata:
  - Comprehensive methodological notes, instrumentation details, and standard QC references are provided to support reproducibility and audit trails.

## Governance, stewardship considerations
- Data governance readiness:
  - The dataset is prepared with robust provenance, processing steps, and QC flagging to support discoverability and reuse.
  - Clear documentation of instruments, sampling regimes, processing software (EddyPRO), and corrections aligns with data management best practices.
- Reuse guidance for data stewards:
  - Use flags to filter data for quality and applicability; treat 000 and 001–004 flags as guidance rather than raw validation.
  - Acknowledge methodological references for flux calculations and QC procedures when reusing data.
  - If further instrument details or calibration data are needed, contact data authors.

## References
- Mauder, M. et al. (2013) A strategy for quality and uncertainty assessment of long-term eddy-c covariance measurements.
- Vickers, D. & Mahrt, L. (1997) Quality Control and flux sampling problems for tower and aircraft data.
- Wilczak, J. M., Oncley, S. P. & Stage, S. A. (2001) Sonic anemometer tilt correction algorithms.
- Nakai, T. et al. (2006) Correction of sonic anemometer angle of attack errors.
- Moncrieff, J. B. et al. (1997) A system to measure surface fluxes of momentum, sensible heat, water vapour and CO2.
- Moncrieff, J. B. et al. (2004) Averaging, detrending and filtering of eddy covariance time series.
- Schotanus, P. et al. (1983) Temperature measurement with a sonic anemometer and its application to heat and moisture fluxes.
- Webb, E. K. et al. (1980) Correction of flux measurements for density effects due to heat and water vapour transfer.