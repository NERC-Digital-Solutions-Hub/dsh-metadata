# Climoor field site in Clocaenog forest. Supporting documentation for data

## Overview
- Describes the Climoor/Clocaenog climate-change manipulation field site (established 1998) using automated roof technology to simulate drought and warming over the next decades.
- Data types span meteorology, plot-level microclimate, rainfall, throughfall, soil/biogeochemistry, and vegetation measurements collected within the experimental plots.
- Intended for use and reuse within the NERC Environmental Information Data Centre (EIDC) and related portals.

## Data Access and Licensing
- Data available via DOI: https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
- Licensing: Open Government Licence; users must comply with terms.
- Citation required for data reuse:
  Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily automatic weather station (AWS) data from Climoor fieldsite in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979

## Dataset Structure and Metadata
- Main dataset: CLM_AWS_2016-2021_summaryQA.csv with 10 columns.
- Data values: missing data marked as NA; faulty records replaced by -9999.
- Columns (example structure): Date (Year-Month-Day), Mean_air_temperature_degC, Minimum_air_temperature_degC, Maximum_air_temperature_degC, Rainfall_mm, Air_pressure_mbar, Solar_radiation_kW_per_m2, Photosynthetic_active_radiation_umol_per_m2_per_sec, Wind_speed_m_per_sec, Wind_direction_degrees.

## Site Context and Environment
- Location: Clocaenog Forest, North East Wales, UK (53°03'19" N, -03°27'55" W).
- Ecosystem: upland moorland dominated by Calluna vulgaris; bryophytes prominent; season: growing June–August; winter dormancy.
- Soil: humo-ferric podzol with variable horizons (Eg, Bh); key soil metrics (N, C, C:N, bases, CEC) detailed in tables.
- Climate (historical context 1997–2014): mean air temp ~8.0 °C; mean soil temp ~7.5 °C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha⁻¹ yr⁻¹.

## Climate Change Treatments
- Experimental design: two treatments (drought and warming), each with three replicate plots plus three controls (9 plots total).
- Drought treatment: retractable polyethylene roof reducing rainfall by ~20% during May–September (1999–2011), later adjusted to April–October due to site changes; limitations include incomplete rain capture and occasional system failures (e.g., 2016 onward due to water accumulation).
- Warming treatment: retractable aluminium mesh curtains reducing nocturnal heat loss; operated by a light sensor with rain-triggered retraction to mitigate rainfall exclusion; curtains not operated in high winds (>10 m/s).
- Maintenance: frames refurbished/replaced around 2016–2017; new frames installed June 2017 to minimize vegetation disturbance.
- Treatment timing and performance data (including Growing Degree Days, GDD) are provided per year (Tables 6a and 6b).

## Data Collection, Equipment and Processing
- Equipment: Automated Weather Station (AWS) and plot-level micro-met sensors; diverse biotic/abiotic data collected on plots.
- AWS sensors (example): air temp (HMP45C), relative humidity (HMP45C), solar radiation (Skye SP1110 pyranometer), PAR (SKP215), net radiation (NR-Lites), rainfall (ARG100 tipping bucket), wind speed/direction (Windsonic).
- Data cadence: measurements logged every minute; hourly averages (and some half-hourly after 2016) for AWS and micro-met data.
- Data quality control: visual inspection in Excel; noted trade-off between automated limits and human interpretation.
- Plot-scale data (micro-met): soil temp (T107 sensors) at multiple depths; soil moisture via TDR (CS616) since 2008; earlier methods varied.
- Rainfall data: site-level storage gauge (biweekly) used as primary rainfall measure; plot-level throughfall data collected biweekly using funnels and bottles; throughfall-based adjustments applied to derive plot rainfall; data quality rules include exclusion of plots when collectors fail or data are compromised (with occasional infilling using year-average reductions).

## Data Types and Processing Details
- AWS meteorological data: daily measurements for multiple variables; micro-met data logged since 1998; post-2016 data sometimes half-hourly.
- Rain gauge and rainfall chemistry: site-level rainfall preferred when hourly data unavailable; throughfall data used to compute treatment-specific rainfall percentages.
- Vegetation and ecosystem measurements: annual vegetation surveys, litterfall, biomass, and chemistry subset; various data stored within EIDC, with some infrequent datasets outside EIDC after June 2015.
- GDD: calculated for control and warming plots using plot-scale air temperature data; recommendation to use percent change in GDD for warming comparisons when data gaps exist.

## Data Availability, Gaps and Limitations
- Not all data stored in EIDC post-June 2015; some datasets outside EIDC; contact primary authors for details.
- Gaps and data quality issues noted:
  - Rainfall sensor on-site broken since Jan 2018.
  - Drought roofs not active from 2016 due to refurbishments and, later, water accumulation issues.
  - Warming roofs operational constraints during high winds.
  - COVID-19 in 2020–2021 restricted field work; data collection and access affected for those years.
  - Throughfall and plot-level data occasionally have incomplete replicates due to data loss; infilling used in some years.

## Appendices and Site Layout
- Figures (not reproduced here) illustrate site layout, quadrats, measurement areas, and the evolution of the climate-manipulation frames.

## Data Stewardship and Contact
- Metadata completeness and data provenance are documented, with guidance to contact researchers for datasets not in EIDC or for clarifications:
  - Sabine Reinsch and Bridget Emmett (enquiries@ceh.ac.uk) at UKCEH Bangor.