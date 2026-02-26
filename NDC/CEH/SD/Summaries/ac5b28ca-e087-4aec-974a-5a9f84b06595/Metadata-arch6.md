# Sediment fluxes, discharge and acoustic Doppler current profiler (aDcp) calibrations for the Mekong Delta, Vietnam between 2005 and 2015

## Summary
- Documents routine flood and water level monitoring in the Mekong Delta, Vietnam, using four ADCP sites to back out sediment fluxes (2005–2015) via calibration of acoustic backscatter to suspended sediment concentrations (SSCs).
- Provides detailed data processing workflow, quality assurance, and data structure to enable reuse and cross-site comparisons.

## Data collection and scope
- Sites: Tan Chau, Chau Doc, Can Tho, and My Thaun with specified coordinates.
- Instruments: Teledyne RDI Workhorse 600 kHz ADCP units and one RiverRay ADCP unit.
- Objective: Calibrate acoustic backscatter signals with observed SSCs to derive sediment fluxes through the delta for daily time series.

## Analytical methods
- Field SSC measurements: 3 L Van Dorn sampler collected at various depths; samples filtered and dried to determine SSC (mg/L).
- Calibration: Match measured SSCs to corresponding ADCP backscatter (dB) at sample depths to create power-law calibration curves.
- Processing workflow: Raw ADCP data processed in WinRiver II, exported as ASCII, then imported into Velocity Mapping Toolbox (MATLAB) for processing and visualization.
- Flux calculation: Convert ADCP-derived fluxes to sediment fluxes using instrument-specific calibration curves; generate daily fluxes by applying sediment ratings curves between sediment flux (kg/s) and discharge (m³/s) to daily discharge records.

## Quality assurance
- Techniques and software are standard, robust, and well-documented in peer-reviewed literature.
- Protocols are robust and consistently monitored by the Vietnamese hydrological agency.
- Flux estimates shown to be consistent with upstream estimates (Darby et al., 2016).

## Data structure and accessibility
- Files provided per site:
  - Flux file: daily sediment fluxes and discharge linkage (columns include Date with year ignored, and 2005–2012 data).
  - Ratings file: Month, Day, Year, Discharge (m³/s), Section-averaged SSC (mg/L), Sediment Flux (kg/s).
- ADCPcalibrations.csv: raw backscatter (ABS dB) and SSC (mg/L) for instrument-specific calibrations; instruments identified by serial numbers (e.g., INST1258; INSTSoton references a Southampton unit).
- Data handling notes:
  - Missing discharge represented as NaN (e.g., February 29 on non-leap years).
  - Year column in flux files is informational only for readability; actual year is ignored in that column.
- Instrument and dataset identifiers enable cross-site comparisons and re-use of calibrations.

## Data provenance and references
- Darby, S.E., Hackney, C.R., Parsons, D.R., Tri, P.D.V (2020) – main dataset description and calibrations.
- Related foundational work:
  - Darby et al. (2016) Nature: Fluvial sediment supply to a mega-delta reduced by shifting tropical-cyclone activity.
  - Hackney et al. (2018) Earth Surface Processes and Landforms: Influence of flow discharge variations on morphodynamics of a diffluence-confluence unit.