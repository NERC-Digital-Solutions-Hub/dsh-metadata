# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2016 to 2018

## Summary
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England (2016–2018).
- Measurements include air temperature, solar radiation (pyranometer), wind speed, and lake water temperature profiles at multiple depths.
- Data collected every 4 minutes; hourly averages computed in an Oracle database; times are in GMT.
- Data are raw (not calibrated or fully quality controlled) but have been visually checked; obvious hardware-related errors removed; gaps due to maintenance or sensor/logger problems.
- Provided as CSV with detailed column definitions; authors: Feuchtmayr, Jones, Clarke, Maberly (2021); funding: NERC NE/R016429/1 (UK-SCaPE programme).

## What’s in the dataset
- Air temperature (degrees C)
- Solar radiation flux (Watts per square meter)
- Wind speed (m/s)
- Lake water temperature at depths: 0.5 m, 1 m, 2 m, 3 m, 4 m, 5 m, 6 m, 7 m, 8 m, 9 m, 10 m, 12 m
- Time stamp: Date GMT
- Coverage: 2016, 2017, 2018
- All data presented in GMT; frequency: 4-minute raw observations with hourly aggregates

## Collection method and provenance
- Location: Blelham Tarn buoy, Cumbria, England
- Instruments: meteorological sensors and platinum resistance thermometers for in-lake temperatures
- Data processing: hourly averages derived from 4-minute measurements within an Oracle database
- Publication: Feuchtmayr et al. (2021)
- Funding and program: Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE National Capability

## Quality control and data maturity
- Status: raw data not yet calibrated or fully quality controlled
- QA performed: visual checks; obvious hardware-related errors removed
- Gaps: due to buoy maintenance or sensor/logger problems
- Implication for users: data require calibration/standard QC and metadata on sensor status and calibration for rigorous reuse

## Data structure and metadata
- Format: comma-separated values (CSV)
- Columns (with meanings): Date GMT; 0.5m temperature; 1m temperature; 2m temperature; 3m; 4m; 5m; 6m; 7m; 8m; 9m; 10m; 12m temperatures; Air Temperature; Pyranometer (solar radiation); Wind Speed
- Units: temperatures (degrees C); solar radiation (W/m^2); wind speed (m/s)
- Documentation: column descriptions provided, including depth-specific temperatures and measurement contexts

## Limitations and governance considerations for Data Stewards
- Calibration status: dataset is raw; plan for calibration, traceable QC, and uncertainty estimates
- Metadata completeness: ensure sensor calibration dates, maintenance history, and data quality flags are captured for future interoperability
- Data quality: gaps exist; implement gap-filling or explicit gap metadata as part of data governance
- Interoperability: standardized time stamps (GMT) and explicit depth descriptors support integration with other datasets, but require consistent QC labels
- Access and licensing: confirm data reuse rights and licensing; consider publishing provenance notes and usage guidance alongside the data
- Update/maintenance: define process for updating the dataset with calibrated QC’d data and any reprocessing results

## Access, availability, and provenance
- Availability: CSV format provided; raw data with documented collection details
- Provenance: clear authorship and funding information; original methodology and processing described
- Suggested governance: accompany data with a data stewardship record detailing provenance, processing steps, and QC plan; specify data access terms and any embargoes or update cycles

## Funding and governance notes
- Funding: Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE National Capability
- Governance implication: ensure funding-informed data management practices, including long-term preservation, metadata standards, and ongoing quality assurance protocols to meet data steward responsibilities.