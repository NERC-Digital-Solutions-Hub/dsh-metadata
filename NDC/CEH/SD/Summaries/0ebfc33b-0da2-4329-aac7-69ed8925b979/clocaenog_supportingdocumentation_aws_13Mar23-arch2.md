# Climoor field site in Clocaenog forest. Supporting documentation for data

- A climate change manipulation experiment at Climoor/Clocaenog field site (established 1998) using automated roof technology to simulate drought and warming conditions expected over the next 20–30 years.
- Data are documented, licensed, and accessible via the provided DOIs; licensing follows the Open Government Licence.

## Data Access and Citation

- Data access: https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
- Primary citation (for AWS data 2016–2021): Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily automatic weather station (AWS) data from Climoor fieldsite in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
- Licensing: Open Government Licence; attribution required.

## Data Structure

- One data file: CLM_AWS_2016-2021_summaryQA.csv
- 10 columns (Date is Year-Month-Day; other fields describe meteorological variables):
  - Date
  - Mean_air_temperature_degC
  - Minimum_air_temperature_degC
  - Maximum_air_temperature_degC
  - Rainfall_mm
  - Air_pressure_mbar
  - Solar_radiation_kW_per_m2
  - Photosynthetic active radiation_umol_per_m2_per_sec
  - Wind_speed_m_per_sec
  - Wind_direction_degrees
- Data quality: missing values marked as 'NA'; faulty data replaced by '-9999'.

## Site Overview

- Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, 03°27'55"W)
- Ecosystem: upland west Atlantic moorland dominated by Calluna vulgaris (heather); other species include Vaccinium myrtillus, Empetrum nigrum, and various bryophytes.
- Climate (1997–2014 context): mean air temp around 8.0°C; mean soil temp in control ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha⁻¹ yr⁻¹.
- Soil: humo-ferric podzol with horizon variability (Eg and Bh present where visible); variable C, N, C:N, and cation data across horizons.
- Vegetation structure: high Calluna presence with substantial bryophyte cover; annual litterfall ~177 g m⁻².

## Climate Change Treatment Information

- Treatments: two climate manipulations (drought and warming) with three replicated plots each, plus three control plots (n=9 total).
- Drought treatment:
  - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor.
  - Timing: generally May–September (1999–2011); extended to April–October since 2012.
  - Effect: ~20% reduction in annual rainfall; up to ~80% of growing-season rain excluded due to sensor limits.
  - Wind constraint: roofs inactive in winds >10 m s⁻¹ to prevent damage.
  - Maintenance: frames refurbished; new frames installed on top of old ones in June 2017.
- Warming treatment:
  - Mechanism: retractable aluminium mesh curtains reducing infrared radiation; nocturnal warming is achieved by limiting heat loss.
  - Controls: roof operation linked to light levels; rain-triggered retraction to protect rainfall within warming plots.
  - Effect: ~14% reduction in annual rainfall; not always identical across years due to operational nuances.
  - Wind constraint: curtains also paused in high winds.
- Combined operation notes: warming and drought roofs can operate together or independently; 2016–2017 frame refurbishments affected operation; some years show partial or no operation due to technical or environmental factors.
- 1997–2021 timeline highlights:
  - Drought operation documented for many years with year-by-year reductions reported (e.g., 1999: 28% annual rainfall reduction; 2001: 28%; 2008+ variations).
  - Warming data accompanying drought data; growing degree days (GDD) calculated to compare warming vs. control; gaps exist in earlier years.
  - 2020–2021: COVID-19 restrictions led to limited field activity; several years have incomplete data.

## Data Collection, Equipment, and Processing

- On-site Automated Weather Station (AWS) and plot-scale micro-met data:
  - Measurements collected: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction, plus plot-level soil temperature and moisture.
  - Sampling: every minute; hourly averages (initially) and later half-hourly averages (post-2016) for micro-met data.
  - Data quality control: manual QC via Excel visual inspection; no hard automated limits described in the document.
- Rainfall data:
  - Site-level rainfall: ground-level rain gauge (biweekly collection; robust against logger/power interruptions).
  - Throughfall data: plot-level rainfall captured via funnels and bottles; sometimes compromised by equipment loss or extreme rainfall events.
  - Method to derive plot rainfall: use percent change from throughfall relative to site rainfall to estimate treatment-specific rainfall; data gaps infilled by year-average reductions when necessary.
- Other data types (as summarized in Table 7):
  - Soil respiration, trace gas flux (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology and pathogen assessments, vegetation chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution and leachate chemistry, among others.
- Storage and accessibility:
  - Some data (especially post-2015 and infrequently collected datasets) are not all stored within the Environmental Information Data Centre (EIDC); contact project leads for full details.

## Data Quality, Gaps, and Limitations

- Data gaps and issues:
  - Drought roofs not operating from 2016 due to frame refurbishments, water accumulation on roofs, and later COVID restrictions.
  - Rainfall sensor on site broken since January 2018 (affects certain GDD and rainfall calculations).
  - Some years (e.g., 2017–2021) include “Off due to COVID” notes affecting data completeness.
  - Throughfall data can be incomplete due to equipment failures (bottles, funnels) or extreme events; treatment means may exclude unreliable plots.
- Data scope:
  - AWS data available 1999–present (daily/micro-meteorological data); extensive site-level and plot-level measurements extend back to 1998, with many datasets collected irregularly across years.
  - Not all data are stored at EIDC; historical and infrequently collected datasets may require direct contact with PI/UKCEH for access.

## Data Storage, Use, and Citation Guidance

- Data storage: primary dataset for 2016–2021 is in CLM_AWS_2016-2021_summaryQA.csv; broader data exist but are not uniformly stored at EIDC.
- Use recommendations:
  - Access the AWS and micro-meteorological data through the provided DOI and reference the primary citation when using the 2016–2021 summary QA data.
  - When using throughfall, rainfall, and plot-level data, apply the described methodology to derive treatment-specific rainfall and acknowledge any data gaps or infill methods.
- Data provenance notes:
  - Documentation includes detailed descriptions of site characteristics, treatment implementation, and data collection protocols to support reproducibility and contextual interpretation.

## Appendix and Contact

- Appendix includes site layout figures and quadrat mapping for measurement areas.
- For enquiries about non-stored/infrequent datasets or data specifics post-2015, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) at UKCEH Bangor.

## Summary of Key Points for Environment Analysts

- Purpose: long-term manipulation of drought and warming to reflect future climate; robust dataset across multiple environmental domains (meteorology, soil, vegetation, trace gases, and ecosystem fluxes).
- Data coverage: extensive temporal span with 1998–2021 contextual data; AWS data 2016–2021 available in a QA-specified CSV; other data types documented but not uniformly stored in one portal.
- Data quality and transparency: explicit notes on data flags, recording gaps, system maintenance events, and operational limitations; clear licensing and citation requirements.
- Analytical value: enables standardized temporal comparisons (e.g., warming vs. control, drought vs. control) and integration with other environmental datasets; awareness of treatment-specific rain adjustments and frame refurbishment events is essential for accurate interpretation.